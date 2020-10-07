# Scoold
Q&amp;A forum Docker setup

Step-up Scoold locally using docker-compose:

Step 1 : Run docker-compose.

    `docker-compose -f "docker-compose.yml" up -d --build`

Step 2 : Hit URL `http://localhost:8080/v1/_setup` and copy the json data and save it.
Json will be like.

    {
    "accessKey" : "<app:para>",
    "message" : "Save these keys - they are shown only once!",
    "secretKey" : "<e8V26Dhm+gREb19F5wm1cnlaz8Yna9AdwUTmPup1mEbpuEVUkBEtyQ==>"
    }


Step 3 : Copy value of `secretKey` and `accessKey`.

Step 4 : Edit `scoold-application.conf` and replace values of `secretKey` and `accessKey`

Step 5 : restart docker-compose.

Step 6 : Open Link localhost:8000


# Addition Setup

You will find these settings in `scoold-application.conf`

* Add Email Configurations Under   `# system email address`
* Update Domain specific Auth setting accordingly `para.approved_domains_for_signups = "<Domain.com>"`
* Add Admin Email for Setup Scoold after deploy `para.admins = "Email@gmail.com"`

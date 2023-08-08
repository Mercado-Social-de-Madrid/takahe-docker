# takahe-docker
Deployment of [Takahe](https://github.com/jointakahe/takahe) instance using Docker

# Deployment
1. Create a new `.env` based on the `.env.template` file and fill all the values.
2. Bring up the containers:
    `docker compose up -d`
3. Run Django migrations:
    `docker exec -it web python manage.py migrate`
4. To apply custom styles run:
    `docker exec -it web python manage.py collectstatic`
5. Create admin user account:
    a. Go to `https://<your_domain>/auth/signup/`
    b. Enter your admin email specified in `TAKAHE_AUTO_ADMIN_EMAIL`
    c. Go to your inbox and activate the account.
    
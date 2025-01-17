# DEVHUB
>#### *Share. Learn. Collaborate. Connect with Developers!*

![DevHub main page](assets/devhub_login.png)
<br>

---

<br>

# **Setup**

### Requirements
- Python 3.x
- Node.js 18.x
- Redis

## *Backend*
``` shell
# Navigate to backend directory
cd backend

# Create a python virtual environment(venv)
python3 -m venv .venv

# Activate your virtual environment:
source .venv/bin/activate

# Install dependencies
pip3 install -r requirements.txt

# Setup flask
flask db migrate
flask db upgrade

# Spin redis
sudo systemctl start redis-server

# Spin the backend
python3 main.py

```
> Copy the backend server url ex: ```http://127.0.0.1:5000``` 

## *Frontend*
### New terminal tab(please!!!)
```shell
# Navigate to frontend directory(now you're in DevHub/backend)
cd ../frontend

# Setup the .env file
echo VITE_API_URL=http://127.0.0.1:5000 >> .env # replace the url with the one you copied

# Install dependencies
npm i

# Spin the frontend
npm run dev
```

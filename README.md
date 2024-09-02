# Paso 1:
Crear en entorno virtual
# Configurar la DB
export FLASK_APP=backend.py
flask db init
flask db migrate -m "Initial migration"
flask db upgrade
# Levantar servidor
flask --app backend run

# EndPoints:
# Register
url: http://127.0.0.1:5000/register
body: (raw-json):{
    "email":"marquez@gmail.com", "password":"123456", "role":"Admin"
}
rta: {
    "msg": "User created successfully"
}
# login
url: http://127.0.0.1:5000/login
body: (raw-json):{
    "email":"marquez@gmail.com", "password":"123456"
}
Rta: {
    "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJmcmVzaCI6ZmFsc2UsImlhdCI6MTcyNTMwOTcwMywianRpIjoiYzNjMWZlNDItOTRjMS00MzZkLTgzODYtMTdjYzBhM2UwYzI3IiwidHlwZSI6ImFjY2VzcyIsInN1YiI6eyJlbWFpbCI6Im1hcnF1ZXpAZ21haWwuY29tIiwicm9sZSI6IkFkbWluIn0sIm5iZiI6MTcyNTMwOTcwMywiY3NyZiI6ImQ1MDVkNGMwLTA5ZDMtNDEzOC1hZDQ1LWVlNTBiNWJiNGJkOCIsImV4cCI6MTcyNTMxMDYwM30.iUGcyq9c1iPLlVfdx1Kp6AkVBbs5JqeJZQdizaYT2to"
}

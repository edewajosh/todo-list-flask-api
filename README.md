# BUILDING A REST API USING FLASK

In order to run this you have install python, flask, flask_httpauth
Remember to install ```bash Curl ``` in order to test a web service 
because is not the best idea to use a web browser.

To flask and flask_httpauth run the following in your virtual environment

```pip install flask```
```pip install flask_httpauth```

Run the following command after installation ```localhost:5000 ``` or ```127.0.0.1``` in your browser

# Below are the methods and their URIs run them in new terminal after running the localhost

## 1. get_tasks()
curl command ```curl -i http://localhost:5000/todo/api/v1.0/tasks```

## 2. get_task()
curl command ```curl -i http://localhost:5000/todo/api/v1.0/tasks/2```

## 3. create_task()
curl command ```curl -i -H "Content-Type: application/json" -X POST -d '{"title":"Read a book"}' http://localhost:5000/todo/api/v1.0/tasks```

## 4. update_task()
curl command ```curl -i -H "Content-Type: application/json" -X PUT -d '{"done":true}' http://localhost:5000/todo/api/v1.0/tasks/2```

## 5. improved get_tasks that returns uri instead of id
curl command ```curl -i http://localhost:5000/todo/api/v1.0/tasks```

## 6. Functions with @auth.login_required decorator
curl command ``` curl -u edewa:python -i http://localhost:5000/todo/api/v1.0/tasks```
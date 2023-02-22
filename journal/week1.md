# Week 1 — App Containerization
- Running CMD in backend-flask/Dockerfile as an external script 
  - Created a file `backend-flask.sh` containing :
```
#!/bin/bash
python3 -m flask run --host=0.0.0.0 --port=4567
````
  - Pointed my Dockerfile to this script to use as CMD `"CMD ["/usr/local/bin/start_flask.sh"]`
 

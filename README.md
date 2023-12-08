# api-ia-hec

## How to connect to the EC2 server

Download `exam-key-aai.pem` file. Useful to connect to the EC2 server.

Run `chmod 400 exam-key-aai.pem` to give to rights access to the key.

Run `ssh -i exam-key-aai.pem ec2-user@ec2-44-206-233-62.compute-1.amazonaws.com` to connect to the server by ssh. 

`ec2-44-206-233-62.compute-1.amazonaws.com` can be switched to another link.

## Clone the repo

Run `git clone git@github.com:Nayel99/ia_optiver.git`

## Build Docker Image

Go to the directory ia_optiver

Run : `docker build -t main .`


## Launch Docker Image

docker run -d -p 8000:8000 main

The API should be exposed at http://0.0.0.0:8000 or http://localhost:8000

Predictions on http://0.0.0.0:8000/predict

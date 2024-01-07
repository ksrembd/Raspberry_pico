
To stop them
sudo -E docker-compose -p zuul-tutorial down
sudo apt-get update
sudo apt-get install docker-compose docker.io git python3-pip
sudo python3 -m pip install git-review


sudo systemctl enable docker.service
sudo systemctl start docker.service





docker run -it ubuntu /bin/bash
Docker run -p 8082:80 httpd
Docker run -p 8083:80 nginx

git clone https://opendev.org/zuul/zuul



cd zuul/doc/source/examples
sudo -E docker-compose -p zuul-tutorial up

Run them in background
sudo -E docker-compose -p zuul-tutorial up -d


To Delete the volumes also
sudo -E docker-compose -p zuul-tutorial down -v



docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)




ssh-keygen


cat  ~/.ssh/id_rsa.pub

git config --global user.name "Your Name"
git config --global user.email "youremail@yourdomain.com"g

git config --global user.email "youremail@yourdomain.com"

git add test.c
git commit -m "my first gerrit commit"







                                         DAY-3
https://github.com/hkshitesh/jenkins-lti.git


Sudo docker run -p 8082:8080 jenkins/jenkins:lts

sudo docker exec -it 8e83a37a0554 /bin/bash


https://github.com/hkshitesh/jenkins-lti.git



https://github.com/hkshitesh/jenkins-lti



cd zuul/doc/source/examples



sudo -E docker-compose -p zuul-tutorial down -v

sudo -E docker-compose -p zuul-tutorial up

C
git clone http://localhost:8080/zuul-config


cd zuul-config
mkdir zuul.d


vi zuul.d/pipelines.yaml



          comment: (?i)^(Patch Set [0-9]+:)?( [\w\\+-]*)*(\n\n)?\s*recheck
    success:
      gerrit:
        Verified: 1
    failure:
      gerrit:
        Verified: -1

- pipeline:
    name: gate
    description: |
      Changes that have been approved are enqueued in order in this
      pipeline, and if they pass tests, will be merged.
    manager: dependent
    post-review: True
    require:
      gerrit:
        open: True
        current-patchset: True
        approval:
          - Workflow: 1
    trigger:
      gerrit:
        - event: comment-added
          approval:vi zuul.d/projects.yaml



- project:
    name: ^.*$
    check:
      jobs: []
    gate:
      jobs: []

- project:
    name: zuul-config
    check:
      jobs:
        - noop
    gate:
      jobs:
        - noop



- project:
    name: ^.*$
    check:
      jobs: []
    gate:
      jobs: []

- project:
    name: zuul-config
    check:
      jobs:
        - noop
    gate:
      jobs:
        - noop





https://opendev.org/zuul/zuul/src/branch/master/doc/source/examples/zuul-config


            - Workflow: 1
    start:
      gerrit:
        Verified: 0
    success:
      gerrit:
        Verified: 2
        submit: true
    failure:
      gerrit:
        Verified: -2






http://localhost:9000/t/example-tenant/status




DAY -4

git clone "http://localhost:8080/test1"



playbooks/testjob.yaml

- hosts: all
 tasks:
   - debug:
       msg: Hello World!


.zuul.yaml

- job:
   name: testjob
   run: playbooks/testjob.yaml


- project:
   check:
     jobs:
       - testjob
   gate:
     jobs:
       - testjob






http://localhost:8080/dashboard/self



https://github.com/hkshitesh/ZUUL-LTI/tree/main/test1/playbooks


https://github.com/hkshitesh/ZUUL-LTI/tree/main/zuul-config

git add playbooks zuul.d/jobs.yaml



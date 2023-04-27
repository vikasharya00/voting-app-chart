1. This is parent helm chart to deploy all the services under voting application in one go. These services are are vote, result, worker, PSQL db, Redis.
![voting app architecture](https://bday2021.play-with-docker.com/images/voting-app/architecture.png)
2. Whole project is set up to use Git-hub as SCM, Jenkins for CI/CD, Helm for creating charts and deployed on kubernetes cluster on minikube.
3. Each individual component i.e. vote, result, worker has their own jenkins. Jenkins files for them are included in theri respective repositories.
4. Once source code of any of the component e.g. vote is updated it will trigger its own pipeline ans well as build the parent-chart i.e. this chart as well and deploy the changes. 
3. Worflow is explained in this documentation [link](https://docs.google.com/document/d/16onAjYJYHIk76hUNTcbKHXnH9bnrX91l1BCHE3kOc2M/edit?usp=sharing)
3. Link for each component's codebase
    - vote [repo-link](https://github.com/vikasharya00/voting-app-vote.git)
    - result [repo-link](https://github.com/vikasharya00/voting-app-result.git)
    - worker [repo-link](https://github.com/vikasharya00/voting-app-worker.git)

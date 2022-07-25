### Kubernetes Homework #1 


#### Kubernetes project that shows price of BitCoin and displays the latest news from Ynet:    
● Presents the Current BitCoin Price, And the Average Price for the last 10 minutes and stores the price in a Redis Database.  
● Reads the “Breaking News” from YNet news service.  
  

## Run With Minikube:

Clone the project

```bash
  git clone https://github.com/MohamadEdris/BitcionPrice_YnetNews.git
```

Go to the project directory

```bash
  cd BitcionPrice_YnetNews
```

Start minikube

```bash
  minikube start
```

Enable ingress addon

```bash
  minikube addons enable ingress
```
Apply Deployment

```bash
  kubectl apply -f .
```

Start minikube tunnel

```bash
  minikube tunnel
```

Access from browser:  
● http://localhost/bitcoin
● http://localhost/ynet  

## Services:
<img width="932" alt="image" src="https://user-images.githubusercontent.com/73100170/180754247-d9286bab-27f1-4fc6-be02-72e409e1c2d9.png">

## Pods:
<img width="932" alt="image" src="https://user-images.githubusercontent.com/73100170/180754422-4f26250f-59ea-44fa-811f-9f645f99dea0.png">

## Ingress:
<img width="932" alt="image" src="https://user-images.githubusercontent.com/73100170/180754538-98a5ef4e-c660-40ac-a458-c4839e384327.png">

## Run the apps with Docker

Run BitCoin image from DockerHub

```bash
  docker pull medris2796/bitcoin-final-task
  docker run -d -p 8000:5000 medris2796/bitcoin-final-task:latest
```
<img width="932" alt="image" src="https://user-images.githubusercontent.com/73100170/180748534-912ff6c8-453e-4794-b4d6-d9b3e1c2ff2d.png">

  
Run Ynet image from DockerHub

```bash
  docker pull medris2796/ynet
  docker run -d -p 8082:5000 medris2796/ynet:latest
```
<img width="919" alt="image" src="https://user-images.githubusercontent.com/73100170/180748931-38107f24-c837-4556-b28b-e52f31c2ac93.png">



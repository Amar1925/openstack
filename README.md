# OpenStack
### t3.large and ubuntu ami

## Installing OpenStack in ubuntu using MicroStack 
```
sudo snap install microstack --beta
```
![image](https://github.com/user-attachments/assets/e561594d-3399-4ac9-a1c8-7d46f4569b71)



### 1. Initialize MicroStack
```
sudo microstack init --auto --control
```
This command:

* Sets up OpenStack services.
* Configures networking.
* Enables an internal bridge for virtual machines.

![image](https://github.com/user-attachments/assets/f9488b15-bad2-4eeb-a51e-49f9fbf8018b)


### 2. Verify OpenStack Services
```
sudo microstack status
```
![image](https://github.com/user-attachments/assets/79b5e085-ca4b-458c-909a-8cd27aeeffcb)


### 3. Access OpenStack Dashboard
Once initialized, you can access the Horizon web dashboard:

-> Find the dashboard IP address:
```
ip a | grep inet
```
for example:-
![image](https://github.com/user-attachments/assets/c53068df-6973-4980-94a3-692f11976791)


-> for password 
```
sudo snap get microstack config.credentials.keystone-password
```

-Go to web browser and search this above IP address:
```
http://<your-ip>:80
```
![Screenshot from 2025-03-02 23-01-20](https://github.com/user-attachments/assets/44381f32-ebc1-40a3-8ab4-8cf9e7a955fe)

## Log in using the default credentials:

* Username: admin
* password: (from above)

![Screenshot from 2025-03-02 23-07-31](https://github.com/user-attachments/assets/02e6d20e-1275-418f-bc35-d1dbfeafe61e)

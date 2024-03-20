# Assignment 2
---------------------
## csd4140 | Antonia Krasoudaki


### Task 1

* a  )
  
Apply manifest and start the pod using the command :

  kubectl apply -f task1.yaml

 ![1](task1/1_a.png)

 * b )
   
Forward to localhost port 80 using the command : kubectl port-forward taskpod 8080:80

 ![1](task1/1_b_2.png)
 ![1](task1/1_b_1.png)

 * c )
   
To view the logs we use the command : kubectl logs taskpod
 ![1](task1/1_c.png)

  * d )
  * 
Create the shell session with the command: kubectl exec -it taskpod  -- //bin//sh
 ![1](task1/1_d_1.png)

Modify the html file:
 ![1](task1/1_d_2.png)

Localhost after modifying : 

 ![1](task1/1_d_3.png)

 * e )

Copy html file from container to local machine with the command : kubectl cp taskpod:usr/share/nginx/html/index.html ./index.html
Copy modified html file from local machine to container with the command : kubectl cp ./index.html taskpod:usr/share/nginx/html/index.html

  ![1](task1/1_e_1.png)

Modified page:

  ![1](task1/1_e_2.png)

* f )

Stopping the pod and removing the yaml file with the command : kubectl delete -f task1.yaml

 ![1](task1/1_f.png)



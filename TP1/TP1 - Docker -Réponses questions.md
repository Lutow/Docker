Answers for TP1 - Docker questions:

Question 1-1: For which reason is it better to run the container with a flag `-e` to give the environment variables rather than put them directly in the Dockerfile?

`-e` is the shorten name for `-env` which allows the user to set the environment variables. It doesn't hide the value but avoid to hardcome them in a file.

Question 1-2: Why do we need a volume to be attached to our postgres container?

We use a volume attached to our database container to make the data persistent. Hence, database is stored within a directory on the Docker host called pgdata. If we delete the container, the volume still exists, meaning the database content inside the volume is preserved.

Question 1-3: Document your database container essentials: commands and Dockerfile.



Question 1-4: Why do we need a multistage build? And explain each step of this dockerfile.

The `myapp-build` compile the source code with Maven, creating the numerous associated files while the second one copies and run the final code of the previous build, without needing to compile again using Maven or any other compiler. This multistage build results in a lighter image size and a faster deployment. If we tried to build using a single image, we would have got the JDK, the source code plus all the dependencies and additionnal configuration files. In our case, this result in a smoother execution.

 


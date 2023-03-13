# Step to the beginning 

### Step 1: Create a DockerFile With
- FROM: The name of the base image to use.
```
FROM python:3.7
```
- COPY: Copy files or folders from source to the dest path in the image's filesystem.
```
COPY hello.txt /absolute/path
```
- Wokdir: Set the working directory for any subsequent ADD, COPY, CMD, ENTRYPOINT, or RUN instructions that follow it in the Dockerfile.
```
WORKDIR /path/to/workdir
```
- RUN: Execute any commands on top of the current image as a new layer and commit the results.
```
RUN pip install -r requirements
```
- CMD: Provide defaults for an executing container. If an executable is not specified, then ENTRYPOINT must be specified as well. There can only be one CMD instruction in a Dockerfile.
```
CMD ["python","app.py"] 
```

### Step 2: Build a Docker Image
```
docker build -t <image-name> .
```

Now Docker image ready for use.

Just write the following command on your terminal:
```
docker run -d -p 5000:8000 <docker image name>
```
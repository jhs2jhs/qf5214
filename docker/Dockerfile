# change to other base image if needed
FROM jupyter/base-notebook 

# setup working directory in container
WORKDIR /usr/src/app

# copy local volume to container and install requirements
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# expose port and run jupyter notebook
EXPOSE 8888
CMD ["jupyter", "notebook", "--ip='*'", "--port=8888", "--no-browser", "--allow-root"]

# use bellow cmds to build image
# cd docker
# ls -lh # make sure Dockerfile is in the directory
# docker build -t my-qf5214-image -f Dockerfile .
# cd ..
# ls -lha # make sure notebook directory is in the directory
# docker run --name qf5214 -p 8888:8888 -v ./notebook:/usr/src/app my-qf5214-image
# if you are using windows, please use correct path in windows. you can use "pwd" command to find the current full path, and then you can replace it with ./notebook. 

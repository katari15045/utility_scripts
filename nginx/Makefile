CONTAINER_NAME?=helloworld_ui
IMAGE_NAME?=helloworld_ui

build_image:
	docker build -t ${IMAGE_NAME} .

start_container:
	docker run -d \
		--name ${CONTAINER_NAME} \
		--network host \
		${IMAGE_NAME}

run: build_image start_container

clean:
	- docker stop ${CONTAINER_NAME}
	- docker rm ${CONTAINER_NAME} 
	- docker rmi ${IMAGE_NAME}

USERNAME = gr00vysky
IMAGE_NAME = devops-agent-multi-arch
  
.PHONY: build  
  
build:  
	docker buildx build --platform linux/amd64 --build-arg TARGETARCH=linux-x64 --push -t $(USERNAME)/$(IMAGE_NAME):amd64 .;
	docker buildx build --platform linux/arm64 --build-arg TARGETARCH=linux-arm64 --push -t $(USERNAME)/$(IMAGE_NAME):arm64 .;
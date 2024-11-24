USERNAME = gr00vysky
IMAGE_NAME = devops-agent-multi-arch
TARGETARCHS = amd64 arm64  
  
.PHONY: build push  
  
build:  
	$(foreach arch,$(TARGETARCHS), docker build --build-arg TARGETARCH=linux-$(arch) -t $(USERNAME)/$(IMAGE_NAME):$(arch) . ;)  
  
push:  
	$(foreach arch,$(TARGETARCHS), docker push $(USERNAME)/$(IMAGE_NAME):$(arch) ;)  
#DockerTF
https://github.com/OT-BUILDPIPER-MARKETPLACE/BP-OT-AWS-TF-MODULES-STEP
https://github.com/OT-BUILDPIPER-MARKETPLACE/BP-NETWORK-SKELETON-STEP/tree/v0.1
https://github.com/opstree/spring3hibernate/tree/master/terraform/network_skeleton

image versions
#build.sh --> change workspace step --> BP-OT-AWS-TF-MOD..
Dockerfile --> Network Skeleton --> ADD NETWORK_SKELETON /opt/buildpiper/modules/NETWORK_SKELETON


docker run -it --rm -v $PWD:/src -e WORKSPACE=/src -e CODEBASE_DIR=/src -e TF_CODE_LOCATION=$PWD -e AWS_ACCESS_KEY_ID=AKIARPMFOGCAKTIRIJXN -e AWS_SECRET_ACCESS_KEY=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 -e INSTRUCTION=plan ot/tf-network-skeleton-step:0.0.1

debug::
docker run -it --rm -v $PWD:/src -e WORKSPACE=/src --entrypoint sh ot/tf-network-skeleton-step:0.1


docker run -it --rm -v $PWD:/src -e WORKSPACE=/src -e AWS_ACCESS_KEY_ID=AKIARPMFOGCAKTIRIJXN -e AWS_SECRET_ACCESS_KEY=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 -e INSTRUCTION=plan ot/tf-network-skeleton-step:0.1


docker build -t ot/tf-dynamodb-step:0.1 .
docker run -it --rm -v $PWD:/src -e WORKSPACE=/src -e AWS_ACCESS_KEY_ID=AKIARPMFOGCAKTIRIJXN -e AWS_SECRET_ACCESS_KEY=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 -e INSTRUCTION=plan ot/tf-dynamodb-step:0.1


docker build -t ot/tf-efs-step:0.1 .
docker run -it --rm -v $PWD:/src -e WORKSPACE=/src -e AWS_ACCESS_KEY_ID=AKIARPMFOGCAKTIRIJXN -e AWS_SECRET_ACCESS_KEY=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 -e INSTRUCTION=plan ot/tf-efs-step:0.1

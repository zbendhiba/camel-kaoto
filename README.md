# camel-kaoto
Demo of kaoto for Apache Camel

Connect to your openshift cluser

Create your secret ==> make sure you have your env variables set

mkdir -p target
cat s3-dev.camel.yaml | envsubst > target/s3.camel.yaml
cat users-dev.camel.yaml | envsubst > target/users.camel.yaml
kamel run --trait jolokia.enabled=true target/users.camel.yaml
rm target




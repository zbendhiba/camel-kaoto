# camel-kaoto
Demo of kaoto for Apache Camel

Connect to your openshift cluser

Create your secret ==> make sure you have your env variables set

oc delete secret s3-secret
mkdir -p target
cat s3.properties | envsubst > target/application.properties
kamel run --build-property file:target/application.properties --trait jolokia.enabled=true users.camel.yaml
rm target/application.properties

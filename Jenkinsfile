pipeline
{
agent any
stages{
stage("maven build"){
when{
branch 'develop'
}
steps{
sh"mvn clean package"
}
}
stage("Sonar Analysis"){
when{
branch 'develop'
}
steps{
  echo "Sonar Analysis"
}
}
stage("Deploy to dev and test"){
when{
branch 'develop'
}
steps{
  echo "deploying to development"
  echo "deploying to test"
}
}
stage("Deploy to UAT"){
when{
branch 'uat'
}
steps{
  echo "deploying to production"
}
}
stage("deploy to prod"){
when{
branch 'master'
}
steps{
  echo "deploying to production"
}
}
stage("upload to Nexus"){
when{
branch 'develop'
}
steps{
  echo "upload war file to nexus analysis"
}
}
}
}

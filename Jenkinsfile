
pipeline {

agent any

stages {


stage('Build') {
steps {
build 'PES2UG21CS106'
sh 'g++ main.cpp -o output'

}

}
stage('Test') {

steps {
s './output'
}

}

stage ('Deploy') {
steps {
echo 'deploy'


}
}
}
post{

failure{
 error 'Pipeline Failed'
}
}
}

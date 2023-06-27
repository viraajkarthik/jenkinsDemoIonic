pipeline{
    agent any
    environment {
        PATH=''
    }

    stages{
        stage('NPM Setup'){
            steps{
                sh 'npm install'
            }
        }

        stage('IOS Build'){
            steps{
                sh 'ionic cordova build ios --release'
            }
        }

        stage('Android Build'){
            steps {
                sh 'ionic cordova build android --release'
            }
        }

        stage('APK Sign'){
            steps {
               echo "Android"
            }
        }

        stage('Stage Web Build'){
            steps {
                sh 'npm run build --prod'
            }
        }

        stage('Publish Firebase Web'){
            steps{
                echo 'Firebase Deploy'
            }
        }

        stage('Publish ioS'){
            steps {
                echo "Publish ios"
            }
        }

        stage('Publish Android'){
            steps{
                echo "Publish Android"
            }
        }
    }
}
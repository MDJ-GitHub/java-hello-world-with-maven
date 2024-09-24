pipeline {

    agent any

    tools {
        jdk 'JAVA_HOME'   // Ensure that 'JAVA_HOME' is defined in Jenkins Global Tool Configuration
        maven 'M2_HOME'   // Ensure that 'M2_HOME' is defined in Jenkins Global Tool Configuration
    }

    stages {

        stage('GIT') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/hwafa/timesheetproject.git'
            }
        }

        stage('Compile Stage') {
            steps {
                sh 'mvn clean compile'
            }
        }
    }
}

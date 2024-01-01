pipeline {
    agent any

    stages {
        stage('SCM Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/H4rsh99/scylladb_role.git'
            }
        }

        stage('Execution') {
            steps {
                script {
                    sh 'ansible-playbook -i scylla/tests/aws_ec2.yml scylla/tests/playbook.yml'
                }
            }
        }
    }
}

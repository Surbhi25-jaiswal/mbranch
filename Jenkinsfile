 steps {
                echo 'Test App'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy App'
            }
        }
    }
    post {
        always {
            emailext body: 'summary', subject: 'pipeline status', to: 'surbhijaiswal013@gmail.com'
        }
    }
}

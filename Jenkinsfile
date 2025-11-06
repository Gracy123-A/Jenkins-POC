pipeline {
    agent any

    stages {
        stage('Copy HTML to Apache') {
            steps {
                // Copy index.html to Apache's web directory
                sh 'sudo cp index.html /var/www/html/index.html'

                // Restart Apache to apply changes
                sh 'sudo systemctl restart apache2'
            }
        }

        stage('Verify') {
            steps {
                echo 'Your site should be live at: http://localhost/index.html'
            }
        }
    }
}

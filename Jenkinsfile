pipeline {
    
    agent {
        label 'agent-vm'
    }


    stages {
        stage('Install apache2'){
            steps {
                echo "Installing Apache2..."
                sh "sudo apt-get install -y apache2"
                echo "Apache2 installed."
            }
        } 
        stage('Copy'){
            steps {
                echo "Copying files..."
                sh "sudo cp index.html /var/www/html/"
                echo "Files copied."
            }
        }
        stage('Restart Apache2'){
            steps {
                echo "Stop Apache2 if it is running..."
                sh "sudo systemctl restart apache2"
            }
        }
   }
}



pipeline {
    
    agent {
        label 'agent-vm'
    }
    
    environment{
        IMAGE_NAME = "mon-image-site-web"
        CONTENEUR_NAME = "mon-conteneur-site-web"
    }


    stages {
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


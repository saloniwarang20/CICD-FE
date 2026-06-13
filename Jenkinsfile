Pipeline{
    Stages{
        Stage('Install'){
            Steps{
                sh 'npm install'
            }
        }
        Stage('Build'){
            Steps{
                sh 'npm run build'
            }
        }
        Stage('Deploy'){
            Steps{
                echo 'Deploying...'
                sh '''
                cp -r dist/* /var/www/html/
                sudo systemctl restart nginx
                '''
            }
        }
    }
}
pipeline{
    agent any
    stages{
        stage('Print Info'){
            steps{
                sh 'echo "Branch: "'
                sh 'echo "Hash: "'
                sh 'echo "g++ version: "'
            }
        }
        stage('Build Executable file'){
            steps{
                // Компилируем main.cpp и сохраняем результат в файл main
                sh 'g++ main.cpp -o main'
            }
        }
        stage('Application Launch Test'){
            steps{
                // Запускаем исполняемый файл main из текущего каталога
                sh './main'
            }
        }
    }
}

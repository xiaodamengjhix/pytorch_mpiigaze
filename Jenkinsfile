pipeline {
    agent any  // 使用任意可用节点（不需要Docker）
    
    stages {
        // 阶段1：拉取代码（自动完成，无需配置）
        
        // 阶段2：运行测试
        stage('Run Hello Test') {
            steps {
                // Windows 用 bat，Linux 用 sh
                bat 'python hello_test.py'
                
                // 可选：验证文件路径
                bat 'dir /b'  
            }
        }
    }
    
    post {
        always {
            echo '测试完成，请查看控制台输出'
        }
    }
}
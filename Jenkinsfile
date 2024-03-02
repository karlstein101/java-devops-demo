import org.springframework.core.env.Environment

//写流水线的脚本（声明式、脚本式）
pipeline{
    //全部的CICD流程都需要在这里定义

    //任何一个代理可用就可以执行
    agent any

    //定义一些环境信息
    Environment{
        hello="123456"
        world="456789"
    }

    //定义流水线的加工流程
    stages{
        //流水线的所有阶段
        //1、编译 "abc"
        //一般单引号写常量，双引号可以写变量
        stage('编译'){
            steps{
                //要做的所有事情
                echo "编译"
                echo "$hello"
                echo "${world}"
                sh 'pwd && ls -alh'
                sh 'printenv'

            }
        }

        //2、测试
        stage('测试'){
            steps{
                //要做的所有事情
                echo "测试"
            }
        }

        //3、打包
        stage('打包'){
            steps{
                //要做的所有事情
                echo "打包"
            }
        }

        //4、部署
        stage('部署'){
            steps{
                //要做的所有事情
                echo "部署"
            }

        }

    }

}

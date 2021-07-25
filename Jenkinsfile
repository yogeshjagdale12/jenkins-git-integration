node('master') 
{
    stage('Checkout') 
    {
CheckoutFunc(GitBranch, GitRepo)
    }
}
    
    def CheckoutFunc(String GitBranch, String GitRepo)
    {
     checkout([
        $class: 'GitSCM', 
        branches: [[name: GitBranch]], 
        doGenerateSubmoduleConfigurations: false, 
        extensions: [[$class: 'CleanCheckout']], 
        submoduleCfg: [], 
        userRemoteConfigs: [[url: GitRepo]]
        ])   
    }

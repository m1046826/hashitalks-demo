#!/usr/bin/env groovy

node() {
  timestamps {
    
     environment {
        env.VAULT_ADDR = 'http://35.175.113.232:8200/'
        env.VAULT_TOKEN = 's.D5MasWJ9m50TIBUxSMBe2nSF'
    }
      
     stage ('Create Wrapped Secret ID') {
      def WRAPPED_SID = ""
      env.WRAPPED_SID = sh(
        returnStdout: true,
        script: "vault write -field=wrapping_token -wrap-ttl=200s -f auth/pipeline/role/pipeline-approle/secret-id"
      )
    }
  }
}

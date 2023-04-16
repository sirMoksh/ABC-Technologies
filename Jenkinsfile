job('job-checkout') {
    
    scm {
        github('sirMoksh/DevOpsClassCodes', 'main')
    }
      
   publishers {
        downstream 'job-compile', 'SUCCESS'
    }
    
}
job('job-compile'){
   
  scm {
        github('sirMoksh/DevOpsClassCodes', 'main')
    }

  steps{
  maven('compile')
  }
 publishers {
        downstream 'job-test', 'SUCCESS'
   }
}

job('job-test'){
   
  scm {
        github('sirMoksh/DevOpsClassCodes', 'main')
    }
  steps{
   maven('test')
  }
 publishers {
        downstream 'job-package', 'SUCCESS'
   }
}

job('job-package'){
   
   scm {
        github('sirMoksh/DevOpsClassCodes', 'main')
    }
  steps{
  maven('package')
  }
}

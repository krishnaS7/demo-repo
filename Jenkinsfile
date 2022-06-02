pipeline
{
agent any
environment
  {
    NEW_Version = '1.0'
  }
stages
{
  stage("build"){
  when 
  {
    expression
    {
      BRANCH_NAME == 'dev' || BRANCH_NAME == 'main' 
    }
  }
    steps
    {
      echo "first build run"
      echo "building test with version ${NEW_Version}"
      echo "Branch name is ${BRANCH_NAME}"
    }
  }
 stage("test")
  {
    steps
    {
      echo "first test run"
      echo "building test with version ${NEW_Version}"
    }
  }
}
}

pipeline
{
agent any
environment
  {
    NEW_Version = '1.0'
  }
  parameters{
  choice(name:'Version',choices:['1.0','2.0','3.0'],description:'')
  booleanParam(name:'executeTests',defaultValue:true,description:'')
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
    when 
  {
    expression
    {
      paarams.executeTests
    }
  }
    steps
    {
      echo "first test run"
      echo "building test with version ${NEW_Version}"
    }
  }
}
}

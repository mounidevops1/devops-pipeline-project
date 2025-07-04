# devops-pipeline-project
A basic DevOps project using GitHub Actions
#!/bin/bash
echo "Hello from DevOps Pipeline!"
name: Run Hello Script

on:
  push:
    branches: [ main ]

jobs:
  run-script:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout code
      uses: actions/checkout@v2

    - name: Run hello.sh script
      run: bash hello.sh
      

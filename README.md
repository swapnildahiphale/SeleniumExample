    # Ready example to run the SeleniumExample tests
    ```
    docker pull swapnildahiphale/selenium-example
    docker run -v /tmp/test-report:/usr/share/app/target/surefire-reports -e TEST_URL=http://<IP>:<port>/ selenium-example:headless
    ```
    
    # Extend the example for your tests
    
    - Modify the selenium tests
    
    - Change the pom.xml as needed
    
    - Modify the Dockerfile to run the tests as needed
    
        Eg: Modify the CMD command as below:
    
        CMD ["mvn", "test"]
    
    - Build new docker image
    
      docker build -t my-selenium-tests
    - Run docker
        ```
        docker run -v /tmp/test-report:/usr/share/app/target/surefire-reports -e TEST_URL=http://<ip>:<port>/  my-selenium-tests
        ```
    - Result
     JUnit results are stored in `/tmp/test-report` directory.

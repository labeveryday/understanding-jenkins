# understanding-jenkins

Repo to learn building a jenkins pipeline utilizing https://joachim8675309.medium.com/jenkins-ci-pipeline-with-python-8bf1a0234ec3

1. First install java

    ```bash
    sudo apt install default-jre
    ```

2. Next add the jenkins key

    ```bash
    wget -q -O - https://pkg.jenkins.io./debian-stable/jenkins.io.key | sudo apt-key add -
    ```

3. Add the jenkins repo

    ```bash
    sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
    ```

4. Get the repo list

    ```bash
    sudo apt update
    ```

5. Install jenkins (At this point jenkins is installed, but you still need to start the service)

    ```bash
    sudo apt install jenkins
    ```

6. Start the jenkins server

    ```bash
    sudo service jenkins start
    ```

7. Check status

    ```bash
    sudo service jenkins status
    ```

8. Give Jenkins admin creds

    ```bash
    sudo visudo

    # Add this to the last line
    jenkins ALL=(ALL) NOPASSWD:ALL


    # Then run this command and copy your jenkins sign key
    sudo cat /var/lib/jenkins/secrets/initialAdminPassword


    ```

9. After logging into `<ip>:8080` add plugins `Blue Ocean` and `GitHub Pipeline for Blue Ocean` then click `install without restart`

10. Once installed go to `<ip>:8080/blue`

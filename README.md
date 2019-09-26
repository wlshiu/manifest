# manifest
repo manifest.xml

+ generate SSH key

    ```
    $ ssh-keygen -t rsa -C "your mail address"
    ```

+ add SSH key (**id_rsa.pub**) to gitlab server
    > profile settings -> SSH Key

+ try to communicate gitlab server

    ```
    $ ssh -T git@gitlabserver.com
    ...
    Welcome to GitLab
    ```

+ download `repo`

    ```
    $ mkdir ~/.bin
    $ curl https://storage.googleapis.com/git-repo-downloads/repo > ~/.bin/repo
    $ sudo chmod a+x ~/.bin/repo
    ```

+ download source code

    ```
    $ repo init -u git@gitlabserver.com:xxx/manifests.git -b master -m default.xml
    $ repo sync
    $ repo start local/test --all
    ```


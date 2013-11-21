to obtain this instruction, do this:

   $ git clone git@github.com:kazurayam/ChefSoloLesson.git

--------------------------------------------------------------------
Login into the AWS EC2 instance:

      in you command-line, do this:

      	 $ ssh -i <your pem file> ec2-user@<the Public DNS of your instance>

 	 for example

	 $ ssh -i Downloads/KazuakiUrayamaKP.pem ec2-user@ec2-54-238-178-103.ap-northeast-1.compute.amazonaws.com



How to install Emacs into AWS EC2 instance:

    $ cd
    $ sudo yum -y install emacs



How to install Git client into AWS EC2 instance:

    * remember you need IP port #9418 to be open in the security
    group outbound from the server to the Internet, plus #80 HTTP and
    #443 HTTPS 

    change directory to home

        $ cd

    use yum to install the git-core, the root privillage will be required

        $ sudo yum install git-core

    verify if installed

        $ git -h


How to install Chef-Solo:

    download the Chef-Solo installer script from the OpsCode web site,
    then execute it.

    	     $ cd
	     $ curl -L http://www.opscode.com/chef/install.sh | sudo bash



Clone the sample Chef-Solo repository provided by OpsCode

       $ git clone git://github.com/opscode/chef-repo.git

       you will have ./chef.repo



Clone my ChefSoloLesson repository provided by me
 
       $ git clone git@github.com:kazurayam/ChefSoloLesson.git

Setup chef-repo with prepared files

    $ cd
    $ cd ./ChefSoloLesson
    $ ./setup	

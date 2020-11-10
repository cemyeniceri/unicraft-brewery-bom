https://blog.10pines.com/2018/06/25/publish-artifacts-on-maven-central/
https://central.sonatype.org/pages/apache-maven.html
run
 mvn clean install -P ossrh -Dgpg.passphrase=<pwd>
 mvn deploy

in case of "gpg: signing failed: Inappropriate ioctl for device" error, 
run the following commands in turn :
export GPG_TTY=$(tty) 
echo "test" | gpg --clearsign
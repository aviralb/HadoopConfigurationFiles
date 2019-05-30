# HadoopConfigurationFiles

These are the port number of hadoop
http://localhost:8088/cluster
http://localhost:50070/
http://localhost:19888/jobhistory

First I downloaded Java JDK and Hadopp 2.7.7 Version By Using Below Command 
and Unzip them ,Setup the path variable 

wget https://download.java.net/openjdk/jdk8u40/ri/jdk_ri-8u40-b25-linux-x64-10_feb_2015.tar.gz


wget http://mirrors.estointernet.in/apache/hadoop/common/hadoop-2.7.7/hadoop-2.7.7.tar.gz

************************After Download ********************
extract downloded file and save them in another folder 
find the path of these file and set up the path variables 

**************************SettingUp Path Variable*******************
gedit ~/.bashrc

export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.212.b04-0.el7_6.x86_64
export PATH="$PATH":"$JAVA_HOME"/bin
export HADOOP_HOME=/home/student/hadoop-2.7.3
export PATH="$PATH":"$HADOOP_HOME"/bin:"$HADOOP_HOME"/sbin


source ~/.bashrc


************************Checking The File Path is Ok Or Not****************
echo $JAVA_HOME
echo $PATH
echo $HADOOP_HOME
echo $PATH

********************Setting up System File Of Hadoop***************

Go to the this path and change some configuration file which are in the link below

/home/hadoop/openfile/hadoop-2.7.7/etc/hadoop

files for hadoop which you can download from here

https://github.com/aviralb/HadoopConfigurationFiles
or 
https://github.com/aviralb/HadoopConfigurationFiles/tree/master/configuration-files




*************************SSH Key-generator****************************

ssh-keygen -t rsa -P '' -f ~/.ssh/id_rsa

cat ~/.ssh/id_rsa.pub>> ~/.ssh/authorized_keys

ssh localhost
*************************Sarting Hadoop Serives ****************

hdfs namenode -format
ssh localhost

*******************Starting Hadoop**************
jps
start-dfs.sh
jps
start-yarn.sh
jps
mr-jobhistory -daemon.sh start historyserver
mr-jobhistory-daemon.sh start historyserver
jps

****************Url For Hadoop Cluster************************

http://localhost:8088/cluster
http://localhost:50070/
http://localhost:19888/jobhistory

**************then bingo*****************

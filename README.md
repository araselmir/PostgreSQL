<h1>What is postgreSQL ? </h1>
PostgreSQL is a powerful, open source object-relational database system that uses and extends the SQL language combined with many features that safely store and scale the most complicated data workloads. The origins of <a href="https://www.postgresql.org/">PostgreSQL</a>  date back to 1986 as part of the POSTGRES project at the University of California at Berkeley and has more than 30 years of active development on the core platform.
</br>
</br>
PostgreSQL has earned a strong reputation for its proven architecture, reliability, data integrity, robust feature set, extensibility, and the dedication of the open source community behind the software to consistently deliver performant and innovative solutions. PostgreSQL runs on <a href="https://www.postgresql.org/download/">all major operating systems</a> , has been <a href="https://en.wikipedia.org/wiki/ACID">ACID</a> -compliant since 2001, and has powerful add-ons such as the popular PostGIS geospatial database extender. It is no surprise that PostgreSQL has become the open source relational database of choice for many people and organisations.
</br>
</br>
<a href="https://www.postgresql.org/docs/current/tutorial.html">Getting started</a> with using PostgreSQL has never been easier - pick a project you want to build, and let PostgreSQL safely and robustly store your data.
</br>
</br>
<h1> Why use PostgreSQL?</h1>
PostgreSQL comes with <a href="https://www.postgresql.org/about/featurematrix/">many features</a>  aimed to help developers build applications, administrators to protect data integrity and build fault-tolerant environments, and help you manage your data no matter how big or small the dataset. In addition to being<a href="https://www.postgresql.org/about/license/">free and open source</a> , PostgreSQL is highly extensible. For example, you can define your own data types, build out custom functions, even write code from<a href="https://www.postgresql.org/docs/current/xplang.html">different programming languages</a>  without recompiling your database!
</br>
</br>
PostgreSQL tries to conform with the <a href="https://www.postgresql.org/docs/current/features.html">SQL standard</a>  where such conformance does not contradict traditional features or could lead to poor architectural decisions. Many of the features required by the SQL standard are supported, though sometimes with slightly differing syntax or function. Further moves towards conformance can be expected over time. As of the version 12 release in October 2019, PostgreSQL conforms to at least 160 of the 179 mandatory features for SQL:2016 Core conformance. As of this writing, no relational database meets full conformance with this standard.
</br>
</br>
<h1> PostgreSQL Install </h1>
</br>
<h3> 1. Windows </h3>
<a href="https://www.enterprisedb.com/downloads/postgres-postgresql-downloads">Download the installer</a> certified by EDB for all supported PostgreSQL versions.
</br>
This installer includes the PostgreSQL server, pgAdmin; a graphical tool for managing and developing your databases, and StackBuilder; a package manager that can be used to download and install additional PostgreSQL tools and drivers. Stackbuilder includes management, integration, migration, replication, geospatial, connectors and other tools.
</br> </br>
This installer can run in graphical or silent install modes.
</br> </br>
The installer is designed to be a straightforward, fast way to get up and running with PostgreSQL on Windows.
</br> </br>
Advanced users can also download a <a href="https://www.enterprisedb.com/download-postgresql-binaries">zip</a>  archive of the binaries, without the installer. This download is intended for users who wish to include PostgreSQL as part of another application installer.
</br></br>
<h3> 2. Ubuntu </h3>
PostgreSQL is available in all Ubuntu versions by default. However, Ubuntu "snapshots" a specific version of PostgreSQL that is then supported throughout the lifetime of that Ubuntu version. Other versions of PostgreSQL are available through the PostgreSQL apt repository.
</br></br>
<pre id="script-box" class="code">
# Create the file repository configuration:
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" &gt; /etc/apt/sources.list.d/pgdg.list'

#Import the repository signing key:
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -

#Update the package lists:
sudo apt-get update

#Install the latest version of PostgreSQL.
#If you want a specific version, use 'postgresql-12' or similar instead of 'postgresql':
sudo apt-get install postgresql</pre>
For more information about the apt repository, including answers to frequent questions, please see the <a href="https://wiki.postgresql.org/wiki/Apt">PostgreSQL Apt Repository</a>  page on the wiki.
</br>
<h3> 3. Mac OS </h3>
</br>
PostgreSQL is the default database on macOS Server as of OS X Server version 10.7. macOS without the macOS Server add-on installed includes only the PostgreSQL libpq shared library.
</br>
macOS Server 10.12 ships with PostgreSQL 9.4. Minor updates are provided by Apple, but not necessarily right after a new PostgreSQL minor release.
</br>
There are several other installers available for PostgreSQL on macOS, which is the recommended way to install.
</br>
<a href="https://www.enterprisedb.com/downloads/postgres-postgresql-downloads">Download the installer</a> certified by EDB for all supported PostgreSQL versions.
</br>
Advanced users can also download a<a href="https://www.enterprisedb.com/download-postgresql-binaries"> zip</a> archive of the binaries, without the installer. This download is intended for users who wish to include PostgreSQL as part of another application installer.
<h1> Basic Comands in Windows </h1>
First of all open the SQL Shell(psql)
</br>
<p>If <code>login</code> option is not given, the role is not permitted to login. Similarly, other options give permission of the features to the roles.</p>
</br>
<p>For adding password separately the following command can be used:</p>
</br><pre><code>\password USER_NAME

</code></pre>
<p>Then password and confirmation of password will be asked. Note that, whatever you type in the command will not be shown. The same command can be used for password update as well.</p>
<h2> Conecting to the DB Server </h2>
<p>From Command Prompt an user can connect with the following command:</p>
<code>psql -d database_name -U user_name

</code>
<p>For remote login, host and port should also be given:</p>
<code>
psql -h host_name -p port_name -U user_name database_name

</code>
</br>
<p>Now type command  <code> help </code> </p>

![Screenshot (11)](https://user-images.githubusercontent.com/62602944/90256036-ecda9580-de66-11ea-93d8-c89a77e1a545.png)

<p> For help with psql comands type  <code> \? </code> </p>

![Screenshot (12)](https://user-images.githubusercontent.com/62602944/90263650-c3733700-de71-11ea-91f0-6b9ed7762945.png)

<p> Show the list of database type <code> \l </code> </p>

![Screenshot (13)](https://user-images.githubusercontent.com/62602944/90263670-c9691800-de71-11ea-86f2-c63e82d13835.png)

<p> For create Database type <code> CREATE DATABASE database_name; </code> </p>

![Screenshot (14)](https://user-images.githubusercontent.com/62602944/90263682-cec66280-de71-11ea-8f83-6c3c438b0b08.png)

<p> For delete database type <code> DROP DATABASE database_name; </code></p>

![Screenshot (16)](https://user-images.githubusercontent.com/62602944/90263717-dd147e80-de71-11ea-822c-996da3821d5c.png)

<p> If you want to connect any databse type <code> \c database_name </code></p>

![Screenshot (18)](https://user-images.githubusercontent.com/62602944/90263764-ec93c780-de71-11ea-8b5a-0f2c0dcdfb7b.png)

<p> If you create database table type </p> </br><pre>
<code> CREATE TABLE table_name (
col_name_01 data_type if_any,
col_name_02 data_type if_any,
col_name_03 data_type if_any,
col_name_04 data_type if_any,
);
</code></pre>

![Screenshot (20)](https://user-images.githubusercontent.com/62602944/90263799-fb7a7a00-de71-11ea-89e9-863fc15b0a71.png)

<p> If you want to see list of relation type <code> \d </code> </p>
  
![Screenshot (21)](https://user-images.githubusercontent.com/62602944/90263822-0208f180-de72-11ea-93b6-af3ea78d2231.png)
  
<p> If you want to see database table type<code> \d table_name </code> </p>

![Screenshot (22)](https://user-images.githubusercontent.com/62602944/90263843-07663c00-de72-11ea-8050-91908165b670.png)

<p> If you want to add table valu type </p> </br><pre>
<code> INSERT INTO table_name (col_01,col_02,col_03.....)        
VALUES ('col_01_values','col_02_values','col_03_values',......);</code></pre>

![Screenshot (23)](https://user-images.githubusercontent.com/62602944/90263855-0c2af000-de72-11ea-89ff-74f48830fa25.png)

<p> If want to see the full table type  <code> SELECT * FROM table_name; </code></p>

![Screenshot (24)](https://user-images.githubusercontent.com/62602944/90263863-10efa400-de72-11ea-9f1d-5a69520e3c56.png)

<p> If you want to delete table type <code> DROP TABLE table_name;</code> </p>
  
![Screenshot (25)](https://user-images.githubusercontent.com/62602944/90263873-15b45800-de72-11ea-8500-5d52a6ae058e.png)
  
  


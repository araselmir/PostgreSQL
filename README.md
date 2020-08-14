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


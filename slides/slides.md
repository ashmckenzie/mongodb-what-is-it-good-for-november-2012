!SLIDE bullets

![MongoDB](mongodb.png)

# What is it (good for) ? #


!SLIDE bullets

# What is MongoDB ? #

* [Document oriented database](http://en.wikipedia.org/wiki/Document-oriented_database)
* Considered a 'NoSQL' database system
* [Originally one piece of a PaaS](http://en.wikipedia.org/wiki/MongoDB#History) but proved very popular
* Mongo comes from 'hu**mongo**us', developed by [10gen](http://10gen.com)


!SLIDE bullets

# Why MongoDB ? #

* Rapid software development due to 'schema-less' design
* No concept of migrations (good and bad)
* Onus is on developer to ensure schema consistency
* Great Ruby ODM libraries - [Mongoid](http://mongoid.org), [MongoMapper](http://mongomapper.com)
* Fun to use!


!SLIDE bullets

# Features #

* Stores data in JSON format (awseome!)
* Supports indexing (primary, secondary, compound)
* Sharding support out-of-the-box
* JavaScript style querying (weird at first)


!SLIDE bullets smbullets

# Basics #

* Database == Database
* Collection == Table
* Document == Row
* Each Document has an `_id` (ObjectId)


!SLIDE bullets smbullets

# ObjectId #

* An ObjectId is a unique identifier and made up of

e.g. 47cc67093475061e3d95369d

<table>
  <tr>
    <td>47cc6709</td>
    <td>347506</td>
    <td>1e3d</td>
    <td>95369d</td>
  </tr>
  <tr>
    <td>Signed epoch (4b)</td>
    <td>First three bytes of MAC MD5 (3b)</td>
    <td>PID of client process (2b)</td>
    <td>Incrementing, starts random (3b)</td>
  </tr>
</table>

!SLIDE bullets

# The mongo shell #

    @@@sh
    $ mongo trawler
    MongoDB sh version: 2.2.1
    connecting to: trawler
    >


!SLIDE

# mongo sh quickies #

<table>
  <tr>
    <td><pre class="sh_sourceCode sh_javascript"><code>help</code></pre></td>
    <td>Lists available help</td>
  </tr>
  <tr>
    <td><pre class="sh_sourceCode sh_javascript"><code>show dbs</code></pre></td>
    <td>Show available databases</td>
  </tr>
  <tr>
    <td><pre class="sh_sourceCode sh_javascript"><code>use trawler</code></pre></td>
    <td>Select trawler database</td>
  </tr>
  <tr>
    <td><pre class="sh_sourceCode sh_javascript"><code>db.log_entries.findOne()</code></pre></td>
    <td>Selects single Document from<br/> log_entries Collection</td>
  </tr>
  <tr>
    <td><pre class="sh_sourceCode sh_javascript"><code>db.log_entries.find({ status_code: 200 }).count()</code></pre></td>
    <td>Count the number of Documents that<br/> have a status_code of 200</td>
  </tr>
</table>

\* Most commands also support \<TAB\> completion


!SLIDE bullets

# Inserting Documents #

Insert a single Document

    @@@sh
    db.play_collection.insert({ key: 'This is our key', value: [ 1, 2, 3 ] })




!SLIDE bullets

# Updating Documents #



!SLIDE bullets

# Querying Documents #


!SLIDE bullets

# Trawler #

## MongoDB use case ##

![Trawler](trawler.png)


!SLIDE bullets

# Handy links #

* [SQL to Mongo mapping chart](http://www.mongodb.org/display/DOCS/SQL+to+Mongo+Mapping+Chart)

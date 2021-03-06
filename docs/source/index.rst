Daybed
######

Daybed is an Open Source Web API providing validation and storage as a service.


Why ?
=====

Usually, when a Web application requires a backend for storage and validation,
one of the following solutions is employed :

* A custom API is developed and deployed (*reinvent the wheel*)
* A commercial and closed-source service is used (*Google Forms*)
* A CMS is used as a backoffice for customizable content types (*twist*)

To avoid those situations and make it easy to get your storage backend ready
in seconds, we've created *Daybed*.

*Daybed* is :

* a minimalist, robust, dynamic and generic API ;
* a validation layer with schemaless storage ;
* a reusable layer of permissions logic ;
* a universal REST endpoint for Web and mobile apps ;
* a key component for rapid application building ;
* a simple service deployed and integrated without coding.


How ?
=====

#. Create a model by posting its definition (*title, fields, ...*)
#. Define the permissions sets (*modify definition, create, update or delete records, ...*)
#. Use the allocated RESTful endpoint in your application (*GET, POST, PUT, ...*)
#. Store and query records !

Since *Daybed* talks REST and JSON, you can basically use it as a remote storage with
any of your favorite technologies (*Python, Android, iOS, AngularJS, Ember.js, Backbone.js, etc.*).

.. note::

    Currently, the authentication relies on Basic authentication and `Hawk
    <https://github.com/hueniverse/hawk>`_


Use Cases
=========

* Mobile apps
* Full JavaScript apps
* Online forms
* Data Wiki
* Collaborative Web mapping

Using *Daybed* in its first versions, we built:

* `daybed-map <http://leplatrem.github.io/daybed-map/>`_, a *geo-pad* where you can create you own maps with custom fields, using `backbone-forms <https://github.com/powmedia/backbone-forms>`_
* A `password manager <https://github.com/spiral-project/daybed-keypass>`_
* A generic `CRUD application <http://spiral-project.github.io/backbone-daybed/>`_ using `backbone-daybed <https://github.com/spiral-project/backbone-daybed>`_ ;
* A `TODO list <http://daybed.lolnet.org/>`_ using `jquery-spore <https://github.com/nikopol/jquery-spore>`_ ;


Technologies
============

*Daybed* uses the following stack by default :

* `Pyramid <http://www.pylonsproject.org>`_, a robust and powerful python Web framework
* `Cornice <https://cornice.readthedocs.org>`_, a REST framework for Pyramid
* `Colander <http://colander.readthedocs.org>`_ for the schema validation part
* `Redis <http://redis.io>`_ as the default persistence backend
* `ElasticSearch <http://www.elasticsearch.org>`_ as indexing and faceted search engine
* `CouchDB <http://couchdb.apache.org>`_ as an alternative persistence backend


Comparison
==========

*Daybed* has many competitors, yet none of them shares the same approach or features set.

===========================  ======  ==================  ==========  ========  ======  ============
Strategy                             Custom              Generated              Competitors
                                     dedicated           code
                                     API
===========================  ======  ==================  ==========  ==============================
Project                              Django REST
                                     framework,
                                     Restify, express,
                             Daybed  Struts...           Python Eve  Loopback  Hoodie  Google Forms
---------------------------  ------  ------------------  ----------  --------  ------  ------------
Minimalist                   ✔       ✔
Validation                   ✔       ✔                   ✔           ✔                 ✔
Permissions                  ✔       ✔                               ✔                 ✔
Dynamic schemas              ✔                                       ✔         ✔       ✔
Reusable instance            ✔                                       ✔                 ✔
Dynamic API end-points       ✔                                       ✔
Raw data access              ✔       ✔                   ✔           ✔         ✔
Agnostic (REST)              ✔       ✔                   ✔           ✔
Requires SDK                                                                   ✔
Open Source                  ✔       ✔                   ✔           ✔         ✔
Faceted search               ✔
===========================  ======  ==================  ==========  ==============================

Sources: http://python-eve.org ; http://hood.ie ; http://loopback.io ;


More documentation
##################

.. toctree::
   :maxdepth: 2

   install
   usage
   fieldtypes
   permissions
   terminology

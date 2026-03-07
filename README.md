# awesome-etl
A curated list of notable ETL (extract, transform, load) frameworks, libraries and software.

- [Awesome ETL](#awesome-etl)
    - [Workflow Management/Engines](#workflow-managementengines)
    - [Job Scheduling](#job-scheduling)
    - [Python](#python)
    - [Ruby](#ruby)
    - [Go](#go)
    - [Java](#java)
    - [Talks/Articles](#talksarticles-1)
    - [Cloud Services](#cloud-services)
    - [Big Data (Hadoop Stack)](#big-data-hadoop-stack)
    - [ETL Tools (GUI)](#etl-tools-gui)

## Related Lists
* [awesome-pipeline](https://github.com/pditommaso/awesome-pipeline)

## Workflow Management/Engines
* [Airflow](https://github.com/apache/airflow) - "Use airflow to author workflows as directed acyclic graphs (DAGs) of tasks. The airflow scheduler executes your tasks on an array of workers while following the specified dependencies. Rich command line utilities make performing complex surgeries on DAGs a snap. The rich user interface makes it easy to visualize pipelines running in production, monitor progress, and troubleshoot issues when needed."
* [Argo](https://argoproj.github.io/) - Container based workflow management system for Kubernetes. Workflows are specified as a directed acyclic graph (DAG), and each step is executed on a container, and the latter is run on a Kubernetes Pod. There is also support for Airflow DAGs.
* [Azkaban](https://azkaban.github.io/) - "a batch workflow job scheduler created at LinkedIn to run Hadoop jobs. Azkaban resolves the ordering through job dependencies and provides an easy to use web user interface to maintain and track your workflows."
* [Dagster](https://dagster.io) - "Dagster is a data orchestrator for machine learning, analytics, and ETL. It lets you define pipelines in terms of the data flow between reusable, logical components, then test locally and run anywhere. With a unified view of pipelines and the assets they produce, Dagster can schedule and orchestrate Pandas, Spark, SQL, or anything else that Python can invoke."
* [Luigi](https://github.com/spotify/luigi) - "a Python module that helps you build complex pipelines of batch jobs. It handles dependency resolution, workflow management, visualization etc. It also comes with Hadoop support built in."
* [Mara Pipelines](https://github.com/mara/mara-pipelines) - "A lightweight opinionated ETL framework, halfway between plain scripts and Apache Airflow"
* [prefect](https://github.com/PrefectHQ/prefect) - "a workflow orchestration framework for building resilient data pipelines in Python."
* [TaskFlow](https://wiki.openstack.org/wiki/TaskFlow) - "allows the creation of lightweight task objects and/or functions that are combined together into flows (aka: workflows) in a declarative manner. It includes engines for running these flows in a manner that can be stopped, resumed, and safely reverted."
* [Temporal](https://temporal.io) - "a durable execution platform for building and running resilient workflows. A popular modern alternative to Airflow for orchestrating complex, long-running pipelines."
* [Toil](https://toil.readthedocs.io/en/latest/) - Similar to Luigi, jobs are classes with a run method. Supports executing jobs on other machines (workers) which can include AWS spot instances.

## Job Scheduling
* [Jenkins](https://github.com/jenkinsci/jenkins) - "the leading open-source automation server. Built with Java, it provides over 1000 plugins to support automating virtually anything, so that humans can actually spend their time doing things machines cannot."

## Java
* [GETL](https://github.com/ascrus/getl) - Groovy toolbox for ETL Tasks from practicing architectures
* [JSR 352](https://www.jcp.org/en/jsr/detail?id=352) - Java native API for batch processing
* [Spring Batch](https://spring.io/projects/spring-batch) - ETL on Spring ecosystem

## Python
### Libraries
* [BeautifulSoup](http://www.crummy.com/software/BeautifulSoup/) - Popular library used to extract data from web pages.
* [Bonobo](https://www.bonobo-project.org/) - Simple, modern and atomic data transformation graphs for Python 3.5+.
* [Celery](https://docs.celeryq.dev/) - "an asynchronous task queue/job queue based on distributed message passing. It is focused on real-time operation, but supports scheduling as well."
* [Dask](https://github.com/dask/dask) - Ever tried using Pandas to process data that won't fit into memory? Dask makes it easy. Dask also has functionality to make it easy to processing continuous streams of data.
* [dataset](https://dataset.readthedocs.org/en/latest/) - A wrapper around SQLAlchemy that simplifies database operations (including upserting).
* [dbt-core](https://github.com/dbt-labs/dbt-core) - "enables data analysts and engineers to transform their data using the same practices that software engineers use to build applications." The de facto standard for SQL-layer transformation in the modern data stack.
* [dlt](https://dlthub.com/docs) - "an open source Python library that makes data loading easy." Lightweight, schema-inference ELT pipelines with built-in normalization and incremental loading.
* [Great Expectations](https://docs.greatexpectations.io/) - "Always know what to expect from your data." De facto standard for data quality validation; embedded in most serious ETL pipelines.
* [hamilton](https://github.com/DAGWorks-Inc/hamilton) - Hamilton helps data scientists and engineers define testable, modular, self-documenting dataflows, that encode lineage and metadata. Runs and scales everywhere python does.
* [ijson](https://github.com/ICRAR/ijson) - Allows processing JSON iteratively (as a stream) without loading the whole file into memory at once.
* [ingestr](https://github.com/bruin-data/ingestr) - CLI tool to copy data between databases with a single command. Supports 50+ sources including Postgres, MySQL, MongoDB, Salesforce, Shopify to any data warehouse.
* [Joblib](https://joblib.readthedocs.io/) - "a set of tools to provide lightweight pipelining in Python."
* [lxml](https://github.com/lxml/lxml) - Parses XML using C libraries libxml2 and libxslt, so it's very fast. Also supports a "recover" mode that will try its best to use invalid xml or discard it. Great for large XML files and advanced functionality (like using xpaths). IBM also has a great article on high-performance parsing with lxml here: http://www.ibm.com/developerworks/library/x-hiperfparse/
* [Meltano](https://meltano.com/) - "the declarative code-first data integration engine." Open-source ELT platform built on the Singer tap/target standard; self-hosted alternative to Fivetran.
* [Pandas](http://pandas.pydata.org/) - Implements dataframes in Python for easier data processing and includes a number of tools that make it easier to extract data from multiple file formats.
* [parse](https://github.com/r1chardj0n3s/parse) - The opposite of Python's format(). Easier to use than regex, but more limited.
* [PETL](https://github.com/petl-developers/petl) - "a general purpose Python package for extracting, transforming and loading tables of data." Slower than Pandas and not as good for larger amounts of data, but simpler.
* [polars](https://github.com/pola-rs/polars) - Dataframes powered by a multithreaded, vectorized query engine, written in Rust
* [PyQuery](https://pyquery.readthedocs.io/) - Extracts data from web pages with a jquery-like syntax.
* [Requests-HTML](https://github.com/kennethreitz/requests-html) - Combines PyQuery, Requests, parse, and other libraries for a pleasant and intuitive web scraping experience.
* [Retrying](https://github.com/rholder/retrying) - Allows you to add a decorator to any function/method to retry on an exception.
* [Ruffus](https://pypi.python.org/pypi/ruffus) - "The Ruffus module is a lightweight way to add support for running computational pipelines."
* [SQLAlchemy](http://www.sqlalchemy.org/) - "the Python SQL toolkit and Object Relational Mapper that gives application developers the full power and flexibility of SQL."
* [Toolz](https://toolz.readthedocs.org/en/latest/) - "A functional standard library for python." Includes a `pipe` function that allows you to pipe a value through a sequence of functions. There's also a cython implementation here: https://github.com/pytoolz/cytoolz
* [xmltodict](https://github.com/martinblech/xmltodict) - Makes working with XML as easy as working with JSON. Also allows streaming so you don't run out of memory on large XML files. Great for simple operations on small XML files.

### Talks/Articles
* http://www.parsely.com/misc/slides/streamparse/notes/

## Ruby
* [Embulk](https://github.com/embulk/embulk) - "a parallel bulk data loader that helps data transfer between various storages, databases, NoSQL and cloud services."
* [Kiba](https://github.com/thbar/kiba) - "Data processing & ETL framework for Ruby"
* [nokogiri](https://github.com/sparklemotion/nokogiri) - an excellent XML parser that "just works"
* [Sequel](https://github.com/jeremyevans/sequel) - "The Database Toolkit for Ruby"

## Go
* [CloudQuery](https://github.com/cloudquery/cloudquery) - An open source high performance ELT Framework.
* [Pachyderm](https://github.com/pachyderm/pachyderm) - A system for running processing pipeline jobs in containers and version controlling all data using a commit-based distributed filesystem.
* [Redpanda Connect](https://www.redpanda.com/connect) - "A declarative stream processing engine for building data pipelines, formerly known as Benthos. Supports 220+ connectors."

## Javascript
* [NoFlo](http://noflojs.org/) - "a JavaScript implementation of Flow-Based Programming"

## Talks/Articles
* https://medium.com/@samson_hu/building-analytics-at-500px-92e9a7005c83
* http://www.slideshare.net/g33ktalk/data-pipeline-acial-lyceum20140624
* http://chairnerd.seatgeek.com/building-out-the-seatgeek-data-pipeline/
* http://www.garynissen.com/etl-hand-code-or-tool/
* http://www.slideshare.net/CasertaConcepts/big-data-warehousing-meetup-bigetl-trad-tool-vs-pig-vs-hive-vs-python-what-to-use-when-slide-set-2
* https://deepfriedcode.com/books/darps/index.html
* http://blog.cloudera.com/wp-content/uploads/2010/01/IntroToPig.pdf
* http://tech.adroll.com/blog/data/2015/10/15/luigi.html?adrolldev

## Cloud Services
* [Alteryx](http://www.alteryx.com/) - Cloud ETL tool with an interface similar to GUI ETL tools.
* [Amazon Simple Workflow Service (SWF)](https://aws.amazon.com/swf/) - "helps developers build, run, and scale background jobs that have parallel or sequential steps. You can think of Amazon SWF as a fully-managed state tracker and task coordinator in the Cloud."
* [AWS Batch](https://aws.amazon.com/batch/) - Allows executing jobs as containerized applications running on Amazon ECS. Also includes features for dynamically bidding for Spot Instances, integration with existing workflow engines, scheduling, monitoring, dependency modeling, and dynamic scaling/provisioning based on amount of work.
* [AWS Glue](https://aws.amazon.com/glue/) - AWS Glue generates the code (using Python and Spark) to execute your data transformations and data loading processes.
* [Cloud Data Fusion](https://cloud.google.com/data-fusion) - "Fully managed, cloud-native data integration platform."
* [Fivetran](https://www.fivetran.com/) - Fully managed ELT service that automatically moves data from 500+ sources into your data warehouse. The most widely adopted managed connector service in the modern data stack.
* [Google Dataflow](https://cloud.google.com/products/dataflow) - "Google Cloud Dataflow provides a simple, powerful model for building both batch and streaming parallel data processing pipelines."
* [Hevo](https://hevodata.com/) - Hevo is a Fully Automated, No-code Data Pipeline Platform that supports 150+ ready-to-use integrations across Databases, SaaS Applications, Cloud Storage, SDKs, and Streaming Services.
* [Microsoft Azure Data Factory](https://azure.microsoft.com/en-us/services/data-factory/) - "A fully managed, serverless data integration service that helps you visually integrate data sources with more than 90 built-in, maintenance-free connectors."
* [Stitch](https://www.stitchdata.com/) - "Stitch is a cloud-first, open source platform for rapidly moving data. A simple, powerful ETL service, Stitch connects to all your data sources – from databases like MySQL and MongoDB, to SaaS applications like Salesforce and Zendesk – and replicates that data to a destination of your choosing."

## Big Data (Hadoop Stack)
* [Apache Beam](https://beam.apache.org/) - "a unified programming model for Batch and Streaming data processing." Write pipelines once and run them on any execution engine (Spark, Flink, Google Dataflow, etc).
* [Apache Flink](https://flink.apache.org/) - "a framework and distributed processing engine for stateful computations over unbounded and bounded data streams." Industry-standard for high-throughput, low-latency stream processing.
* [Kafka Connect](https://kafka.apache.org/documentation/#connect) - A framework for streaming data between Apache Kafka and other systems at scale using pre-built source and sink connectors. Part of the Apache Kafka ecosystem.
* [Pig](https://pig.apache.org/) - "a platform for analyzing large data sets that consists of a high-level language for expressing data analysis programs, coupled with infrastructure for evaluating these programs."
* [Spark](https://spark.apache.org/) - "a fast and general-purpose cluster computing system. It provides high-level APIs in Scala, Java, and Python that make parallel jobs easy to write, and an optimized engine that supports general computation graphs. It also supports a rich set of higher-level tools including Shark (Hive on Spark), MLlib for machine learning, GraphX for graph processing, and Spark Streaming."

## ETL Tools (GUI)
*Warning*: If you're already familiar with a scripting language, GUI ETL tools are not a good replacement for a well structured application written with a scripting language. These tools lack flexibility and are a good example of the ["inner-platform effect"](https://en.wikipedia.org/wiki/Inner-platform_effect). With a large project, you will most likely run into instances where "the tool doesn't do that" and end up implementing something hacky with a script run by the GUI ETL tool. Also, the GUI can conceal complexity and the files these tools generate are impossible to code review. However, the GUI and out-of-the-box functionality can make some tasks simpler, especially for people not comfortable with writing code.
* [Airbyte](https://airbyte.com/) - "Airbyte is an open-source data integration engine that helps you consolidate your data in your data warehouses, lakes and databases"
* [Apache NiFi](https://nifi.apache.org/) - "a rich, web-based interface for designing, controlling, and monitoring a dataflow."
* [CDAP](https://cdap.io/) - "Use Cask Data Application Platform to visually build and manage data applications in hybrid and multi-cloud environments."
* [Informatica PowerCenter](https://www.informatica.com/products/data-integration/powercenter.html) - "a toolset for establishing and maintaining enterprise-wide data warehouses. It has a customer base of over 5,000 companies."
* [Microsoft SSIS](https://learn.microsoft.com/en-us/sql/integration-services/sql-server-integration-services) - "a component of the Microsoft SQL Server database software that can be used to perform a broad range of data migration tasks."
* [N8n](https://github.com/n8n-io/n8n) - "Free and open fair-code licensed node based Workflow Automation Tool. Easily automate tasks across different services."
* [Pentaho Data Integration (PDI)](https://www.hitachivantara.com/en-us/products/pentaho-platform/data-integration-analytics.html) - The most popular open-source graphical ETL tool.

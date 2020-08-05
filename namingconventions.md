Contents
========

[Contents 1](#_Toc47479401)

[Document Control 2](#document-control)

[Change Record 2](#change-record)

[Reviewers 2](#reviewers)

[Distribution 2](#distribution)

[Naming Conventions 3](#naming-conventions)

[Category of Naming Conventions 3](#category-of-naming-conventions)

[Typical Scope of Naming Conventions
3](#typical-scope-of-naming-conventions)

[Naming Conventions Advantages 4](#naming-conventions-advantages)

[Naming Conventions Type 4](#naming-conventions-type)

[Database Naming Conventions 5](#database-naming-conventions)

[Coding Naming Conventions 7](#coding-naming-conventions)

[Database Versioning Rules 8](#database-versioning-rules)

[Application Versioning Rules 9](#application-versioning-rules)

[Document Versioning Rules 10](#document-versioning-rules)

Document Control
================

Change Record
-------------

  -------------- -------------------- --------- --------------------------------------------------
  Date           Author               Version   Change Reference
                                                
  Aug 04, 2020   Meilyana Indriyani   V.0.0     Create Naming Conventions Standard Documentation
  -------------- -------------------- --------- --------------------------------------------------

Reviewers
---------

  -------------------- -------------------------
  Name                 Position
                       
  Alfa Pungki Irawan   IT Architecture Manager
  -------------------- -------------------------

Distribution
------------

+----------+------+----------+
| Copy No. | Name | Location |
+----------+------+----------+
|          |      |          |
+----------+------+----------+
| 1.       |      |          |
+----------+------+----------+
| 2.       |      |          |
+----------+------+----------+

Naming Conventions
==================

In general, code is written once but read multiple times, by others in
the project team or even those from other teams. Readability is
therefore important. Readability is nothing more than figuring out what
the code does in less time.

Among the many best practices of coding, is the way variables,
functions, classes and even files are named in a project. A common
naming convention that everyone agrees to follow must be accompanied by
consistent usage. This will result in developers, reviewers and project
managers communicate effectively with respect to what the code does.

While there are well-established naming conventions, there\'s no single
one that fits all scenarios. Each programming language recommends its
own convention. Each project or organization may define its own
convention.

Category of Naming Conventions
------------------------------

It\'s common to categorize a naming convention as one of these:

-   Typographical: This relates to the use of letter case and symbols
    such as underscore, dot and hyphen.

-   Grammatical: This relates to the semantics or the purpose. For
    example, classes should be nouns or noun phrases to identify the
    entity; methods and functions should be verbs or verb phrases to
    identify action performed; annotations can be any part of
    speech; interfaces should be adjectives.

Grammatical conventions are less important for variable names or
instance properties. They are more important for classes, interfaces and
methods that are often exposed as APIs.

Typical Scope of Naming Conventions
-----------------------------------

Naming convention is applicable to constants, variables, functions,
modules, packages and files. In object-oriented languages, it\'s
applicable to classes, objects, methods and instance variables.

Naming Conventions Advantages
-----------------------------

Naming conventions are probably not important if the code is written by
a single developer, who\'s also the sole maintainer. However, typical
real-world projects are developed and maintained by teams of developers.
Particularly in the context of open source projects, code is shared,
updated and merged by many individuals across organizations and
geographies. Naming conventions are therefore important.

Naming conventions lead to predictability and discoverability. A common
naming convention, coupled with a consistent project structure, makes it
easier to find files in a project.

Naming Conventions Type
-----------------------

In this document, we will explain more about naming conventions for:

-   Database Naming Conventions

-   Coding Naming Conventions

-   Database Versioning Rules

-   Document Versioning Rules

-   Application Versioning Rules

### Database Naming Conventions

There are two key elements to any software experience: the application
and the data. Both elements need to be present for a functional end-user
experience.

The application component is stateless, so the teams can simply
overwrite the application with the latest version when releasing new
software experiences. However, unlike the application, the database
component cannot simply be overwritten. Data is a persistent and
valuable resource. Unlike applications, databases are stately. As a
result, the database is one of the most valuable and important assets to
the organization -- therefore database version control is needed.

Database versioning begins with database schema, or the structure of the
database. In order to effectively version a database, you need to track
and understand the changes that are happening.

Things to consider:

-   Identifiers should be written entirely in lower case. This includes
    tables, views, column, and everything else too. Mixed case
    identifier names means that every usage of the identifier will need
    to be quoted in double quotes. Example: use first_name not
    "First_name".

-   Data types are not names. Database object names, particularly column
    names, should be a noun describing the field or object. Avoid using
    words that are just data types such as text or timestamp

-   Underscores separate words. Object name that are comprised of
    multiple words should be separated by underscores.

Example: word_count or team_member_id, not wordcount or wordCount.

-   Full words, not abbreviations. Object names should be full English
    words. In general, to avoid abbreviations. Example: use middle_name
    not mid_nm.

-   Tables, views, and other relations that hold data should have
    singular names, not plural. This means our tables and views would be
    name team, not teams

-   The sentences are consistency and unambiguous.

-   Single column primary key fields should be named "id"

-   Foreign key fields should be a combination of the name of the
    referenced table and the name of the referenced fields.

-   Object names should not include the object types of them.

-   All modern databases support some form of namespacing. For example,
    in postgresql you can create schemas to group database objects. If
    you have multiple applications sharing the same database and want to
    prevent them from clobbering each other, use schemas instead.

-   Some database commands that create database objects do not require
    you specify a name. You should be explicitly specifying names.

-   Indexes should be explicitly names and include both the table name
    and the column name(s) indexed.

-   Similar to indexes, constraints should give descriptive names. This
    is especially true for check constraints. It's much easier to
    diagnose an errant insert if the check constraints that was violated
    lets you know the cause.

### Coding Naming Conventions

Coding naming conventions is a rule to follow as you decide what to name
your identifiers such as class, package, variable, constant, method,
etc. By using this standard, make your code easier to read for yourself
and other programmers.

The following are the key rules that must be followed by every
identifier:

-   The name must not contain any white spaces.

-   The name should not start with special characters like &
    (ampersand), \$ (dollar), \_ (underscore).

-   Consistency names in classes, objects, methods, and instance
    variables.

-   In general, use nouns for classes, verbs for functions, and names
    that show purpose for variables, attributes and arguments.

-   Separators objections:

    a.  With Camel Case and Pascal Case, there are no word separators.
        Readability is achieved by capitalizing the first letter of each
        word. Language adopting: Pascal, Modula, Java, and .NET.

    b.  With Snake Case, underscore is the separator. This practice is
        common in Python, Ruby, C/C++ standard libraries, and WordPress.

    c.  With Kebab Case, hyphen is the separator. Language adopting:
        COBOL, Lisp, Perl 6, and CSS. Since hyphen in many languages is
        used for subtraction, Kebab Case is less common than Snake Case.

```{=html}
<!-- -->
```
-   Things to consider:

a.  Reveal intentions: fileName is better f; maxPugs is better than
    pugs.

b.  Make distinctions; moneyInDollars is better than money.

c.  Put the distinguishing aspect first: dollarMoney and rupeeMoney are
    better than moneyInDollars and moneyInRupees.

d.  Easy to pronounce: timeStamp is better than ts.

e.  Verbs for functions: getName() and isPosted() are
    good; hasWeight() or isMale() when boolean values are
    returned; toDollars() for conversions.

f.  One word, one concept: fetch, retrieve, get all imply the same
    thing: use one of them consistently.

g.  Relate to business context: AddCustomer is better
    than IncrementCounter.

h.  Use shortforms judiciously: PremiumCust may be used
    over PremiumCustomer to emphasize \"Premium\"; but fn is not a good
    substitute for fileName.

i.  Describe content rather than storage: user_info is better
    than user_list.

j.  Plurals for containers: fruitNames is better than fruit for an array
    of fruit names.

### Database Versioning Rules

Provides schema management to ensure always have the same schema
structure for tables, views, procedures, etc. It
provides database revisions where you can create change set scripts and
queries, commit them to your source control system, and share them with
your team.

Things to consider:

-   Prepare the application database and the reference data in it as
    regular code.

That means should store both its schema and the reference data in a
source control system.

-   Store every change in the database schema and in the reference data
    explicitly.

This means that for every modification we make we should create a
separate SQL script with the changes. If the modification affects both
the schema and the reference data, they should be reflected in a single
script.

-   Every SQL script file must be immutable after it is deployed to
    production or staging environment.

-   All changes in the database's schema and reference data have to be
    applied through the scripts. Neither of them can be
    applied manually.

-   Every developer in the team should have their own database instance.

-   Database version should be stored in the database itself. Usually
    tend to create a separate table named Settings and keep the version
    there. Don't use complex notations like \"x.y.z\" for the version
    number, just use a single integer.

### Application Versioning Rules

Semantic versioning (aka SemVer), currently the best known and most
widely adopted version scheme in this category, uses a sequence of three
digits (Major.Minor.Patch), an optional pre-release tag and optional
build meta tag. In this scheme, risk and functionality are the measures
of significance.

-   Major version numbers change whenever there is some significant
    > change being introduced. For example, a large or potentially
    > backward-incompatible change to a software package.

-   Minor version numbers change when a new, minor feature is introduced
    > or when a set of smaller features is rolled out.

-   Patch numbers change when a new build of the software is released to
    > customers. This is normally for small bug-fixes or the like.

Other variations use build numbers as an additional identifier. So you
may have a large number for X.Y.Z.build if you have many revisions that
are tested between releases. I use a couple of packages that are
identified by year/month or year/release. Thus, a release in the month
of September of 2010 might be 2010.9 or 2010.3 for the 3rd release of
this year.

### Document Versioning Rules

Refer to following guidelines:

-   **Document dates**; The author of the document will ensure the date
    the document is created or revised is identified on the first page
    and, when possible, is incorporated into the header or footer of the
    document and appears on every succeeding page.

-   **Version numbers**; The author of the document will ensure the
    current version number is identified on the first page and, when
    possible, is incorporated into the header or footer of the document
    and appears on every succeeding page.

-   **Draft document version number**

a.  The first draft of a document will be Version 0.1.

b.  Subsequent drafts will have an increase of "0.1" in the version
    number (e.g., 0.2, 0.3, 0.4, ...0.9, 0.10, 0.11).

-   **Final document version number and date**

a.  The author (or investigator) will deem a protocol or other document
    (consent/assent form, case report form, manual of procedures) final
    after all reviewers have provided final comments and the comments
    have been addressed.

b.  The first final version of a document will be Version 1.0. Include
    the date when the document becomes final. Generally, the final
    version is submitted to the Institutional Review Board (IRB) and/or
    FDA.

c.  Subsequent final documents will have an increase of "1.0" in the
    version number (1.0, 2.0, etc.).

-   **Final documents undergoing revisions**; Final documents undergoing
    revisions will be Version X.1 for the first version of the
    revisions. While the document is under review, subsequent draft
    versions will increase by "0.1" (e.g., 1.1, 1.2, 1.3, etc.). When
    the revised document is deemed final, the version will increase by
    "1.0" over the version being revised (e.g., the draft 1.3 will
    become a final 2.0).

-   **Documenting substantive changes**; A list of changes from the
    previous draft or final documents will be kept. The list will be
    cumulative and identify the changes from the preceding document
    versions. The list of changes made to a protocol and consent/assent
    should be submitted to the IRB with the final protocol and
    consent/assent documents.

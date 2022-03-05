
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Deploying with Git | Heroku Dev Center</title>
<link rel="shortcut icon" type="image/x-icon" href="https://www.herokucdn.com/favicons/favicon.ico" />
<link rel="mask-icon" type="image/png" href="https://www.herokucdn.com/favicons/icon.svg" />
<link rel="apple-touch-icon" type="image/x-icon" href="https://www.herokucdn.com/favicons/apple-touch-icon.png" color="#79589f" />
<link rel="apple-touch-icon" type="image/png" href="https://www.herokucdn.com/favicons/apple-touch-icon.png" />
<link rel="icon" type="image/png" href="https://www.herokucdn.com/favicons/android-icon.png" size="192x192" />
<link rel="apple-touch-icon" type="image/png" href="https://www.herokucdn.com/favicons/apple-touch-icon-152x152.png" size="152x152" />
<link rel="apple-touch-icon" type="image/png" href="https://www.herokucdn.com/favicons/apple-touch-icon-167x167.png" size="167x167" />
<link rel="apple-touch-icon" type="image/png" href="https://www.herokucdn.com/favicons/apple-touch-icon-180x180.png" size="180x180" />

  <link rel="alternate" type="application/atom+xml" title="Heroku Recent Articles" href="http://feeds.feedburner.com/herokudevcenterarticles" />
  <link rel="alternate" type="application/atom+xml" title="Heroku Changelog" href="http://feeds.feedburner.com/herokuchangelog" />
<link rel="search" type="application/opensearchdescription+xml" title="Heroku Dev Center" href="/opensearch.xml">

<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta content="IE=edge,chrome=1" http-equiv="X-UA-Compatible">
<meta name="csrf-param" content="authenticity_token" />
<meta name="csrf-token" content="7Nd+gUjWvr2ZZBiQn9DipkCDwHkttxwkfrt4gapZNEL3+Bit0aDcp8GtcybR31Ez6RvCbcJRKgOoAcPIoBlCmg==" />

  <meta name="description" content="Git is a powerful decentralized revision control system, and is the means for deploying apps to Heroku." />

  <meta name="twitter:card" content="summary" />
  <meta name="twitter:site" content="@herokudevcenter" />
  <meta name="twitter:title" content="Deploying with Git | Heroku Dev Center" />
  <meta name="twitter:description" content="Git is a powerful decentralized revision control system, and is the means for deploying apps to Heroku." />
  <meta name="twitter:image" content="https://www.herokucdn.com/images/og.png" />

  <link rel="alternate" hreflang="en" href="https://devcenter.heroku.com/articles/git" />
    <link rel="alternate" hreflang="ja" href="https://devcenter.heroku.com/ja/articles/git" />


<meta property="og:image:secure_url" content="https://www.herokucdn.com/images/og.png">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">

<meta name="google-site-verification" content="V8eEvIkb6RQqJca9Wf-o9baurAQMe54VKxd06IeaFeg">


<meta name="slack-app-id" content="A1QME020P">


<link rel="stylesheet" media="screen, print" href="https://devcenter0.assets.heroku.com/assets/public-982dcb4cc4cdc8caa54c553d99f4c4a25d43bbe1a63a186c91429e71759efdb9.css" />

      <link href="https://developer.salesforce.com/shared-components/css/index.css" rel="stylesheet" type="text/css"/>
      <link rel="modulepreload" href="https://developer.salesforce.com/shared-components/helmet/import.js" />
  </head>
  <body>
    <div class="page-wrapper">
        <dx-helmet variant="light" title="Salesforce Developers"></dx-helmet>
      <header aria-label="Global Dev Center site header" role="banner">
        <div id="primary-header">
          <a class="visuallyhidden skip-link" href="#skip-link">Skip Navigation</a><nav aria-label="Global Dev Center site navigation" id="navigation-devcenter" role="navigation"><span aria-hidden="true" class="mobile-nav-devcenter">Show nav<span></span><span></span><span></span><span></span></span><div><div id="logo-devcenter"><a class="heroku-brand" href="/"><span class="logo-text">Heroku Dev Center</span></a></div><div class="mobile-nav-wrapper"><ul class="main-nav"><li class="getting-started"><a href="/start">Get Started</a></li><li class="reference"><a href="/categories/reference">Documentation</a></li><li class="changelog"><a href="/changelog">Changelog</a></li><li class="search"><a href="/search">Search</a></li></ul></div><div class="nav-wrapper"><ul class="main-nav"><li class="getting-started has-dropdown"><a href="/start">Get Started</a><ul class="dropdown dropdown-sm"><li><a aria-label="Get started with Node.js" href="/articles/getting-started-with-nodejs">Node.js</a></li><li><a aria-label="Get started with Rails 6" href="/articles/getting-started-with-rails6">Ruby on Rails</a></li><li><a aria-label="Get started with Ruby" href="/articles/getting-started-with-ruby">Ruby</a></li><li><a aria-label="Get started with Python" href="/articles/getting-started-with-python">Python</a></li><li><a aria-label="Get started with Java" href="/articles/getting-started-with-java">Java</a></li><li><a aria-label="Get started with PHP" href="/articles/getting-started-with-php">PHP</a></li><li><a aria-label="Get started with Go" href="/articles/getting-started-with-go">Go</a></li><li><a aria-label="Get started with Scala" href="/articles/getting-started-with-scala">Scala</a></li><li><a aria-label="Get started with Clojure" href="/articles/getting-started-with-clojure">Clojure</a></li></ul></li><li class="reference"><a href="/categories/reference">Documentation</a></li><li class="changelog"><a href="/changelog">Changelog</a></li><li class="has-dropdown"><a class="nav-more" href="#">More</a><div class="dropdown more"><section aria-label="Additional Heroku web resources" class="more-resources"><span class="more-title">Additional Resources</span><ul><li><a href="https://www.heroku.com/home">Home</a></li><li><a href="https://elements.heroku.com/">Elements</a></li><li><a href="https://www.heroku.com/products">Products</a></li><li><a href="https://www.heroku.com/pricing">Pricing</a></li><li><a href="https://www.heroku.com/careers">Careers</a></li><li><a href="https://help.heroku.com/">Help</a></li><li><a href="https://status.heroku.com/">Status</a></li><li><a href="https://www.heroku.com/events">Events</a></li><li><a href="https://www.heroku.com/podcasts">Podcasts</a></li><li><a href="https://www.heroku.com/compliance">Compliance Center</a></li></ul></section><section aria-label="Heroku Blog posts" class="more-blog" id="more-blog"><span class="more-title">Heroku Blog</span><h3><a class="js-blog-link" href="https://blog.heroku.com">Heroku Blog</a></h3><p class="js-blog-date"></p><p class="js-blog-content">Find out what's new with Heroku on our blog.</p><a class="button btn-default btn-sm btn-inline" href="https://blog.heroku.com">Visit Blog</a></section></div></li></ul><ul class="tool-nav"><li class="search" role="search"><div id="search-field-desktop"><form class="search-form" name="devcentersearch" action="/search" accept-charset="UTF-8" method="get"><input name="utf8" type="hidden" value="&#x2713;" /><div class="search-input-group"><input placeholder="Search Dev Center" aria-label="Search terms" class="form-control" type="text" spellcheck="false" autocomplete="off" name="q" title="search" id="header-search-input" tabindex="1" /><button type="submit" value="Submit search" aria-label="Submit search" tabindex="2" /></div></form></div></li><li class="user"><a href="/login?back_to=%2Farticles%2Fgit">Log in</a><span>or</span><a class="sign-up highlight" data-trackable="{&quot;category&quot;:&quot;Sign Up Links&quot;,&quot;action&quot;:&quot;Clicked&quot;,&quot;label&quot;:null}" href="https://signup.heroku.com">Sign up</a></li></ul><span id="skip-link"></span></div></div></nav>
        </div>
      </header>

      <div class="container" role="main">
        






<div class="search-nav-wrap col-md-4 sidebar nocontent">
  <div class="left-nav">
    <div class="toggle-left-nav" data-hide-message="Hide categories">View categories</div>
    <div class="left-nav-content">
      <h1>Categories</h1>
          <ul class="">
    <li class="top-level ">
        <span class="expander"></span>
      <a class="category" href="/categories/heroku-architecture">
          <svg class="category-icon">
            <use xlink:href="#marketing-spaces-48"></use>
          </svg>
        Heroku Architecture
</a>          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/dynos">
        Dynos (app containers)
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/stacks">
        Stacks (operating system images)
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/networking-dns">
        Networking &amp; DNS
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/platform-policies">
        Platform Policies
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/platform-principles">
        Platform Principles
</a></li></ul>
</li></ul>
          <ul class="">
    <li class="top-level ">
      <a class="category" href="/categories/command-line">
          <svg class="category-icon">
            <use xlink:href="#marketing-cli-48"></use>
          </svg>
        Command Line
</a></li></ul>
          <ul class="">
    <li class="top-level active">
        <span class="expander expanded"></span>
      <a class="category" href="/categories/deployment">
          <svg class="category-icon">
            <use xlink:href="#marketing-deploy-48"></use>
          </svg>
        Deployment
</a>          <ul class="indent">
    <li class=" active">
      <a class="active" href="/categories/deploying-with-git">
        Deploying with Git
</a></li></ul>
          <ul class="indent">
    <li class=" ">
      <a class="" href="/categories/deploying-with-docker">
        Deploying with Docker
</a></li></ul>
          <ul class="indent">
    <li class=" ">
      <a class="" href="/categories/deployment-integrations">
        Deployment Integrations
</a></li></ul>
</li></ul>
          <ul class="">
    <li class="top-level ">
        <span class="expander"></span>
      <a class="category" href="/categories/continuous-delivery">
          <svg class="category-icon">
            <use xlink:href="#marketing-pipelines-48"></use>
          </svg>
        Continuous Delivery
</a>          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/continuous-integration">
        Continuous Integration
</a></li></ul>
</li></ul>
          <ul class="">
    <li class="top-level ">
        <span class="expander"></span>
      <a class="category" href="/categories/language-support">
          <svg class="category-icon">
            <use xlink:href="#marketing-code-48"></use>
          </svg>
        Language Support
</a>          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/nodejs-support">
        Node.js
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
        <span class="expander"></span>
      <a class="" href="/categories/ruby-support">
        Ruby
</a>          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/working-with-bundler">
        Working with Bundler
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/rails-support">
        Rails Support
</a></li></ul>
</li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
        <span class="expander"></span>
      <a class="" href="/categories/python-support">
        Python
</a>          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/working-with-django">
        Working with Django
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/background-jobs-in-python">
        Background Jobs in Python
</a></li></ul>
</li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
        <span class="expander"></span>
      <a class="" href="/categories/java-support">
        Java
</a>          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/working-with-maven">
        Working with Maven
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/java-database-operations">
        Java Database Operations
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/working-with-the-play-framework">
        Working with the Play Framework
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/java-advanced-topics">
        Java Advanced Topics
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/working-with-spring-boot">
        Working with Spring Boot
</a></li></ul>
</li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/php-support">
        PHP
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
        <span class="expander"></span>
      <a class="" href="/categories/go-support">
        Go
</a>          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/managing-go-dependencies">
        Go Dependency Management
</a></li></ul>
</li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/scala-support">
        Scala
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/clojure-support">
        Clojure
</a></li></ul>
</li></ul>
          <ul class="">
    <li class="top-level ">
        <span class="expander"></span>
      <a class="category" href="/categories/data-management">
          <svg class="category-icon">
            <use xlink:href="#marketing-data-48"></use>
          </svg>
        Databases &amp; Data Management
</a>          <ul class="indent nav-hidden">
    <li class=" ">
        <span class="expander"></span>
      <a class="" href="/categories/heroku-postgres">
        Heroku Postgres
</a>          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/postgres-basics">
        Postgres Basics
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/postgres-performance">
        Postgres Performance
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/postgres-data-transfer-preservation">
        Postgres Data Transfer &amp; Preservation
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/postgres-availability">
        Postgres Availability
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/postgres-special-topics">
        Postgres Special Topics
</a></li></ul>
</li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/heroku-redis">
        Heroku Redis
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/kafka">
        Apache Kafka on Heroku
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/other-data-stores">
        Other Data Stores
</a></li></ul>
</li></ul>
          <ul class="">
    <li class="top-level ">
        <span class="expander"></span>
      <a class="category" href="/categories/monitoring-metrics">
          <svg class="category-icon">
            <use xlink:href="#marketing-metrics-48"></use>
          </svg>
        Monitoring &amp; Metrics
</a>          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/logging">
        Logging
</a></li></ul>
</li></ul>
          <ul class="">
    <li class="top-level ">
      <a class="category" href="/categories/app-performance">
          <svg class="category-icon">
            <use xlink:href="#marketing-control-2-48"></use>
          </svg>
        App Performance
</a></li></ul>
          <ul class="">
    <li class="top-level ">
        <span class="expander"></span>
      <a class="category" href="/categories/add-ons">
          <svg class="category-icon">
            <use xlink:href="#marketing-addon-48"></use>
          </svg>
        Add-ons
</a>          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/add-on-documentation">
        All Add-ons
</a></li></ul>
</li></ul>
          <ul class="">
    <li class="top-level ">
      <a class="category" href="/categories/collaboration">
          <svg class="category-icon">
            <use xlink:href="#marketing-team-48"></use>
          </svg>
        Collaboration
</a></li></ul>
          <ul class="">
    <li class="top-level ">
        <span class="expander"></span>
      <a class="category" href="/categories/security">
          <svg class="category-icon">
            <use xlink:href="#marketing-lock-48"></use>
          </svg>
        Security
</a>          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/app-security">
        App Security
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/identities-authentication">
        Identities &amp; Authentication
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/compliance">
        Compliance
</a></li></ul>
</li></ul>
          <ul class="">
    <li class="top-level ">
        <span class="expander"></span>
      <a class="category" href="/categories/heroku-enterprise">
          <svg class="category-icon">
            <use xlink:href="#marketing-enterprise-48"></use>
          </svg>
        Heroku Enterprise
</a>          <ul class="indent nav-hidden">
    <li class=" ">
        <span class="expander"></span>
      <a class="" href="/categories/private-spaces">
        Private Spaces
</a>          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/private-space-infrastucture-networking">
        Infrastructure Networking
</a></li></ul>
</li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/enterprise-accounts">
        Enterprise Accounts
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/enterprise-teams">
        Enterprise Teams
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
        <span class="expander"></span>
      <a class="" href="/categories/heroku-connect">
        Heroku Connect (Salesforce sync)
</a>          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/heroku-connect-admin">
        Heroku Connect Administration
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/heroku-connect-reference">
        Heroku Connect Reference
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/heroku-connect-troubleshooting">
        Heroku Connect Troubleshooting
</a></li></ul>
</li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/sso">
        Single Sign-on (SSO)
</a></li></ul>
</li></ul>
          <ul class="">
    <li class="top-level ">
      <a class="category" href="/categories/best-practices">
          <svg class="category-icon">
            <use xlink:href="#marketing-architecture-48"></use>
          </svg>
        Patterns &amp; Best Practices
</a></li></ul>
          <ul class="">
    <li class="top-level ">
        <span class="expander"></span>
      <a class="category" href="/categories/extending-heroku">
          <svg class="category-icon">
            <use xlink:href="#marketing-api-48"></use>
          </svg>
        Extending Heroku
</a>          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/platform-api">
        Platform API
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/app-webhooks">
        App Webhooks
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/labs">
        Heroku Labs
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
        <span class="expander"></span>
      <a class="" href="/categories/building-add-ons">
        Building Add-ons
</a>          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/add-on-development-tasks">
        Add-on Development Tasks
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/add-on-apis">
        Add-on APIs
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/add-on-guidelines-requirements">
        Add-on Guidelines &amp; Requirements
</a></li></ul>
</li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/building-cli-plugins">
        Building CLI Plugins
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/buildpacks">
        Developing Buildpacks
</a></li></ul>
          <ul class="indent nav-hidden">
    <li class=" ">
      <a class="" href="/categories/devcenter">
        Dev Center
</a></li></ul>
</li></ul>
          <ul class="">
    <li class="top-level ">
      <a class="category" href="/categories/billing">
          <svg class="category-icon">
            <use xlink:href="#marketing-user-48"></use>
          </svg>
        Accounts &amp; Billing
</a></li></ul>
          <ul class="">
    <li class="top-level ">
      <a class="category" href="/categories/troubleshooting">
          <svg class="category-icon">
            <use xlink:href="#marketing-support-48"></use>
          </svg>
        Troubleshooting &amp; Support
</a></li></ul>
    </div>
  </div>
</div>


<div class="col-md-8 content">
  <article class="js-autolink contributed">

    <nav aria-label="Breadcrumb"><ul class="bread-crumb"><li><a href="/categories/deployment">Deployment</a></li><li><a href="/categories/deploying-with-git">Deploying with Git</a></li><li class="bread-crumb-current"><a aria-current="page" href="/articles/git">Deploying with Git</a></li></ul></nav>

    

    
    

    <div class="title-and-language">
      <h1 data-category="deploying-with-git">Deploying with Git</h1>
      <nav aria-label="Article languages" class="language-select">English &mdash; <a href="/ja/articles/git">日本語に切り替える</a></nav>
    </div>


    <p class="last-updated"><span class="icon-clock" />Last updated February 14, 2022</p>
    
    

      <div id="table-of-contents"><h2><span class="icon-list"></span>Table of Contents</h2><ul><li><a href="#prerequisites-install-git-and-the-heroku-cli">Prerequisites: Install Git and the Heroku CLI</a></li><li><a href="#create-a-heroku-remote">Create a Heroku Remote</a></li><li><a href="#deploy-your-code">Deploy Your Code</a></li><li><a href="#multiple-remotes-and-environments">Multiple Remotes and Environments</a></li><li><a href="#detach-from-the-build-process">Detach From the Build Process</a></li><li><a href="#behavior-of-simultaneous-deploys">Behavior of Simultaneous Deploys</a></li><li><a href="#http-git-authentication">HTTP Git Authentication</a></li><li><a href="#reset-a-git-repository">Reset a Git Repository</a></li><li><a href="#keep-your-repository-size-small">Keep Your Repository Size Small</a></li><li><a href="#limits">Limits</a></li><li><a href="#deploy-code-tracked-in-subversion-or-other-revision-control-systems">Deploy Code Tracked in Subversion or Other Revision Control Systems</a></li><li><a href="#additional-resources">Additional Resources</a></li></ul></div>
      <p>Heroku manages app deployments with <a href="https://git-scm.com/">Git</a>, the popular version control system. You don’t need to be a Git expert to deploy code to Heroku, but it’s helpful to learn the basics.</p>

<p>This article describes how to deploy code using Git and Heroku Git remotes. If you already track your code in GitHub, consider <a href="https://devcenter.heroku.com/articles/github-integration">deploying with the Heroku GitHub integration</a> instead of following the steps in this article.</p>

<h2 id="prerequisites-install-git-and-the-heroku-cli">Prerequisites: Install Git and the Heroku CLI</h2>

<p>You must have Git and the Heroku CLI installed to deploy with Git.</p>

<ul>
<li><p><a href="https://git-scm.com/book/en/v2/Getting-Started-Installing-Git">Git installation instructions</a></p></li>
<li><p><a href="https://devcenter.heroku.com/articles/heroku-cli#install-the-heroku-cli">Heroku CLI installation instructions</a></p></li>
</ul>

<p>Before you can deploy your app to Heroku, initialize a local Git repository and commit your application code to it.</p>

<p>The following example demonstrates initializing a Git repository for an app that lives in the <code>example-app</code> directory:</p>
<pre class="language-term"><code class="language-term">$ cd example-app
$ git init
Initialized empty Git repository in .git/
$ git add .
$ git commit -m "My first commit"
Created initial commit 5df2d09: My first commit
 44 files changed, 8393 insertions(+), 0 deletions(-)
 create mode 100644 README
 create mode 100644 Procfile
 create mode 100644 app/controllers/source_file
...
</code></pre>
<div class="callout">
<p>Initialize the Git repository in your app’s root directory. If your app is in a subdirectory of your repository, it doesn’t run when pushed to Heroku.</p>
</div>

<p>You’re now tracking your app’s code in a local Git repository. It doesn’t yet exist on any remote servers.</p>

<h2 id="create-a-heroku-remote">Create a Heroku Remote</h2>

<p>Git <a href="http://git-scm.com/book/en/Git-Basics-Working-with-Remotes">remotes</a> are versions of your repository that live on other servers. You deploy your app by pushing its code to a special Heroku-hosted remote that’s associated with your app.</p>

<div class="note">
<p>Heroku Git is a convenience for deployment and not intended to be a stable git repository. Use <a href="http://github.com/">GitHub</a> (recommended), <a href="https://about.gitlab.com/">GitLab</a>, <a href="https://bitbucket.org/">BitBucket</a>, or another version control system to track your codebase.</p>
</div>

<h3 id="for-a-new-app">For a New App</h3>

<p>The <code>heroku create</code> CLI command creates a new empty application on Heroku, along with an associated empty Git repository. If you run this command from your app’s root directory, the empty Heroku Git repository is automatically set as a remote for your local repository.</p>
<pre class="language-term"><code class="language-term">$ heroku create -a example-app
Creating app... done, ⬢ example-app
https://thawing-inlet-61413.herokuapp.com/ | https://git.heroku.com/example-app.git
</code></pre>
<p>You can use the <code>git remote</code> command to confirm that a remote named <code>heroku</code> has been set for your app:</p>
<pre class="language-term"><code class="language-term">$ git remote -v
heroku  https://git.heroku.com/example-app.git (fetch)
heroku  https://git.heroku.com/example-app.git (push)
</code></pre>
<h3 id="for-an-existing-app">For an Existing App</h3>

<p>Add a remote to your local repository with the <code>heroku git:remote</code> command. All you need is your Heroku app’s name:</p>
<pre class="language-term"><code class="language-term">$ heroku git:remote -a example-app
set git remote heroku to https://git.heroku.com/example-app.git
</code></pre>
<h3 id="rename-a-remote">Rename a Remote</h3>

<p>By default, the Heroku CLI names all of the Heroku remotes it creates for your app <code>heroku</code>. You can rename your remotes with the <code>git remote rename</code> command. For example, rename <code>heroku</code> to <code>heroku-staging</code>:</p>
<pre class="language-term"><code class="language-term">$ git remote rename heroku heroku-staging
</code></pre>
<p>Renaming your Heroku remote can be handy if you have multiple Heroku apps that use the same codebase. In this case, each Heroku app has its own remote in your local repository.</p>

<p>The Dev Center documentation assumes your app has a single Heroku remote that is named <code>heroku</code>.</p>

<h2 id="deploy-your-code">Deploy Your Code</h2>

<p>To deploy your app to Heroku, use the <code>git push</code> command to push the code from your local repository’s <a href="https://devcenter.heroku.com/articles/git-branches">main branch</a> to your <code>heroku</code> remote. For example:</p>
<pre class="language-term"><code class="language-term">$ git push heroku main
Initializing repository, done.
updating 'refs/heads/main'
...
</code></pre>
<p>Use this same command whenever you want to deploy the latest committed version of your code to Heroku.</p>

<p>Heroku only deploys code that you push to the <a href="https://devcenter.heroku.com/articles/git-branches">master or main</a> branches of the remote. Pushing code to another branch of the <code>heroku</code> remote has no effect.</p>

<h3 id="deploy-from-a-branch-besides-main">Deploy From a Branch Besides main</h3>

<p>To deploy code to Heroku from a non-<code>main</code> branch of your local repository (for example, <code>testbranch</code>), use the following syntax push it to the remote’s <code>main</code> branch:</p>
<pre class="language-term"><code class="language-term">$ git push heroku testbranch:main
</code></pre>
<div class="note">
<p>This method supports applications that rely on Git submodules, in addition to many other <a href="https://devcenter.heroku.com/articles/git-submodules">dependency resolution strategies</a>.</p>
</div>

<p class="devcenter-parser-special-block-separator" style="display:none">&nbsp;</p>

<div class="warning">
<p>Heroku doesn’t support <a href="https://git-lfs.github.com/">git lfs</a>. Using this method can cause pushes to fail.</p>
</div>

<h2 id="multiple-remotes-and-environments">Multiple Remotes and Environments</h2>

<p>You can use the same techniques used to deploy to production can be used to deploy a development branch of your application to a staging application on Heroku. See <a href="https://devcenter.heroku.com/articles/multiple-environments">Managing Multiple Environments for an App</a> for more info.</p>

<h2 id="detach-from-the-build-process">Detach From the Build Process</h2>

<p>After you initiate a Heroku deploy with <code>git push</code>, you can detach from the resulting build process by pressing Ctrl + C. Detaching doesn’t cancel the build or the deploy. The build continues in the background and creates a new <a href="https://devcenter.heroku.com/articles/releases">release</a> as soon as it completes.</p>

<h2 id="behavior-of-simultaneous-deploys">Behavior of Simultaneous Deploys</h2>

<p>It’s possible to initiate a deploy before a <em>previous</em> deploy of the same app completes. For example, two collaborators on an app push different commits to the <code>heroku</code> remote at roughly the same time.</p>

<p>If this situation occurs, the different versions of your app deploy to Heroku in the order in which their respective builds complete. This order can differ from the order in which the pushes occurred.</p>

<p>For example, consider two builds, A and B. If Build B starts <em>after</em> Build A but finishes <em>before</em> it, Heroku deploys Build B <em>first</em>. Then, when Build A eventually completes, Heroku deploys it, replacing Build B.</p>

<h2 id="http-git-authentication">HTTP Git Authentication</h2>

<div class="note">
<p>By default, Heroku uses HTTP as its Git transport. The Heroku CLI automatically places credentials in the <code>.netrc</code> file on <code>heroku login</code>. The Git client uses cURL when interacting with HTTP remotes, and cURL uses the credentials from the <code>.netrc</code> file. See the <a href="https://devcenter.heroku.com/articles/authentication">CLI authentication article</a> for details.</p>
</div>

<p class="devcenter-parser-special-block-separator" style="display:none">&nbsp;</p>

<div class="callout">
<p>You can’t authenticate with the Heroku HTTP Git endpoint using your Heroku username (email) and password. The Heroku HTTP Git endpoint only accepts API-key based <a href="http://en.wikipedia.org/wiki/Basic_access_authentication">HTTP Basic</a> authentication. Use an API key as described in this section.</p>
</div>

<p>If you authenticate to the Git service with incorrect credentials, you get this error:</p>
<pre class="language-term"><code class="language-term">remote: ! WARNING:
remote: ! Do not authenticate with username and password using git.
remote: ! Run `heroku login` to update your credentials, then retry the git command.
remote: ! See documentation for details: https://devcenter.heroku.com/articles/git#http-git-authentication
</code></pre>
<p>If you’re using other Git clients, such as EGit or Tower, configure them to use an empty string for username and your account API key for password. The API key is <a href="https://devcenter.heroku.com/articles/authentication#retrieving-the-api-token">available in the CLI</a> and in the <a href="https://dashboard.heroku.com/account">dashboard</a>.</p>

<h2 id="reset-a-git-repository">Reset a Git Repository</h2>

<p>To reset or purge an app’s Heroku Git repository, use the <a href="https://github.com/heroku/heroku-repo">heroku-repo</a> CLI plugin:</p>
<pre class="language-term"><code class="language-term">$ heroku plugins:install heroku-repo
$ heroku repo:reset --app appname
</code></pre>
<div class="warning">
<p>Resetting the Git repository deletes all source code and Git history, so make sure you have another copy of the repository first.</p>
</div>

<h2 id="keep-your-repository-size-small">Keep Your Repository Size Small</h2>

<p>The uncompressed size of a checkout of <code>HEAD</code> from the repository, combined with the size of restored submodules, can’t exceed 1 GB.</p>

<p>It’s not recommended to deploy large repositories over 600 MB They can cause timeouts and slow pushes overall. Running <code>heroku apps:info</code> shows you your repository size.</p>

<p>Common causes of large repositories are binary files checked into the repository or constantly changing development logs. You can remove files committed by accident with <a href="http://git-scm.com/book/en/Git-Internals-Maintenance-and-Data-Recovery#_removing_objects">git filter-branch</a>. After running it, you must push your changes with the <code>--force</code> option, requiring coordination among your team.</p>

<p>After reducing the size of your repository locally, you must <a href="#reset-a-git-repository">reset the app’s Git repository</a> before pushing it to Heroku again.</p>

<h2 id="limits">Limits</h2>

<p>To protect the Git service, Heroku imposes certain limits on Git repository use and content size.</p>

<p>Heroku limits users to a rolling window of 75 Git requests per hour, per user, per app. After reaching this limit, Heroku denies Git requests until request levels drop below the limit for a few minutes. You see an error message like:</p>
<pre><code> !  Too many requests for this Git repo. Please try again later.
</code></pre>
<p>If you reach this limit, ensure there are not automated processes or scripts polling the Git repository.</p>

<p>In addition, the uncompressed size of a checkout of <code>HEAD</code> from the repository, combined with the size of restored submodules, can’t exceed 1 GB.</p>

<h2 id="deploy-code-tracked-in-subversion-or-other-revision-control-systems">Deploy Code Tracked in Subversion or Other Revision Control Systems</h2>

<p>While Git is one of the best choices available for revision control, you don’t need to stop using your current revision control system. You can use Git purely as a deployment mechanism, existing side by side with your other tool.</p>

<div class="callout">
<p>You can learn much more about <code>.gitignore</code> in <a href="https://devcenter.heroku.com/articles/gitignore">our article on the topic</a>.</p>
</div>

<p>For example, if you’re using Subversion, initialize your Git repository as described in the <a href="#prerequisites-install-git-and-the-heroku-cli">Pre-requisites</a> section. Then, add a <code>.gitignore</code> file to tell Git to ignore your Subversion directories.</p>
<pre class="language-term"><code class="language-term">$ git init
$ echo .svn &gt; .gitignore
$ git add .
$ git commit -m "using git for heroku deployment"
</code></pre>
<p>Now tell Subversion to ignore Git:</p>
<pre class="language-term"><code class="language-term">$ svn propset svn:ignore .git .
property 'svn:ignore' set on '.'
$ svn commit -m "ignoring git folder (git is used for heroku deployment)"
</code></pre>
<div class="callout">
<p>It’s recommended to use the <code>-f</code> (force flag) to avoid conflicts with other developers’ pushes. Since you’re using Git for your revision control, but as a transport only, using the force flag is a reasonable practice.</p>
</div>

<p>Each time you wish to deploy to Heroku:</p>
<pre class="language-term"><code class="language-term">$ git add -A
$ git commit -m "commit for deploy to heroku"
...

$ git push -f heroku
</code></pre>
<h2 id="additional-resources">Additional Resources</h2>

<ul>
<li><a href="http://railscasts.com/episodes/96">Git on Rails</a> shows common conventions for using Git to track Rails apps.</li>
<li><a href="http://res.cloudinary.com/hy4kyit2a/image/upload/SF_git_cheatsheet.pdf">Git cheat sheet</a></li>
<li><a href="http://git.or.cz/course/svn.html">Git - SVN Crash Course</a></li>
<li>The <a href="https://git-scm.com/book">Pro Git book</a> is a great resource that covers all of Git.</li>
</ul>

    <div class="article-footer panel">
      <div class="nocontent keep-reading" id="keep-reading"><h3><span class="icon-book-open"></span><a href="#keep-reading">Keep reading</a></h3><ul class="list-icons"><li><span class="icon-files"></span><a href="/categories/deploying-with-git">Deploying with Git</a></li></ul></div>

      <div class="article-feedback" id="feedback"><h3><a href="#feedback"><span class="icon-discussion"></span>Feedback</a></h3><p><a href="/login?back_to=%2Farticles%2Fgit&amp;utm_campaign=login&amp;utm_medium=feedback&amp;utm_source=web">Log in to submit feedback.</a></p></div>
    </div>
  </article>
</div>

  <div class="pagination">
    <a rel="prev" href="/articles/gitignore">Using .gitignore</a>
    <a rel="next" href="/articles/git-submodules">Resolving Application Dependencies with Git Submodules</a>

      </div>
    </div>

    <?xml version="1.0" encoding="UTF-8" standalone="no"?>
<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" style="position:absolute;width:0;height:0;visibility:hidden">
  <defs>
    <linearGradient x1="0%" y1="0%" x2="100%" y2="100%" id="gradient-purple">
  <stop stop-color="#AC8ECE" offset="0%"></stop>
  <stop stop-color="#79589F" offset="100%"></stop>
</linearGradient><linearGradient x1="0%" y1="0%" x2="100%" y2="100%" id="gradient-gray">
  <stop stop-color="#CFD7E6" offset="0%"></stop>
  <stop stop-color="#62738D" offset="100%"></stop>
</linearGradient><linearGradient x1="0%" y1="0%" x2="100%" y2="100%" id="gradient-dark-gray">
  <stop stop-color="#919CAE" offset="0%"></stop>
  <stop stop-color="#62738D" offset="100%"></stop>
</linearGradient><linearGradient x1="0%" y1="0%" x2="100%" y2="100%" id="gradient-blue">
  <stop stop-color="#8EBDF1" offset="0%"></stop>
  <stop stop-color="#006DEB" offset="100%"></stop>
</linearGradient><linearGradient x1="0%" y1="0%" x2="100%" y2="100%" id="gradient-green">
  <stop stop-color="#86CF95" offset="0%"></stop>
  <stop stop-color="#008700" offset="100%"></stop>
</linearGradient><linearGradient x1="0%" y1="0%" x2="100%" y2="100%" id="gradient-red">
  <stop stop-color="#DE7575" offset="0%"></stop>
  <stop stop-color="#DE0A0A" offset="100%"></stop>
</linearGradient><linearGradient x1="0%" y1="0%" x2="100%" y2="100%" id="gradient-orange">
  <stop stop-color="#FA9F47" offset="0%"></stop>
  <stop stop-color="#CE4C01" offset="100%"></stop>
</linearGradient>
   
  </defs>
</svg>

    <div hidden id='heroku-uuid' data-uuid=""></div>

    <!-- Google Tag Manager -->
<noscript><iframe src="//www.googletagmanager.com/ns.html?id=GTM-JD26"
height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
<script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
'//www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
})(window,document,'script','dataLayer','GTM-JD26');</script>
<!-- End Google Tag Manager -->
<script src="https://devcenter3.assets.heroku.com/assets/public-59973301ef87f6c004c486a90556128433dc8fc914b514abe6a0cdd42471b56c.js"></script>

<!--[if lt IE 9]>
<script src="https://devcenter3.assets.heroku.com/assets/public/vendor/selectivizr-1.0.min-5bcdad5ca1fd04e741f38ea80702024cb0b080f9e1763eb8fa4e79b1b6508b79.js"></script>
<![endif]-->

<script>
  
</script>

    
  </body>

    <script type="module" src="https://developer.salesforce.com/shared-components/helmet/import.js"></script>
</html>



Advanced Data Science and Innovation Autumn 2022
================================================

Assignment 1 Weekly Submissions

Week 1 13-Feb-2022 - Logistic Regression, Neural Net Multi Layer Perceptron 

Week 2 20-Feb-2022 - XGBoost, SMOTE, hyperparameter tuning

Setting up the environment
------------
1. Please put test.csv and train.csv inside /data/raw from the Kaggle competition https://www.kaggle.com/c/uts-advdsi-22-02-nba-career-prediction/data
2. Install dependencies in the requirements.txt `pip install -r requirements.txt`
3. Activate your virtual environment and run Jupyter notebook `pipenv run jupyter notebook`

Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>

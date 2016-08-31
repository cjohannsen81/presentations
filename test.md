Types of customer: (don't say Config Management)

      **Customer State**                   **Topics**                                                             **Value Message**                                                                                                        **Benefit**
  --- ------------------------------------ ---------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------ --------------------------------------
  1   New to C.M (less likely)             Automate (**Compliance**, CM , Local Dev, Delivery)                                                                                                                                             Speed and control
  2   New to Chef, CM Experienced          Automate (**Compliance**, Local Dev, Workflow, Visibility)             Benefit from our experience and our tools                                                                                Avoid 'worked in dev', deploy faster
  3   Existing Chef (upsell to Automate)   Automate (**Compliance**, Workflow, Visibility ~~Local Dev)~~          Benefit from our experience and our tools                                                                                Avoid 'worked in dev', deploy faster
  4   Existing Chef w CI                   Automate (**Compliance**, Visibility, Workflow for cookbook writing)   Find possible problems (compliance), develop better cookbooks with more confidence, see what’s happening (visibility).   
  5   New to Chef, (other) CM in use       Automate (**Compliance**, Local Dev, Workflow, Visibility              Complete lifecycle not just CM                                                                                           Deliver Faster, Make More £

Before run-through **setup**:

TODO: Write exhaustive set-up instructions (notes for large screens
too).

-   Kick-off ‘kitchen converge’ in the workstation to speed things
    > up later.

-   Sign into your chef interfaces

    -   **Chef Server** (Tab titled: "Chef Manage") - UN: delivery | PW:
        > Cod3Can!

    -   **Automate** - UN: delivery | PW: Cod3Can! | Organization
        > 'automate'

    -   **Compliance** - (N.B. you must select 'Use a Different
        > Provider' then select 'Chef Server' )

        -   UN: delivery | PW: Cod3Can

-   Run a scan before running the demo (Compliance)

    -   Once in, in the bottom left corner change from 'Delivery; to
        > 'Automate Org'

    -   Go to 'Delivered' and 'aut-rehearsal-node', click scan

        -   Unselect 'Operating System Patch' select
            > 'Automate-Org/cis-apachetomcat-8.0-level1.&gt;&gt; Click
            > Scan @ bottom.

-   Set your start screen to be Automate showing Visibility (as it
    > echo's your messaging).

### Presenting to small screens from a big screen

**Zoom in on apps:**

ConEmu - Settings , Main, set font to 24

Visual Studio Code: \[Ctrl\] \[+\]

Putty - Settings, window, appearance, change

Chrome, little three line button,

Set zoom to 150 or similar.

Change compliance to be CAD not ADMIN.

Principals:

-   People rarely pay attention for more than 20 minutes, your demo
    > should be around the 20 minute mark,

    -   You can consider the demo 'done' when you get past the Union
        > stage, referring occasionally to the progress and continue
        > the conversation.

-   Tell them what you're going to tell them, tell them it, tell them
    > what you told them.

-   Some people are visual learners, some learn by hearing, some by
    > seeing things done, we'll hit all three where possible, make sure
    > you hit on the point in **Bold** during your talk.

KEY:

-   **Bold** are the key parts of what you tell them

-   *Blue = instructor notes*

-   %consol is about code, code you add or code you must find and
    > point out.

-   Grey is a digression, a further explanation you can give if your
    > audience would appreciate it.

-   Red, customer question, ask this question to avoid a long pause.

Slide Deck Here: LINK TBC

  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **PHASE / Screen**   **Script**
  -------------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  INTRO                I'm going to show you how Automate will help your teams operate at **higher velocity.**
                       
  Slide 1              That is, making **changes** to your **systems** and **applications faster**, then, **shipping** those changes more **frequently** and with more **confidence.**
                       
                       Using these very tools Chef has seen it's own **productivity increase** by:
                       
                       Statistics xxx
                       
                       Xxxx
                       
                       Xxx
                       
                       **Let's set the scene:**
                       
                       I am a **DevOps engineer,** I manage **production** and **test environments** for **multiple applications** and **infrastructures** and all of these systems are **Under Control** of or simply **Overseen** by **Chef.**
                       
                       **I am going to show:**
                       
                       -   How we find out if **change is needed** (**Chef Compliance**)
                       
                       -   How we **develop** a change/feature **locally** (**Chef Kitchen**)
                       
                       -   How changes from **local dev** into a **Collaborative Continuous Delivery Pipeline** (Chef **Workflow)**
                       
                       -   We will see how we **systematically build our confidence** in these changes using chef's testing language **(Inspec), abstracting you from the how so you can focus on the what.**
                       
                       -   Finally how we **oversee** all of this **'Progress'** through a **cohesive interface** - Chef **Visibility**.
                       
                       

  VISIBILITY           You can see here an **overview** of **all** of your **chef estate.**
                       
  Automate tab /       The aim is to give you a **meaningful dashboard** of everything chef is managing for you.
                       
  Welcome              TOP LEFT We've got an **overview** of **last 8 hours** of our **chef controlled systems**, successes, failures and cookbook changes, workflow changes. This graphic **could represent all of your infrastructure** and it's showing that it is in your **desired state**.
                       
                       TOP RIGHT we have an overview of **automated testing nodes** and how much testing they've handled in the **past two weeks**.
                       
                       Lower Centre We have an **overview** of how much **change** is being put through your **Workflow Pipeline** over the last **two weeks**.
                       
                       We are using this very tool (automate/workflow) to develop the product you see here, and we'll be delivering more functionality for Compliance overviews and habitat in the coming months.

  AUTOMATE             Let's take a look at the **nodes** in **more detail**:
                       
  Node Detail          Click '**Nodes**' (centre top under 'Chef Automate')
                       
                       **EXPLAIN NODEs:**
                       
                       To chef a **Node** is some **compute** that Chef is **controlling** or **communicating** with.
                       
                       > physical machines, VMs, network equipment (e.g. F5 loadbalancer) cloud servers (private/public), docker container.
                       
                       **Converge Status** the green here tells us that **all our nodes** are in their **desired state** as set by our open source product and namesake Chef, **in Chef** we **define** in code the **Desired State** and **Chef makes it happen**.
                       
                       > This **saves time** and **reduces errors** as the tools are already written and in use by the community**.**

  AUTOMATE             Click '**Compliance Status**' (upper left)
                       
  Compliance           **Compliance Status**
                       
                       In the last screen we saw that chef’s nodes are in their **Desired State**.
                       
                       Here we are **testing** these nodes against a **compliance Profile** and seeing how our systems measure against that profile.
                       
                       **Compliance** allows you **agentless audit** of **Windows** and **Unix** nodes against a **Profile** (often for **security), **
                       
                       That **Profile** is either from **our library** of **policies** or **written by your to conform to your requirements.**
                       
                       > Profiles we offer are currently CIS (Centre of Internet Security), we have Apache, mysql, postgres, ssh… we’re working on a PCI Profile expected by 2017.
                       
                       These checks are run either on a schedule of your choosing, or when you decide to run the checks through this interface.
                       
                       You can see that we have '**critical** compliance issues here, and issues are categorized by severity to help you prioritize.
                       
                       > *This could be because:*
                       >
                       > we've adopted a **new Compliance Profile**,
                       >
                       > We've added **new nodes** to be **overseen**
                       >
                       > Whatever the reason **nodes are noncompliant** with the **Profile** they’re being **measured against**.
                       
                       Let's look into why…
                       
                       CLICK into the 'aut-prodweb-node' by clicking the failed profile red exclamation
                       
                       We can see, **passes**, **failures** and **warnings** for each Profile requirement.
                       
                       SCROLL DOWN.
                       
                       **All but one** have passed their checks except **'Restrict\_access to Tomcat Web application directory'**
                       
                       These requirements have come from CIS's Apache Tomcat benchmarks.
                       
                       CLICK ON THE ROW OF THE ERROR
                       
                       We have explanation of the issue in English,
                       
                       > "The Tomcat webaps directory contains web apps …. The ownership of this directory should be apache-tomcat and they're not world readable / writable"
                       
                       Then below the code that's used to ascertain if this server is compliant.
                       
                       > "the code will return an empty string if the directory is owned by the apache-tomcat users"
                       
                       What's this server’s role?
                       
                       We're managing a tomcat application here on-top of a virtual machine.
                       
                       Here's the product:
                       
                       CLICK 'Pet Clinic' tab
                       
                       Through **Chef Compliance** we have identified a **critical security issue,** we’ll now **remedy** this with with Chef using a systematic and collaborative approach.

  LOCAL DEV            Local Development
                       
  Terminal             The first step of solving a problem is **recreating** it in a **non-disruptive test environment**.
                       
                       As we've got the **application** and **configuration** all as code being **managed by Chef**, this is very **easy**!
                       
                       SWITCH to the terminal
                       
                       RUN (explain later) %Kitchen converge
                       
                       Chef has **suite** of **tools** for **developers - Chef Kitchen**, these automated tools help develop with **confidence** and **speed**.
                       
                       We have just instructed our development suite to recreate production for us that is:
                       
                       **Recreate** the **Tomcat server,**
                       
                       **Deploy** the app**,**
                       
                       **Apply the hardening instructions**
                       
                       **Re-run the same test suite as we saw in production.**
                       
                       > This suite is available on all major platforms (Windows, Mac, Ubuntu, Redhat, Debian)
                       
                       Kitchen has **provisioned an instance** on **AWS** just for me.
                       
                       It could deploy all of chef’s supported environments:
                       
                       > **Azure**, **OpenStack**, **VMWare**, Bare Metal, Containers like **Docker** or even Vagrant VMs on your laptop.
                       
                       This can **minimise costs** by having **ephemeral** **test** **environments** for development.
                       
                       You could write a recipe that puts an 'always up' test environment to a known state at the start of each testing procedure.
                       
                       Where do your developers currently deploy their tests to?
                       
                       Are their plans to change that?
                       
                       %Kitchen Verify
                       
                       No one wants to **fail**, but it's **part of progress**, so... if you must fail, **fail fast…**
                       
                       As part of the Chef-Client run on the test instance it has been tested against that same Compliance Profile.
                       
                       ERROR is in red, same explanation as Compliance.
                       
                       That's the **issue Recreated**, let's fix it…

  LOCAL DEV            Still in terminal
                       
  VS code              We'll first **create** a feature **branch** as this is a collaborative project with a **repository**:
                       
                       %git checkout -b fixtcweb
                       
                       SWITCH into Visual Studio Code
                       
                       Here we have both the Java Application Code in 'src' source
                       
                       We also have under '**Cookbooks**' Chef Code, in here we defined the desired state of the instances within this solution.
                       
                       SELECT "Cookbooks/Recipes/default.rb"
                       
                       Here we have a **recipe** (which forms **part** **of** **a** **cookbook**), and this particular recipe will be applied to any instance employing the 'Spring-Pletclinic app deploy" cookbook.
                       
                       Move to:
                       
                       Package 'curl' do
                       
                       action :install
                       
                       This using the chef '**Resource**' - '**Package**' installs the Linux package '**curl**' which is used later within this recipe.
                       
                       **We** **don't** **explain to Chef** where to get this package or **how to install** it.
                       
                       > In fact if the default action of the package resource is to install so you could simply write 'package curl do'
                       
                       There are **many resources** from **Chef** and our **thriving community** to say **'what',** rather than **'how'.**
                       
                       > E.g. Scheduler, Windows Services, users, environment variables...
                       
                       Scroll to the include for recipe 'Tomcat Hardening'
                       
                       **Within** this **default** recipe there's an i**nclude** for the recipe **'tomcat hardening'** allowing for **Reuse** and **Inheritance**.
                       
                       This has been written as a **security layer** to make this **compliant** with the **CIS tomcat profile**… **almost**.
                       
                       There's **one** **remaining issue** which we've seen in compliance.
                       
                       Move to the file :
                       
                       /tomcat/hardening.rb
                       
                       At the top of the recipe
                       
                       %w(bin conf logs temp)
                       
                       We see that the **\$webapps directory** is **not** **included** in this permission setting.
                       
                       Add the 'webapps' to your code:
                       
                       %w(bin conf logs temp ***webapps***)
                       
                       > This will loop through the folders in this list and apply the permission 0750 to the folders in the list allowing World no access, Group Read and execute and user Read Write eXecute.
                       
                       **Software** **dependencies** **are very important**, we can use **versions** so that we know when we deploy to production our tests remain valid.
                       
                       Move to file /cookbooks/ spring-pet-clinic-app-deploy/ metadata.rb
                       
                       > In metadata.rb we can version the dependant cookbooks as well as this cookbook for ‘version pinning’ for references to this cookbook.
                       
                       Increase 'version' by x.x.+1

  LOCAL DEV            SWITCH back to the terminal
                       
  Terminal             % kitchen Converge
                       
                       We’ll now **locally test** that our **change resolves the issue**,
                       
                       -   The changes we've made are now being **copied across** to the already created **environment**, we could tear it down and start again… but we'll see why that's not necessary later.
                       
                           -   The system is **evaluating** if is in the **desired state already**, if it were it would do nothing.
                       
                       -   ***Note that**: If configuration requirements have been removed, say tomcat was no longer required on this node…*
                       
                       > *Chef would not change anything about tomcat on that node making removals of requirements safe.*
                       >
                       > *If you did want to remove tomcat, you would write a removal Recipe.*
                       
                       -   *Rather than modeling each role entirely, some customers prefer by controlling certain aspects of systems with Chef and extend Chef’s remit on the servers as required.*
                       
                       <!-- -->
                       
                       -   Chef now sees that the majority of the system is as it should be except the permissions on our folder
                       
                       -   It then decides based on the underlying operating system how it should make this change.
                       
                       Question: (if using chef) are you using any of these tools already?
                       
                       % kitchen verify
                       
                       Highlight - 'Restrict-Access-to-tomcat-web-application'
                       
                       n.b around 7 down from start of repetition
                       
                       So now we see that we have fixed that issue (our test now passes) (they don’t)
                       
                       We will **commit** this success to our **repository**.
                       
                       % git add .
                       
                       % git commit -m "set correct permissions on webapp dir"
                       
                       Question: Are we now happy to push this change out to production?
                       
                       **We believe** that it **works**, we're certain it's **compliant, but** were **not certain it won’t** cause issues on **dependant** **systems**.
                       
                       Next we push this change into our Collaborative pipeline, Chef Workflow.
                       
                       % delivery review

  WORKFLOW             *Frame Workflow, you've got time to kill:*
                       
  Intro                The pipeline we have here is **borne** from **our experience**:
                       
                       > Our **experience** **working** with **customers** from **fortune 100s** to **Start-ups**
                       >
                       > Our **experience** of both authoring **Premium Applications** and as a **Steward** of **Collaborative** **Open**-**Source** **Software** .
                       >
                       > **Chef** use **Workflow** to **Deliver Automate**’s suite and Habitat. **Chef** **Workflow** **empowers** **Chef** to **deliver** **features;**
                       >
                       > **more** **frequently**, with **less** **effort** and with **more** **confidence** to our customers.
                       >
                       > Which helps our customers do the same.
                       
                       **Workflow** (as we will see) works for **Both, Application** **Code** and Cookbook **Code**. It also **works** **for** **Windows**; if you want to use it for **.NET and MSSQL no problem.**
                       
                       Show Pipeline Slide
                       
                       The **Pipeline shape** has **Evolved t**hrough use by **chef** and **customers,** to the Stages (across the top) and Phases (below):
                       
                       We’ll discuss each one.
                       
                       **Notice** that we’ve got **two Human Gates** which allow us to do what we **Humans** are **great at, considered decisions**, the **Chef** **Workflow’s** going to take care of the **Repetitive** **Tedious** **Work**.
                       
                       If you're using this pipeline to develop distinct projects here's how that could look SLIDE X

  WORKFLOW             Verify Stage.
                       
  Verify               **Initially** we are **testing against** our local '**feature branch**',
                       
                       > This gives your developers the ability to experiment without disrupting your releasable product in the 'Master Branch'
                       
                       The aim of this Stage is to carry out the **basic tests** that you'd **expect** **any code base to pass**, on the **local branch**. These include…
                       
                       -   **Unit** tests - Run the suite of unit tests against this change, do they pass?
                       
                           -   This is running **Junit** tests against the Java Code
                       
                           -   It's also running **Chefspec** (Rspec) Tests against the Chef Code
                       
                       <!-- -->
                       
                       -   **Lint** Tests - Is the Code **conforming** to **industry** or and **company style**?
                       
                           -   **Food critic** checks you cookbooks adhere to industry standards.
                       
                           -   Java equiv?
                       
                       -   **Syntax tests** - can the system see any problems with the code before taking trying to build from it?
                       
                           -   **Rubocop** checks the syntax of your cookbook code
                       
                           -   Java equiv?
                       
                       

  WORKFLOW             Approve Stage
                       
  Approve              The changes should pass these basic tests but **does** **someone** **else** in your **organisation** need to **approve changes?**
                       
                       **Peer** or **Management** **review** is applied here,
                       
                       > “Is what it's doing a good idea”, does someone else think it will work?
                       
                       This is the **first** of **two human gates…**
                       
                       Click Review(left of centre of screen)
                       
                       We can see the **line by line changes** in a **GUI** which is **intuitive** and **familiar** to many.
                       
                       This is **how it will look** when merged with the **master branch**.
                       
                       Here we can add a comment...
                       
                       > Code review, with the best will in the world can be a 'dry' activity.
                       >
                       > If your team want to they can drop in any rich web assets, including Gifs, Youtube Videos etc…
                       
                       ADD A COMMENT
                       
                       Once we're happy that the changes are a good idea, we **'Approve’** which **merges** them **into** the **Master** Branch
                       
                       TOP RIGHT GREEN BUTTON & confirm.

  WORKFLOW             Build Stage
                       
  Build                Here we're running the **same tests** again but this time **against the master branch**, so making sure that the changes we've made in isolation **don't damage** the code on the **Master** branch.
                       
                       We want **Master** to **remain ship-able**.
                       
                       We can **look deeper** into what's happening **behind** **the** **scenes** by clicking on the title of each stage.
                       
                       Click Syntax
                       
                       **Errors** and **warnings** are all **colour coded** making it **easier** to interpret.
                       
                       It's a good place to **investigate failures** which will happen as you push code through this pipeline.
                       
                       > You can see 'execute knife cookbook test -o /var/opt/… is being used to test our cookbook,
                       >
                       > We're also executing a 'Maven' compile % 'execute mvn compile' which assists with the building of the java assets
                       
                       There are **two additional Phases** which will run additional tests you define **under** the **remits** of **Quality** and **Security**.
                       
                       **In the Publish Stage**
                       
                       For application code, we are sending it to be put into your **desired** **end format**, that could be through a **something** like **Jenkins**, into a packaging tool like JFrog putting it somewhere that it can be accessed as a built artifact.
                       
                       In our example we are uploading our artifact to Amazon S3 where it’s available to our build processes , We are also **publishing** the Chef **Cookbook**s to the **Chef Server**.

  WORKFLOW             Acceptance Stage
                       
  Acceptance           The **Acceptance** stage and the **subsequent three stages** (Union, Rehearsal & Delivery) perform the same phases**.**
                       
                       **Chef Workflow** can be configured to **provision a new environment** for each stage, in our case it is deploying to existing environments.
                       
                       Workflow is ensuring that the infrastructure is in the defined Desired State when the tests are run if new or an existing environment.
                       
                       **Provision -** if necessary provision **new** **infrastructure** for this environment.
                       
                       **Deploy** - **Publish** the **code** to that node and apply it.
                       
                       **Smoke -** tests that show it is working at all.
                       
                       > The term originates from Electrical engineering, when applying power to a circuit for the first time if there was a problem it would smoke… or worse catch fire.
                       
                       **Functional -** Test that show it is working as expected
                       
                       ***How are you currently testing?***
                       
                       -   Are there human processes?
                       
                           -   Are they documented in a way that lends itself to being automated?
                       
                       -   Do you have application tests already in place which could be used in this pipeline?
                       
                       -   Do you test their application in an automated way?
                       
                       -   How is code reviewed currently?
                       
                       

  WORKFLOW             **Human Gate \#2 Deliver?**
                       
  Deliver Human Gate   Show node status of acceptance node (tab)
                       
                       Then in workflow: Click Approve
                       
                       Once approved…
                       
                       All being well this will **go** through **to** **delivered…** but **Delivered** **can mean many things**…
                       
                       -   Perhaps it goes out in your next nightly release,
                       
                       -   It may be published to your customers user acceptance environment
                       
                       -   It could immediately be applied to your production environments by Chef and PushJobs
                       
                       *Current Release Cycle Questions:*
                       
                       -   How often are you currently releasing?
                       
                           -   How often would you like to release?
                       
                               -   What would the advantages for you of releasing more frequently?
                       
                       -   In the current method of delivering what’s keeping you from releasing more frequently?
                       
                       -   Do you ever need to release very quickly?
                       
                           -   Has that been problematic in the past?
                       
                       

  WORKFLOW             Union Stage
                       
  Union Stage          **Union runs** the **same tests** as in **Acceptance** but now, It **pulls** in all the **dependencies** of this system which are **managed within Chef** and gives you a more **complete test experience**,
                       
                       *Questions) this is a Collaborative pipeline.*
                       
                       -   What challenges have you seen with teams working together on the same codebase?
                       
                       -   How are dependencies tracked and tested currently?
                       
                       -   How is your code currently reviewed
                       
                       -   How do you manage / test applications that are dependant on each other.
                       
                       -   How do you share the progress of testing and the status of other teams code, visibility could help with this.
                       
                       

  WORKFLOW             Rehearsal Stage
                       
  Rehearsal            This would be your most production like environment,
                       
                       You may have simulated loads and HA, it's as 'life like' as you want it to be.
                       
                       Often the pipeline gets errors at union. Rehearsal allows you to make sure once fixed in that more issue prone environment it works cleanly in Rehearsal.
                       
                       This could be your most production like test environment.
                       
                       Questions)
                       
                       -   What are your testing environments today?
                       
                       -   From what we’ve seen do they map up with what we’ve outlined here?
                       
                       -   How are you updating your test environments?
                       
                       
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

AH 2016-08-26 WORKING ON THIS: ….

To summerize:

**Chef is able to manage**:

The **identification** and review of security flaws in systems under its
control and under it’s supervision with an agentless system

The **provisioning** of the **infrastructure** that this sits on, in
this case AWS but it could be **any** of the **Prevalent Industry
Platforms**.

The **configuration** of the **instance** through **desired state
configuration** of both **Windows** and **Linux**

The **development**, **testing** and **deployment** of the i**nstance
Configuration** and **Application** code.

All from one integrated toolchain.

This is a **Collaborative**, **Capable** and **Customisable** solution.

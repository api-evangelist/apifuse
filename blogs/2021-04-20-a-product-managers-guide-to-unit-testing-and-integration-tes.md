---
title: "A Product Manager’s Guide to Unit Testing And Integration Testing"
url: "https://apifuse.io/blog/product-managers-guide-to-unit-testing-integration-testing/"
date: "Tue, 20 Apr 2021 08:58:02 +0000"
author: "Mike Clarke"
feed_url: "https://apifuse.io/blog/feed/"
---
<p>A crucial part of developing a SaaS application is testing. There are many different approaches to examining whether the code of the software application is working as expected or not. Two of them are <a href="https://en.wikipedia.org/wiki/Unit_testing">unit testing</a> and <a href="https://en.wikipedia.org/wiki/Integration_testing">integration testing</a>.</p>
<p>Both these testing types require coding as opposed to other test techniques such as screen recording. Unit and integration tests can often be performed using similar tools. Also, it is advised to include both in the continuous integration and continuous delivery pipeline.</p>
<p>Barring these similarities between the two tests, they are quite different. We drill down on each here.</p>
<h2><b>What is Unit Testing?</b></h2>
<p><img alt="" class="aligncenter size-full wp-image-552" height="774" src="http://apifuse.io/blog/wp-content/uploads/2021/04/What-is-unit-testing.jpg" width="1480" /></p>
<p>The target audience of most testing techniques, be it manual or automated, is the end-user. The test serves as solid proof that the software meets the requirements of the final user. Unit testing is unique in that the target audience is not the user but the developer.</p>
<p><b>Unit tests are written and read by developers to verify if a small part of the code they wrote is working as it should</b>. The isolated piece of the codebase is called a <b>unit</b>. It is the smallest component of the application.</p>
<p>The individual unit test must be completely secluded from all external factors for three reasons:</p>
<ol>
<li style="font-weight: 400;">It increases the <b>speed</b>. When tests have to depend upon databases or other things, it slows the process.</li>
<li style="font-weight: 400;">It enables <b>determinism</b>. In other words, if the test passes, it continues to do so until the code is changed and vice versa.</li>
<li style="font-weight: 400;">It allows for <b>precise feedback</b>. If the test fails, a developer knows the issue is with that excerpt to the code.</li>
</ol>
<p>A test case is a portion of the code that uses the production code and then checks if the behavior is as intended. It can verify that the classes or modules of your SaaS software function correctly.</p>
<ul>
<li style="font-weight: 400;">Unlike several other automated testing, unit tests don’t exercise the user interface. They communicate with the API directly.</li>
<li style="font-weight: 400;">They are close to the application source, so at a lower level and with a narrow scope.</li>
<li style="font-weight: 400;">They are easy to write and implement. Moreover, it is <b>cheaper</b> to automate them.</li>
<li style="font-weight: 400;">Because unit tests are meant for the developer, they’re not much use to others.</li>
</ul>
<h3><b>What is the objective of a unit test?</b></h3>
<p><img alt="" class="aligncenter size-full wp-image-553" height="774" src="http://apifuse.io/blog/wp-content/uploads/2021/04/What-is-the-objective-of-a-unit-test-1.jpg" width="1480" /></p>
<p><b>A unit test’s primary goal is to find bugs at the first stage of software development.</b> When you skip unit testing, other testing cycles become more challenging. Since, by then, units have been integrated, they impact the entire application.</p>
<p><b>Another purpose of unit tests is documentation</b>. The logs offer the team a comprehensive description of the SaaS application at an atomic level. The documentation is particularly helpful when new developers come on board.</p>
<p>With unit testing, developers are confident that the written code has no issues. This <b>improves code reusability.</b></p>
<p>Lastly, unit tests offer a great framework to understand and handle API.</p>
<h2><b>What is integration testing?</b></h2>
<p>Integration testing assesses the communication between the different modules of the <a href="http://apifuse.io/blog/improve-saas-customer-retention-with-integration/">SaaS application</a>. An integration test verifies that all the pieces of the application work together as expected. It demonstrates to others and not just programmers and developers that the application works.</p>
<ul>
<li style="font-weight: 400;">Integration tests rely on other resources like hardware or databases.</li>
<li style="font-weight: 400;">They are heavier on the pocket because they check several parts of the app.</li>
<li style="font-weight: 400;">Integration testing is the second step of the development process, and it happens after unit testing.</li>
</ul>
<p>According to <a href="https://martinfowler.com/bliki/IntegrationTest.html">Martin Fowler</a>, you can divide integration tests into narrow and broad. Narrow integration tests are those with limited scope. They exercise a part of the code that communicates with a separate service. Narrow integration test “<i>uses test doubles of those services, either in process or remote.”</i></p>
<p>Broad integration tests need hefty network access and an optimum test environment since they use live versions of all services. They are not limited to the portion of the code that talks to services. They “<i>exercise code paths through all services.” </i>The majority of software application developers consider only broad integration tests as valid integration testing.</p>
<p>There are four primary integration testing approaches top-down, bottom-up, big bang, and mixed.</p>
<ul>
<li style="font-weight: 400;">When complicated modules are tested before low-level ones, it is a top-down integration test.</li>
<li style="font-weight: 400;">When the low-level and basic modules are tested first and then complex ones, it is a bottom-up integration test.</li>
<li style="font-weight: 400;">When all modules are tested together, it is a big bang integration test after they are completed.</li>
<li style="font-weight: 400;">When teams use both top-down and bottom-up approaches, it is called a mixed integration test.</li>
</ul>
<p>Each method has its pros and cons. For instance, the mixed approach doesn’t require the team to wait for a module to be coded. They can begin testing at any time. With the bottom-up approach, the time is reduced because basic modules are completed faster and easier to test.</p>
<h3><b>What is the objective of integration testing?</b></h3>
<p><img alt="" class="aligncenter size-full wp-image-554" height="774" src="http://apifuse.io/blog/wp-content/uploads/2021/04/What-is-the-objective-of-integration-testing.jpg" width="1480" /></p>
<p>The fundamental purpose of an integration test is to <b>ensure that all modules of the application work well after integration</b>. The connectivity of each part should match the requirements.</p>
<p>Another goal of the test is <b>to expose interface faults </b>or errors when two units interact. The test validates functional and non-functional elements. Further, it makes sure that <b>all modules are in sync</b>. And finally, it is essential for <b>fixing weak spots </b>and reducing risk before the final build.</p>
<p>Since integration tests encompass the whole application, they require more effort. Each test uses factual internal and external dependencies. Often, to complete an integration test, the team will have to create configuration files, test stubs, or generate realistic but bogus test data.</p>
<p>These additional tasks make integration testing harder. On top of it, after the test is completed, you have to remove any trace of these tasks. Else, they create problems for the next test run.</p>
<h2><b>Unit vs. Integration Testing: Crucial Differences</b></h2>
<p>A SaaS application is typically developed by a whole team, which requires dividing the app into modules. Each module is then split between different developers of the team.</p>
<p>Say you are one such developer. You write the code for a common function of the app and then test it. This falls under unit testing. Now assume another developer in the team has completed his or her module. You want to make sure that your module, when integrated with the other, works as required. That will fall under integration testing.</p>
<p>This was the underpinning difference between unit tests and integration tests. Another distinction between the two is dependencies. Unit tests check internal consistencies and don’t rely on outside systems. In comparison, integration tests convince people that they play nice even with external systems.</p>
<p>For example, a unit test would verify that your libraries work. An integration test demonstrates that your code communicates correctly with another code.</p>
<p><img alt="" class="aligncenter size-full wp-image-555" height="1772" src="http://apifuse.io/blog/wp-content/uploads/2021/04/Unit-Test-Vs-Integration-Test.jpg" width="1024" /></p>
<p>*<a href="https://en.wikipedia.org/wiki/White-box_testing"><i>White Box or clear box testing</i></a><i> are tests that analyze the internal elements and structure of an application. Behavioral or Black box testing does the reverse. It analyses the functionality of the application without knowing the internal structure.</i></p>
<p>Any test is a financial investment. Ergo, a crucial difference between unit and integration testing is the cost. Unit testing is cheaper in terms of writing code. It doesn’t require extensive developer time.</p>
<p>Since unit tests don’t demand external sources to create a unique environment, they are <b>less expensive</b> to run. And for the same reason, unit tests can be completed as quickly as a few milliseconds.</p>
<p>Maintaining a unit test is also pretty light on the pocket. Moreover, you can run parallel unit testing as each unit is isolated. This saves time further, which in turn is less costly.</p>
<p>Compared to the different areas where unit tests save costs, integration testing turns out to be more expensive. For instance, maintaining integration tests is costly.</p>
<p>But just because they are costlier doesn’t mean you can skip them. The feedback integration testing delivers to a SaaS application is equally important and valuable. The only difference is that you should make more strategic use of integration tests.</p>
<h2><b>When to use which testing method?</b></h2>
<p>The rule of thumb with testing is &#8211; test early and often. It reduces the cost to you. Experience proves that fixing issues as soon as possible is about four to five times cheaper than correcting them after a release.</p>
<p>Since unit tests validate the behavior of basic code and are fast, you should prioritize them over integration tests. Plus, you don’t need a skilled team of testers to perform unit testing. The developers can conduct them too.</p>
<p>So, run them on excerpts of your code that don’t rely on external dependencies frequently. After you’ve corrected the defects that break the design contracts and improved the codebase, perform integration testing.</p>
<h2><b>Unit and Integration Testing are Important to your Test Pyramid</b></h2>
<p>The <a href="https://martinfowler.com/articles/practical-test-pyramid.html">testing pyramid</a> for any application has many layers of tests, each with different granularity. All have their place because every test accomplishes an additional requirement. That&#8217;s why both unit testing and integration testing have value.</p>
<p>With a unit test, a developer gains a safety net. They have access to fast tests that offer exact feedback. With integration tests, teams can test real scenarios – situations that come as close to the end-user experience as possible. In short, integration testing walks paths that unit tests just cannot.</p>
<p>So, when testing your SaaS application, don’t move forward with an ‘either/or’ approach. Take an ‘and’ approach. Unit tests and integration tests both are essential to application testing as they complement each other by detecting bugs and defects at an early stage.</p>
<p><a href="https://apifuse.io/">API Fuse</a> enables you to offer on-demand integrations and to rapidly respond to end-users integration requests. With our solution and <a href="https://www.apifuse.io/pricing">range of plans</a>, you can offer users native or custom integrations embedded directly into your SaaS app in minutes to accelerate your product roadmap and reduce technical debt. <a href="https://apifuse.io/signup">Request a demo today for more information</a>!</p>
<p>The post <a href="https://apifuse.io/blog/product-managers-guide-to-unit-testing-integration-testing/" rel="nofollow">A Product Manager’s Guide to Unit Testing And Integration Testing</a> appeared first on <a href="https://apifuse.io/blog" rel="nofollow">API Fuse</a>.</p>

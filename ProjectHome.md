# Ehcache Annotations for Spring #

A successor in spirit of the annotations provided by the Spring-Modules Cache library that allows declarative, aspect based caching to be added to a [Spring Framework](http://www.springsource.org) based application by simple annotation.

Ehcache Annotations for Spring is available via maven, simply add the following dependency to your pom.xml

```
<dependency>
  <groupId>com.googlecode.ehcache-spring-annotations</groupId>
  <artifactId>ehcache-spring-annotations</artifactId>
  <version>1.2.0</version>
</dependency>
```

If you're new to EhCache please read their [Getting Started with EhCache](http://ehcache.org/documentation/getting_started.html) documentation before digging into this library. EhCache Spring Annotations is an addition to Spring & EhCache, it still requires you have a working knowledge of both technologies.

To get started, read the documentation on using [@Cacheable](UsingCacheable.md) and [@TriggersRemove](UsingTriggersRemove.md).

Also take a look at this [Quick Start](http://blog.goyello.com/2010/07/29/quick-start-with-ehcache-annotations-for-spring/) article by Rafał Borowiec.



<table border='0'>
<tr>
<td>
<wiki:gadget url="http://www.ohloh.net/p/482071/widgets/project_users.xml" height="100" border="0"/><br>
</td>
<td>
<wiki:gadget url="http://www.ohloh.net/p/482071/widgets/project_partner_badge.xml" height="53" border="0"/><br>
</td>
<td>
<a href='https://ehcache-spring-annotations.ci.cloudbees.com/'><img src='http://web-static-cloudfront.s3.amazonaws.com/images/badges/BuiltOnDEV.png' /></a>
</td>
</tr>
</table>

## 1.2.0 Release - September 19, 2011 ##
  * [Issue 50](https://code.google.com/p/ehcache-spring-annotations/issues/detail?id=50): Add attribute to @Cacheable to prevent caching of null values
  * [Issue 55](https://code.google.com/p/ehcache-spring-annotations/issues/detail?id=55): Add Self Refreshing Cache
  * [Issue 57](https://code.google.com/p/ehcache-spring-annotations/issues/detail?id=57): Fix incompatibility with Google App Engine
  * [Issue 60](https://code.google.com/p/ehcache-spring-annotations/issues/detail?id=60): Added interceptor API for Cacheable and TriggersRemove annotations
  * [Issue 65](https://code.google.com/p/ehcache-spring-annotations/issues/detail?id=65): Switch Cacheable to use Ehcache.getWithLoader instead of just Ehcache.get
  * [Issue 66](https://code.google.com/p/ehcache-spring-annotations/issues/detail?id=66): Replaced weak-valued concurrent map from Guice with MapMaker using Guava
  * [Issue 70](https://code.google.com/p/ehcache-spring-annotations/issues/detail?id=70): Add max-wait option for using self populating cache to avoid hung threads
  * [Issue 79](https://code.google.com/p/ehcache-spring-annotations/issues/detail?id=79): Fix NPE from missing chained exception when using selfPopulating cache
  * [Issue 80](https://code.google.com/p/ehcache-spring-annotations/issues/detail?id=80): commons-codec is now an optional dependency
  * See the  [1.2.0 Fixed Issues](http://code.google.com/p/ehcache-spring-annotations/issues/list?can=1&q=label%3AMilestone-Release1.2.0) list for full release details

## 1.1.2 Release - July 6 2010 ##
  * [Issue 38](https://code.google.com/p/ehcache-spring-annotations/issues/detail?id=38): Fix dependency cycles between packages found by jDepend
  * [Issue 39](https://code.google.com/p/ehcache-spring-annotations/issues/detail?id=39): Update 1.1 XSD to reference Spring 2.5 instead of 3.0 so things work correctly in Spring 2.5
  * See the full [1.1.2 Fixed Issues](http://code.google.com/p/ehcache-spring-annotations/issues/list?can=1&q=label%3AMilestone-Release1.1.2) list for full release details

## 1.1.1 Release - June 30 2010 ##
  * [Issue 35](https://code.google.com/p/ehcache-spring-annotations/issues/detail?id=35): Add new [@PartialCacheKey](UsingPartialCacheKey.md) annotation that allows for only specific method arguments to be used for key generation
  * [Issue 34](https://code.google.com/p/ehcache-spring-annotations/issues/detail?id=34): Allow for multiple caches to be specified in a [@TriggersRemove](UsingTriggersRemove.md) annotation.
  * Some minor performance improvements around runtime annotation configuration lookup.
  * See the full [1.1.1 Fixed Issues](http://code.google.com/p/ehcache-spring-annotations/issues/list?can=1&q=label%3AMilestone-Release1.1.1) list for full release details

## 1.1.0 Release - June 28, 2010 ##
  * Add new [@KeyGenerator](UsingKeyGenerator.md) annotation that allows key generation to be configured in the [@Cacheable](UsingCacheable.md) and [@TriggersRemove](UsingTriggersRemove.md) annotation
  * Refactor key generation classes so that all key generators can take advantage of reflection and common code paths
  * Add a new ehcache:config element which can configure a background task to execute evictExpiredElements on caches.
  * Add ability to specify if the cache remove action from [@TriggersRemove](UsingTriggersRemove.md) happens before or after the advised method executes.
  * Add OSGi support in the released JAR.
  * Fixed some bugs with the namespace handler that prevented property placeholders from working correctly.
  * See the full [1.1.0 Fixed Issues](http://code.google.com/p/ehcache-spring-annotations/issues/list?can=1&q=label%3AMilestone-Release1.1.0) list for full release details


## 1.1.0-RC2 Release - June 18, 2010 ##
  * Add ability to specify if the cache remove action from [@TriggersRemove](UsingTriggersRemove.md) happens before or after the advised method executes.
  * Add OSGi support in the released JAR.
  * Fixed some bugs with the namespace handler that prevented property placeholders from working correctly.
  * See the full [1.1.0 Fixed Issues](http://code.google.com/p/ehcache-spring-annotations/issues/list?can=1&q=label%3AMilestone-Release1.1.0) list for full release details

## 1.0.5 Release - May 28, 2010 ##
  * Fix hash code key generation for Floats & Doubles
  * [1.0.5 Fixed Issues](http://code.google.com/p/ehcache-spring-annotations/issues/list?can=1&q=label%3AMilestone-Release1.0.5)

## 1.1.0-RC1 Release - May 17, 2010 ##
  * Add new @KeyGenerator annotation that allows key generation to be configured in the @Cacheable annotation
  * Refactor key generation classes so that all key generators can take advantage of reflection and common code paths
  * Add a new ehcache:config element which can configure a background task to execute evictExpiredElements on caches.
  * See the full [1.1.0 Fixed Issues](http://code.google.com/p/ehcache-spring-annotations/issues/list?can=1&q=label%3AMilestone-Release1.1.0) list for full release details

## 1.0.4 Release - May 17, 2010 ##
  * Use CacheManager.getEhcache instead of getCache to support decorated caches
  * Fix Spring API usage so that both Spring 2.5 and 3.0 are supported by a single library.
  * [1.0.4 Fixed Issues](http://code.google.com/p/ehcache-spring-annotations/issues/list?can=1&q=label%3AMilestone-Release1.0.4)

## 1.0.3 Release - Apr 25, 2010 ##
  * Fixes incorrect spring.schema file to point to the correct XSD.
  * Clean up JavaDocs.
  * The List returned by ListCacheKeyGenerator caches the calculated hashCode.
  * [1.0.3 Fixed Issues](http://code.google.com/p/ehcache-spring-annotations/issues/list?can=1&q=label%3AMilestone-Release1.0.3)

## 1.0.2 Release - Apr 16, 2010 ##
Fixes cross-JVM consistency issues when an Enum is a method argument.
[1.0.2 Fixed Issues](http://code.google.com/p/ehcache-spring-annotations/issues/list?can=1&q=label%3AMilestone-Release1.0.2)


## 1.0.1 Release - Apr 6, 2010 ##
Our initial production-ready release is available as a download here and from the central maven repository. This release accomplishes our initial goals of providing an annotations based approach for applying caching to a Spring 3.x project.
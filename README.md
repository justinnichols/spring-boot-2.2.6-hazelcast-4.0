# spring-boot-2.2.6-hazelcast-4.0

The impetus of creating this repository is due to Spring Boot 2.2.6 (possibly 2.2.x) not picking the right Hazelcast 4.0 spring bean to create when attempting to use the embedded Hazelcast IMDG.  The bean it should create is a HazelcastInstance implementation of HazelcastServerConfiguration due to the fact that the Hazelcast configuration XML is <hazelcast> and not <hazelcast-client>.

This repository depicts two projects:
* spring-boot-hazelcast-error
  * This project shows the original method of specifying the `spring.hazelcast.config` to point to a specific hazelcast configuration file.
* spring-boot-hazelcast-working
  * This project shows a workaround for now by simply putting hazelcast.xml in the root of the classpath.

Credits:
Thank you to @mesutcelik for his help on Gitter.

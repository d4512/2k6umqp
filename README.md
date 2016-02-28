# Welcome to [ShibpurHub](https://shibpurhub.com) #
To go to a particular section navigate as follows:

- [Deployment](#deployment)
- [How to add a new module](#new-workflow)

## ShibpurHub-Ultimate App ##
ShibpurHub-Ultimate differs from ShibpurHub-RealTime that the former supports a robust back-end which works asyncronously and can be extensible with different features or modules called workflows.

*`2k6umqp`* is the Phase-I implementation of this application.
### 2k6umqp ###
2k6umqp stands for 2kChakka-Ultimate-Message\_Queueing\_Protocol.
The primary tetents of this application are:

- Central Server
- Replicator
- Engine
- FrontEnd

The roles and responsibilities of each layer are as follows:

- **Central Server** holds the transactional & relational databases and serves the REST api. It also serves traditional website for administration purpose and SPA mobile-App for non-Android users. Phase-I implementation is done with `no-ssl`, `php (5.5)` & `MySQL (5.5)`(MariaDB 10) in shared hosted `Apache(2) Server`. It also facilitates as a replicator(Hourly cornjob) which synchronises transactional & relational databases.
- **Replicator** is a single or group of node(s) which replicates and backsup transactional & relational databases as and when required. In phase-I it is `php` & `shell-script` based. In phase-II it may be extended in `java`-based for platform indepence.  
- **Engine** is the heart of `2k6umqp`. Phase-I implements `ActiveMQ(5.13)` with `STOMP` protocol. To learn about more on implementation click [here](#http://2k6.esy.es/mqp)   
- ** FrontEnd **

### Deployment ###

### New-Workflow ###
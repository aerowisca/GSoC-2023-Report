# GSoC 2023 Report



**Author**: [Mahfooz Alam](https://github.com/aerowisca)

**Organization**: [Keploy](https://www.keploy.io/)

**Project**: [Keploy CLI Refactoring](https://github.com/keploy/gsoc/tree/main/2023#projects-list)

**Mentors**: [Sarthak Shyngle](https://github.com/Sarthak160), [Charan Kamarapu](https://github.com/charankamarapu), [Gaurav Kumar](https://github.com/gouravkrosx), [Neha Gupta](https://github.com/nehagup), [Shubham Jain](https://github.com/slayerjain), [Ritik Jain](https://github.com/re-Tick)

## Project Description

Keploy is a toolkit for generating E2E tests for APIs, along with the mocks for the dependency calls (database, redis, gRPC, etc). However, traditionally, it followed the SDK approach, wherein each developer had to add a hook in their handlers that would let Keploy capture the traffic. This approach, although working, is not feasible for scaling across multiple languages, and different routers for the underlying APIs. It also assumes that the caller has the access to the source code of the application.

To overcome this problem, I worked with Keploy on V2 of this project, which would be language agnostic, as it captures the traffic on the TCP connection level.

## Completed Tasks
###  `MAJOR TASKS` :
- **Docker Network task** : 
     - Add docker internal client to extract network from container name and inject to an existing network. 
     - Related PR : [#688](https://github.com/keploy/keploy/pull/688)
- **Implementing grpcParser** : 
    - Wrote the grpc Parser for the proxy server to record and replay gRPC calls. 
    - Related PR : [#729](https://github.com/keploy/keploy/pull/729)

### `MINOR TASKS` :
- **Added unit test for proxy package** : 
     - Related PR : [#692](https://github.com/keploy/keploy/pull/692)
- **Added global flags to redirect logs to a file** : 
    - Related PR : [#576](https://github.com/keploy/keploy/pull/576)
- **Unit test for handling connections** : 
    - Related PR : [#691](https://github.com/keploy/keploy/pull/691)
- **Refactor file system to decouple it from OS functionalities** : 
     - Related PR : [#575](https://github.com/keploy/keploy/pull/575)
### `BONUS TASKS` :
* **[WIP]Streaming RPCs** : 
    - I added streaming support to the existing unray gRPC parser .As part of the feature it included client side ,server side  and the bi-directional streaming.
    - The feature is ready and tested on small scale. Though ,before releasing it for production use , it requires extensive testing.



## Future Tasks
* **Intergration testing for keploy v2**:
    - Integration testing are always more reliable than the unit testings .So, I plan to work on writing a script based approach for the integration testing of keploy v2 .
    
## Challenges and Takeaways
- I have invested a good amount of time during the project start for developing understanding on the overall architecture and tech stack for the keploy proxy server. Thanks to my mentors, with their mentorship and guidance, I was able to move faster with the deliverables of the project.
- One of the most exciting parts of this project were my learnings on time management. I have to manage my priorities between my college classroom sessions, semester exams, hackathons and projects. My mentors were supportive throughout and helped me to complete all the planned deliverables with quality.
- My code quality and documentation ability has improved drastically, thanks to detailed reviews from mentors over the course of this project.

## Related Blogs:
1. [Capturing gRPC traffic from server](https://contratiempo.netlify.app/gsoc/wireshark/capture_grpc_traffic_from_server/)
2. [Bidirectional pipe for grpc](https://contratiempo.netlify.app/gsoc/wireshark/bidirectional_pipe_for_grpc/)
## Acknowledgements
I'd like to thank all my mentors for helping me throughout this project. A special shoutout to [Sarthak Shyngle](https://github.com/Sarthak160) and [Charan Kamarapu](https://github.com/charankamarapu) for guiding me throughout my entire GSOC period.
Contributing to Keploy has been amazing, and I am looking forward to contributing more in the future! I am glad to have worked with the amazing set of people in Keploy. I am extremely thankful to Google Summer of Code for providing me with this opportunity to enhance my programming skills and learn a lot about open-source development along the way.

## Thank you [Keploy](https://keploy.io/) for an amazing summer of code!

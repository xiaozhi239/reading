# Design patterns for container-based distributed systems

[link to the paper](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45406.pdf)

## single-container management patterns

[<img src="images/single-container.png" alt="Image" width=500 />](https://docs.google.com/drawings/d/1Kw52gkTjsClCCKBvjZyw5Ms6wrin48BZYDhi4WJM6ao/edit)

## single-node, multi-container application patterns

* sidecar: delegate specialized operations
* ambassador: represent the external world to internal usage
* adaptor: represent the internal implementation to the external world
  
<img src="images/sidecar.png" alt="Image" width=500 />

<img src="images/ambassador.png" alt="Image" width=500 />

<img src="images/adaptor.png" alt="Image" width=500 />

## multi-node application patterns

* leader election
* work queue
* scatter / gather

<img src="images/work-queue.png" alt="Image" width=500 />

<img src="images/scatter-gather.png" alt="Image" width=500 />

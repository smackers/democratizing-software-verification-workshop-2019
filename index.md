
In the past decades we have witnessed major advances in the power of automated reasoning engines like Satisfiability Modulo Theories (SMT) and Horn clause solvers. As a consequence, there has been a renaissance of software verification based on this technology. Currently, there are a number of mature verifiers available coming both from academia and industry. However, despite these advances, the bar for newcomer researchers to contribute to this field is still very high. One of the main obstacles is the very large cost of development of a new software verifier from scratch. Hence, several groups have been independently working on implementing open software verification infrastructures, which would allow for easier prototyping of research ideas in this space, e.g., new algorithms for verifying relational or timing properties, thereby democratizing software verification.

This workshop aims to bring together the developers of open software verification infrastructures and their potential clients, meaning researchers and practitioners interested in developing prototypes of software verification algorithms. We will structure the workshop to facilitate the exchange of ideas and discussions between the developers and clients. First, the workshop will start with short tutorials on several open software verification infrastructures, such as [SMACK] and [SeaHorn]. This will be followed by presentations of projects that already leverage these infrastructures, such as a side-channel attacks verifier and a firmware verifier. We also hope to attract potential new clients as well, who would present the requirements of their projects through a series of lightning talks. Through open discussions we will solicit feedback from the community on the requirements and functionality that open research infrastructures should include to make them more widely usable.

As further discussion topics, we will solicit talks and feedback on benchmarking issues, reproducibility, input languages, and potential licence issues, all of which are important to have a viable software verification research ecosystem that can be leveraged by both industry and academia.

## Location

The New School, Room 620

## Program

| Time  | Description |
| ------------- | ------------- |
| 9:00-10:00  | Opening Remarks on SMACK and SeaHorn |
| 10:00-10:30 | Coffee break |
| 10:30-11:10 | Aaron Tomb (Galois): *The Software Analysis Workbench as a Platform for Verification Research* |
| 11:10-11:50 | Stephen F. Siegel (University of Delaware): *A CIVLized Platform for Verification of Scientific Software* |
| 11:50-12:30 | Daniel Schwartz-Narbonne (Amazon): *Memory Safety and Functional Correctness of AWS C Common* |
| 12:30-14:30 | Lunch   |
| 14:30-15:10 | Yakir Vizel (Technion): *Efficient Information-Flow Verification under Speculative Execution using SeaHorn* |
| 15:10-15:50 | Subodh Sharma (IIT Delhi): *Analysing Smart Contracts using SeaHorn* |
| 16:00-16:30 | Coffee break |
| 16:30-17:10 | Kedar Namjoshi (Nokia Bell Labs): *Designing Self-Certifying Compilers* |
| 17:10-17:30 | Lewis Young (Secregen): *Is Software Verification Technology Ready for Industry?* |
| 17:30-18:00 | Discussion and Wrap-up |
| 18:00-20:00 | Workshop Dinner |


## Invited Speakers

### Aaron Tomb (Galois): *The Software Analysis Workbench as a Platform for Verification Research*

**Abstract:** The Software Analysis Workbench (SAW) is a tool intended to be a
flexible platform for software analysis and verification. It was originally
developed internally at Galois and later released as open source. Although its
original design focused on some immediate Galois needs, as it has matured it
has moved toward being a flexible, modular analysis system that we hope can be
a viable platform for future verification research. This talk will cover the
current architecture and capabilities of SAW, the philosophy that has guided
that architecture, and some longer-term ideas about one form a comprehensive
software verification platform might take. Some of these characteristics match
with existing SAW features or immediate plans. Others are more aspirational or
go in entirely different directions, and may be more applicable to other tools.
Hopefully these thoughts may in some small way inspire future work in reusable
verification platforms.

**Short bio:** Aaron Tomb is a Principal Researcher at Galois, focused on
building tools to help programmers build correct software more easily, with a
particular emphasis on the verification of cryptographic software. He received
his B.S., M.S., and Ph.D. in computer science from the University of
California, Santa Cruz. His academic work focused on programming language
theory, and particularly on the use of programming language technology to
improve software reliability, building on type theory, automated reasoning,
program analysis, and a bit of subjective exploration into what makes languages
and tools pleasant to use.

### Stephen F. Siegel (University of Delaware): *A CIVLized Platform for Verification of Scientific Software*

**Abstract:** CIVL is an open source model checking and symbolic execution
framework which targets scientific software. Two predominant characteristics of
such software are (1) widespread use of various parallel programming APIs, such
as MPI for message-passing, OpenMP or Pthreads for shared-memory parallelism,
and CUDA for GPU programming; and (2) an abundance of real arithmetic. The CIVL
approach to the first issue is based on an intermediate language, CIVL-C, which
provides a small set of simple but general concurrency primitives and related
data structures used to represent a wide variety of concurrency mechanisms.
Source programs using the APIs are automatically translated into the
intermediate form. For the second issue, CIVL extends the usual SMT proving
capabilities with a number of computer algebra techniques that allow it to
manipulate and reason about large, complicated real-valued expressions. These
capabilities enable CIVL to verify a number of interesting properties of
programs, such as the (real) functional equivalence of a trusted sequential
algorithm and a more complicated, optimized, parallel implementation.

**Short bio:** Stephen Siegel received the PhD in Mathematics from the
University of Chicago. His mathematical research deals with the representation
theory and cohomology of finite groups, and introduced new symbolic algebra
techniques for Lie algebras. Later, Dr. Siegel worked as a software engineer in
a software engineering research laboratory at the University of Massachusetts,
where he developed finite-state verification tools for concurrent programs. He
joined the faculty at the University of Delaware in 2007, where he is an
Associate Professor in Computer and Information Sciences with joint appointment
in the Department of Mathematical Sciences. His research currently focuses on
model checking, symbolic execution, and deductive approaches for the
verification of scientific software.

### Daniel Schwartz-Narbonne (Amazon): *Memory Safety and Functional Correctness of AWS C Common*

**Abstract:** We proved memory safety properties of key data structures and
their methods in AWS C Common, a key library used by AWS services like the AWS
Encryption SDK for C. In the process, we formulated a set of functional
invariants, and proved that they are preserved by methods in the APIs of these
data structures. The service team accepted these invariants (and improvements
to the code discovered during proof construction) into the code base, and they
are now routinely checked during testing. The proofs themselves are rechecked
against each push and pull request to the repository as a fundamental step in
AWS’s continuous-integration workflow. 

**Short bio:** Daniel is a Senior Applied Scientist in the AWS Automated
Reasoning Group. Prior to joining Amazon, he earned a PhD at Princeton, where
he developed a software framework to debug parallel programs. As a postdoc at
New York University, he designed a tool that automatically isolates and
explains the cause of crashes in C programs. At Amazon, he has been focusing on
integrating formal reasoning into the industrial workflow, enabling the
continuous verification of key AWS software.  When he’s not working, you might
find Daniel in the kitchen making dinner for his family, in a tent camping, or
volunteering as an EMT with a local ambulance squad.
 
### Yakir Vizel (Technion): *Efficient Information-Flow Verification under Speculative Execution using SeaHorn*

**Abstract:** In this talk we will discuss formal verification of
information-flow properties in the presence of speculative execution and
side-channels. In addition, we will discuss how this approach is implemented in
SeaHorn.  Verifying security properties of programs often requires augmentation
of the original program with additional logic. There are two sources of
augmentation that are required in order to verify information-flow properties
in the presence of speculative execution. First, the program being verified is
augmented with the required logic for speculative execution. This logic consist
of (i) a formal model that includes speculative execution semantics and (ii) a
model for information leakage under speculation. Second, implementing an
information-flow verification algorithm requires the augmentation of the
program with information-flow tracking code, e.g. for the purpose of
taint-analysis and self-composition. We will discuss several possibilities to
implement these information-flow verification techniques. Lastly, we will
present experimental data that shows the efficiency of our approach.

**Short bio:** Yakir Vizel is an Assistant Professor in the Computer Science
Department at The Technion. Previously he was a Postdoctoral Research Associate
at Princeton University working under the supervision of Prof. Sharad Malik at
the Electrical Engineering Department. He has received a B.Sc. in Mathematics
and CS from the Technion and a Ph.D. in CS from the Technion - working with
Prof. Orna Grumberg on SAT-based Model Checking. He has worked on developing
Formal Verification algorithms for hardware and software verification at Intel,
Jasper Design Automation, Cadence, and Mellanox.

### Subodh Sharma (IIT Delhi): *Analysing Smart Contracts using SeaHorn*

**Abstract:** Smart contracts are central to blockchain platforms and are a key
enabler in multi-party interactions among mutually distrusting peers.
Interestingly, smart contracts are immutable; thus, they are hard to patch for
bugs once they are committed to a blockchain. The (in)famous DAO bug leading to
losses worth around USD 50 million is a case in point. In this talk, I will
begin by discussing some of the common bug patterns in smart contracts that
open the door to potential exploitation. I will then present our experiences
building a symbolic analysis framework (ZEUS) to discover these bugs, which
uses SeaHorn as a backend decision procedure.

**Short bio:** Subodh Sharma is an Assistant Professor in the Department of
Computer Science at IIT Delhi, India. Before joining IIT Delhi, he was a
postdoctoral fellow at the University of Oxford in the systems verification
group (working in Prof. Daniel Kroening's group). He obtained his Ph.D. from
the University of Utah. His primary research interests lie in the verification
of parallel and distributed systems.

### Kedar Namjoshi (Nokia Bell Labs): *Designing Self-Certifying Compilers*

**Abstract:** Production-quality optimizing compilers such as GCC and LLVM are
enormous programs, with millions of lines of code. How can one have confidence
in the correct working of such a complex artifact? In this talk, I explore an
unusual approach to this challenge, which is to design a compiler in a manner
that makes it more amenable to verification.  The compiler is designed to
produce a mathematical proof object (a "certificate") for the correctness of
each optimization step. The operation of such a "self-certifying" compiler can
then be validated by checking the certificates that are generated during
compilation.  I will sketch our experience building self-certification into the
LLVM compiler framework. Crucially, neither the compiler implementation nor the
certificate generation code have to be formally verified or trusted. This
reduces the size of the trusted code base by at least two orders of magnitude.
I will also touch upon intriguing open questions, such as certification of
security. 

**Short bio:** Kedar Namjoshi is a member of technical staff at Bell Labs in
Murray Hill, NJ. He received his Ph.D. from the University of Texas at Austin
with E. Allen Emerson, and the B.Tech. degree from the Indian Institute of
Technology, Madras, both in the Computing Sciences. His research interests
include program semantics, specification logics, program verification, model
checking, static program analysis, distributed computing, and programming
methodology.

### Lewis Young (Secregen): *Is Software Verification Technology Ready for Industry?*

**Abstract:** Formal verification has been known for its mathematical rigor in
achieving software correctness and proving specific properties. Academia has
been studied challenging issues such as invariance and scalability for decades.
Have academic advances provided a satisfactory solution for industrial demands
of guaranteeing code safety and correctness? Based on using the state-of-art
software verification tool in projects for industrial users, I will analyze the
gaps between the state-of-art and the industrial needs. Then I will discuss
potential research directions that bridge the gaps.

**Short bio:** Lewis Young is the CTO of Secregen Inc., which is a startup that
applies program analysis and formal technology to meet the need for code safety
and security. He held a Ph.D. in Computer Science at the University of Utah. He
had worked as a senior and principal engineer in the application security
field, researching and developing program analysis and verification
technologies that discover vulnerabilities and prove security properties.


## Registration

Please register for the workshop through the CAV registration [page](http://i-cav.org/2019/registration).


## Organization

This workshop will be held on July 14, 2019, and colocated with the [31st International Conference on Computer-Aided Verification (CAV)][CAV]. The workshop is chaired by principle developers of [SMACK] and [SeaHorn]:

* Michael Emmi, SRI International
* Arie Gurfinkel, University of Waterloo
* Jorge Navas, SRI International
* Zvonimir Rakamaric, University of Utah

[SMACK]: http://smackers.github.io
[SeaHorn]: https://seahorn.github.io
[CAV]: http://i-cav.org/2019/


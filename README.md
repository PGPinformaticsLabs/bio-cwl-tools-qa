`bio-cwl-tools` Maintenance and QA
==================================

`bio-cwl-tools` is a collection of essential bioinformatics tools with their
[Common Workflow Language (CWL)][cwl] bindings. The CWL files enable developers
and scientists to implement reliable, accountable, and reproducible workflow
pipelines while encouraging practices based on the [FAIR principles][fair]
(Findable, Accessible, Interoperable, and Reusable).

In practice, the `bio-cwl-tools` implements the FAIR ideas mainly by leveraging
containerized packages (see [BioContainers][bc]). This project aims to
complement this with an open-source, community-driven framework where the
underlying container build instructions (Dockerfiles) can also be integrated
into the curated `bio-cwl-tools` repo. In addition, we will develop workflows
that build and test the underlying packages and verifies their CWL bindings, to
help with `bio-cwl-tools` maintenance and quality-assurance.can be 

Technical requirements (draft)
------------------------------

1. Dockerfiles of underlying package images should be gathered or created, and
   there should be 1-1 correspondance of a tagged image in the BioContainers
   collection and its Dockerfile.
2. The building and testing workflows themselves shall be implemented as CWL
   pipelines.
3. For any package that provides its own self-testing functionality, those
   tests should be exercised. For packages that unfortunately lack testing, we
   should provide them, based on public bioinformatics data if necessary.
4. Build pipelines should be as fully reproducible as possible.


[bct]: https://github.com/common-workflow-library/bio-cwl-tools
[cwl]: https://www.commonwl.org/
[fair]: https://www.go-fair.org/fair-principles/
[bc]: https://biocontainers.pro/

# TRON Improvement Proposal(TIP)

TRON Improvement Proposals (TIPs) describe standards for the TRON platform, including core protocol specifications, client APIs, and contract standards.

The TIPS repository is [https://github.com/tronprotocol/TIPs](https://github.com/tronprotocol/TIPs)

<h2>To Submit a TIP</h2>

1.&nbsp;Fork the repository by clicking "Fork" in the top right.

2.&nbsp;Add your TIP to your fork of the repository. There is a [TIP template](https://github.com/tronprotocol/TIPs/blob/master/template.md) here.

3.&nbsp;Submit a Pull Request to TRON's TIPs repository.

Your first PR should be a first draft of the final TIP. It must meet the formatting criteria enforced by the build (largely, correct metadata in the header). An editor will manually review the first PR for a new TIP and assign it a number before merging it. Make sure you include a discussions-to header with the URL to a discussion forum or open GitHub issue where people can discuss the TIP as a whole.

When you believe your TIP is mature and ready to progress past the draft phase, you should do one of two things:

- For a Standards Track TIP of type Core, ask to have your issue added to the agenda of an upcoming All Core Devs meeting, where it can be discussed for inclusion in a future hard fork. If implementers agree to include it, the TIP editors will update the state of your TIP to 'Accepted'.

- For all other TIPs, open a PR changing the state of your TIP to 'Final'. An editor will review your draft and ask if anyone objects to its being finalised. If the editor decides there is no rough consensus, they may close the PR and request that you fix the issues in the draft before trying again.

<h2>TIP Status</h2>

- **Draft**: A TIP that is undergoing rapid iteration and changes.

- **Last Call**: A TIP that is done with its initial iteration and ready for review by a wide audience.

- **Accepted**: A core TIP that has been in Last Call for at least 2 weeks and any technical changes that were requested have been addressed by the author. The process for Core Devs to decide whether to encode an TIP into their clients as part of a hard fork is not part of the TIP process. If such a decision is made, the TIP will move to final.

- **Final (non-Core)**: A TIP that has been in Last Call for at least 2 weeks and any technical changes that were requested have been addressed by the author.

- **Final (Core)**: A TIP that the Core Devs have decided to implement and release in a future hard fork or has already been released in a hard fork.

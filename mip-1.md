---
mip: 1
title: MIP Purpose and Guidelines
status: Draft
type: Meta
author: Russ (@bitruss)
created: 2022-07-26
---

## What is a MIP?

MIP stands for Meson Improvement Proposal. An MIP is a design document providing information to the Meson community, or describing a new feature for Meson or its processes or environment. The MIP should provide a concise technical specification of the feature and a rationale for the feature. The MIP author is responsible for building consensus within the community and documenting dissenting opinions.

## MIP Rationale

We intend MIPs to be the primary mechanisms for proposing new features, for collecting community technical input on an issue, and for documenting the design decisions that have gone into Meson. Because the MIPs are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.

For Meson implementers, MIPs are a convenient way to track the progress of their implementation. Ideally each implementation maintainer would list the MIPs that they have implemented. This will give end users a convenient way to know the current status of a given implementation or library.

## MIP Types

There are three types of MIP:

- A **Standards Track MIP** describes any change that affects most or all Meson implementations, such as—a change to the network protocol, a change in block or transaction validity rules, proposed application standards/conventions, or any change or addition that affects the interoperability of applications using Meson. Standards Track MIPs consist of three parts—a design document, an implementation, and (if warranted) an update to the formal specification. Furthermore, Standards Track MIPs can be broken down into the following categories:

- A **Meta MIP** describes a process surrounding Meson or proposes a change to (or an event in) a process. Process MIPs are like Standards Track MIPs but apply to areas other than the Meson protocol itself. They may propose an implementation, but not to Meson's codebase; they often require community consensus; unlike Informational MIPs, they are more than recommendations, and users are typically not free to ignore them. Examples include procedures, guidelines, changes to the decision-making process, and changes to the tools or environment used in Meson development. Any meta-MIP is also considered a Process MIP.

- An **Informational MIP** describes an Meson design issue, or provides general guidelines or information to the Meson community, but does not propose a new feature. Informational MIPs do not necessarily represent Meson community consensus or a recommendation, so users and implementers are free to ignore Informational MIPs or follow their advice.

It is highly recommended that a single MIP contain a single key proposal or new idea. The more focused the MIP, the more successful it tends to be. A change to one client doesn't require an MIP; a change that affects multiple clients, or defines a standard for multiple apps to use, does.

An MIP must meet certain minimum criteria. It must be a clear and complete description of the proposed enhancement. The enhancement must represent a net improvement. The proposed implementation, if applicable, must be solid and must not complicate the protocol unduly.

## MIP Work Flow

Parties involved in the process are you, the champion or *MIP author*, the [*MIP editors*](#MIP-editors), and the [*Meson Core Developers*](https://github.com/daqnext/pm).

:warning: Before you begin, vet your idea, this will save you time. Ask the Meson community first if an idea is original to avoid wasting time on something that will be rejected based on prior research (searching the Internet does not always do the trick). It also helps to make sure the idea is applicable to the entire community and not just the author. Just because an idea sounds good to the author does not mean it will work for most people in most areas where Meson is used. Examples of appropriate public forums to gauge interest around your MIP include [the Issues section of this repository](https://github.com/daqnext/MIPs/issues), and [the Meson community chat](https://meson.network/discord). In particular, [the Issues section of this repository](https://github.com/daqnext/MIPs/issues) is an excellent place to discuss your proposal with the community and start creating more formalized language around your MIP.

Your role as the champion is to write the MIP using the style and format described below, shepherd the discussions in the appropriate forums, and build community consensus around the idea. Following is the process that a successful MIP will move along:

```
[ Idea ] -> [ Draft ] -> [ Review ] -> [ Last Call ] -> [ Accepted ] -> [ Final ]
```

Each status change is requested by the MIP author and reviewed by the MIP editors. Use a pull request to update the status. Please include a link to where people should continue discussing your MIP. The MIP editors will process these requests as per the conditions below.

**Idea** - An idea that is pre-draft. This is not tracked within the MIP Repository.

**Draft** - The first formally tracked stage of an MIP in development. An MIP is merged by an MIP Editor into the MIP repository when properly formatted.

**Review** - An MIP Author marks an MIP as ready for and requesting Peer Review.

**Last Call** - This is the final review window for an MIP before moving to `Final`. An MIP editor will assign `Last Call` status and set a review end date (`last-call-deadline`), typically 14 days later.

If this period results in necessary normative changes it will revert the MIP to `Review`.

**Accepted** - proposals which are awaiting implementation or deployment.

**Final** - This MIP represents the final standard. A Final MIP exists in a state of finality and should only be updated to correct errata and add non-normative clarifications.

**Stagnant** - Any MIP in `Draft` or `Review` or `Last Call` if inactive for a period of 6 months or greater is moved to `Stagnant`. An MIP may be resurrected from this state by Authors or MIP Editors through moving it back to `Draft` or it's earlier status. If not resurrected, a proposal may stay forever in this status. 

>*MIP Authors are notified of any algorithmic change to the status of their MIP*

**Withdrawn** - The MIP Author(s) have withdrawn the proposed MIP. This state has finality and can no longer be resurrected using this MIP number. If the idea is pursued at later date it is considered a new proposal.

**Living** - A special status for MIPs that are designed to be continually updated and not reach a state of finality. This includes most notably MIP-1.

## What belongs in a successful MIP?

Each MIP should have the following parts:

- Preamble - RFC 822 style headers containing metadata about the MIP, including the MIP number, a short descriptive title (limited to a maximum of 44 characters), a description (limited to a maximum of 140 characters), and the author details. Irrespective of the category, the title and description should not include MIP number. See [below](./MIP-1.md#MIP-header-preamble) for details.
- Abstract - Abstract is a multi-sentence (short paragraph) technical summary. This should be a very terse and human-readable version of the specification section. Someone should be able to read only the abstract to get the gist of what this specification does.
- Motivation _(optional)_ - A motivation section is critical for MIPs that want to change the Meson protocol. It should clearly explain why the existing protocol specification is inadequate to address the problem that the MIP solves. This section may be omitted if the motivation is evident.
- Specification - The technical specification should describe the syntax and semantics of any new feature or process. Technical specifications should be detailed enough to allow competing, interoperable implementations for any of the current Meson platforms.
- Rationale - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale should discuss important objections or concerns raised during discussion around the MIP.
- Backwards Compatibility _(optional)_ - All MIPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their consequences. The MIP must explain how the author proposes to deal with these incompatibilities. This section may be omitted if the proposal does not introduce any backwards incompatibilities, but this section must be included if backward incompatibilities exist.
- Test Cases - Test cases for an implementation are mandatory for MIPs that are affecting consensus changes. Other MIPs can choose to include links to test cases if applicable.
- Reference Implementation _(optional)_ - An optional section that contains a reference/example implementation that people can use to assist in understanding or implementing this specification. This section may be omitted for all MIPs.
- Security Considerations - All MIPs must contain a section that discusses the security implications/considerations relevant to the proposed change. Include information that might be important for security discussions, surfaces risks and can be used throughout the life-cycle of the proposal. E.g. include security-relevant design decisions, concerns, important discussions, implementation-specific guidance and pitfalls, an outline of threats and risks and how they are being addressed. MIP submissions missing the "Security Considerations" section will be rejected. An MIP cannot proceed to status "Final" without a Security Considerations discussion deemed sufficient by the reviewers.
- Copyright Waiver - All MIPs must be in the public domain. The copyright waiver MUST link to the license file and use the following wording: `Copyright and related rights waived via [CC0](../LICENSE.md).`

## MIP Formats and Templates

MIPs should be written in [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) format. There is a [template](https://github.com/daqnext/MIPs/blob/main/mip-template.md) to follow.

## MIP Header Preamble

Each MIP must begin with an [RFC 822](https://www.ietf.org/rfc/rfc822.txt) style header preamble, preceded and followed by three hyphens (`---`). The headers must appear in the following order. Headers marked with "*" are optional and are described below. All other headers are required.

`MIP`: *MIP number* (this is determined by the MIP editor)

`title`: *The MIP title is a few words, not a complete sentence*

`description`: *Description is one full (short) sentence*

`author`: *The list of the author's or authors' name(s) and/or username(s), or name(s) and email(s). Details are below.*

`discussions-to`: *The url pointing to the official discussion thread*

`status`: *Draft, Review, Last Call, Final, Stagnant, Withdrawn, Living*

`last-call-deadline`: *The date last call period ends on* (Optional field, only needed when status is `Last Call`)

`type`: *One of `Standards Track`, `Meta`, or `Informational`*

`category`: *One of `Core`, `Networking`, `Interface`, or `ERC`* (Optional field, only needed for `Standards Track` MIPs)

`created`: *Date the MIP was created on*

`requires`: *MIP number(s)* (Optional field)

`withdrawal-reason`: *A sentence explaining why the MIP was withdrawn.* (Optional field, only needed when status is `Withdrawn`)

Headers that permit lists must separate elements with commas.

Headers requiring dates will always do so in the format of ISO 8601 (yyyy-mm-dd).

#### `author` header

The `author` header lists the names, email addresses or usernames of the authors/owners of the MIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the `author` header value must be:

> Random J. User &lt;address@dom.ain&gt;

or

> Random J. User (@username)

if the email address or GitHub username is included, and

> Random J. User

if the email address is not given.

It is not possible to use both an email and a GitHub username at the same time. If important to include both, one could include their name twice, once with the GitHub username, and once with the email.

At least one author must use a GitHub username, in order to get notified on change requests and have the capability to approve or reject them.

#### `discussions-to` header

While an MIP is a draft, a `discussions-to` header will indicate the mailing list or URL where the MIP is being discussed. As mentioned above, examples for places to discuss your MIP include the an issue in this repo. 

#### `type` header

The `type` header specifies the type of MIP: Standards Track, Meta, or Informational. If the track is Standards please include the subcategory (core, networking, interface, or ERC).

#### `category` header

The `category` header specifies the MIP's category. This is required for standards-track MIPs only.

#### `created` header

The `created` header records the date that the MIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.

#### `requires` header

MIPs may have a `requires` header, indicating the MIP numbers that this MIP depends on.

## Linking to External Resources

Links to external resources **SHOULD NOT** be included. External resources may disappear, move, or change unexpectedly.

## Linking to other MIPs

References to other MIPs should follow the format `MIP-N` where `N` is the MIP number you are referring to.  Each MIP that is referenced in an MIP **MUST** be accompanied by a relative markdown link the first time it is referenced, and **MAY** be accompanied by a link on subsequent references.  The link **MUST** always be done via relative paths so that the links work in this GitHub repository, forks of this repository, the main MIPs site, mirrors of the main MIP site, etc.  For example, you would link to this MIP with `[MIP-1](./mip-1.md)`.

## Auxiliary Files

Images, diagrams and auxiliary files should be included in a subdirectory of the `img` folder for that MIP as follows: `img/mip-N` (where **N** is to be replaced with the MIP number). When linking to an image in the MIP, use relative links such as `../img/mip-1/image.png`.

## Transferring MIP Ownership

It occasionally becomes necessary to transfer ownership of MIPs to a new champion. In general, we'd like to retain the original author as a co-author of the transferred MIP, but that's really up to the original author. A good reason to transfer ownership is because the original author no longer has the time or interest in updating it or following through with the MIP process, or has fallen off the face of the 'net (i.e. is unreachable or isn't responding to email). A bad reason to transfer ownership is because you don't agree with the direction of the MIP. We try to build consensus around an MIP, but if that's not possible, you can always submit a competing MIP.

If you are interested in assuming ownership of an MIP, send a message asking to take over, addressed to both the original author and the MIP editor. If the original author doesn't respond to the email in a timely manner, the MIP editor will make a unilateral decision (it's not like such decisions can't be reversed :)).

## MIP Editors

The current MIP editors are

- Sndnsos (@sndnsos)
- Russ (@bitruss)

## MIP Editor Responsibilities

For each new MIP that comes in, an editor does the following:

- Read the MIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
- The title should accurately describe the content.
- Check the MIP for language (spelling, grammar, sentence structure, etc.), markup (GitHub flavored Markdown), code style

If the MIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the MIP is ready for the repository, the MIP editor will:

- Assign an MIP number (generally the PR number, but the decision is with the editors)
- Merge the corresponding [pull request](https://github.com/daqnext/MIPs/pulls)
- Send a message back to the MIP author with the next step.

Many MIPs are written and maintained by developers with write access to the Meson codebase. The MIP editors monitor MIP changes, and correct any structure, grammar, spelling, or markup mistakes we see.

The editors don't pass judgment on MIPs. We merely do the administrative & editorial part.

## History

This document was derived heavily from [Ethereum's EIP-1](https://github.com/ethereum/EIPs) written by Martin Becze and Hudson Jameson, which was derived from [Bitcoin's BIP-0001](https://github.com/bitcoin/bips) written by Amir Taaki, which in turn was derived from [Python's PEP-0001](https://www.python.org/dev/peps/). In many places text was simply copied and modified. The authors of the previous texts on which this process is based are not responsible for the Meson Improvement Process and should not be bothered with questions. Please direct all comments to the MIP editors.

### July 26, 2022: MIP-1 created from MIP-1

See [the revision history for further details](https://github.com/daqnext/MIPs/blob/main/mip-1.md), which is also available by clicking on the History button in the top right of the MIP.

## Copyright

Copyright and related rights waived via [CC0](../LICENSE.md).
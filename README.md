# New Work Item Proposal

Define a new DID method, did:tag, derived from IETF tagURIs.

## Include Link to Abstract or Draft

- Current Draft: https://wyman.us/public/unofficial-did-method-tag.html
- GitHub Repository: https://github.com/bobwyman/did_method_tag

## List Owners

Bob Wyman, @bobwyman

## Work Item Questions

> Answer the following questions in order to document how you are meeting the requirements for a new work item at the W3C Credentials Community Group. Please note if this work item supports the Silicon Valley Innovation program or another government or private sector project.

> 1. Explain what you are trying to do using no jargon or acronyms.

I define a did:tag Decentralized Identifier (DID) method that provides a combination of capabilities and qualities not currently provided by any single previously defined DID method. Those capabilities of most interest include: DIDs which are unique over time, a DID resolution method which can be implemented with minimal software or system support, a DID resolution method which supports asynchronous use, and a means to specify an alternative DID resolution service.

> 2. How is it done today, and what are the limits of the current practice?

A great many DID methods have been defined. However, most of have one or more of the following characteristics:

- They are defined to have only a single entity authorized to issue or resolve DIDs.
- They supporting only DIDs which are composed of long strings which are unintelligiable to humans and thus suitable only for machine processing.
- They don't provide mechanisms, other than probability, to ensure that DIDs are not duplicated over time.
- They only provide a synchronous resolution mechanism.
- They only support a single DID resolution mechanism.
- Because of their implementation requirements and dependencies (Blockchain, web servers, DNSnames, etc.) the universe of users and entities capable of or willing to use the methods is dramatically smaller than the full universe of online users.

> 3. What is new in your approach and why do you think it will be successful?

The proposed method is derived from the RFC4151 tagURI specification and thus incorporates a ``date'' component which eases the facility with which DID controllers are able to ensure that DIDs are unique over potentially long periods of time. Additionally, by supporting the minting of DIDs from tagURIs that use an email address as an authorityName, support is provided for asychronous resolution of DIDs. Given that the vast majority of online users have access to an email account, yet only a small subset of them are able or wiling to maintain a website, the support of asynchronous resolution via well established email protocols dramatically increases the universe of those who are able to usefully create and manage DIDs.

The AltResolution service provides a means by which a DID document may specify alternative means by which it might be resolved in the future. This mechanism is particularly useful when supporting asynchronous resolution.

I believe this specification will be successful since it provides a super-set of capabilities provided by the already well-received did:web method, but addresses some important issues not satisfactorily addressed by that method. Of particular interest, when comparing to did:web, is the fact that did:tag allows asynchronous resolution via widely used email protocols and thus overcomes the objection that did:web is too limited in the universe of users who can make use of it.

> 4. How are you involving participants from multiple skill sets and global locations in this work item? (Skill sets: technical, design, product, marketing, anthropological, and UX. Global locations: the Americas, APAC, Europe, Middle East.)

By publishing this proposal to this community group, it is my hope to attract that participation of those who could either provide the diversity of viewpoint described in the question or who could provide suggestions on how to obtain such diverse feedback.

> 5. What actions are you taking to make this work item accessible to a non-technical audience?

If CCG review indicates that doing so will have value, I will do my best to prepare easily understood documentation and explanations for the method as well as develop easy to use reference implementations.


Note: This is my first submission to the CCG. If there are any errors in format, content, or whatever, please do not hesitate to let me know.

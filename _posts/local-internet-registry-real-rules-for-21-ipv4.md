---
layout: post
title: "Local Internet Registry: Real Rules for /21 IPv4"
date: 2026-08-21
canonical_url: https://wirez.top/posts/local-internet-registry-real-rules-for-21-ipv4/
---

A Local Internet Registry operates as the critical distribution layer receiving resources directly from a Regional Internet Registry like the [RIPE NCC](https://www.ripe.net/). This role demands strict adherence to distribution hierarchies where a **minimum allocation size** of **/21** applies to IPv4 requests, while IPv6 allocations require a **/32** prefix and a verified plan for usage within two years. These thresholds prevent fragmentation and ensure that limited number resources are not wasted on inefficient historical practices. The system forces organizations to justify their need before expanding their footprint in the global routing table.

Efficiency relies on the **assignment window**, which dictates the maximum number of addresses an LIR can assign without seeking further approval from the registry. This control structure supports the broader goal of **aggregation** by encouraging the announcement of whole allocations rather than scattered prefixes. Understanding these mechanics is necessary because **IP address space** and **AS Numbers** remain finite resources that demand rigorous conservation strategies to maintain Internet scalability.

## The Strategic Role of Local Internet Registries in Global IP Governance

### LIR Definition: Direct Resource Recipients from RIPE NCC

A **Local Internet Registry** functions as the authorized entity obtaining IP blocks and ASNs straight from a Regional Internet Registry like the **RIPE NCC**. Most LIRs operate as ISPs, standing apart from end-users who must acquire resources through an LIR rather than tapping the global pool directly. Organizations can set up a Local Internet Registry status to manage large-scale network resources independently, effectively bypassing traditional ISP intermediaries. This direct relationship enables precise control over **BGP** multihoming and removes dependency on upstream providers for **CIDR** aggregation strategies.

The **RIPE Database** acts as the public ledger recording these allocations to guarantee global uniqueness and contactability. Every LIR maintains specific database objects, including person, maintainer, and organization records, to validate ownership claims accurately. Some entities choose to work with an LIR sponsor to manage Provider Independent resources, yet direct membership offers superior flexibility for expanding networks. A limitation exists in the administrative burden of complying with strict conservation policies while maintaining accurate registry data continuously.

InterLIR helps network operators navigate this hierarchy by optimizing existing [IPv4](https://en.wikipedia.org/wiki/IPv4) resources without requiring immediate direct RIR membership. This approach allows organizations to scale efficiently while adhering to the rigorous **assignment window** constraints imposed by regional policies.

### Applying Registration, Aggregation, and Conservation Goals

Uniqueness enforcement within the **RIPE Database** ensures every IP block maps to a single organization through verified contact records. This mechanism prevents address conflicts that alter global routing stability. Operators rely on membership guidelines to maintain accurate registry entries rather than guessing ownership details.

**Aggregation** counters routing table expansion by encouraging the announcement of whole allocations instead of fragmented prefixes. The hierarchy flows from [IANA](https://www.iana.org/) holding a /8 down to LIRs receiving a /21 for further distribution. End users typically receive smaller blocks like /23 or /25 segments depending on verified need. Adopting **CIDR** principles allows networks to summarize these paths effectively. Strict aggregation can limit multihoming flexibility for smaller sites requiring specific prefix visibility.

  
| Resource Level | Typical Block Size | Primary Function |
| --- | --- | --- |
| IANA | /8 | Global pool management |
| RIR | /8 | Regional distribution |
| LIR | /21 | Local assignment |
| End User | /23 - /25 | Final deployment |

Conservation efforts address the reality that IPv4 space remains finite despite available [IPv6](https://datatracker.ietf.org/doc/html/rfc8200) capacity; the central registry pool has fallen from 25% available to 16%. InterLIR helps operators optimize existing IPv4 resources to extend their utility within these tight constraints. Non-ISP entities may become LIRs, though most participants still function as traditional service providers. The tension between conserving addresses and enabling growth requires careful planning of assignment windows.

### LIR Membership vs End-User Status: Flexibility and BGP Multihoming

Becoming a **Local Internet Registry** grants operators direct control over **IP address** blocks, whereas end-users remain dependent on upstream providers for resource allocation. This structural difference defines the ability to implement **BGP multihoming** strategies without seeking permission from third-party networks. Standard users must sign specific agreements for independent resources, while **LIR members** manage assignments directly through the **RIPE NCC** hierarchy.

  
| Feature | End-User Status | LIR Membership |
| --- | --- | --- |
| Resource Source | Upstream ISP | Direct from RIR |
| **BGP** Control | Limited by provider | Fully Independent |
| Policy Scope | Provider Rules | **RIPE Policies** |
| Flexibility | Low | High |

Operators choosing LIR status gain the autonomy to optimize **IPv4** utilization based on actual traffic patterns rather than provider constraints. Organizations must account for the costs associated with becoming a member of the **RIPE NCC**, as membership is a prerequisite for this elevated status. Unlike end-users who face rigid assignment windows, LIRs can strategically distribute space to match growth. InterLIR supports this transition by facilitating access to the very **IPv4 resources** needed to maximize new independence. Administrative overhead increases, yet the reward is total routing sovereignty.

## Hierarchical Mechanics of IPv4 IPv6 Allocation and AS Number Distribution

### IPv4 /21 and IPv6 /32 Minimum Allocation Thresholds

  
  Hierarchical Mechanics of IPv4 IPv6 Allocation and AS Number Distribution

Regional Internet Registries enforce strict prefix lengths to keep global routing stable. Only a Local Internet Registry can request these resources directly, drawing a hard line between infrastructure managers and standard users. The rules demand a minimum allocation size of **/21** for IPv4 blocks and **/32** for IPv6 space.

  
| Resource Type | Minimum Allocation | Recipient Status |
| --- | --- | --- |
| IPv4 Address Space | /21 | LIR |
| IPv6 Address Space | /32 | LIR |

Companies unable to join as an LIR often turn to IP address leasing for flexibility. This separation keeps the **routing table** scalable and stops the global pool from fragmenting. Recipients must advertise their allocation as a single prefix to maintain aggregation efficiency. Splitting these announcements breaks the core concept of **CIDR** conservation. InterLIR helps operators navigate these thresholds by optimizing current IPv4 holdings instead of forcing expansion. Efficient redistribution of unused blocks maximizes utility within the **/21** and **/32** frameworks without hurting compliance.

### Executing Multihoming with 16-Bit and 32-Bit AS Numbers

Autonomous System Numbers are necessary for **multihomed** connections or **peering agreements** with upstream providers. The 16-bit pool offered limited space in the past. Today, the 16-bit pool sits at only 28% available according to data from potaroo.net. Scarcity drives the shift to 32-bit AS numbers, which became the default in 2010. Routing hardware must support these extended identifiers before anyone requests resources.

Getting an ASN requires specific steps for network growth:

  Verify the necessity of an independent **routing policy** versus single-homed connectivity.
  Become a member of a Regional Internet Registry to access the hierarchical distribution model.
  Submit the request demonstrating the technical requirement for multiple upstream links.
  Configure border routers to handle the new AS path attributes correctly.

InterLIR Marketplace reduces the administrative load of acquiring resources. The service optimizes existing IPv4 resources while checking AS number requests against technical criteria. Legacy gear often drops packets with 32-bit AS path attributes, causing outages even with correct config. Firmware upgrades are frequently required for modern multihoming.

  
| Feature | 16-Bit ASN | 32-Bit ASN |
| --- | --- | --- |
| **Capacity** | Limited (65,535) | Expanded (4+ Billion) |
| **Availability** | Scarce | Readily Available |
| **Support** | Universal | Requires Modern Hardware |

Planning ahead avoids expensive renumbering projects down the road. Networks grow smoothly when architectural ceilings do not block progress.

### Transition Checklist for 32-Bit AS Number Compatibility

Router support for 32-bit AS numbers needs immediate verification since the industry moved from 16-bit defaults to exclusive 32-bit usage by 2027.

  Audit all border gateways to confirm they handle **extended ASN** fields without truncation errors.
  Contact your hardware vendor to certify firmware compatibility with the full 32-bit address space.
  Update internal documentation to reflect that only 32-bit numbers are assigned for new multihoming requests.

  
| Era | Default Assignment | Request Availability |
| --- | --- | --- |
| 2007-2008 | 16-bit AS | 32-bit on request |
| 2009 | 32-bit AS | 16-bit on request |
| 2010+ | 32-bit AS | 16-bit unavailable |

Legacy equipment risks **routing table** corruption when injecting modern prefixes into outdated systems. The constraint is clear: any device failing to parse the full 32-bit integer drops valid BGP updates, causing immediate connectivity loss. Network availability depends entirely on firmware currency rather than policy preference. Internal teams must prepare for this reality because the window for 16-bit compatibility closed long ago. Neglecting this transition leaves networks unable to interconnect with modern peers enforcing 32-bit.

## Operationalizing Resource Management Through Assignment Windows and Database Objects

### Assignment Window Limits for New LIRs and Existing Allocations

  
  Operationalizing Resource Management Through Assignment Windows and Database Objects

The **Assignment Window** sets the maximum IPv4 volume an LIR assigns to a single end user within **12 months** without external approval. New members begin with an **AW** of zero, a constraint that pauses immediate distribution until operational history forms. Six months after receiving a first allocation, this limit expands to a **/21** prefix size, enabling quicker service deployment for expanding networks. Operators must track cumulative requests per customer carefully because exceeding this threshold triggers a mandatory evaluation by the **RIPE NCC**. The process involves collecting technical justification, choosing specific addresses, and registering the block in the **RIPE DB** to maintain global uniqueness. Standard assignments follow these flexible windows, yet requesting Independent Internet Number Resources requires distinct agreements and sponsoring arrangements outside the standard **AW** progression. Strategic planning around the six-month milestone ensures uninterrupted address distribution.

### Executing LIR Assignment Steps and RIPE Database Object Registration

Operational workflow begins by collecting customer data to evaluate if a request fits within the current **Assignment Window** limits. When a valid need exists, the LIR chooses specific IPv4 blocks and registers them in the **RIPE DB** to ensure global uniqueness. This process requires three mandatory entries: a **person object**, a **maintainer object**, and an **organisation object** to establish clear ownership chains. Syntax precision matters notably here, as comments are denoted by # while continuation lines require starting with whitespace.

  
| Object Type | Purpose | Key Attribute |
| --- | --- | --- |
| Person | Identifies individual contact | nic-hdl |
| Maintainer | Secures update authority | auth |
| Organisation | Links resources to entity | org-name |

Using a **role object** allows a single reference point for technical contacts, simplifying future updates across the entire portfolio. This approach reduces errors when contact information changes, whereas scattered personal references require updating every single IP block individually. For resources requiring portability between providers, LIRs may also manage Independent Internet Number Resources under distinct maintenance agreements. Proper database hygiene ensures that routing policies remain accurate and that abuse contacts are always reachable.

### Role Object Efficiency Versus Repeated Person Handles in inetnum Entries

Managing multiple **inetnum** entries without **Role Objects** forces operators to repeat individual **tech-c** handles like &quot;JS123-RIPE&quot; and &quot;SB456-RIPE&quot; across every single IP block. This approach creates immediate data redundancy when assigning sequential ranges such as 80.35.61.0 or 80.35.62.0 to customers. Operators instead define a single **role** object with a dedicated **nic-hdl**, allowing one reference to serve network segments efficiently.

  
| Feature | Repeated Person Handles | Single Role Object |
| --- | --- | --- |
| **Update Effort** | High (manual updates per block) | Low (centralized definition) |
| **Data Consistency** | Low (prone to fragmentation) | High (centralized definition) |
| **Scalability** | Poor for large portfolios | Excellent for growth |

A phone number change for an administrator would otherwise require updating every individual **inetnum** record manually. Implementing **Role Objects** immediately helps simplify future maintenance tasks. This structural choice prevents data fragmentation and ensures accurate routing information remains available globally.

## Securing Registry Integrity via Maintainer Authentication and Update Protocols

### The mntner Object as the Central Authorization Key

Every database entry demands an explicit link to an authorized maintainer through the mnt-by attribute. The mntner object serves as the secure vault holding cryptographic keys required to authorize updates for network resources. Supported schemes include MD5-PW, PGPKEY, and X509, providing flexibility for differing security postures.

  
  Securing Registry Integrity via Maintainer Authentication and Update Protocols

To configure this protection correctly, follow these implementation steps:

  Create the **mntner object** containing your chosen authentication method.
  Reference the maintainer name in the mnt-by field of your inetnum or aut-num objects.
  Submit updates accompanied by the correct password or digital signature to pass validation.
  Verify that resources managed under your LIR status align with your new authentication policies.

This hierarchy allows an allocation maintained by a higher-level maintainer to delegate control to a lower **LIR-MNT** for specific assignments. Operational rigidity is the price; losing access to mntner credentials halts all modifications until recovery finishes. InterLIR assists network operators in managing these critical **authorization keys** to prevent accidental lockouts while maintaining strict registry integrity.

### Configuring Multi-Layered Authentication with MD5-PW and PGPKEY

Operators configure the **mntner** object with multiple **auth** lines so any single valid credential authorizes an update. This redundancy prevents lockout when a specific key expires or a password is lost during critical maintenance windows. The mechanism functions as a logical OR gate; the database accepts the update if the submitted **MD5-PW** hash or the **PGPKEY** signature matches any configured line. When multiple authentication methods are configured, any one of the configured authentication methods suffices to authorize an update.

  Define the **mntner** object including both auth: MD5-PW and auth: PGPKEY attributes.
  Link your resource objects to this maintainer using the **mnt-by** attribute.
  Submit updates by appending the clear-text password or signing the message with the private key.

Managing multiple secrets increases the operational surface for human error during rotation. Network teams must track which credential corresponds to which administrator to maintain an effective audit trail. Users must contact the RIPE NCC to initiate recovery procedures if a password is forgotten. Relying on a single factor creates a single point of failure that can halt network renumbering projects.

### Troubleshooting Authentication Failures and Forgotten Credentials

Resolve update rejections by verifying the hierarchical chain where parent maintainers protect blocks above your **LIR-MNT**.

  Confirm your **inetnum** object references the correct maintainer in the mnt-by field.
  Check that your submitted password matches the stored **MD5-PW** hash exactly.
  Contact the RIPE NCC immediately if credentials are lost to reset access.
  Ensure your update includes the password: attribute or a valid **PGPKEY** signature.

  
| Issue | Verification Step | Recovery Path |
| --- | --- | --- |
| Wrong Maintainer | Check mnt-by value | Edit object hierarchy |
| Forgotten Password | Test hash match | Contact RIPE NCC |
| Missing Signature | Inspect update header | Add auth credentials |

**Hierarchical authorization** allows a higher maintainer to modify lower objects if the chain breaks, a detail operators often overlook. This dependency means a forgotten password at the top level blocks all downstream assignments. Total lockout occurs until manual support intervenes. InterLIR recommends configuring multiple **auth** methods to prevent this single point of failure.

## About

**Vladislava Shadrina**, Customer Account Manager at **InterLIR**, brings direct operational expertise to the complex subject of Local Internet Registries (LIRs). In her daily role managing client relations within the IP resources domain, she guides organizations through the critical processes of obtaining and registering IP assets, mirroring the core responsibilities of an LIR outlined in the RIPE NCC tutorial. Her work at InterLIR, a specialized marketplace for IPv4 resources, involves ensuring **security** and **compliance** for clients seeking network independence and **BGP** multihoming capabilities. This practical experience allows her to translate high-level registry policies into actionable strategies for businesses facing IPv4 scarcity. By connecting theoretical registry goals with real-world resource acquisition, Shadrina provides valuable context on how **InterLIR** supports the IT sector through transparent, efficient solutions for IP address distribution and management.

## Conclusion

Operational fragility in IP resource management stems from rigid authentication chains where a single lost credential halts all downstream assignments. As the central registry pool shrinks to only 16% available, the cost of manual recovery through registry support becomes an unacceptable delay for network scaling. Operators cannot afford downtime while waiting for external intervention to reset access. We recommend migrating immediately to a multi-factor authentication strategy that combines MD5-PW hashes with PGP signatures before initiating any new block distributions. This approach eliminates the single point of failure inherent in password-only schemes. Start this week by auditing your current **mntner** objects to ensure at least two distinct auth methods are active on every critical maintainer record. InterLIR provides the specialized tooling necessary to automate these complex registry updates and secure your hierarchy against lockout. Our solutions enable network teams to manage **hierarchical authorization** without relying on fragile manual processes or risking total project stoppage. Secure your infrastructure now by implementing redundant authentication protocols that match the critical nature of your IP assets.

  
## Frequently Asked Questions

  
    
      What percentage of the global IPv4 pool remains available today?
    
    
      Current data indicates that only 16% of the central registry pool is still available for distribution. This scarcity forces Local Internet Registries to strictly justify their usage plans to secure necessary address space efficiently.

    
  
  
    
      How much of the 16-bit AS Number pool is currently left?
    
    
      Research shows that just 28% of the 16-bit Autonomous System Number pool remains available globally. Networks must therefore consider 32-bit ASNs or rigorous conservation strategies to ensure long-term routing scalability and stability.

    
  
  
    
      Why was the historical IPv4 availability figure of 25% significant?
    
    
      The pool previously sat at 25% available before dropping to current critical levels like 16%. This rapid depletion highlights why strict conservation policies and accurate registration are now mandatory for all registry members.

    
  
  
    
      Can small entities become an LIR without large upfront capital costs?
    
    
      Becoming a member requires both a one-time sign-up fee and a recurring annual fee, so no single headline figure covers the total cost. Organizations must weigh these expenses against the operational independence gained for BGP multihoming and resource control.

    
  
  
    
      What financial scale does the global IP resource market represent?
    
    
      While some valuations reach significant levels, the primary focus for LIRs remains efficient management of finite resources. Proper aggregation and conservation prevent waste more effectively than chasing speculative market value trends alone.

    
  

## References

[Regional Internet registry - Wikipedia: A local Internet registry](https://en.wikipedia.org/wiki/Regional_Internet_registry)[Number Resource Policy Manual - American Registry for Internet](https://www.arin.net/participate/policy/nrpm)[How to setup a LIR: A Local Internet Registry](https://afrinic.net/support/lir-setup)

        

        
        
        
          Need expert help with IP resources and routing compliance?
          InterLIR provides LIR services, ASN management, and IPv4/IPv6 allocation for network operators across Europe. Sign in to the InterLIR portal to manage your IP resources.

          [Sign in to portal &rsaquo;](https://portal.interlir.com/login)
        
        

        
        
          
        

        
        
        
        
          
## Related Articles

          
            
            
              Local registry fees: what the admin cost really means
              Jul 25, 2026
            
            
            
              Local Internet Registry: Your 2026 Cost Breakdown
              Jul 24, 2026
            
            
            
              Local Internet Registry: Stop Renting, Start Owning Space
              Jul 19, 2026
            
            
            
              Local IPv6 Registry: Skip RIPE NCC Bureaucracy
              Jul 14, 2026
            
            
          
        
        

        
        
          
          
          
            
              [interlir](https://wirez.top/tags/interlir/)
            
              [internet](https://wirez.top/tags/internet/)
            
              [registry](https://wirez.top/tags/registry/)
            
              [resources](https://wirez.top/tags/resources/)
            
              [local](https://wirez.top/tags/local/)
            
              [ripe](https://wirez.top/tags/ripe/)
            
              [global](https://wirez.top/tags/global/)
            
              [direct](https://wirez.top/tags/direct/)
            
          
          
          

  

  

  

  

  

  
    
  

  
  
  
  
    Vladislava Shadrina
    
  

        

      

      
      

        
        
        
        
          Contents
          
            
              
              
              
              [The Strategic Role of Local Internet Registries in Global IP Governance](#the-strategic-role-of-local-internet-registries-in-global-ip-governance)
              
              
              
              [Hierarchical Mechanics of IPv4 IPv6 Allocation and AS Number Distribution](#hierarchical-mechanics-of-ipv4-ipv6-allocation-and-as-number-distribution)
              
              
              
              [Operationalizing Resource Management Through Assignment Windows and Database Objects](#operationalizing-resource-management-through-assignment-windows-and-database-objects)
              
              
              
              [Securing Registry Integrity via Maintainer Authentication and Update Protocols](#securing-registry-integrity-via-maintainer-authentication-and-update-protocols)
              
              
              
              [About](#about)
              
              
              
              [Conclusion](#conclusion)
              
            
          
        
        

        
        
        
          Tags
          
            
              [interlir](https://wirez.top/tags/interlir/)
            
              [internet](https://wirez.top/tags/internet/)
            
              [registry](https://wirez.top/tags/registry/)
            
              [resources](https://wirez.top/tags/resources/)
            
              [local](https://wirez.top/tags/local/)
            
              [ripe](https://wirez.top/tags/ripe/)
            
              [global](https://wirez.top/tags/global/)
            
              [direct](https://wirez.top/tags/direct/)
            
          
        
        

        
        
        
          Author
          
            
            
            
            
            
            
            
            
              Vladislava Shadrina
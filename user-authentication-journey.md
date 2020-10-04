# User Authentication Journey

Coupling security and usability effectively may pose a challenge for enterprises. Companies are constantly trying to apply the most effective methods to protect sensitive data. At the same time, they cannot discourage users from using their systems by enforcing excessive authentication methods as this could simply lead to a business loss.

Let's take a look at basic authentication concepts, challenges the authentication complexity brings to users, and ways of making the whole journey frictionless and yet as safe as possible.

## Authentication vs. authorization

Nowadays, we authenticate on a daily basis. The entry point depends on the system you use and can include logging into the computer at work, accessing websites, or unlocking your phone. In each case, you are required to confirm your identity before you can start using the system or device.

This is when authentication comes along. This concept basically refers to a process of identifying identities that are trying to access a given system and validating if they are who they claim to be.

There are various methods used to authenticate identities. They can be roughly divided into these [three groups](https://www.pearsonitcertification.com/articles/article.aspx?p=1718488):
- Something you know (such as a password)
- Something you have (such as a smart card)
- Something you are (such as a fingerprint)

Depending on the complexity of the authentication process, we can distinguish the following authentication methods:

- **Single-factor authentication** like a username and password. In a passwordless flow, that is gaining in popularity in enterprises, this can be a “magic code” in the form of a one-time token or "magic link" delivered to the registered email or phone number, biometric data like fingerprints, or even [microchips](https://www.dailymail.co.uk/sciencetech/article-6306569/Thousands-Swedes-getting-microchip-IDs-inserted-hands.html) inserted into people's hands to access offices or events.

- **Multi-factor authentication** (MFA) which is basically a combination of two or more of the above method types.

Authentication, however, is no security on its own. It allows a person to prove they are who they say they are, returning details about their identity. At this point, authorization kicks in. It enforces permissions for the authenticated identity, granting or denying access to different kinds of data based on the roles or attributes assigned to one’s identity.

## Policies and events

For security reasons, user accounts and devices must meet a set of criteria before they are connected to a certain service. These criteria are set and governed by authentication policies that act as a sort of link between authentication and authorization. The policies control if a user has required permissions, a device they are using is trusted, the usual login location has not changed. Depending on the number and sort of conditions met, policies either grant or deny access to the service. This way, they aim to only allow for authorized access to minimize system security threats.

Each authentication policy is unique, has a predefined authentication scheme, and defines what is considered a successful or failed login attempt. All such attempts are logged in the form of authentication events. If the user tries to log into the system and meets the required permissions, access is granted and a successful event is logged for this legitimate behavior. If the user fails to meet policy requirements, this attempt is logged as well. The authentication events specify such information as the event type, username, IP address, or a login date and time. Both successful and failed authentication can be used to modify the policy accordingly and decrease or increase the risk level for certain criteria. If an enterprise uses dynamic rather than static authentication policies, or a combination of both, the system monitors typical user activities and adapts to them. If the system detects some unusual behavior, such as different login time, location, or device, policies may enforce additional authentication methods. You may be prompted to enter a code sent via mobile phone, accept the link sent via email, or answer a security question.

## Risk-trust balance

It would seem that the more policies and authentication factors are complex, the better. Although from the security perspective that might be true, that is not necessarily the case for the users. It would be extremely frustrating and daunting for the user to be constantly redirected from a website to an email account or a mobile phone to validate their identity in a multitude of ways just to access a simple, low-risk system. Having customer experience in mind, enterprises are constantly seeking ways to strike a balance between the user trust and the system risk level. The authentication complexity level is determined based on such factors as the sensitivity of customer data, system popularity, or the number of its users. Online banking is probably the most notable example of an application with high security demands that require MFA for certain high-risk activities, such as money transfer. See the diagram that exemplifies this flow:

![MFA](./mfa.svg)

## Continuous risk-based authentication

More and more often, low- and medium-risk enterprises are turning to a more adaptive authentication model called risk-based authentication (RBA). This model is based on the rule that the authentication policy becomes more restrictive as the risk increases. This method is context-aware which means that it depends on the login time and location, the IP address of the device from which you authenticate, and the risk this context implies. The system monitors the user's typical behavior and account history. When it spots something out of the ordinary that might pose a risk, it tightens up the authentication policy. For example, if an employee logs into a portal from the corporate internet, no additional authentication is required, but when they log into the portal from outside the office, they must provide an additional certificate to authenticate. Same with online banking - if you access your bank account from an unfamiliar location, you may be required to answer some additional security questions to access your account.

Given its flexibility, it comes as no surprise that [usability tests](https://riskbasedauthentication.org/) show users prefer RBA over two-factor (2FA) or any other MFA method for low-risk online services, such as social websites. Of course, RBA may also be a bit of a nuisance when many providers that participate in the authentication process use RBA, but that's a topic for a different blog post.

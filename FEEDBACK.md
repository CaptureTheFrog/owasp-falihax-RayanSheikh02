
[comment]: # (Generated from JSON file by generate_feedback_md.py)
[comment]: # (Intended to be read in GitHub's markdown renderer. Apologies if the plaintext formatting is messy.)

# RayanSheikh02's OWASP Falihax Hackathon Feedback
*Marked by [CyberSoc](https://cybersoc.org.uk/?r=falihax-marking-rayansheikh02)*

This is RayanSheikh02's specific feedback. See below for the full vunerability list, including ones you may have missed.

[General hackathon feedback with full vulnerability list and solutions](https://github.com/CyberSoc-Newcastle/owasp-falihax/blob/main/VULNS.md)
## Summary
**Total mark:** 6

A partial understanding of a few vulnerabilities, however with some mistakes in the writeup. Unfortunately, no working fixes were completed so only a limited number of marks could be awarded.

Note: No marks were awarded for the "error on signup page still changes to an authenticated user page" vulnerability in the writeup, as I couldn't replicate this or find any reason this would occur in the code. If screenshot evidence was provided or some attempt to fix it, more marks could have been awarded.

## Marking Scheme Used
We used the following marking scheme to award marks for each vulnerability, where the mark awarded for the vulnerability is the highest row in the following table fulfilled by your solution. A tick means you had to have done this to get the mark, a cross means this mark does not apply if you did this, and a dash means this is ignored for this possible mark. This mark scheme was decided after the entries had been submitted and was not known to entrants during the competition, although hints were provided as to what to include for good marks.

For each vulnerability, this is how many marks we would award:
| State a valid vulnerability | Show where it is in code | Demo it | Describe how it could be mitigated | Attempt a reasonable fix | Fix works | Explain your fix | Marks |
|-----------------------------|--------------------------|---------|------------------------------------|--------------------------|-----------|------------------|-------|
| ✔                           | ❌                        | ❌       | ❌                                  | ❌                        | -         | -                | 1     |
| ✔                           | ✔                        | ❌       | ❌                                  | ❌                        | -         | -                | 2     |
| ✔                           | -                        | ✔       | ❌                                  | ❌                        | -         | -                | 3     |
| ✔                           | -                        | -       | ✔                                  | ❌                        | -         | -                | 4     |
| ✔                           | -                        | -       | -                                  | ✔                        | ❌         | -                | 4     |
| -                           | -                        | ❌       | -                                  | ✔                        | ✔         | ❌                | 5     |
| -                           | -                        | ✔       | -                                  | ✔                        | ✔         | ❌                | 6     |
| -                           | -                        | -       | -                                  | ✔                        | ✔         | ✔                | 7     |

## Vulnerabilites Found
### [A01-03: No access control on the admin page](https://github.com/CyberSoc-Newcastle/owasp-falihax/blob/main/VULNS.md#a01-03-no-access-control-on-the-admin-page)
| State | Show | Demo | Mitigate | Attempt fix | Fix works | Explain fix | Mark |
|-------|------|------|----------|-------------|-----------|-------------|------|
| ✔     | ❌    | ❌    | ❌        | ✔           | ❌         | ❌           | 4    |

Nice work spotting this one! However, a mark was lost as the solution provided doesn't work 100% - since the admin view is returned immediately if the user is admin, the credit score processing code afterwards that is run when a POST request is recieved from the form can no longer run.


### [B02-01: Bad or No Input Validation (General Cases)](https://github.com/CyberSoc-Newcastle/owasp-falihax/blob/main/VULNS.md#b02-01-bad-or-no-input-validation-general-cases)
*Maximum mark of 1 for this category*
| State | Show | Demo | Mitigate | Attempt fix | Fix works | Explain fix | Mark |
|-------|------|------|----------|-------------|-----------|-------------|------|
| ✔     | ❌    | ❌    | ❌        | ❌           | ❌         | ❌           | 1    |

## Bonus marks
Bonus marks were awarded for great non-security critical things that really stood out to us, specific to your project. Each entry below gets you one bonus mark.

### Password field not set to not null
You are correct in that this is a mistake in the web app, however it's not security critical. I'm not sure if I misunderstood your writeup, but "not null" doesn't have anything to do with validating passwords, it simply means if the field is allowed to be empty or not in the database. For a field with some contents, it makes no difference in use in this way.

I couldn't replicate your claim that you can sign in as any user just with a username, nor was any evidence provided so this can only be given one mark as a quality of life fix unfortunately.

*+1 bonus mark awarded.*

## Total mark
4 + 1 + 1 = 6

**Your total mark is 6**
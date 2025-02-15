# Risk Register with OWASP Risk Scoring

Opinions vary on the usage of the OWASP risk scoring, but I noted the inclusion in CISO Assistant (and it seems to have been a requested feature there) so though it might be useful to put an Excel version together.

The great thing about this is that it provides a structured method of scoring, based on a set of 16 criteria and simply applying an average to the scores.

*Note - the final score uses this approach too, not just the likelihood and impact scores; this varies from the typical approach of multipling the likeiihood and impact values to get the risk score.*

It can also be customised.  For example:
* Some people think the **Skill** rating list should be the other way around.  In the attached just change this in the **lkOWASPRA** sheet.
* For **Privacy Violation** scores, maybe your organisation doesn't have millions of customers and wants to set these values more appropriately (**lkOWASPRA** sheet again).
* You could change the formaulae to provide more weighting to certain criteria...
* ... eg. I've changed the formula for business impact so that a financial rating of 9 (bankruptcy) will always take precedence.
* You could exclude certain values, add others, change descriptions to suit your organisation.

An advantage to this approach is that it helps take some of the guesswork and perhaps some bias out of the process.  Results may be more consistent if repeated.

For example, an asset owner might regard impact on their own assets as '9', and perhaps other asset owners disagree (and vice versa).  With the OWASP approach, the business impact and technical impact values are always worked through with respect to the organisation and assets.  This helps remove that bias and helps everyone understand where the assets site.



## Instructions
*See 'Instructions' worksheet in the workbook for up to date information*

* Populate the **Assets** and **Stakeholders** sheets *-these are used for selection in the **Risk** sheet*
* In the **Risk** sheet - Enter your risk id and description, and select the Asset name.  Repeat as needed.
* In the **AssessInherent** sheet - assign values against this risk as needed for the *inherent risk*.
* The totals will update automatically back in the *Risk* sheet.

### When risk treatments have been decided:
* In the **Risk** sheet - Update all the treatment details options and enter any relevant notes.  Repeat as needed.
* In the **AssessResidual** sheet - assign values against each risk as needed now for the *residual risk*.
* The totals will update automatically back in the **Risk** sheet.

### To Customise:
* the lookup tables for the Assesment sheets and criteria are located in the **lkOWASPRA** sheet
* Note that OWASP's formula is simply to average all the scores to form the final score (!)...
* ... the main formulae for this are in columns H, M, S, X in **AssessInherent** and I, N, T, Y in **AssessResidual**
* You could consider weighting certain columns, e.g. I have updated the 'Business Impact Score' to give precedence to high financial impact values
* (and sorry about all the LEFT commands in the formulae :) I wanted something to play nice with the drop down lists)

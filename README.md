### State Diagram


## State - claims report details

States: ["No claim", "Claim initiated", "Claim processing/review", "Approved claim"]

State: 0

Vehicle: {
	Make:"", 
	Model:"",
	Year:"", 
	Registration:"",
	Licence plate number:"",
}

Accident details: {
	Other Driver’s name:"",
	Other Driver’s licence number:""
}

Incident details: {
	Date of incident:"", 
	Time of incident:"",
	Location of accident:"",
	Number of passengers:"",
	Description:"",
}

Claimant insurance company:""
Claimant policy number:""

Other driver's insurance company:""
Other driver's policy number:""

Investigating officer: {
	name:"",
	badge number:""
}

## Transitions

a. fileReport([policy_no,... claims report details])
b. submitClaim(claim_id)
c. approveClaim(claim id, amount)
d. requestReview(claim id)

## Functions & Roles 

fileReport([... claims report details]) - Insured/Claimant
submitClaim(claim_id) - Broker/Agent/Insurance Company

requestPOLForm(claim_id, policy_no) - claims adjuster
determineClaimAmount (claim_id, ...incident details) - Claims Adjuster
approveClaimAmount(claim_id, amount) - claims adjuster
requestReview(claim_id) - Insured/Claimant
checkClaimStatus(claim_id) -- Insured/Claimant/Broker/Agent/Insurance Company

Keys:
a. [Insured/Claimant] is the person filing the claim
b. [Broker/Agent/Insurance Company] broker or agent or insurance company of the claimant


# ChainInsure: A Decentralized Insurance Contract

ChainInsure is a blockchain-based decentralized insurance platform that enables users to create, purchase, and claim insurance policies in a secure and transparent manner. Built on the Clarity language for the Stacks blockchain, this contract allows users to participate in insurance coverage with a focus on trust and automation.

## Key Features

- **Create Insurance Policies**: The contract owner can create insurance policies, defining coverage amounts, premiums, and durations.
- **Purchase Insurance**: Users can purchase insurance policies by transferring the required premium to the contract, ensuring coverage for the specified duration.
- **File Claims**: Users can file claims if they encounter an event that requires compensation, up to the coverage amount defined in their policy.
- **Automated Claims Payout**: Upon approval of the claim, the contract automatically transfers the claimed amount from the contract’s insurance fund to the policyholder.
- **Insurance Fund**: The contract maintains an insurance fund, which is used to payout claims and is replenished when users pay premiums.

## Contract Components

- **Insurance Policies**: A map to store user-specific insurance policies, including coverage amount, premium, and expiration.
- **Claims**: A map to store claims filed by users, with the amount requested and the claim status.
- **Insurance Fund**: A variable that holds the contract's funds, used to pay out claims.

## Functions

### Admin Functions

- **create-policy**: Allows the contract owner to create an insurance policy with a defined coverage amount, premium, and duration.

### User Functions

- **purchase-policy**: Allows a user to purchase an insurance policy by transferring the required premium. The policy becomes active for the specified duration.
- **file-claim**: Allows a user to file a claim if an insurable event occurs. The contract will check if the user’s claim amount is within their policy’s coverage and process the claim.

### Read-Only Functions

- **get-policy-details**: Retrieves details of a user's insurance policy (coverage amount, premium, expiration).
- **get-claim-details**: Retrieves details of a user’s claim (amount requested, claim status).
- **get-fund-balance**: Returns the balance of the insurance fund.

## How to Use

1. **Purchase a Policy**: Users can purchase insurance by calling the `purchase-policy` function and paying the required premium.
2. **File a Claim**: If you experience an event that requires coverage, file a claim by calling the `file-claim` function and providing the amount.
3. **Admin Role**: The contract owner has the ability to create insurance policies for users, setting terms for coverage, premium, and duration.

## Example Use Cases

1. **A user purchases insurance** to protect against potential damages for a defined coverage period. They pay the premium, and the contract ensures they are covered.
2. **A user files a claim** after experiencing an event that requires compensation. If the claim amount is valid, the contract automatically transfers the funds from the insurance pool to the claimant.

## Conclusion

ChainInsure leverages the power of blockchain to decentralize insurance services, providing users with transparency, security, and efficiency in managing their insurance needs. By automating policy management and claims processing, ChainInsure removes intermediaries and provides a seamless experience.
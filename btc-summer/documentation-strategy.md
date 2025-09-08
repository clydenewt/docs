# BTC Summer Documentation Strategy & Planning

## Purpose & Scope

This document outlines the strategic approach for overhauling the BTC Summer campaign documentation, and also as a template for future bespoke documentation created in Neutron.

## Target Audiences

### Primary Audience: Users (General Crypto Participants)

**Background:**
- Coming from various corners of crypto (general DeFi users, yield farmers, Bitcoin maxi's, potential institutional participants)
- Varying levels of technical expertise
- Different comfort levels with cross-chain operations
- May be unfamiliar with Neutron ecosystem

**Key Needs:**
- Clear understanding of participation options
- Simple decision framework for choosing their path
- Step-by-step guidance for their chosen approach
- Understanding of risks, rewards, and time commitments
- Confidence in the technical implementation

### Primary User Personas (Based on Key Decision Factors)

**Key Decision Factors:**
- **Ecosystem Origin**: Coming from EVM (Ethereum) or Neutron/Cosmos?
- **Complexity Level**: Do they want simple exposure or maximum control?
- **DeFi Experience**: Are they new to DeFi or experienced with advanced strategies?
- **Scale Requirements**: Do they need KYC compliance or have institutional needs?

**Practical Personas:**
1. **EVM Bitcoin Holder** — Has BTC/BTC LSTs on Ethereum, wants yield, minimal DeFi experience, comfortable with MetaMask/EVM wallets, prefers simple exposure.
2. **EVM DeFi Experienced** — Familiar with Aave/Compound/Ethereum DeFi, understands leverage looping and basis trading, comfortable with advanced strategies, uses EVM wallets.
3. **Neutron/Cosmos Native** — Already familiar with Neutron ecosystem, uses Keplr/Cosmos wallets, wants maximum control and access to advanced boost mechanisms.
4. **Cross-Chain Experienced** — Comfortable across multiple ecosystems (EVM + Cosmos), may have positions on both networks, understands cross-chain coordination.
5. **Institutional/Whale** — Large capital allocators, may need KYC-compliant options, looking for scalable yield opportunities, could be from either ecosystem.

### Secondary Audience: Integrators (Asset Issuers & Partners)

**Background:**
- BTC LST issuers and technical teams wanting to integrate with points API and reward distribution
- Protocols wanting to understand potential integration or collaboration opportunities with Neutron BTCFi/maxBTC ecosystem

**Key Needs:**
- **Points API specifications** and real-time data access
- **Address linking implementation guide** for cross-chain interfaces
- **UI/UX patterns** for handling boost coordination and conflicts
- **Smart contract integration** requirements and ABIs
- **Error handling specifications** for edge cases
- **Technical support channels** and integration timelines

### Documentation Intent & Goals

1. **Reduce Friction**: Make participation in BTC Summer as simple as possible for all user types
2. **Build Confidence**: Clearly explain security, risks, and technical robustness
3. **Drive Participation**: Guide users to the most appropriate participation path
4. **Enable Self-Service**: Users should be able to participate without support
5. **Enable Integrations**: Support partner and asset issuer onboarding
6. **Showcase Neutron's Capabilities**: Demonstrate Neutron and it's features as a premier BTCFi hub to existing/potential users and partners, cross-link to other relevant Neutron documentation and underlying principles within docs.neutron.org

---

---

## Information Architecture and Page contents

### Documentation Structure Diagram

```
btc-summer/
├── index.mdx                    # Landing Page + maxBTC Overview
├── campaign-details.mdx         # Comprehensive Campaign Mechanics
├── ethereum-path.mdx            # Evergreen evm Participation Guide 
│   ├── epoch-1.mdx              # First epoch of BTC Summer
├── neutron-path.mdx             # Evegreen Neutron Participation Guide
│   ├── epoch-1.mdx              # First epoch of BTC Summer
├── rewards.mdx                  # Reward Strategies (explanation of how the rewards program works clearly enough that users who wish to maximize may do so, but NFA, nor explicitly giving strats for rewards max'ing)
├── overview.mdx                 # The 'Why' of BTC Summer Strategic Context & Value Proposition (Keep Current Content, appended to the end of non-technical documentation)
├── faq.mdx                      # Common Questions & Troubleshooting
├── technical/                   # Technical Documentation Folder
│   ├── overview.mdx             # Technical Architecture Overview
│   ├── integrators.mdx          # Integration Guide (Points API, Asset Issuers, Partners)
│   ├── address-linking.mdx     # Cross-chain Address Coordination System
│   └── reference.mdx           # Complete Technical Reference (includes contracts, tokens, ABIs)
```

1. **Landing Page + Getting Started** (New `index.mdx`)

**Purpose:** First impression and immediate pathway selection with quick links

**Content:**

- Brief campaign introduction and $10M rewards highlight (https://daodao.zone/dao/neutron1suhgf5svhu4usrurvxzlgn54ksxmn8gljarjtxqnapv8kjnp4nrstdxvff/proposals/A80)
- Hook: overview of the problem, and an introduction to 'Why BTC Summer'
- Interactive path selector (Ethereum vs Neutron) with decision criteria
- Quick start buttons for each path
- Wallet compatibility and pre-requisites
- High-level timeline and key dates
- Quick links to detailed overview and user flows

### 2. **Campaign Details** (Refined from `campaign.mdx`)

**Purpose:** Comprehensive campaign mechanics and rules

To include an overall explanation of the rewards, a cross link to rewards.mdx, but the high levle of 

**Content:**

- Epoch structure and timeline
- Points system explanation (simplified, no crawler details)
- Soft-lock incentive model details
- Reward distribution model specifics
- Tiered accounting explanation (to be explained on a pure impact basis. i.e. We are incentivizing *positions, not just vaults, so you can deposit to either and get rewards.)*
- Claiming and vesting options
- Important dates and deadlines
- Terms and conditions

### 3. **Ethereum Path** (Updated `vaults.mdx`)

> 💡 To cover all EVM path vaults listed in [vault listings] and include the relevant vault behavior from **Specific Vault Behavior**

**Purpose:** Complete guide for users depositing via Ethereum vaults

**Content:**

- Step-by-step deposit process
- Available vault options (simplified presentation, focus on outcomes not mechanics)
- Reward expectations and calculations
    - This will also change per epoch so would have factual data (e.g. the actual rewards budget, not the projected apr) in the subpage of the epoch, not the top level.
- Withdrawal process and timing
    - key point being, users understand that the withdrawals are processed on the neutron side (and how they can find their positions (they get Supervault LP tokens + any assets they were lending back to their wallet)
- Address linking guidance for boost coordination
    - Key information here being that if they deposited BTC using vaults / their EVM address, then they need to boost *their evm address*
        - Add a reference to the rewards page here (as opposed to re-explaining everything wrt NTRN locking setup)

### 4. **Neutron Path** (New page)

**Purpose:** Complete guide for direct Neutron participation

**Content:**

- Neutron wallet setup (account creation + onboarding funds)
- Explain very clearly that if you are looking to participate in the campaign directly from Neutron, you should not seek to deposit to vaults, you should deposit directly to DeFi positions
- Relevant protocols (Amber, Mars) +  Supervaults (again another cross link to [supervaults](https://docs.neutron.org/defi/supervaults) docs)
- Direct deposit processes
- Advanced boost opportunities
- Address linking simplified guidance (core concepts only)
    - Most importantly, clarify that if you deposited with your Neutron address, you should boost that Neutron address, not any other address
- Links to Amberfi for leveraged looping and base trading
    - deposit page is: [app.amberfi.io/](http://app.amberfi.io/)
    - Strategies page is: [app.amberfi.io/strategies](http://app.amberfi.io/strategies)
- Links to Supervaults docs for automated market making

### 5. **Rewards** (Refined from AdvancedRewards.txt + Understanding Rewards section of campaignOverview.txt, slimmed down for users)

**Purpose:** Advanced strategies for increasing earnings

**Content:**

- List available reward categories (Asset rewards (maxbtc, lsts, etc), Neutron rewards, DeFi rewards (Supervault trading fees, Amber lending rewards, Mars points), Asset issuer rewards (solv, lombard etc).

- Explain the general reward context: how ntrn rewards are distributed and where to see what positions are eligible to what other rewards 

- Then explain the concept of multipliers / boosters

- Introduce the first mechanism to get the multiplier:

- NTRN locking strategies and calculations
- Explain Boost pointing / address linking (which is required to do properly for the boost to work) and remind the user to properly point it at the address where they have deposited TVL from. Also explain that you can only boost 1 address at a time. Updating the address you're boosting updates all of your previous boosts too.
- Reward calculation examples
- Link to Amber for leverage looping/lending (no strat recommendations, NFA)
- Talk a bit about the tradeoffs / risk of each vault too

e.g., when lending is good / risky and when supervaults is good / risky
    - Get Input form Elijah for more details on this
    
    ### 6. **Strategic Overview** (Keep current `overview.mdx`)
    
    > 💡 Essentially [Why are we doing this campaign?] as-is, with some cross-links
    
    **Purpose:** Comprehensive value proposition and strategic context 
    
    **Content:**
    
    - "The Problem" — Bitcoin yield scarcity, market opportunity, more in depth than the index.mdx
    
    If you have assets on Neutron and want to participate in the campaign, you don't deposit to a vault. You deposit straight to eligible Amber or Supervault positions. 
    
    - Leverage Looping & Basis Trading explanations with market context ($6bn+ markets)
    - Appropriate Initial highlight of [Amber.fi](http://Amber.fi) leveraged looping and basis trading with appropriate links (de-emphasizing mars perps, will follow-up with @Elijah Fox for reveiw on that point)
        - deposit page is: [app.amberfi.io/](http://app.amberfi.io/)
        - Strategies page is: [app.amberfi.io/strategies](http://app.amberfi.io/strategies)
    - maxBTC introduction and what makes Bitcoin DeFi possible
    - Supervaults automated market making (with links to Supervaults docs pages where relevant)
    - Neutron's integrated infrastructure value proposition
    - Campaign goals and technical infrastructure showcase
    
    ### **7. FAQ** (New page)
    
    (referenced from faq.txt)
    
    **Purpose:** Address common questions and edge cases
    
    **Content:**
    
    - General participation questions
    - Technical troubleshooting
    - Cross-chain coordination issues
    - Reward calculation examples
    - Cross-link to our 'Why btc summer' (overview.mdx)
    
    ### 8. **Technical Section** (`technical/` folder)
    
    **Purpose:** Comprehensive technical documentation for developers and integrators
    
    **8a. Technical Overview** (`technical/overview.mdx`)
    
    - High-level architecture
    - System components and interactions
    - Security considerations
    
    **8b. Integrators Guide** (`technical/integrators.mdx`)
    
    - Points API specification for system integration
    - Asset issuer integration guide (BTC LST issuers)
    - Partnership integration opportunities and requirements
    - Technical requirements and timelines
    
    **8c. Address Linking System** (`technical/address-linking.mdx`)
    
    - Cross-chain address coordination system architecture
    - Boost Pointer Contract specifications
    - Address binding mechanics and implementation
    - Scenario handling and conflict resolution logic
    - Integration requirements for supporting cross-chain users
    
    **8d. Technical Reference** (`technical/reference.mdx`)
    
    - Complete technical specifications
    - Smart contract addresses and ABIs
    - Token denominations and standards
    - Network-specific details
    - Advanced implementation details
    - Troubleshooting guides

### Information Assessment: What to Include vs Remove

#### ❌ **REMOVE - Internal/Development Information**
**From Technical.mdx:**
- Crawler implementation details (users don't need to know how data is collected)
- Points contract internals (smart contract architecture details)
- Gas cost calculations for data pulls
- Alternative implementation discussions
- Database schema considerations
- Backend infrastructure details

**From Address-linking.mdx (Moving to Technical/Integrators):**
- Complex scenario matrices → Move to `technical/integrators/address-linking.mdx`
- Detailed conflict resolution logic → Technical documentation for integrators
- Technical implementation of address binding → Integrator reference
- Edge case handling specifics → Technical troubleshooting for partners
- Developer-focused error handling → Integration documentation

**From Current Docs:**
- Internal development considerations
- Detailed vault behavior mechanics (users care about outcomes, not mechanisms)
- Complex forfeiture rules (simplify to "withdraw early, forfeit rewards")

#### ✅ **INCLUDE - User-Actionable Information**
**Essential User Information:**
- Clear participation pathways and decision criteria
- Step-by-step processes for deposits and withdrawals
- Reward calculation examples with real numbers
- Risk explanations and mitigation strategies
- Wallet setup and compatibility requirements

**Cross-Chain Coordination (User-Facing Simplified):**
- Core concept: "NTRN locking requires Neutron wallet, even if you deposit on Ethereum"
- Best practice: "Choose one primary network for simplicity"
- Simple guidance: "If you want boosts, set up the required wallet"

**Address Linking System (Technical - For Integrators):**
- Complete cross-chain coordination system architecture
- Boost Pointer Contract specifications
- Address binding mechanics and implementation
- Scenario handling and conflict resolution logic
- Integration requirements for supporting cross-chain users

**Technical Information (For Integrators):**
- API specifications and endpoints
- Smart contract addresses and ABIs
- Token denominations and standards
- Integration requirements and timelines
- Partnership opportunities with Structured Protocol

#### 🔄 **SIMPLIFY - Complex Concepts Made Accessible**
**Vault Information:**
- Focus on "what you get" rather than "how it works internally"
- Emphasize outcomes: yields, risks, time commitments
- Simple categorization by user intent (simple vs advanced)

**Reward Mechanisms:**
- Basic explanation of points system (no crawler details)
- Clear boost calculation examples
- Practical scenarios for maximizing rewards

**NFT Collection Boosts:**
- Basic explanation only (not primary feature)
- Simple tier structure
- Focus on NTRN locking as main boost mechanism

---

## User Flow Design & Key Journeys

### Primary Decision Points (Users)

1. **Entry Point — "What's your preferred approach?"**
    - **Simple Exposure** → *Ethereum Path* (familiar wallets, automated strategies)
    - **Direct Control** → *Neutron Path* (native access, advanced features)
    - **Learn More** → *Overview* page for context
2. **Path Selection Factors**
    - **Wallet Preference:** MetaMask/EVM vs Keplr/Cosmos
    - **Asset Holdings:** Which BTC derivatives you hold
    - **KYC Tolerance:** Willing to complete KYC for certain vaults?
    - **Complexity Preference:** Automated vs manual strategy management
3. **Ethereum Path Decisions**
    - Asset type → determines eligible vaults
    - KYC willingness → unlocks additional vaults
    - Risk tolerance → guides strategy selection
4. **Neutron Path Decisions**
    - Protocol selection by goal: lending (Amber), LP (Supervaults), trading (Mars)
    - Immediate access to boost mechanisms
    - Direct control over positions and strategies
5. **Optimization (Both Paths)**
    - **NTRN locking** for reward multipliers
    - **Address linking** coordination (primarily for Ethereum users)
    - **Advanced strategies** scale with capital size
    - Cross-chain coordination (advanced users only)


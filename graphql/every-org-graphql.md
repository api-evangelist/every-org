# Every.org GraphQL API

Every.org is a nonprofit giving platform that enables individuals, companies, and developers to discover verified nonprofits, create fundraising campaigns, and process donations. The platform serves donors, nonprofits, and corporate giving programs through a partner API.

## Overview

The Every.org Partner API supports nonprofit search, donor-advised fund (DAF) giving, crypto and stock gifts, matching gifts, campaign management, and donation widgets. The GraphQL schema captures the full domain model for charitable giving, including nonprofit discovery, fund management, disbursements, and compliance data.

## API Access

- Base URL: `https://partners.every.org/v0.2`
- Documentation: https://docs.every.org
- Partner Reference: https://partners.every.org
- GitHub Organization: https://github.com/everydotorg

Authentication uses API keys issued to approved partners. Webhook support is available for real-time donation and disbursement events.

## Schema Source

Schema derived from Every.org public API documentation, partner API reference, and nonprofit data model covering nonprofit discovery (EIN, NTEE codes, SDGs), fund and campaign management, payment processing (card, ACH, DAF, crypto, stock), matching gifts, and disbursements.

## Key Capabilities

- **Nonprofit Discovery**: Search 1.8M+ IRS-verified nonprofits by name, EIN, category, or location
- **Donations**: Process one-time and recurring gifts across multiple payment methods
- **Funds**: Create and manage donor-advised fund accounts and allocations
- **Campaigns**: Fundraising campaigns with goals, events, and widgets
- **Matching Gifts**: Employer matching gift programs and match verification
- **Disbursements**: Track fund distributions to nonprofits with status reporting
- **Crypto & Stock**: Accept cryptocurrency and stock gift donations
- **Webhooks**: Real-time event notifications for donations and disbursements

## Types

The schema defines 58 named types across the following domains:

| Domain | Types |
|--------|-------|
| Nonprofit | Nonprofit, NonprofitDetails, NonprofitSlug, NonprofitName, NonprofitDescription, NonprofitMission, NonprofitWebsite, NonprofitEIN, NonprofitNTEE, NTEE, NonprofitCategory, NonprofitLocation, City, State, Zip, Country, NonprofitSize, RevenueData, NonprofitLogo, NonprofitCover, NonprofitTheme |
| SDG | SDG |
| Fund | Fund, FundDetails, FundSlug, FundBalance, FundAllocation |
| Donation | Donation, DonationDetails, DonationAmount |
| Donor | Donor, DonorProfile, DonorTotal, Anonymous |
| Payment | Payment, PaymentMethod, Card, ACH, DAF, DAFDetails, CryptoGift, CryptoCurrency, StockGift |
| Matching | MatchingGift, MatchingEmployer, MatchingMatch |
| Allocation | Allocation |
| Disbursement | Disbursement, DisbursementDetails, DisbursementStatus |
| Campaign | Campaign, CampaignDetails, CampaignGoal |
| Event | Event, EventDetails, EventCampaign |
| Widget | BtnDonate, DonateWidget |
| Auth | APIKey, Token, Webhook |

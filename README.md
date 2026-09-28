# CRA Blockchain

A zero-cost prototype exploring how blockchain/DLT can support
Credit Rating Agencies (CRAs) in a tokenised corporate bond ecosystem.

## Objective

The project explores how a CRA's rating information can be made
verifiable and tamper-evident using blockchain, while keeping
sensitive company and rating documents off-chain.

## Problem

In a tokenised corporate bond ecosystem, multiple participants need
to trust information such as:

- Corporate bond identity
- Credit rating
- Rating date
- Rating changes / migrations
- Rating reports
- Supporting documents

The objective is to create a verifiable link between the CRA's
published information and a blockchain record.

## Proposed Flow

Company
    ↓
Corporate Bond
    ↓
CRA performs rating
    ↓
CRA publishes rating
    ↓
Generate cryptographic hash
    ↓
Store proof + essential metadata on blockchain
    ↓
Investor / Regulator verifies
    ↓
Original document remains off-chain

## Core Features

### 1. CRA Rating Registry

Allow a CRA user to register:

- Issuer
- Bond
- Credit rating
- Rating date
- Rating outlook
- Report/document hash

### 2. Rating History

Maintain an immutable history of rating changes.

Example:

    ABC Ltd
    AA+ → AA → AA-

Each change creates a new blockchain record.

### 3. Document Verification

A rating report is hashed before being registered.

If the document changes later:

    Original Hash ≠ New Hash

The system can therefore identify that the document is different.

### 4. Public Verification

An investor or regulator can enter a Bond ID and verify:

- Rating
- Rating date
- Blockchain record
- Document hash
- Rating history

## AI Layer — Future

AI will be added after the blockchain MVP works.

Possible capabilities:

- Extract rating information from reports
- Summarise rating rationale
- Identify key risks
- Detect important changes between rating reports
- Assist CRA analysts

AI output will NOT automatically publish a rating.
Human/CRA approval remains required.

## Blockchain Layer

The prototype will initially use a local blockchain and/or
free public testnet.

No real money or real securities will be used.

## Important Design Principle

Sensitive documents and personal/company data should not be stored
directly on-chain.

Blockchain will primarily store:

- Cryptographic hashes
- Identifiers
- Timestamps
- Essential rating metadata
- Verification records

## Project Roadmap

### Phase 1 — Blockchain Foundation
- Solidity smart contract
- Local blockchain
- Rating registry
- Rating history
- Hash verification

### Phase 2 — CRA Web Application
- CRA dashboard
- Rating creation
- Document upload
- Verification page

### Phase 3 — Testnet
- Deploy smart contract
- Connect wallet
- Public blockchain verification

### Phase 4 — AI
- Rating report extraction
- AI summarisation
- Risk analysis
- Human approval workflow

### Phase 5 — Tokenised Bond Ecosystem Research
Explore how the CRA component could interact with a
tokenised corporate bond ecosystem such as the proposed
Demat 2.0 direction.

## Status

🚧 Prototype — Research / Development

## Disclaimer

This is an experimental technology prototype.

It is not connected to real securities, real investors,
real CRA systems, RBI, SEBI, or any production financial infrastructure.

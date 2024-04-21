- [Introduction to Janus: The Embedded DSL for NFT Distribution Plans](#introduction-to-janus-the-embedded-dsl-for-nft-distribution-plans)
  - [What is a DSL?](#what-is-a-dsl)
  - [Introducing Janus Operations](#introducing-janus-operations)
    - [Why Operations?](#why-operations)
    - [Utilizing Janus Operations](#utilizing-janus-operations)
      - [CREATE\_ALLOWLIST Operation](#create_allowlist-operation)
        - [Overview](#overview)
        - [Parameters](#parameters)
      - [GET\_COLLECTION\_TRANSFERS Operation](#get_collection_transfers-operation)
        - [Overview](#overview-1)
        - [Parameters](#parameters-1)
      - [TRANSFER\_POOL\_CONSOLIDATE\_WALLETS Operation](#transfer_pool_consolidate_wallets-operation)
        - [Overview](#overview-2)
        - [Parameters](#parameters-2)
      - [CREATE\_TOKEN\_POOL Operation](#create_token_pool-operation)
        - [Overview](#overview-3)
        - [Parameters](#parameters-3)
      - [TOKEN\_POOL\_CONSOLIDATE\_WALLETS Operation](#token_pool_consolidate_wallets-operation)
        - [Overview](#overview-4)
        - [Parameters](#parameters-4)
      - [CREATE\_CUSTOM\_TOKEN\_POOL Operation](#create_custom_token_pool-operation)
        - [Overview](#overview-5)
        - [Parameters](#parameters-5)
      - [CREATE\_WALLET\_POOL Operation](#create_wallet_pool-operation)
        - [Overview](#overview-6)
        - [Parameters](#parameters-6)
      - [ADD\_PHASE Operation](#add_phase-operation)
        - [Overview](#overview-7)
        - [Parameters](#parameters-7)
      - [ADD\_COMPONENT Operation](#add_component-operation)
        - [Overview](#overview-8)
        - [Parameters](#parameters-8)
      - [ADD\_ITEM Operation](#add_item-operation)
        - [Overview](#overview-9)
        - [Parameters](#parameters-9)
      - [Building Blocks of the Distribution Plan](#building-blocks-of-the-distribution-plan)
        - [Modifying the Distribution Plan State](#modifying-the-distribution-plan-state)
      - [ITEM\_EXCLUDE\_TOKEN\_IDS Operation](#item_exclude_token_ids-operation)
        - [Overview](#overview-10)
        - [Parameters](#parameters-10)
      - [ITEM\_SELECT\_TOKEN\_IDS Operation](#item_select_token_ids-operation)
        - [Overview](#overview-11)
        - [Parameters](#parameters-11)
      - [ITEM\_SORT\_WALLETS\_BY\_TOTAL\_TOKENS\_COUNT Operation](#item_sort_wallets_by_total_tokens_count-operation)
        - [Overview](#overview-12)
        - [Parameters](#parameters-12)
      - [ITEM\_SORT\_WALLETS\_BY\_UNIQUE\_TOKENS\_COUNT Operation](#item_sort_wallets_by_unique_tokens_count-operation)
        - [Overview](#overview-13)
        - [Parameters](#parameters-13)
      - [ITEM\_SORT\_WALLETS\_BY\_MEMES\_TDH Operation](#item_sort_wallets_by_memes_tdh-operation)
        - [Overview](#overview-14)
        - [Parameters](#parameters-14)
      - [ITEM\_REMOVE\_FIRST\_N\_TOKENS Operation](#item_remove_first_n_tokens-operation)
        - [Overview](#overview-15)
        - [Parameters](#parameters-15)
      - [ITEM\_REMOVE\_LAST\_N\_TOKENS Operation](#item_remove_last_n_tokens-operation)
        - [Overview](#overview-16)
        - [Parameters](#parameters-16)
      - [ITEM\_SELECT\_FIRST\_N\_TOKENS Operation](#item_select_first_n_tokens-operation)
        - [Overview](#overview-17)
        - [Parameters](#parameters-17)
      - [ITEM\_SELECT\_LAST\_N\_TOKENS Operation](#item_select_last_n_tokens-operation)
        - [Overview](#overview-18)
        - [Parameters](#parameters-18)
      - [ITEM\_REMOVE\_FIRST\_N\_WALLETS Operation](#item_remove_first_n_wallets-operation)
        - [Overview](#overview-19)
        - [Parameters](#parameters-19)
      - [ITEM\_SELECT\_FIRST\_N\_WALLETS Operation](#item_select_first_n_wallets-operation)
        - [Overview](#overview-20)
        - [Parameters](#parameters-20)
      - [ITEM\_REMOVE\_WALLETS\_FROM\_CERTAIN\_COMPONENTS Operation](#item_remove_wallets_from_certain_components-operation)
        - [Overview](#overview-21)
        - [Parameters](#parameters-21)
      - [ITEM\_REMOVE\_WALLETS\_FROM\_CERTAIN\_TOKEN\_POOLS Operation](#item_remove_wallets_from_certain_token_pools-operation)
        - [Overview](#overview-22)
        - [Parameters](#parameters-22)
      - [COMPONENT\_SELECT\_RANDOM\_WALLETS Operation](#component_select_random_wallets-operation)
        - [Overview](#overview-23)
        - [Parameters](#parameters-23)
      - [COMPONENT\_SELECT\_RANDOM\_PERCENTAGE\_WALLETS Operation](#component_select_random_percentage_wallets-operation)
        - [Overview](#overview-24)
        - [Parameters](#parameters-24)
      - [COMPONENT\_ADD\_SPOTS\_TO\_ALL\_ITEM\_WALLETS Operation](#component_add_spots_to_all_item_wallets-operation)
        - [Overview](#overview-25)
        - [Parameters](#parameters-25)

## Introduction to Janus: The Embedded DSL for NFT Distribution Plans

Welcome to the official documentation for Janus, a Domain Specific Language (DSL) designed exclusively for creating robust and versatile NFT (Non-Fungible Token) distribution plans. Built with JavaScript, Janus provides developers with a straightforward approach to creating deeply customized distribution strategies.

### What is a DSL?

A Domain Specific Language (DSL) is a specialized set of programmatic functions crafted for a specific problem domain. More focused than general-purpose languages, designed to solve a wide range of problems, DSLs are tailored to a particular set of tasks, offering optimized solutions for those specific scenarios. This focused nature of DSLs often results in more concise, readable, and expressive code for the given domain, making them a preferred choice for sectors that require specialized computational tasks.

### Introducing Janus Operations

When building an NFT distribution plan, numerous specific operations come into play. These are the core constructs that enable developers to define, refine, and execute potentially complex distribution plans. 

Operations expressively dictate how actions are carried out, how data flows, and how outcomes are produced. For NFT distribution, this means determining who gets what, when, and under which conditions. Operations help convert plain-language descriptions into running code.

Operations become the building blocks of your distribution plan. By assembling the right combination of desired operations, your code can programmatically handle multiphase allowlists based on a wide number of criteria you select.

#### CREATE_ALLOWLIST Operation

##### Overview

The `CREATE_ALLOWLIST` operation serves as the foundational stone for curating allowlists within the Janus NFT distribution system. Similar to the main function in numerous programming languages, this operation not only kickstarts the allowlist creation but also ensures that a structured, identifiable, and descriptive scaffold is in place for subsequent operations.

##### Parameters

- **id (String)**:
  - **Description**: A unique identifier for the allowlist.
  - **Requirements**:
    - Must be a valid string.
    - Must be unique across the system.
- **name (String)**:

  - **Description**: A user-friendly name for the allowlist to provide an easily recognizable label.
  - **Requirements**:
    - Must be a valid string.

- **description (String)**:
  - **Description**: A detailed description providing context, use-case, or any pertinent information regarding the allowlist.
  - **Requirements**:
    - Must be a valid string.

#### GET_COLLECTION_TRANSFERS Operation

##### Overview

The `GET_COLLECTION_TRANSFERS` operation is fetching a list of NFT transfers (transfer pool) associated with a specified contract. This operation downloads transfers up to a provided block number.

##### Parameters

- **id (String)**:
  - **Description**: A unique identifier for the downloaded transfers.
  - **Requirements**:
    - Must be a valid string.
    - Must be unique across the system.
- **name (String)**:

  - **Description**: A descriptive name for the transfers pool, aiding quick identification.
  - **Requirements**:
    - Must be a valid string.

- **description (String)**:
  - **Description**: A detailed description providing context, use-case, or any pertinent information regarding the transfer pool.
  - **Requirements**:
    - Must be a valid string.
- **contract (String)**:
  - **Description**: The specific contract's address whose NFT transfers you aim to fetch.
  - **Requirements**:
    - Must be a valid ERC721/ERC1155 contract address
- **blockNo (Number)**:
  - **Description**: The block number up to which the NFT transfers should be fetched.
  - **Requirements**:
    - Must be a valid numerical value.
    - Represents the upper limit, ensuring that transfers are only retrieved up to this specific block.

#### TRANSFER_POOL_CONSOLIDATE_WALLETS Operation

##### Overview

The `TRANSFER_POOL_CONSOLIDATE_WALLETS` operation is employed for consolidating wallets by leveraging the delegation tool's consolidations as captured in a specified snapshot block.

##### Parameters

- **transferPoolId (String)**

  - **Description**: The unique identifier of the transfer pool that will undergo wallet consolidation.
  - **Requirements**:
    - Must be a valid string, corresponding to an existing transfer pool in the Janus system.

- **consolidationBlockNumber (Number)**
  - **Description**: The block number that will serve as the snapshot for the consolidation process.
  - **Requirements**:
    - Must be a positive integer.
    - Should reference a valid block number in the blockchain.

#### CREATE_TOKEN_POOL Operation

##### Overview

The `CREATE_TOKEN_POOL` operation offers a structured approach to curate a dedicated pool of NFT tokens. This tool provides the flexibility to consolidate wallet holdings, focus on specific token IDs, and define a specific blockchain depth, encapsulated by the block number.

##### Parameters

- **id (String)**

  - **Description**: A unique identifier for the token pool.
  - **Requirements**:
    - Must be a valid string.
    - Must be unique across the system.

- **name (String)**

  - **Description**: A user-friendly name for the token pool.
  - **Requirements**:
    - Must be a valid string.
    - Offers a brief insight into the token pool's purpose or nature.

- **description (String)**

  - **Description**: Context or supplementary information about the token pool.
  - **Requirements**:
    - Must be a valid string.
    - Encapsulates the essence of the token pool for enhanced clarity.

- **contract (String)**

  - **Description**: The contract address from which the NFT tokens are sourced.
  - **Requirements**:
    - Must be a valid contract address.
    - Pertains to the NFTs in question.

- **blockNo (Number)**

  - **Description**: The block number serving as the upper limit for fetching data.
  - **Requirements**:
    - Must be a valid number.
    - Defines the range of the blockchain data to be considered.

- **consolidateWallets (Boolean)**

  - **Description**: Determines whether to consolidate tokens from different wallets into a unified view.
  - **Requirements**:
    - Must be `true` or `false`.
    - Streamlines the token pool by merging fragmented holdings.

- **tokenIds (String, Optional)**
  - **Description**: Specific token IDs to be considered for the pool.
  - **Requirements**:
    - Comma-separated string of token IDs (example: 1,2,3,4-10,12)
    - If provided, only these specific tokens are curated into the pool.

#### TOKEN_POOL_CONSOLIDATE_WALLETS Operation

##### Overview

The `TOKEN_POOL_CONSOLIDATE_WALLETS` operation streamlines the wallets within a token pool using the advanced mechanisms of the delegation tool's consolidations, anchored at a specified snapshot block.

##### Parameters

- **tokenPoolId (String)**

  - **Description**: The unique identifier for the token pool slated for wallet consolidation.
  - **Requirements**:
    - Must be a valid string, matching an existing token pool within the Janus system.

- **consolidationBlockNumber (Number)**
  - **Description**: The specific block number that will act as the reference snapshot during the consolidation process.
  - **Requirements**:
    - Must be a positive integer.
    - Should correlate to a legitimate block number on the blockchain.

#### CREATE_CUSTOM_TOKEN_POOL Operation

##### Overview

The `CREATE_CUSTOM_TOKEN_POOL` operation empowers users to curate a personalized pool of NFT tokens based on specific input criteria. Unlike the standard token pool, this custom operation allows for a more granular approach, where the emphasis is on explicit token owners and optional token IDs. In the absence of provided IDs, Janus takes the initiative, sequentially assigning IDs in the order of their listing: 1, 2, 3, and so forth.

##### Parameters

- **id (String)**

  - **Description**: A unique identifier for the custom token pool.
  - **Requirements**:
    - Must be a valid string.
    - Must be unique across the system.

- **name (String)**

  - **Description**: A concise name representing the essence of the custom token pool.
  - **Requirements**:
    - Must be a valid string.
    - Captures the purpose or nature of the custom token pool.

- **description (String)**

  - **Description**: Elaborate details or context about the custom token pool.
  - **Requirements**:
    - Must be a valid string.
    - Should encapsulate the nuances of the token pool's creation or intent.

- **tokens (Array of Objects)**
  - **Description**: An array detailing each token's ownership and optional ID.
  - **Object Structure**:
    - **owner (String)**:
      - **Description**: The address representing the owner of a particular token.
      - **Requirements**:
        - Must be a valid wallet address.
    - **id (String, Optional)**:
      - **Description**: A unique identifier for the token.
      - **Requirements**:
        - Must be a valid string if provided.
        - In the absence of an ID, Janus will automatically assign an ID based on the token's order: 1, 2, 3, etc.

#### CREATE_WALLET_POOL Operation

##### Overview

The `CREATE_WALLET_POOL` operation is designed to curate and consolidate a specific set of wallet addresses. By centralizing these addresses into a pool, users can conveniently manage and reference them for subsequent modifications or operations within the Janus ecosystem.

##### Parameters

- **id (String)**

  - **Description**: A unique identifier for the wallet pool.
  - **Requirements**:
    - Must be a valid string.
    - Must be unique across the system to ensure distinct identification of this pool.

- **name (String)**

  - **Description**: A descriptive name for the wallet pool that briefly captures its intent or content.
  - **Requirements**:
    - Must be a valid string.

- **description (String)**

  - **Description**: Detailed context about the purpose, origin, or nuances of the wallet pool.
  - **Requirements**:
    - Must be a valid string.

- **wallets (Array of Strings)**
  - **Description**: A collection of wallet addresses intended for inclusion in the pool.
  - **Requirements**:
    - An array of valid wallet addresses.
    - Each wallet address should be unique within the array.

#### ADD_PHASE Operation

##### Overview

The `ADD_PHASE` operation introduces a structured phase or stage within distribution plan.

##### Parameters

- **id (String)**

  - **Description**: A unique identifier for the phase.
  - **Requirements**:
    - Must be a valid string.
    - Must be unique across the system to ensure distinct identification of this phase.

- **name (String)**

  - **Description**: A concise name representing the essence or primary focus of the phase.
  - **Requirements**:
    - Must be a valid string.

- **description (String)**
  - **Description**: Detailed context providing insights, objectives, or nuances associated with the phase.
  - **Requirements**:
    - Must be a valid string.

#### ADD_COMPONENT Operation

##### Overview

The `ADD_COMPONENT` operation allowing users to create distinct components, or snapshot groups, within a defined phase.

##### Parameters

- **id (String)**

  - **Description**: A unique identifier for the component.
  - **Requirements**:
    - Must be a valid string.
    - Must be unique across the system to ensure distinct identification of this component.

- **name (String)**

  - **Description**: A representative name that conveys the primary purpose or nature of the component.
  - **Requirements**:
    - Must be a valid string.

- **description (String)**

  - **Description**: An elaborate narrative that offers insights into the objectives, nuances, or relevance of the component.
  - **Requirements**:
    - Must be a valid string.

- **phaseId (String)**
  - **Description**: The unique identifier of the phase under which the component is to be nested.
  - **Requirements**:
    - Must be a valid string, corresponding to an existing phase within the system.

#### ADD_ITEM Operation

##### Overview

The `ADD_ITEM` operation allows users to integrate specific snapshot or token pools directly into a designated component.

##### Parameters

- **id (String)**

  - **Description**: A unique identifier for the item.
  - **Requirements**:
    - Must be a valid string.
    - Must be unique across the system to ensure distinct identification of this item.

- **name (String)**

  - **Description**: A title that succinctly captures the essence of the item.
  - **Requirements**:
    - Must be a valid string.

- **description (String)**

  - **Description**: Detailed context shedding light on the importance, role, or specifics of the item.
  - **Requirements**:
    - Must be a valid string.

- **componentId (String)**

  - **Description**: The unique identifier for the component where the item is intended to be nested.
  - **Requirements**:
    - Must be a valid string, corresponding to an existing component within the system.

- **poolType (String)**

  - **Description**: Specifies the type of pool being added, allowing for distinction between standard and custom token pools.
  - **Accepted Values**:
    - 'TOKEN_POOL'
    - 'CUSTOM_TOKEN_POOL'

- **poolId (String)**
  - **Description**: A unique identifier for the specific snapshot or token pool being integrated into the component.
  - **Requirements**:
    - Must be a valid string, representing a pre-existing pool in the system.

---

#### Building Blocks of the Distribution Plan

The aforementioned operations serve as the foundational building blocks for crafting a precise and efficient NFT distribution plan. They allow for the definition and organization of pivotal snapshots and the overarching structure, encapsulated within distinct phases. By utilizing these operations, users can shape the blueprint of their distribution.

---

##### Modifying the Distribution Plan State

While the initial operations provide structure and content, subsequent operations empower users to modify and fine-tune the state of their distribution plan.

---

#### ITEM_EXCLUDE_TOKEN_IDS Operation

##### Overview

The `ITEM_EXCLUDE_TOKEN_IDS` operation introduces a dynamic filtering mechanism within the Janus system. With this operation, users can selectively remove specific tokens from an item based on their token IDs. This becomes especially valuable when certain tokens within an item need to be excluded due to varied reasons, such as changes in strategy, exclusivity criteria, or data refinement.

##### Parameters

- **itemId (String)**

  - **Description**: The unique identifier of the item from which tokens are to be excluded.
  - **Requirements**:
    - Must be a valid string, pointing to an existing item in the system.

- **tokenIds (String)**
  - **Description**: A delimited string indicating which token IDs should be excluded from the item.
  - **Format**: Token IDs are represented as comma-separated values, with the ability to denote ranges using hyphens. E.g., "1,2,3,4-10,12" represents individual tokens with IDs 1, 2, 3, 12 and a range from 4 to 10.
  - **Requirements**:
    - Must adhere to the defined format.

#### ITEM_SELECT_TOKEN_IDS Operation

##### Overview

The `ITEM_SELECT_TOKEN_IDS` operation provides an inverse functionality to its exclusion counterpart. By using this operation, users can explicitly specify which tokens they wish to retain within an item based on their token IDs. This allows for a targeted approach, ensuring that only the most relevant or desired tokens remain a part of the item, thereby streamlining the content to match strategic needs or criteria.

##### Parameters

- **itemId (String)**

  - **Description**: The unique identifier of the item where tokens are to be selectively retained.
  - **Requirements**:
    - Must be a valid string, referencing an existing item in the system.

- **tokenIds (String)**
  - **Description**: A delimited string indicating which token IDs should be kept within the item.
  - **Format**: Token IDs are expressed as comma-separated values, with ranges signified using hyphens. E.g., "1,2,3,4-10,12" denotes individual tokens with IDs 1, 2, 3, 12 and a range from 4 to 10.
  - **Requirements**:
    - Must conform to the prescribed format.

#### ITEM_SORT_WALLETS_BY_TOTAL_TOKENS_COUNT Operation

##### Overview

The `ITEM_SORT_WALLETS_BY_TOTAL_TOKENS_COUNT` operation introduces a mechanism to organize tokens within an item based on the cumulative count of tokens associated with each owner or wallet. By doing so, it facilitates an ordered perspective, making it easier for users to identify and engage with wallets based on their token abundance within a specific item.

##### Parameters

- **itemId (String)**
  - **Description**: The unique identifier of the item whose tokens are to be sorted.
  - **Requirements**:
    - Must be a valid string, referencing an existing item in the Janus system.

#### ITEM_SORT_WALLETS_BY_UNIQUE_TOKENS_COUNT Operation

##### Overview

The `ITEM_SORT_WALLETS_BY_UNIQUE_TOKENS_COUNT` operation is designed to arrange tokens within an item based on the unique count of tokens owned by each wallet. This sorting method emphasizes the diversity of token ownership, allowing users to prioritize and engage with wallets that possess a varied set of unique tokens within the specified item.

##### Parameters

- **itemId (String)**
  - **Description**: The unique identifier of the item to be sorted.
  - **Requirements**:
    - Must be a valid string, referencing an existing item in the Janus system.

#### ITEM_SORT_WALLETS_BY_MEMES_TDH Operation

##### Overview

The `ITEM_SORT_WALLETS_BY_MEMES_TDH` operation streamlines tokens within an item based on the MEMES TDH (Total Days Held)\* score of each wallet. By leveraging the TDH snapshot at a specified block number, this operation allows users to organize and prioritize wallets based on their TDH score within the MEMES ecosystem.

##### Parameters

- **itemId (String)**

  - **Description**: The unique identifier of the item that requires sorting.
  - **Requirements**:
    - Must be a valid string, referencing an existing item in the Janus system.

- **tdhBlockNumber (Number)**
  - **Description**: The specific block number indicating which TDH snapshot to utilize for sorting.
  - **Requirements**:
    - Must be a valid block number.

\* TDH (Total Days Held) is a custom metric used within The Memes project to identify long-term collectors of the Memes. TDH version 1.1 is currently being used by Janus. More info at https://seize.io/community-metrics

#### ITEM_REMOVE_FIRST_N_TOKENS Operation

##### Overview

The `ITEM_REMOVE_FIRST_N_TOKENS` operation provides users with a mechanism to remove a specified number of tokens from the beginning of an item's token list.

##### Parameters

- **itemId (String)**

  - **Description**: The unique identifier of the item from which tokens will be removed.
  - **Requirements**:
    - Must be a valid string, referencing an existing item in the Janus system.

- **count (Number)**
  - **Description**: Specifies the number of tokens to be removed from the beginning of the item.
  - **Requirements**:
    - Must be a positive integer.
    - Should not exceed the total number of tokens in the specified item.

#### ITEM_REMOVE_LAST_N_TOKENS Operation

##### Overview

The `ITEM_REMOVE_LAST_N_TOKENS` operation offers a straightforward method for users to eliminate a defined number of tokens from the end of a specific item's token list.

##### Parameters

- **itemId (String)**

  - **Description**: The unique identifier of the item from which the tokens will be subtracted.
  - **Requirements**:
    - Must be a valid string, referencing an existing item in the Janus system.

- **count (Number)**
  - **Description**: Denotes the number of tokens to be purged from the end of the item.
  - **Requirements**:
    - Must be a positive integer.
    - Should not surpass the total count of tokens present in the denoted item.

#### ITEM_SELECT_FIRST_N_TOKENS Operation

##### Overview

The `ITEM_SELECT_FIRST_N_TOKENS` operation allows users to refine an item's token list by retaining only the first "N" tokens and discarding the rest.

##### Parameters

- **itemId (String)**

  - **Description**: The unique identifier of the item to be refined.
  - **Requirements**:
    - Must be a valid string, referencing an existing item in the Janus system.

- **count (Number)**
  - **Description**: The number of tokens to be retained from the beginning of the item.
  - **Requirements**:
    - Must be a positive integer.
    - Should not exceed the total number of tokens in the specified item.

#### ITEM_SELECT_LAST_N_TOKENS Operation

##### Overview

The `ITEM_SELECT_LAST_N_TOKENS` operation equips users with the ability to retain only the last "N" tokens from an item's list, discarding all preceding tokens.

##### Parameters

- **itemId (String)**

  - **Description**: The unique identifier of the item to be adjusted.
  - **Requirements**:
    - Must be a valid string, referencing an existing item in the Janus system.

- **count (Number)**
  - **Description**: The number of tokens to be retained from the end of the item.
  - **Requirements**:
    - Must be a positive integer.
    - Should not exceed the total number of tokens in the chosen item.

#### ITEM_REMOVE_FIRST_N_WALLETS Operation

##### Overview

The `ITEM_REMOVE_FIRST_N_WALLETS` operation provides a way for users to trim their item's wallet list by removing the first "N" wallets.

##### Parameters

- **itemId (String)**

  - **Description**: The unique identifier of the item whose wallets are to be modified.
  - **Requirements**:
    - Must be a valid string, referencing an existing item in the Janus system.

- **count (Number)**
  - **Description**: The number of wallets to be removed from the beginning of the item.
  - **Requirements**:
    - Must be a positive integer.
    - Should not exceed the total number of wallets in the specified item.

#### ITEM_SELECT_FIRST_N_WALLETS Operation

##### Overview

The `ITEM_SELECT_FIRST_N_WALLETS` operation empowers users to curate an item's wallet list by preserving only the first "N" wallets and discarding all that follow.

##### Parameters

- **itemId (String)**

  - **Description**: The unique identifier of the item to be curated.
  - **Requirements**:
    - Must be a valid string, referencing an existing item in the Janus system.

- **count (Number)**
  - **Description**: The number of wallets to be kept from the start of the item.
  - **Requirements**:
    - Must be a positive integer.
    - Should not exceed the total number of wallets in the designated item.

#### ITEM_REMOVE_WALLETS_FROM_CERTAIN_COMPONENTS Operation

##### Overview

The `ITEM_REMOVE_WALLETS_FROM_CERTAIN_COMPONENTS` operation lets users refine an item's token list by excluding wallets that have already been given spots from specific components.

##### Parameters

- **itemId (String)**

  - **Description**: The unique identifier of the item that needs refinement.
  - **Requirements**:
    - Must be a valid string, referencing an existing item in the Janus system.

- **componentIds (String Array)**
  - **Description**: An array of component IDs which are used to identify wallets that have already been allocated spots.
  - **Requirements**:
    - Each component ID in the array should be a valid string, referencing existing components within Janus.

#### ITEM_REMOVE_WALLETS_FROM_CERTAIN_TOKEN_POOLS Operation

##### Overview

The `ITEM_REMOVE_WALLETS_FROM_CERTAIN_TOKEN_POOLS` operation allows users to refine an item's token list by excluding wallets that are associated with the specified token pools.

##### Parameters

- **itemId (String)**

  - **Description**: The unique identifier of the item that needs refinement.
  - **Requirements**:
    - Must be a valid string, referencing an existing item in the Janus system.

- **pools (Object Array)**

  - **Description**: An array of pools from which wallets will be removed. Each pool object contains:

    - **poolType (String)**

      - **Description**: Specifies the type of the pool.
      - **Valid Values**:
        - `TOKEN_POOL`
        - `CUSTOM_TOKEN_POOL`
        - `WALLET_POOL`

    - **poolId (String)**
      - **Description**: The unique identifier for the token or wallet pool.
      - **Requirements**:
        - Must be a valid string, referencing an existing pool within Janus.

#### COMPONENT_SELECT_RANDOM_WALLETS Operation

##### Overview

The `COMPONENT_SELECT_RANDOM_WALLETS` operation offers a method to diversify and inject an element of randomness into your NFT distribution plans. By targeting a specific component, users can select a random set of wallets from the combined pool of all wallets in the component's items. Only the selected wallets are retained, and all others are excluded, ensuring that a randomized subset of wallets is prioritized for distribution.

##### Parameters

- **componentId (String)**

  - **Description**: The unique identifier of the component that's the subject of random wallet selection.
  - **Requirements**:
    - Must be a valid string, referencing an existing component in the Janus system.

- **count (Number)**

  - **Description**: The number of random wallets to be selected and retained from the component's aggregate wallet list.
  - **Requirements**:
    - Must be a positive integer.
    - Should not exceed the total number of unique wallets across all items in the specified component.

- **seed (String)**
  - **Description**: A seed value to initialize the randomization process, ensuring consistent and replicable results across multiple runs.
  - **Requirements**:
    - Must be a valid string.

#### COMPONENT_SELECT_RANDOM_PERCENTAGE_WALLETS Operation

##### Overview

The `COMPONENT_SELECT_RANDOM_PERCENTAGE_WALLETS` operation provides users with a method to select a random subset of wallets based on a percentage of the total wallets within a given component's items.

##### Parameters

- **componentId (String)**

  - **Description**: The unique identifier of the component undergoing random wallet selection.
  - **Requirements**:
    - Must be a valid string, referencing an existing component in the Janus system.

- **percentage (Number)**

  - **Description**: Specifies the percentage of total wallets that should be randomly selected and retained.
  - **Requirements**:
    - Must be a positive integer or floating-point number between 0 and 100 (inclusive).
    - Represents the desired percentage ratio of the total wallets to be selected.

- **seed (String)**
  - **Description**: A seed value utilized to initiate the randomization mechanism, assuring reproducible and consistent outcomes across multiple executions.
  - **Requirements**:
    - Must be a valid string.

#### COMPONENT_ADD_SPOTS_TO_ALL_ITEM_WALLETS Operation

##### Overview

The `COMPONENT_ADD_SPOTS_TO_ALL_ITEM_WALLETS` operation enhances the adaptability of NFT distribution strategies by allowing users to allocate a specific number of spots to every wallet within a given component's items. This operation simplifies the process of ensuring each wallet receives a predetermined number of spots, thereby maintaining an even distribution mechanism within the component.

##### Parameters

- **componentId (String)**

  - **Description**: The unique identifier of the component where spots will be added to all item wallets.
  - **Requirements**:
    - Must be a valid string, referencing an existing component in the Janus system.

- **spots (Number)**
  - **Description**: The number of spots to be assigned to each wallet across all items within the specified component.
  - **Requirements**:
    - Must be a positive integer.

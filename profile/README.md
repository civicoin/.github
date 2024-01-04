# Civicoin

Modular full-stack solution designed to empower communities and clubs by establishing their own localized digital economy.

Civicoin provides the ability to create your own local financial systems where administrators issue coins and participants exchange. It could be very useful for communities that want to start the local economy, or for closed clubs with paid memberships that can be bought with virtual coins accrued for some activity.

## Architecture and Services

### Interfaces

The primary UI is the **Frontend** with the **BFF** server. Due to API openness, there may be a lot of other interfaces: bots, automated integrations, etc.

### Backend

The main service and entry point — **Gateway**. It is the platform itself. Handles system and user authentication and management; routes requests to appropriate services.

Cores manage coin transactions. Initially there is only one — the centralized **Core**. It processes transactions, holds and statements. In fact, cores are just internal services that are selected for use for each system: centralized, decentralized with blockchain, with external interactions, etc.

For synchronous instant communication between services *REST* is used (for example to check the balance), for asynchronus — *RabbitMQ* (transactions sending)

![image](https://github.com/civicoin/.github/assets/60748898/b3f6f7d7-1779-4a16-8452-20ec6d19b2ac)

---

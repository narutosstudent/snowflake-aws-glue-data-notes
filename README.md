# Data Warehousing

## Facts and Dimensions

A fact table is like a central hub in the database that keeps track of all the important actions and their keys to places containing more information about the specific key.

That place is called a dimension table. A dimension table is a table that contains information about the keys in the fact table.

So a fact table contains both foreign keys and core quantitative data that's commonly desired, also called measures.

## Star Schema

A star schema is a way of organizing the fact and dimension tables in a way that optimizes the data retrieval process. You will have one fact table in the center, and dimension tables surrounding it like a star.

## Snowflake Schema

A snowflake schema is a more complex type of data warehouse schema that is a variation of the star schema. It is called snowflake because its diagram resembles a Snowflake. The fact table is surrounded by dimension tables, which are in turn surrounded by sub-dimension tables.

It is more complex than a star schema and requires more foreign key joins to fetch the data.

# Snowflake

Snowflake is a fully-managed service that provides cloud-based data storage and analytics. It's not just a data warehouse. It's a complete data platform.

## Architecture

Snowflake's architecture is a significant departure from traditional shared-disk or shared-nothing architectures. It's designed as a hybrid of both, optimized for the cloud.

## Three layers

**Database Storage Layer:** This is where all the data is stored. Snowflake manages all aspects of data storage automatically, including organization, file size, structure, compression, and metadata. The storage is highly scalable and can store both structured and semi-structured data.

**Query Processing Layer:** This consists of virtual warehouses (compute clusters) that execute data processing tasks. Each virtual warehouse operates independently, which means that workloads don't compete for compute resources.

**Cloud Services Layer:** This is the brain of the Snowflake environment. It manages tasks like authentication, infrastructure management, metadata management, query compilation and optimization, and access control.

## Virtual warehouses

Think of a virtual warehouse in Snowflake as a powerful computer in the cloud that's dedicated to processing your data. It's not a physical warehouse but a virtual one, where all the heavy lifting of analyzing and querying your data happens.

### Key Concepts

- **Separate From Storage:** In Snowflake, the place where your data is stored (data warehouse) is separate from the place where it's processed (virtual warehouse). This means you can use as much or as little processing power as you need, without affecting your data storage.
- **Scalable:** You can adjust the size of a virtual warehouse to make it more powerful (for faster processing) or less powerful (to save costs) depending on your needs at any given time. It's like having a computer that you can make more powerful or less powerful as needed.
- **Concurrent Usage:** Multiple virtual warehouses can operate at the same time without affecting each other. This is like having several computers, each dedicated to different tasks, so they don't slow each other down.
- **Pay for What You Use:** With virtual warehouses, you only pay for the processing power when you're using it. If the virtual warehouse is turned off, you're not charged for compute resources.
- **Elasticity:** You can turn virtual warehouses on and off as needed. This means you can scale up or down as needed, and you only pay for the processing power when you're using it.

## Data sharing

Snowflake allows for seamless and secure sharing of live data with other Snowflake users. This is done without copying or moving the data, making it a highly efficient process.

## Data cloning and time travel

Snowflake enables creating full copies of databases, schemas, or tables quickly and without additional storage costs. These clones are useful for development, testing, or recovery.

This feature allows users to access historical data (up to 90 days), enabling them to restore data to any point within the specified period or analyze historical data.

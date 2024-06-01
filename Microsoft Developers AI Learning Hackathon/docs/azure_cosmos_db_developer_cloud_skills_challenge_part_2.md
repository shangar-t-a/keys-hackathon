# Azure Cosmos DB Developer Cloud Skills Challenge Part 2

URL: <https://learn.microsoft.com/en-us/collections/zkgzhp65nxoy?WT.mc_id=cloudskillschallenge_60d54986-b94f-45e3-9653-2917c91648e7>

- [Azure Cosmos DB Developer Cloud Skills Challenge Part 2](#azure-cosmos-db-developer-cloud-skills-challenge-part-2)
  - [Implement vCore-based Azure Cosmos DB for MongoDB](#implement-vcore-based-azure-cosmos-db-for-mongodb)
    - [vCore-based Azure Cosmos DB for MongoDB](#vcore-based-azure-cosmos-db-for-mongodb)
    - [Create a vCore-based Azure Cosmos DB for MongoDB cluster](#create-a-vcore-based-azure-cosmos-db-for-mongodb-cluster)
    - [Exercise: Deploy a vCore-based Azure Cosmos DB for MongoDB cluster](#exercise-deploy-a-vcore-based-azure-cosmos-db-for-mongodb-cluster)
      - [Create vCore-based Azure Cosmos DB for MongoDB account](#create-vcore-based-azure-cosmos-db-for-mongodb-account)
      - [Connect to your vCore-based Azure Cosmos DB for MongoDB account using the Azure portal](#connect-to-your-vcore-based-azure-cosmos-db-for-mongodb-account-using-the-azure-portal)
      - [Connect to your vCore-based Azure Cosmos DB for MongoDB account using the Azure portal's Mongo Shell](#connect-to-your-vcore-based-azure-cosmos-db-for-mongodb-account-using-the-azure-portals-mongo-shell)
      - [Clean Up](#clean-up)

## Implement vCore-based Azure Cosmos DB for MongoDB

- Scalability and compatibility for MongoDB applications.

### vCore-based Azure Cosmos DB for MongoDB

- Fully managed, MongoDB-compatible database service.
- Seamless Azure integration.
- Low cost of ownership. Leveraging scalability and flexibility from Azure.

1. AI-driven applications simplified.
   - Vector search feature.
   - Simplifies data indexing and querying.
2. Seamless Azure integration
   - Integration with Azure ecosystem.
3. Cost-effective cluster management
   - Tiered offering. Choose right level of resources for the cluster without over-spending.
4. Flexible and efficient scaling
   - Easy scaling both horizontally and vertically, without downtime.
   - This flexibility ensures effective scaling without immediate need for shard key.

### Create a vCore-based Azure Cosmos DB for MongoDB cluster

- Applications needing high scalability, complex query processing and high availability.
- Ideal for both migration and new applications.
- Key advantages:
  - Migration and new projects.
  - Complex workloads.
  - High availability and scalability.
  - Vector search.
- Mongo DB compatibility.
  - <https://learn.microsoft.com/en-us/azure/cosmos-db/mongodb/vcore/compatibility>
  - Seamless integration.
- Creating a vCore-based Azure Cosmos DB for MongoDB cluster.
  - Can be created using Azure portal and Azure CLI.
  - For CLI, can be created with a bicep, Azure Resource Manager template or Terraform.

### Exercise: Deploy a vCore-based Azure Cosmos DB for MongoDB cluster

#### Create vCore-based Azure Cosmos DB for MongoDB account

1. Sign in to Azure portal.
2. Create a new resource.
3. Search for Azure Cosmos DB.
4. Click on Create.
5. In `Create Azure Cosmos DB Account`, select `Azure Cosmos DB for MongoDB` and click on `Create`.
6. In `Create Azure Cosmos DB Account - Choose Architecture`, select `vCore cluster (Recommended)` and click create.
7. In `Create Azure Cosmos DB for MongoDB cluster` window, fill in details.
   1. Basics tab
      - Subscription: Choose subscription.
      - Resource Group: Choose resource group.
      - Cluster Name: Enter a unique name.
      - Location: Choose location.
      - Cluster Tier: Choose tier. Select `Configure` and familiarize with the options in `Scale` window. Select
        `Free Tier` and `Save`.
      - MongoDB Version: 6.0
      - Admin Username: Enter username.
      - Password: Enter password.
      - Note: Only 1 free tier cluster per Azure account. `High Availability` on `Cluster Tier`, strongly consider
        to prevent downtime but incurs additional cost.
   2. Networking tab
      - Connectivity method: Public access (allowed IP addresses).
      - Firewall rules: `Allow public access from Azure services and resources within Azure to this cluster`. Allow
        to use Azure portal Mongo shell.
      - Firewall rules: Manually add IP ranges.
      - On Production:
        - Private Access and use virtual network and subnet.
        - Private endpoints.
        - Firewall rules:
          - `Add current IP address (your current public IP address)` and `Add 0.0.0.0 - 255.255.255.255`.
          - First option benign if client public IP never changes.
          - Second option allows access to add range of `ALL` IP addresses. Use with caution.
8. Click on `Review + Create` and `Create`.

#### Connect to your vCore-based Azure Cosmos DB for MongoDB account using the Azure portal

1. Sign in to Azure portal.
2. In search bar, type `Azure Cosmos DB`.
3. Select the Azure Cosmos DB account.
4. Options including: `Overview`, `Quit start`, `Networking` and `Connection String`.
5. Overview:
   - Provides details on the account.
   - Reset password.
6. Quick start
7. Networking
   - Add IP addresses to firewall rules.
   - Private endpoint connections.
   - Allow public access from Azure services and resources within Azure to this cluster.
8. Connection String
   - Connection string for applications.
   - Copy only to secure locations.

#### Connect to your vCore-based Azure Cosmos DB for MongoDB account using the Azure portal's Mongo Shell

1. In `Azure Cosmos DB for MongoDB (vCore)`, select `Quick start`. Note: Need public access from Azure services and
   resources within Azure to this cluster.
2. In `Quick start`, select `Launch quick start`. Creates sample database to test on.
   - Enter password for admin created when vCore based Azure Cosmos DB for MongoDB account was created. Select
     `Next`.
   - `Create mew database and collection` and `Next`. MongoDB commands will be executed in the shell.
   - `Load data` and `Next`. Data will be loaded into the collection. `insertMany` command will be executed in the
     shell.
   - Three queries can be ran to test the data. Select `Try query` for each query.
   - `Done` to exit the quick start.
3. In `Quick start`, select `Mongo Shell`.
   - Enter password for admin created when vCore based Azure Cosmos DB for MongoDB account was created.
   - Test connection:
     - Show databases.

     ```bash
     show dbs
     ```

     - switch to `quickstartDB` database.

     ```bash
     use quickstartDB
     ```

     - Show collections.

     ```bash
     show collections
     ```

     - Find all documents in `sampleCollection` collection.

     ```bash
     sampleCollection.find()
     ```

   - Exit Mongo Shell.

     ```bash
     bash exit
     ```

#### Clean Up

1. Delete resource group.
2. Manually delete individual resources.
3. Verify deletion.
4. Review billing.

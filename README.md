
# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

# How to run this project

## Prerequisites

To complete this quickstart: 

* Install [Ruby](https://www.ruby-lang.org/en/downloads/)
* Install the [Azure Storage library for Ruby](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-ruby-how-to-use-blob-storage#configure-your-application-to-access-storage) using the rubygem package. 

If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.

## Create a storage account using the Azure portal

First, create a new general-purpose storage account to use for this quickstart. 

1. Go to the [Azure portal](https://portal.azure.com) and log in using your Azure account. 
2. On the Hub menu, select **New** > **Storage** > **Storage account - blob, file, table, queue**. 
3. Enter a name for your storage account. The name must be between 3 and 24 characters in length and may contain numbers and lowercase letters only. It must also be unique.
4. Set `Deployment model` to **Resource manager**.
5. Set `Account kind` to **General purpose**.
6. Set `Performance` to **Standard**. 
7. Set `Replication` to **Locally Redundant storage (LRS)**.
8. Set `Storage service encryption` to **Disabled**.
9. Set `Secure transfer required` to **Disabled**.
10. Select your subscription. 
11. For `resource group`, create a new one and give it a unique name. 
12. Select the `Location` to use for your storage account.
13. Check **Pin to dashboard** and click **Create** to create your storage account. 

After your storage account is created, it is pinned to the dashboard. Click on it to open it. Under SETTINGS, click **Access keys**. Select a key and copy the CONNECTION STRING to the clipboard, then paste it into Notepad for later use.

## Configure your storage connection string
In the application, you must provide your storage account name and account key to create the `Client` instance for your application. Open the `example.rb` file from the Solution Explorer in your IDE. Replace the **accountname** and **accountkey** values with your account name and key. 

```ruby
client = Azure::Storage.client(storage_account_name: account_name, storage_access_key: account_key)
```

To run the application on a terminal or command prompt, Go to the `example.rb` file directory and run the following command: 

```
ruby example.rb
```

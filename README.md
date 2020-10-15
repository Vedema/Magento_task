# Magento_task
Technical Test with Magento 2.4

# Step 1
Step 1

1.	On XAMMP, Start Apache and MySQL then create a blank database
2.	[Downloaded magento 2.4 and sample data with composer (open source version) from the] (https://magento.com/tech-resources/download).
3.	Magento download was saved under the magento2 root directory on the htdocs of the xampp folder.
4.	[Download and install Elastic Search from] (https://www.elastic.co/downloads/elasticsearch).
5.	Run/start elastic search to check that elastic search is installed and green using some commands (e.g . `curl -X GET "localhost:9200/_cluster/health?pretty"`) on the magento2 project folder.
6.	Elastic search remained open until magento2 installation was completed.
7.	Placed the Elastic Search folder on the same directory as magento 2
8.	Changed a few files on the new magento folder to clear the elastic search no alive node error.
9.	Installed magento 2.4 with database credentials
10.	Run the following commands
 - Index files: `php bin/magento indexer:reindex`.
 - Upgrade files: `php bin/magento setup:upgrade`.
 - Deploy files: `php bin/magento setup:static-content:deploy -f`.
 - Disable Two Factor Auth: `php bin/magento module:disable Magento_TwoFactorAuth`. 
 - Clear cache: `php bin/magento cache:flush`.

# STEP 2
1.	Open the magento2 folder on Visual Studio Code.
2.	Created a new module on magento2/app/code folder with vendor name as product.
3.	Created a module named banner under the magento2/app/code/product directory.
4.	Created an etc folder, which contains the module.xml file under the magento2/app/code/product/banner directory.
5.	Module name was specified as name="Product_Banner"  and setup_version="1.0.0" on the module.xml file.
6.	Created the registration.php file to register the new module under the magento2/app/code/product/banner directory.
7.	Run php bin/magento setup:upgrade to make the new module is active. Then looked out for the Product_Banner module name.
8.	Created a view/frontend under the magento2/app/code/product/banner directory. Then created layout directory under frontend. This directory contains the catalog_product_view.xml file, 
9.	Created the templates folder under the frontend directory, which then contains the banner_popup.phtml file. This file contains the main frontend codes, which includes both the styling and JavaScript codes applied to the page.
10.	Cache was cleared by running the command `php bin/magento cache/clean` on the root directory magento2.
11.	 [The view url is] (http://localhost/magento2/index.php/hera-pullover-hoodie.html).


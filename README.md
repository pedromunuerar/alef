## Trying to migrate products from Prestashop 1.6 to Woocommerce ##
Use at your own risk, this code is shared only for educational purpose. **Don't use it.** It can produce severe damage in your wordpress site. **NEVER use it on your site.**
This is not a plugin, It's a place where I store my code. Many of this snippets may content errors and can be dangerous. This code is under development.

A very nice plugin has been developed to get this job done https://es.wordpress.org/plugins/fg-prestashop-to-woocommerce/ obviusly this is the best cost/benefit solution. But we want learn how to do it by our own hands.

#### The plan ####
1. Get the prestashop database
2. Install at local mysql
3. Figure out where is the data we need
4. Generate PHP code witch create categories, media and products
5. Run it over destination wordpress site
6. Enjoy the results and drink a beer (most important step)

Points 1 and 2 are so trivial... let's start document 3rd point

### 3. Figure out where is the data we need ###
-Categories
    wp_insert_term( 'My New Category', 'product_cat', array(
    'description' => 'Description for category', // optional  
    'parent' => 0, // optional
    'slug' => 'my-new-category' // optional
    ) );
 
https://www.businessbloomer.com/woocommerce-programmatically-create-product/
https://wordpress.stackexchange.com/questions/256830/programmatically-adding-images-to-media-library



# -preselect-chosen-shipping-method

$table_name = $wpdb->prefix . "woocommerce_order_items";
$sql = "SELECT order_item_name FROM  $table_name WHERE order_id = $order_id AND order_item_type = 'shipping'";
$shippingpaid = $wpdb->get_results ( $sql );
$method = $shippingpaid[0]->order_item_name;
					
if($method == 'FedEX 2 Day'){ 
$methodtouse = 'FEDEX_2_DAY';
}

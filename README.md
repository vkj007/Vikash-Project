# Vikash-Project
/*
Plugin Name:MSP Vikash
Description: Create Hello India message
Version: 1.0
Author: Vikash
*/
define('MSP_HELLOINDIA_DIR', plugin_dir_path(__FILE__));
define('MSP_HELLOINDIA_URL', plugin_dir_url(__FILE__));
function msp_helloindia_load(){
		
    if(is_admin())
        require_once(MSP_HELLOINDIA_DIR.'includes/admin.php');
        
    require_once(MSP_HELLOINDIA_DIR.'includes/core.php');
}
msp_helloindia_load();
register_activation_hook(__FILE__, 'msp_helloindia_activation');

function msp_helloindia_activation()

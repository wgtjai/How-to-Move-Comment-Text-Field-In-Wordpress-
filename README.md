# How-to-Move-Comment-Text-Field-In-Wordpress


You can simply add this code snippet in your theme’s functions.php file or in a wordpress site-specific plugin. 


function wgtjai_move_comment_field_to_bottom( $fields ) {
$comment_field = $fields['comment'];
unset( $fields['comment'] );
$fields['comment'] = $comment_field;
return $fields;
}
 
add_filter( 'comment_form_fields', 'wgtjai_move_comment_field_to_bottom' );

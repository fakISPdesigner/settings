# Settings function mytheme_recommended_widgets($widgets){
    if( empty($widgets['My_Custom_Widget']) ){
        $widgets['My_Custom_Widget'] = array(
            'class' => 'My_Custom_Widget',
            'title' => __('Custom Widget', 'siteorigin-panels'),
            'description' => __('My custom widget description', 'mytheme'),
            'installed' => false,
            'plugin' => array(
                'name' => __('Custom Widget Plugin', 'siteorigin-panels'),
                'slug' => 'plugin-slug'
            ),
            'groups' => array('recommended'),
            'icon' => 'dashicons dashicons-edit',
        );
    }

    return $widgets;
}
add_filter('siteorigin_panels_widgets', 'mytheme_recommended_widgets');
The SiteOrigin theme settings framework

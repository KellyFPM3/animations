# Website Animations

1. Add the CSS and JS folders to your theme directory.

2. Enqueue the JS and CSS for the animations by adding the following code to the functions.php file:

```
	function register_fpm3_animations($hook) {
		wp_enqueue_script('WOW-js', get_template_directory_uri() . '/js/WOW.js','','',true); // Required for animations
		wp_enqueue_script('fpm3-template-js', get_template_directory_uri() . '/js/fpm3-template.js','','',true);
		wp_enqueue_style('animate-css', get_template_directory_uri() . '/css/animate.css');
	}

	add_action('wp_enqueue_scripts', 'register_fpm3_animations');
```

3. Add these classes to the elements of the page that you want to animate: wow flipInY

The "wow" class is what tells the JS to animate that element, the "flipInY" class is the effect that is to be used. The other animation effects that can be used can be found here:

https://github.com/daneden/animate.css

Demos:

https://daneden.github.io/animate.css/

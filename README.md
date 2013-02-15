AMD_selectivizr
===============

Selectivizr.js as AMD module


Usage: require as you normally would any other AMD module.

Selectivizr must be initialized AFTER the DOM [and stylesheets] have loaded.

To do this:

	$(function() {

		//initialize selectivizr if IE is 8 or less
		
		if($.browser.msie){
			var ieVersion = /MSIE (\d+)/.exec(navigator.userAgent)[1];
			if(ieVersion < 9){
				//Instantiate selectivizr
				var selectivizr = new Selectivizr();
				//Kick off its instance to trigger init
				selectivizr.startup();	
			}	
		}
		
	});

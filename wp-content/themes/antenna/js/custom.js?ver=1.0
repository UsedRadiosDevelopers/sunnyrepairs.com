/*
 * Custom v1.0
 * DesignOrbital.com
 *
 * Copyright (c) 2013-2014 DesignOrbital.com
 *
 * License: GNU General Public License v2 or later
 * http://www.gnu.org/licenses/gpl-2.0.html
 *
 */

( function( $ ) {

	var antenna = {

		// Menu
		menuInit: function() {

			// Superfish Menu
			$( 'ul.sf-menu' ).superfish({
				delay: 			1200,
				animation: 		{ opacity : 'show', height : 'show' },
				speed: 			'fast',
				autoArrows: 	false,
				cssArrows: 		true 
			});

			// Clone the Primary Menu and remove classes from clone to prevent css issues
			$primaryMenuClone = $( '.primary-menu' ).clone().removeAttr( 'class' ).addClass( 'primary-menu-mobile' );
			$primaryMenuClone.find( '*' ).each( function( i,e ) {
				$( e ).removeAttr( 'style' );
			} );
			$primaryMenuClone.appendTo( '.mobile-navigation' );

			// Superfish Menu Separtor
			$( '<li class="prepend_item"><span>&nbsp;</span></li>' ).prependTo( 'ul.primary-menu.sf-menu' );
			$( '<li class="append_item"><span>&nbsp;</span></li>' ).appendTo( 'ul.primary-menu.sf-menu' );

			// Mobile Menu Toggle
			$( '.toggle-menu' ).pageslide({ 
				direction: 'right'
			});

		},

		// CSS3 Animation
		animationInit: function() {

			// On Hover
			$( '.img-postlist, .img-featured' ).hover(
				function() {
					$( this ).addClass( 'opacity-in' );
				}, function() {
					$( this ).removeClass( 'opacity-in' );
				}
			);

		},

		// Fitvids
		fitvidsInit: function() {

			// Fitvids - For responsive videos
			setTimeout( function() {
				$( '.entry-content' ).fitVids();
			}, 500 );

		}

	}

	/** Document Ready */
	$( document ).ready( function() {

		// Menu
		antenna.menuInit();

		// CSS3 Animation
		antenna.animationInit();

		// Fitvids - For responsive videos
		antenna.fitvidsInit();

		// Tooltip
		$( '.social-links-tooltip' ).tooltip();

		// Infinite Scroll Post Load
		$( document.body ).on( 'post-load', function () {
	        antenna.fitvidsInit();
	    } );

	} );

} )( jQuery );
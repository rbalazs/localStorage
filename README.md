localStorage
============

Highly compatible localStorage achieve perfect support IE series browsers, and provide a simplified interface to the secondary packaging.

** ** Supported browsers

	IE6 / IE7 / IE8 / IE9 / IE10 / IE11 / FireFox / Chrome / Opera / Safri

**Instructions**

Storage.js be introduced within the head tag.

	<Script src = 'storage.js'> </ script>
** ** Interface examples

	window.LS.set ("hello", "world"); // Set
	window.LS.get ("hello"); // read, if not the content, it returns undefined
	window.LS.remove ("hello"); // Delete
	window.LS.clear (); // Clear
	window.LS.each (function (key, value) {// traverse
		// Do something
	});
	var list = window.LS.obj (); // Get a list of locally stored objects
	var listNum = window.LS.length; // get the number of the local store

If you have jQuery before storage.js, is to add jQuery jQuery.LS interface consistent with window.LS function.  

** ** Rationale

! [Local Storage Compatibility] (http://pic002.cnblogs.com/images/2012/422834/2012070316413785.jpg "Local Storage Compatibility")

Pictured localStorage compatibility described in IE, there is a stuff called userData can simulate achieve localStorage interface. <br/>

But some high version of IE, although there localStorage, but there are many problems, the present components through continuous optimization detection scheme, select a <br/>
Appropriate programs to achieve analog interface does not support localStorage or localStorage question IE browser to realize a simulation of <br/>
Like, and then create a unified interface window.LS to provide related functions.

 * Native Interface localStorage a little winded, so the interface window.LS offer are very easy to understand. <br/>
 * If you do not like this wrapper interface, this component does not support localStorage browser add window.localStorage interfaces, <br/>
It can also be used, but you will have problems all native loacalStorage may encounter.

** Known Issues **

 * Native locally stored key is case sensitive, does not distinguish between simulated objects (because userData not distinguish key case)
 * Clear method of mock objects can only clean up the data set through this component
 * Actual storage capacity mock objects are different with native local store
 * Mock object does not support any event member localStorage

OptionalChaining
================

**IDE:** Xcode 6 Beta 4

**Language:** Swift

**Date:** 7/24/2014

Swift Conditional Optional Chaining is an extension that provides convenient syntax chaining for Optionals. Follow these simple steps to start:

* Add OptionalChaining.swift to your project

* Demo code:

		var planning:String?
		var analyzing:Array<String>?
		var coding:Dictionary<String, Int>?
		var testing:Bool?
		var packages: Int?
		
		planning = "OK"
		analyzing = [ "Phase 1", "Phase 2" ]
		coding = [ "Model developer": 5, "UI developer":4 ]
		testing = true
		packages = 950
		
		// Normally we want to check if variables are nil use this
        if planning && analyzing && coding && testing && packages {
            println("\(packages!) packages shipped")
        }
        
        // Instead we write this
        // Why? Because this is readable
        if planning?.then(analyzing)?.then(coding)?.then(testing)?.then(packages) {
            println("\(packages!) packages shipped")
        }

* Result

		950 packages shipped
		

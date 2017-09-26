# MithrilTypes-0.2-for-ts2.4
@types for legacy Mitrhil 0.2.x for TypeScript 2.4 or later

# Why

TypesScript 2.4 has introduced a breaking change called (WeakTypes)[https://github.com/Microsoft/TypeScript/wiki/Breaking-Changes]. If you are still maintaining Mithril 0.x code, your index.d.ts will break.

# If You Do Not Want to Bother With This

Fortunately, there is a single line that's causing the WeakType for now. Comment out onunloaded? under the interface Controller as below.

	/**
	* The basis of a Mithril controller instance.
	*/
	interface Controller {
		/**
		* An optional handler to call when the associated virtual element is
		* destroyed.
		*
		* @param evt An associated event.
		*/
		// onunload?(evt: Event): any;
	}


Media Assets Bug? — [Radar here](http://openradar.appspot.com/radar?id=5306801998266368)
-----------------
- The `media.xcassets` only needs to be added to the `.xcworkspace` for it to be *seen* already by the `.storyboard`. Is this normal?

- You might start by removing that reference to `media.xcassets` from the `.xcodeproj` (or remove it from the target). It will compile, but you'll see this at runtime

>Could not load the "image" image referenced from a nib in the bundle with identifier "biz.pomcast.rdar-workspace-asset"

	
- You would think having that `media.xcassets` in the target (thus also in `Copy Bundle Resources) solves the problem. So did I think.
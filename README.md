# OnBackPressedCallback (Fragment onBackPressed()) Sample

```kotlin
val callback = object : OnBackPressedCallback(true) {
    override fun handleOnBackPressed() {
        if (some-condition-here) {
            // your fragment onBackPressed() behavior
        } else {
            // default onBackPressed() behavior
            isEnabled = false // DON'T FORGET THIS!
            requireActivity().onBackPressedDispatcher.onBackPressed()
        }
    }
}
requireActivity().onBackPressedDispatcher.addCallback(callback)
```

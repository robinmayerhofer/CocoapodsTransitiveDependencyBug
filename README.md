# Poc For a Bug

Reproducible with `cocoapods 1.10.1`.

This project is not runnable in any form, it is just a proof of concept in order to reproduce a bug.

Use `bundle install` to install `cocoapods`, then `bundle exec pod install` to install the pods.
This creates this file: `Pods/Target Support Files/Pods-CocoapodsTransitiveDependencyBug/Pods-CocoapodsTransitiveDependencyBug-frameworks.sh `. It includes transitive dependencies of the original pod, although the pod itself is not included due to `:configurations => 'Debug'`.


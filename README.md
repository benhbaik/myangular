# Documentation/Notes for Build Your Own AngularJS

## Scope

### Scope Methods

#### $watch

##### scope.$watch(watchFn, listenerFn)

watchFn(scope)

    Returns value to be watched

listnerFn(newVal, oldVal)

    Function to be called when return value in watchFn changes

Registers watchers in scope.$$watchers.

#### $digest()

Iterates through $$watchers and checks all watchFn return values for changes.
If watchFn value has changed it calls corresponding listenerFn.

### Scope Properties

#### $$watchers

Store for all registered watchers.
# SampleHandler Class

`ISTEST`

This class is a sample trigger handler for use while testing 
the metadataTriggerHandler. Because custom metadata cannot be inserted, and 
because the MetadataTriggerHandler instantiates handler classes from custom 
metadata records, even when we stub/mock the metadata record retrieval we 
still need an actuall class that it can instantiate. 
 
Note, this class is annotated with `@isTest` to prevent it&#x27;s use outside of 
tests, not because it contains tests.

**Inheritance**

[TriggerHandler](../shared-code/TriggerHandler.md)

## Fields
### `context`

*Inherited*

`TESTVISIBLE`

#### Signature
```apex
protected context
```

#### Type
TriggerContext

## Methods
### `beforeInsert()`

#### Signature
```apex
public override void beforeInsert()
```

#### Return Type
**void**

---

### `beforeUpdate()`

#### Signature
```apex
public override void beforeUpdate()
```

#### Return Type
**void**

---

### `afterInsert()`

#### Signature
```apex
public override void afterInsert()
```

#### Return Type
**void**

---

### `afterupdate()`

#### Signature
```apex
public override void afterupdate()
```

#### Return Type
**void**

---

### `beforeDelete()`

#### Signature
```apex
public override void beforeDelete()
```

#### Return Type
**void**

---

### `afterDelete()`

#### Signature
```apex
public override void afterDelete()
```

#### Return Type
**void**

---

### `afterUndelete()`

#### Signature
```apex
public override void afterUndelete()
```

#### Return Type
**void**

---

### `run()`

*Inherited*

This is main brokering method that is called by the trigger. 
It&#x27;s responsible for determining the proper context, and calling the 
correct method

#### Signature
```apex
public virtual void run()
```

#### Return Type
**void**

#### Example
```apex
AccountTriggerHandler.run();
```

---

### `setMaxLoopCount(max)`

*Inherited*

Allows developers to prevent trigger loops, or allow 
a limited number of them by setting the maximum number of times 
this trigger is called.

#### Signature
```apex
public void setMaxLoopCount(Integer max)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| max | Integer | A valid number (generally 1) of times you&#x27;d like 
to allow the trigger to run. |

#### Return Type
**void**

#### Example
In the context of a `TriggerHandler` class: 
```apex
this.setMaxLoopCount(5);
```

---

### `clearMaxLoopCount()`

*Inherited*

Allows developers to turn off the max loop count

#### Signature
```apex
public void clearMaxLoopCount()
```

#### Return Type
**void**

#### Example
In the context of a `TriggerHandler` class: 
```apex
this.clearMaxLoopCount();
```

---

### `bypass(handlerName)`

*Inherited*

Allows developers to conditionally bypass (disable) 
other triggers that *also* implement this triggerHandler

#### Signature
```apex
public static void bypass(String handlerName)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| handlerName | String | Class name (String) of the trigger handler to bypass |

#### Return Type
**void**

#### Example
```apex
TriggerHandler.bypass('AccountTriggerHandler');
```

---

### `clearBypass(handlerName)`

*Inherited*

Removes a given trigger handler class name from 
the list of bypassed trigger handlers.

#### Signature
```apex
public static void clearBypass(String handlerName)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| handlerName | String | Handler class name to remove from the bypass list |

#### Return Type
**void**

#### Example
```apex
TriggerHandler.clearBypass('AccountTriggerHandler');
```

---

### `isBypassed(handlerName)`

*Inherited*

Allows developers to check whether a given trigger 
handler class is currently bypassed.

#### Signature
```apex
public static Boolean isBypassed(String handlerName)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| handlerName | String | The name of the trigger handler class to check for |

#### Return Type
**Boolean**

#### Example
```apex
TriggerHandler.isBypassed('AccountTriggerHandler');
```

---

### `clearAllBypasses()`

*Inherited*

removes all classes from the bypass list

#### Signature
```apex
public static void clearAllBypasses()
```

#### Return Type
**void**

#### Example
```apex
Triggerhandler.clearAllBypasses();
```

---

### `addToLoopCount()`

*Inherited*

`TESTVISIBLE`

increment the loop count

#### Signature
```apex
protected void addToLoopCount()
```

#### Return Type
**void**

#### Throws
Throws: loop count exception if the max loop count is reached

---

### `validateRun()`

*Inherited*

`TESTVISIBLE`

make sure this trigger should continue to run

#### Signature
```apex
protected Boolean validateRun()
```

#### Return Type
**Boolean**

#### Throws
TriggerHandlerException: thrown when executing outside of a,[object Object],trigger
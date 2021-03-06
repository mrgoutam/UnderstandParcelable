# Basic Understanding of Parcelable

### Why use of Parcelable?
When it comes to pass data from one activity to another activity, usually we do it via `getExtra` and  `putExtra` methods of our `intent` object. Like below
```
# Sending data from Activity1
intent.putExtra("name", "MrGoutamD");
```

```
# Receiving data in Activity2
Bundle data = getIntent().getExtras();
String nameStr = data.getString("name");
```
But this works in basic data types like `String`, `Boolean` and `Integer`. The above process doesn't work for `Objects`. For that we can use  **Serialization** and **Parcelable**. It is recommanded to use **Parcelable** because it is faster than **Serialization**.

### Introduction to Parcelable
Parcelable is an Android specific interface which is used to serialize a class so its property can be transferred from one activity to another.

*Note: Serialization is a process or mechanism of converting state of object into byte stream.*


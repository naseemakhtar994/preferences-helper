# preferences-helper
SharePreferences is very popular with any project and all most all project has SharePreferences for saving data. This library will help you faster in configuration and use SharePreferences in your project. Let's setup and enjoy!

# Setup
1. Add to build.gradle in app level
```
compile 'com.github.tntkhang:preferences-helper:1.0.0'
```


2. Init the PreferencesHelper in your CustomApplication.java extend from Application with 2 ways:
   
   - Will use app name as of Preferences file name ```PreferencesHelper.initHelper(this);```
   
   - Will use ```CustomName``` as the name of SharePreferences file ```PreferencesHelper.initHelper(this, "CustomName");```
   
3. How to use

```
   //SET VALUE:
   
   PreferencesHelper.getInstance().setValue(KEY_BOOLEAN, true);
   
   PreferencesHelper.getInstance().setValue(KEY_DOUBLE, 123.123);
   
   PreferencesHelper.getInstance().setValue(KEY_FLOAT, 234.234f);
   
   PreferencesHelper.getInstance().setValue(KEY_INT, 345);
   
   PreferencesHelper.getInstance().setValue(KEY_LONG, Long.MAX_VALUE);
   
   PreferencesHelper.getInstance().setValue(KEY_STRING, "Khang");

   UserModel userModel = new UserModel("KhangTran", 27);
   
   PreferencesHelper.getInstance().setValue(KEY_OBJECT, userModel);
   
   
   GET VALUE:
   
   boolean booleanValue = PreferencesHelper.getInstance().getBooleanValue(KEY_BOOLEAN, false);
   
   double doubleValue = PreferencesHelper.getInstance().getDoubleValue(KEY_DOUBLE, Double.MIN_VALUE);
   
   float floatValue = PreferencesHelper.getInstance().getFloatValue(KEY_FLOAT, Float.MIN_VALUE);
   
   int intValue = PreferencesHelper.getInstance().getIntValue(KEY_INT, Integer.MIN_VALUE);
   
   long longValue = PreferencesHelper.getInstance().getLongValue(KEY_LONG, Long.MIN_VALUE);
   
   String stringValue = PreferencesHelper.getInstance().getStringValue(KEY_STRING, "Empty");
   
   UserModel userModel = PreferencesHelper.getInstance().getObjectValue(KEY_OBJECT, UserModel.class);
   ```
   ###### END ##############

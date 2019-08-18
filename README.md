### automon
---
https://github.com/stevensouza/automon

```java
// automon/src/main/java/org/automon/utils/AutomonPropertiesLoader.java

public class AutomonPropertiseLoader {
  private static final String EMPTY_DEFAULT_OPEN_MON = "";
  private String[] fileNames;
  private Properties automonProps;
  
  private static final String ASPECTJ_CONFIG_FILE = "org.aspectj.weaver.loadtime.configuration";
  
  public static final String CONFIGURED_OPEN_MON = "org.automon";
  
  private boolean configFileFound = false;
  
  SysProperty sysProperty = new SysProperty();
  
  public AutomonPropertiesLoader() {
    this(System.getProperty(ASPECTJ_CONFIG_FILE, null), DEFAULT_PROPS_CONFIG_FILE, DEFAULT_FILE1, DEFAULT_XML_CONFIG_FILE2);
  }
  
  
  
  private void replaceWithSystemProps(Properties properties) {
    properties.putAll(sysProperty.getProperties());
  }
  
  Properties getDefaults() {
    Properties defaults = new Properties();
    defaults.put(CONFIGURED_OPEN_MON, EMPTY_DEFULT_OPEN_MON);
    return defaults;
  }
  
  static class SysProperty {
    public String getProperty(String key) {
      return System.getProperty(key);
    }
    
    public Properties getProperties() {
      return System.getProperties();
    }
  }
}

```

```
```

```
```



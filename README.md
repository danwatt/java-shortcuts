java-one-liners
===============

## Libraries to include
* Apache commons-lang(3)
* Apache commons-collections
* Apache commons-io
* Apache commons-codec
* Apache commons-are-you-noticing-a-trend-yet ...
* Google Guava 

## Strings
``` java
// org.apache.commons.lang3.RandomStringUtils
RandomStringUtils.randomAlphabetic(10);     //ajsdiqdIQq
RandomStringUtils.randomNumeric(10);        //1928912391
RandomStringUtils.randomAlphaNumeric(10);   //698jd19dn1

//org.apache.commons.lang3.text.WordUtils
WordUtils.capitalize("hello WORLD");        //Hello WORLD
WordUtils.uncapitalize("hello WORLD");      //hello wORLD
WordUtils.capitalizeFully("hello WORLD");   //Hello World
WordUtils.initials("hello WORLD");          //hW

// org.apache.commons.codec.digest.DigestUtils
DigestUtils.shaHex("hello world");          //2aae6c35c94fcfb415dbe95f408b9ce91ee846ed

//org.apache.commons.lang3.StringUtils
StringUtils.isBlank(null);                  //true
StringUtils.isBlank("");                    //true
StringUtils.isBlank("   ");                 //true
StringUtils.isBlank("\t\t");                //true
StringUtils.isBlank("Something");           //false
StringUtils.isNotBlank("Something");        //true
StringUtils.isEmpty(null);                  //true
StringUtils.isEmpty("");                    //true
StringUtils.isEmpty("   ");                 //false
StringUtils.isEmpty("\t\t");                //false
StringUtils.isEmpty("Something");           //false
StringUtils.isNotEmpty("Something");        //true
```

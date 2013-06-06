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

//com.google.common.hash.Hashing
Hashing.sha1().hashString("hello world").toString(); //2aae6c35c94fcfb415dbe95f408b9ce91ee846ed

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
## Collections

``` java
//java.util.Arrays
//Create a List
List<String> myList = Arrays.asList("A","B","C");

//java.util.Collections
//Sort a List in place
Collections.sort(myList);

//Reverse a List
Collections.reverse(myList);

//Randomize a List
Collections.shuffle(myList);

//Create am immutable collection of one item
Set<String> set = Collections.singleton("Value");
List<String> list = Collections.singletonList("Value");
Map<String,String> map = Collections.singletonMap("Key","Value");

//Wrap a collection so that it is immutable
Collection<String> immutable = Collections.unmodifiableCollection(myList);

//Apache commons-collections
CollectionUtils.isEmpty(null);                //true
CollectionUtils.isEmpty(emptyArray);          //true
CollectionUtils.isEmpty(Arrays.asList("A"));  //false

//Google Guava Collections
//com.google.common.collect.Lists
List<String> l = Lists.newArrayList("A","B","C");
List<List<String>> lol = Lists.partition(Lists.newArrayList("A","B","C","D"), 2); // Creates [[A,B],[C,D]]
```

## IO
``` java
//org.apache.commons.io.FileUtils
List<String> lines = FileUtils.readLines(new File("/tmp/test.txt"));
FileUtils.writeLines(new File("/tmp/test.txt"), Arrays.asList("A","B","C"));
String contents = FileUtils.readFileToString(new File("/tmp/test.txt"));

//org.apache.commons.io.IoUtils
IOUtils.closeQuietly(inputStream);      //Close an input stream without throwing an IOException
HexDump.dump(data, 0, System.out, 0);   //Write a hex dump of data (byte[]) to System.out

```

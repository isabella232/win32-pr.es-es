---
description: A continuación se muestra la lista completa del esquema del archivo de configuración del publicador.
ms.assetid: 501151ee-67f5-4127-b048-91ea4a42f9e7
title: Publisher Esquema del archivo de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a8e3d86adc71efda144bb5eed72876bf99911a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071338"
---
# <a name="publisher-configuration-file-schema"></a>Publisher Esquema del archivo de configuración

A continuación se muestra la lista completa del esquema del archivo de configuración del publicador.

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<Schema name="Microsoft Publisher Configuration Schema" xmlns="urn:schemas-microsoft-com:xml-data"
                        xmlns:dt="urn:schemas-microsoft-com:datatypes">  
<!-- Attributes -->
<AttributeType name="manifestVersion" dt:type="enumeration" dt:values="1.0"/> 
<AttributeType name="name" dt:type="string"/>
<AttributeType name="type" dt:type="enumeration" dt:values="win32-policy win32" required="yes"/>
<AttributeType name="publicKeyToken" dt:type="bin.hex"/>
<AttributeType name="language" dt:type="string"/>
<AttributeType name="processorArchitecture" dt:type="string"/>
<AttributeType name="version" dt:type="string"/>
<AttributeType name="oldVersion" dt:type="string"/>
<AttributeType name="newVersion" dt:type="string"/>
 
<!-- Elements-->
<ElementType name="assembly" model = "closed" content="eltOnly">
      <attribute type ="manifestVersion" required="yes"/>
      <element type="assemblyIdentity" minOccurs="1" maxOccurs="1"/>
      <element type="dependency" minOccurs="0" maxOccurs="*"/>
</ElementType>
<ElementType name="assemblyIdentity" model = "closed">
      <attribute type="type"  required="yes"/>
      <attribute type="name" required="yes"/>
      <attribute type="publicKeyToken" required="no"/>
      <attribute type="language" required="no"/>
      <attribute type="processorArchitecture"  required="yes" />
      <attribute type="version" required="no"/>
</ElementType>
<ElementType name="dependency" model = "closed" content="eltOnly">
      <element type="dependentAssembly" minOccurs="0" maxOccurs="1"/>
</ElementType>
<ElementType name="dependentAssembly"  model = "closed" content="eltOnly">
      <element type="assemblyIdentity" minOccurs="1" maxOccurs="1"/>
      <element type="bindingRedirect" minOccurs="1" maxOccurs="1"/>
</ElementType>
<ElementType name="bindingRedirect"  model = "closed">
      <attribute type="oldVersion" required="yes"/>
      <attribute type="newVersion" required="yes"/>
</ElementType>
</Schema>
```

 

 




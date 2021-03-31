---
description: A continuación se muestra la lista completa del esquema del archivo de configuración de la aplicación.
ms.assetid: c673dbff-cb64-4e90-88a8-c5f2c259f1d3
title: Esquema del archivo de configuración de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b964775755cf1bcbb8ec78e563b4b39f71e3cc7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277151"
---
# <a name="application-configuration-file-schema"></a><span data-ttu-id="be114-103">Esquema del archivo de configuración de la aplicación</span><span class="sxs-lookup"><span data-stu-id="be114-103">Application Configuration File Schema</span></span>

<span data-ttu-id="be114-104">A continuación se muestra la lista completa del esquema del archivo de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="be114-104">The following is the complete listing of the application configuration file schema.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<Schema name="Microsoft per Application Configuration Schema" xmlns="urn:schemas-microsoft-com:xml-data"
                        xmlns:dt="urn:schemas-microsoft-com:datatypes">  
<!-- Attributes -->
<AttributeType name="manifestVersion" dt:type="enumeration" dt:values="1.0"/> 
<AttributeType name="name" dt:type="string"/>
<AttributeType name="type" dt:type="enumeration" dt:values="win32" required="yes"/>
<AttributeType name="publicKeyToken" dt:type="bin.hex"/>
<AttributeType name="language" dt:type="string"/>
<AttributeType name="processorArchitecture" dt:type="string"/>
<AttributeType name="version" dt:type="string"/>
<AttributeType name="oldVersion" dt:type="string"/>
<AttributeType name="newVersion" dt:type="string"/>
 
<!-- Elements-->
<ElementType name="configuration" model = "closed" content="eltOnly">
      <element type ="windows" minOccurs="0" maxOccurs="1"/>
</ElementType>
<ElementType name="windows" content="eltOnly">
      <element type="assemblyBinding" minOccurs="0" maxOccurs="1"/>
</ElementType>
<ElementType name="assemblyBinding" content="eltOnly">
      <element type="assemblyIdentity" minOccurs="1" maxOccurs="1"/>
      <element type="dependentAssembly" minOccurs="0" maxOccurs="*"/>
</ElementType>
<ElementType name="assemblyIdentity" model = "closed">
      <attribute type="type"  required="yes"/>
      <attribute type="name" required="yes"/>
      <attribute type="publicKeyToken" required="no"/>
      <attribute type="language" required="no"/>
      <attribute type="processorArchitecture"  required="yes" />
      <attribute type="version" required="no"/>
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

 

 




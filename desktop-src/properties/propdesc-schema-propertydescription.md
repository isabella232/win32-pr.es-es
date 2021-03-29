---
description: Describe una única propiedad canónica única.
ms.assetid: 1a36ec83-5d8a-4fc5-be3d-a8c2f0983057
title: propertyDescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233f6d9b1242a9f02b2edbb2bb29cefaef625c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001571"
---
# <a name="propertydescription"></a>propertyDescription

Describe una única propiedad canónica única. Cada una de estas propiedades pensadas para estar disponibles en el sistema debe tener un elemento [propertyDescription]() correspondiente.

## <a name="syntax-for-windows-7"></a>Sintaxis para Windows 7


```
<!-- propertyDescription for Windows 7-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
            <xs:element ref="relatedPropertyInfo" minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="propid" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-vista"></a>Sintaxis para vista


```
<!-- propertyDescription for Windows Vista-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                           | Elementos secundarios                                                   |
|--------------------------------------------------------------------------|------------------------------------------------------------------|
| [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) | [searchInfo](./propdesc-schema-searchinfo.md)                   |
|                                                                          | [labelInfo](./propdesc-schema-labelinfo.md)                     |
|                                                                          | [Requerida](./propdesc-schema-typeinfo.md)                       |
|                                                                          | [aliasInfo](./propdesc-schema-aliasinfo.md)                     |
|                                                                          | [displayInfo](./propdesc-schema-displayinfo.md)                 |
|                                                                          | [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) |



 

## <a name="attributes"></a>Atributos



| Atributo | Descripción                                                                                                                                                                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name      | Necesario. Nombre canónico de la propiedad, único para el sistema; por ejemplo, `System.Rating` . Esta cadena es de tipo canónico-Type y está limitada a 64 caracteres. El nombre distingue entre mayúsculas y minúsculas y debe usar la sintaxis siguiente: Publisher. Application. PropertyName. [**IPropertyDescription:: GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) devuelve este valor. |
| formatID  | Obligatorio. Identificador de formato de la propiedad (FMTID). El valor debe incluir llaves envolventes; por ejemplo, `{64440492-4C8B-11D1-8B70-080036B11A03}` . [**IPropertyDescription:: GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) devuelve este valor.                                                                                                                       |
| propID    | Obligatorio. Identificador de propiedad (PID); por ejemplo, `9` . [**IPropertyDescription:: GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) devuelve este valor. Este valor debe ser mayor o igual que 2. El sistema reserva los valores 0 y 1.                                                                                                                  |



 

 

 

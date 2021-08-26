---
description: El elemento propertyStore opcional especifica la ubicación de un IPropertyStore basado en XML para almacenar los metadatos abiertos &lt; para este conector de &gt; búsqueda. Este elemento no tiene atributos y solo un elemento secundario.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: elemento propertyStore (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c617f560e0471062064bcec8020dd5e6efa026
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886794"
---
# <a name="propertystore-element-search-connector-schema"></a>elemento propertyStore (esquema del conector de búsqueda)

El elemento propertyStore opcional especifica la ubicación de un IPropertyStore basado en XML para almacenar los metadatos abiertos &lt; para este conector de &gt; búsqueda. Este elemento no tiene atributos y solo un elemento secundario.

## <a name="syntax"></a>Syntax


```
<!-- propertyStore -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0">
            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                                                                   | Elementos secundarios                                                                                            |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)](search-schema-searchconnectordescription.md) | [elemento property de propertyStore (esquema del conector de búsqueda)](search-schema-sconn-propstore-property.md) |



 

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra &lt; un elemento propertyStore &gt; con dos elementos de &lt; &gt; propiedad.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 




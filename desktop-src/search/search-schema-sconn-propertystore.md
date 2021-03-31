---
description: El <propertyStore> elemento opcional especifica la ubicación de un IPropertyStore basado en XML para almacenar los metadatos abiertos para este conector de búsqueda. Este elemento no tiene atributos y solo un elemento secundario.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: Elemento propertyStore (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11f8cda6457de764b00519a81a1134e7eecc8638
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808899"
---
# <a name="propertystore-element-search-connector-schema"></a>Elemento propertyStore (esquema del conector de búsqueda)

El <propertyStore> elemento opcional especifica la ubicación de un IPropertyStore basado en XML para almacenar los metadatos abiertos para este conector de búsqueda. Este elemento no tiene atributos y solo un elemento secundario.

## <a name="syntax"></a>Sintaxis


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
| [Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)](search-schema-searchconnectordescription.md) | [Elemento Property de propertyStore (esquema del conector de búsqueda)](search-schema-sconn-propstore-property.md) |



 

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra un <propertyStore> elemento con dos <property> elementos.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 




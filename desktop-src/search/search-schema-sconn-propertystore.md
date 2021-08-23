---
description: El elemento opcional especifica la ubicación de un IPropertyStore basado en XML para <propertyStore> almacenar los metadatos abiertos para este conector de búsqueda. Este elemento no tiene atributos y solo un elemento secundario.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: elemento propertyStore (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de5a9e801163bd85635b82c1915394f24c39d3dfdafcb64c81fcff0bf84a219
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351855"
---
# <a name="propertystore-element-search-connector-schema"></a>elemento propertyStore (esquema del conector de búsqueda)

El elemento opcional especifica la ubicación de un IPropertyStore basado en XML para <propertyStore> almacenar los metadatos abiertos para este conector de búsqueda. Este elemento no tiene atributos y solo un elemento secundario.

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

En el ejemplo siguiente se muestra <propertyStore> un elemento con dos elementos <property> .


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 




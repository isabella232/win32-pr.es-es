---
description: El <propertyBag> elemento requerido especifica un conjunto de una o varias propiedades utilizadas por este proveedor de ubicación.
ms.assetid: 63f8f2e4-3b52-4d6e-8d3a-2e133aac0e86
title: Elemento propertyBag (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb9e80691e929f7fcceaff3dded4b99a242e92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082010"
---
# <a name="propertybag-element-search-connector-schema"></a>Elemento propertyBag (esquema del conector de búsqueda)

El <propertyBag> elemento requerido especifica un conjunto de una o varias propiedades utilizadas por este proveedor de ubicación.

## <a name="syntax"></a>Sintaxis


```
<!-- propertyBag -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
                            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
                        </xs:element>
                    </xs:all>
                <xs:attribute name="clsid" use="required"/>
                <xs:attribute name="codebase" type="xs:string"/>
            </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                                                 | Elementos secundarios                                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Elemento locationProvider (esquema del conector de búsqueda)](search-schema-sconn-locationprovider.md) | [Elemento Property (esquema del conector de búsqueda)](search-schema-sconn-locationproviderproperty.md) |



 

## <a name="example-of-a-propertybag-element-and-property-elements"></a>Ejemplo de elemento PropertyBag y elementos Property


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 




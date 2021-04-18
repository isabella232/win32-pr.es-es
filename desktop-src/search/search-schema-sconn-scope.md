---
description: El <scope> elemento opcional especifica una colección de <scopeItem> elementos que definen las inclusiones y exclusiones del ámbito de este conector de búsqueda concreto.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: Elemento Scope (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f49041170db80de48d312596249d5c4dca835e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696261"
---
# <a name="scope-element-search-connector-schema"></a>Elemento Scope (esquema del conector de búsqueda)

El <scope> elemento opcional especifica una colección de <scopeItem> elementos que definen las inclusiones y exclusiones del ámbito de este conector de búsqueda concreto. Si <scope> está presente, debe contener al menos un <scopeItem> elemento. Este elemento no tiene atributos.

## <a name="syntax"></a>Sintaxis


```
<!-- scope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                       ...
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                                                                   | Elementos secundarios                                                                    |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)](search-schema-searchconnectordescription.md) | [elemento scopeItem (esquema del conector de búsqueda)](search-schema-sconn-scopeitem.md). |



 

## <a name="remarks"></a>Observaciones

Use los <scope> <scopeItem> elementos y para identificar las ubicaciones en las que se debe buscar y qué ubicaciones se deben excluir de la búsqueda.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra un ámbito de búsqueda que incluye C: \\ ExampleFolder y todas sus carpetas secundarias excepto c: \\ ExampleFolder \\ ExcludeMe.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder</url>
        </scopeItem>
        <scopeItem>
            <mode>Exclude</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 




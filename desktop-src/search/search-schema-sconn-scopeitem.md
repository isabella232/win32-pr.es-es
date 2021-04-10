---
description: El <scopeItem> elemento representa una única entrada en la tabla de ámbito de inclusión/exclusión.
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: Elemento scopeItem (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2033202be6d904880ec9c4efa1c60db4bb7e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153933"
---
# <a name="scopeitem-element-search-connector-schema"></a>Elemento scopeItem (esquema del conector de búsqueda)

El <scopeItem> elemento representa una única entrada en la tabla de ámbito de inclusión/exclusión. <scopeItem> extiende el tipo shellLinkType estándar agregando tres nuevos elementos que controlan la inclusión y exclusión de carpetas, controlan la profundidad de los resultados y especifican la ubicación del ámbito. Si el <scope> elemento existe, este elemento es obligatorio. Tiene tres elementos secundarios y ningún atributo.

## <a name="syntax"></a>Sintaxis


```
<!-- scopeItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                <xs:element name="mode" default="Include">
                                    ...
                                </xs:element>
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    ...
                                </xs:element>
                                <xs:element name="url" type="xs:anyURI"/>
                            </xs:all>
                        </xs:complexType>
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



| Elemento primario                                                           | Elementos secundarios                                                                        |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Elemento Scope (esquema del conector de búsqueda)](search-schema-sconn-scope.md) | [elemento Scope (esquema del conector de búsqueda)](search-schema-sconn-scope-mode.md).        |
|                                                                          | [elemento Scope (esquema del conector de búsqueda)](search-schema-sconn-scope-depth.md).       |
|                                                                          | [elemento URL scopeItem (esquema del conector de búsqueda)](search-schema-sconn-scope-url.md). |



 

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



 

 




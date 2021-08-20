---
description: El <scopeItem> elemento representa una sola entrada en la tabla de ámbito de exclusión o inclusión.
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: elemento scopeItem (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bf8cc7ba9d296503a9703845d8a03287006ed178dca7f51228e89827a0c710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118051507"
---
# <a name="scopeitem-element-search-connector-schema"></a>elemento scopeItem (esquema del conector de búsqueda)

El <scopeItem> elemento representa una sola entrada en la tabla de ámbito de exclusión o inclusión. <scopeItem> extiende el tipo shellLinkType estándar agregando tres nuevos elementos que controlan la inclusión y exclusión de carpetas, controlan la profundidad de los resultados y especifican la ubicación del ámbito. Si el <scope> elemento existe, este elemento es obligatorio. Tiene tres elementos secundarios y no tiene atributos.

## <a name="syntax"></a>Syntax


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
| [elemento scope (esquema del conector de búsqueda)](search-schema-sconn-scope.md) | [elemento scope (esquema del conector de búsqueda).](search-schema-sconn-scope-mode.md)        |
|                                                                          | [elemento scope (esquema del conector de búsqueda).](search-schema-sconn-scope-depth.md)       |
|                                                                          | [elemento scopeItem url (esquema del conector de búsqueda).](search-schema-sconn-scope-url.md) |



 

## <a name="remarks"></a>Comentarios

Use los <scope> elementos y para identificar qué ubicaciones se deben buscar y qué ubicaciones deben <scopeItem> excluirse de la búsqueda.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra un ámbito de búsqueda que incluye C: ExampleFolder y todas sus carpetas secundarias excepto \\ C: \\ ExampleFolder \\ ExcludeMe.


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



 

 




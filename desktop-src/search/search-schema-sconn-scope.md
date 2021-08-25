---
description: El elemento opcional especifica una colección de elementos que definen las inclusiones y exclusiones del ámbito <scope> para este conector de búsqueda <scopeItem> determinado.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: elemento scope (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d5fcdb3908f495d07199c61a2005a4f97ba5a01c641fb4e854961489e7abe0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944305"
---
# <a name="scope-element-search-connector-schema"></a>elemento scope (esquema del conector de búsqueda)

El elemento opcional especifica una colección de elementos que definen las inclusiones y exclusiones del ámbito <scope> para este conector de búsqueda <scopeItem> determinado. Si <scope> está presente, DEBE contener al menos un <scopeItem> elemento. Este elemento no tiene atributos.

## <a name="syntax"></a>Syntax


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
| [Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)](search-schema-searchconnectordescription.md) | [elemento scopeItem (esquema del conector de búsqueda).](search-schema-sconn-scopeitem.md) |



 

## <a name="remarks"></a>Comentarios

Use los <scope> elementos y para identificar qué ubicaciones se deben buscar y qué ubicaciones se deben excluir de la <scopeItem> búsqueda.

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



 

 




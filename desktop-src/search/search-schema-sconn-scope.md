---
description: El elemento scope opcional especifica una colección de elementos scopeItem que definen las inclusiones y exclusiones de ámbito &lt; para este conector de búsqueda &gt; &lt; &gt; determinado.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: elemento scope (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c011eee8def80a7f1d395a7a52a72d30fb4935
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886701"
---
# <a name="scope-element-search-connector-schema"></a>elemento scope (esquema del conector de búsqueda)

El elemento scope opcional especifica una colección de elementos scopeItem que definen las inclusiones y exclusiones de ámbito &lt; para este conector de búsqueda &gt; &lt; &gt; determinado. Si &lt; el ámbito está &gt; presente, DEBE contener al menos un elemento &lt; &gt; scopeItem. Este elemento no tiene atributos.

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

Use los elementos scope y scopeItem para identificar qué ubicaciones se deben buscar y qué ubicaciones &lt; se deben excluir de la &gt; &lt; &gt; búsqueda.

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



 

 




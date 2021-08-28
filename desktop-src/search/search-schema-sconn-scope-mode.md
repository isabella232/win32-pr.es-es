---
description: El &lt; elemento mode especifica si la dirección URL debe incluirse o &gt; excluirse del ámbito del conector de búsqueda. Los valores permitidos son Include y Exclude. Este elemento no tiene elementos secundarios ni atributos.
ms.assetid: 7654c04a-31c4-4260-a51c-0600804e62a9
title: elemento mode (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e096bb21d634da6107359c014b82f1b367aba1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886745"
---
# <a name="mode-element-search-connector-schema"></a>elemento mode (esquema del conector de búsqueda)

El &lt; elemento mode especifica si la dirección URL debe incluirse o &gt; excluirse del ámbito del conector de búsqueda. Los valores permitidos son `Include` y `Exclude`. Este elemento no tiene elementos secundarios ni atributos.

## <a name="syntax"></a>Syntax


```
<!-- mode -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="mode" default="Include">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Include"/>
                                            <xs:enumeration value="Exclude"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                </xs:element>
                                ...
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



| Elemento primario                                                                   | Elementos secundarios |
|----------------------------------------------------------------------------------|----------------|
| [elemento scopeItem (esquema del conector de búsqueda)](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a>Comentarios

No se puede buscar ni examinar un ámbito excluido. Puede anidar direcciones URL de scopeItem. Por ejemplo, puede incluir un ámbito primario y todos sus elementos secundarios excepto uno agregando la dirección URL primaria como se incluye, con el valor de profundidad Deep y excluyendo la dirección URL secundaria.

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
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 




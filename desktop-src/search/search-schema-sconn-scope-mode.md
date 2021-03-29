---
description: El <mode> elemento especifica si la dirección URL se debe incluir o excluir del ámbito del conector de búsqueda. Los valores permitidos son include y exclude. Este elemento no tiene ningún elemento secundario y no tiene atributos.
ms.assetid: 7654c04a-31c4-4260-a51c-0600804e62a9
title: Elemento Mode (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8c09b4c6de138e6e390d2c31a82fe5d1f56566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808894"
---
# <a name="mode-element-search-connector-schema"></a>Elemento Mode (esquema del conector de búsqueda)

El <mode> elemento especifica si la dirección URL se debe incluir o excluir del ámbito del conector de búsqueda. Los valores permitidos son `Include` y `Exclude`. Este elemento no tiene ningún elemento secundario y no tiene atributos.

## <a name="syntax"></a>Sintaxis


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
| [Elemento scopeItem (esquema del conector de búsqueda)](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a>Observaciones

No se puede buscar ni examinar un ámbito excluido. Puede anidar las direcciones URL de scopeItem. Por ejemplo, puede incluir un ámbito primario y todos sus elementos secundarios, excepto uno, agregando la dirección URL primaria tal como se incluye, con un valor de profundidad de profundidad y sin incluir la dirección URL secundaria.

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
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 




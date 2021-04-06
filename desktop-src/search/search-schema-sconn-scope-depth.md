---
description: El <depth> elemento especifica si el ámbito del conector de búsqueda debe incluir direcciones URL secundarias. Los valores permitidos son Deep y Shallow. Este elemento no tiene ningún elemento secundario y no tiene atributos.
ms.assetid: 859decab-cbe3-4cec-b37c-6d0e7c353876
title: Depth (elemento) (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf68bcbc96b6d1beb2c381f0a17532272b8d397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000994"
---
# <a name="depth-element-search-connector-schema"></a>Depth (elemento) (esquema del conector de búsqueda)

El <depth> elemento especifica si el ámbito del conector de búsqueda debe incluir direcciones URL secundarias. Los valores permitidos son `Deep` y `Shallow`. Este elemento no tiene ningún elemento secundario y no tiene atributos.

## <a name="syntax"></a>Sintaxis


```
<!-- depth -->
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
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Shallow"/>
                                            <xs:enumeration value="Deep"/>
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

Si la profundidad es profunda, los usuarios pueden examinar o buscar elementos en el nivel de dirección URL de scopeItem o en cualquier dirección URL secundaria.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra un ámbito de búsqueda que incluye C: \\ FolderA y todas sus carpetas secundarias y c: \\ FolderB, pero ninguna de sus carpetas secundarias.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\FolderA</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\FolderB</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 




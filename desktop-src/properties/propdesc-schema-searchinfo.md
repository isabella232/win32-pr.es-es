---
description: Especifica cómo configurar el motor de búsqueda de Windows con respecto a una definición de propiedad determinada.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: searchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee94585aaa66a761e527ac6ada1c33b0d23966d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666852"
---
# <a name="searchinfo"></a>searchInfo

Especifica cómo configurar el motor de búsqueda de Windows con respecto a una definición de propiedad determinada. Si no se proporciona ningún elemento [searchInfo]() , la propiedad no se incluye en el motor de búsqueda de Windows. Este elemento ha cambiado para Windows 7.

## <a name="syntax-for-windows-7"></a>Sintaxis para Windows 7


```
<!-- searchInfo for Windows 7-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                    <xs:enumeration value="OnDiskAll"/>
                    <xs:enumeration value="OnDiskVector"/>
                    <xs:enumeration value="OnDemand"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="512"/>
        <xs:attribute name="mnemonics" type="xs:string"/>                            
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-windows-vista"></a>Sintaxis de Windows Vista


```
<!-- searchInfo for Windows Vista-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="128"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                   | Elementos secundarios |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | None           |



 

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>inInvertedIndex</td>
<td>Público. Opcional. Indica si el valor de la propiedad se debe almacenar en el índice invertido. Esto permite que los usuarios finales realicen consultas de texto completo sobre los valores de esta propiedad. El valor predeterminado es &quot;false&quot;.</td>
</tr>
<tr class="even">
<td>isColumn</td>
<td>Público. Opcional. Indica si la propiedad también debe almacenarse en la base de datos de Windows Search como una columna, de modo que los fabricantes de software independientes (ISV) puedan crear consultas basadas en predicado (por ejemplo, &quot; Select * donde &quot; System. title &quot; = ' QQQ ' &quot; ). Si el creador del esquema desea permitir que los usuarios finales (o los desarrolladores) creen consultas basadas en predicado en las propiedades, debe establecerse en &quot; true &quot; . El valor predeterminado es &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>isColumnSparse</td>
<td>Público. Opcional. El valor predeterminado es &quot;true&quot;. Si la propiedad tiene varios valores, este atributo siempre es &quot; true &quot; .</td>
</tr>
<tr class="even">
<td>columnIndexType</td>
<td>Público. Opcional. Para optimizar la ordenación y agrupación, el motor de búsqueda de Windows puede crear índices secundarios para propiedades que tengan isColumn = &quot; true &quot; . Este atributo solo es útil cuando inInvertedIndex es &quot; true &quot; en Windows Vista o cuando isColumn es &quot; true &quot; en Windows 7. Si los usuarios suelen ordenar la propiedad con frecuencia, se debe especificar este atributo. El valor predeterminado en Windows Vista es &quot; NotIndexed &quot; . El valor predeterminado en Windows 7 es &quot; OnDemand &quot; . Los valores siguientes son válidos.
<ul>
<li><strong>NotIndexed</strong>: nunca cree un índice de valor.</li>
<li><strong>Disco</strong>: crea un índice de valor de forma predeterminada para esta propiedad.</li>
<li><strong>OnDiskAll</strong> (solo Windows 7 y versiones posteriores): cree un índice de valor de forma predeterminada para esta propiedad y, si es una propiedad de Vector, también un índice de valor para todos los valores de vector concatenados.</li>
<li><strong>OnDiskVector</strong> (solo Windows 7 y versiones posteriores): compilar un índice de valor de forma predeterminada para los valores de vector concatenados.</li>
<li><strong>OnDemand</strong> (solo Windows 7 y versiones posteriores): solo se generan índices de valor por demanda, es decir, solo se usan por primera vez para una consulta.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tamañomáximo</td>
<td>Público. Opcional. Tamaño máximo, en bytes, permitido para una determinada propiedad almacenada en la base de datos de Windows Search. El valor predeterminado es:
<ul>
<li><strong>Windows Vista</strong>: 128 bytes</li>
<li><strong>Windows 7 y versiones posteriores</strong>: 512 bytes</li>
</ul>
Tenga en cuenta que este tamaño máximo se mide en bytes, no en caracteres. El número máximo de caracteres depende de su codificación.<br/></td>
</tr>
<tr class="even">
<td>teclas de acceso</td>
<td><strong>Windows 7 y versiones posteriores.</strong> Público. Opcional. Una lista de valores de tecla de tecla que se pueden usar para hacer referencia a la propiedad en consultas de búsqueda. La lista está delimitada por el carácter "|".</td>
</tr>
</tbody>
</table>



 

 

 

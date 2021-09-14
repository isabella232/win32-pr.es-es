---
description: Especifica cómo configurar el motor de búsqueda Windows con respecto a una definición de propiedad determinada.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: searchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbcfc901dfb4610210c4990c962b5251710e5653
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268247"
---
# <a name="searchinfo"></a>searchInfo

Especifica cómo configurar el motor de búsqueda Windows con respecto a una definición de propiedad determinada. Si no se proporciona ningún elemento [searchInfo,]() la propiedad no se incluye en el motor de Windows búsqueda. Este elemento ha cambiado para Windows 7.

## <a name="syntax-for-windows-7"></a>Sintaxis de Windows 7


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




| Atributo | Descripción | 
|-----------|-------------|
| inInvertedIndex | Público. Opcional. Indica si el valor de propiedad debe almacenarse en el índice invertido. Esto permite a los usuarios finales realizar consultas de texto completo sobre los valores de esta propiedad. El valor predeterminado es "false". | 
| isColumn | Público. Opcional. Indica si la propiedad también debe almacenarse en la base de datos de búsqueda de Windows como una columna, de modo que los proveedores de software independientes (ISV) puedan crear consultas basadas en predicados (por ejemplo, "Select * Where "System.Title"='qqq'"). Si el creador del esquema quiere permitir que los usuarios finales (o desarrolladores) creen consultas basadas en predicados en las propiedades, debe establecerse en "true". El valor predeterminado es "false". | 
| isColumnSparse | Público. Opcional. El valor predeterminado es "true". Si la propiedad tiene varios valores, este atributo siempre es "true". | 
| columnIndexType | Público. Opcional. Para optimizar la ordenación y la agrupación, Windows motor de búsqueda puede crear índices secundarios para las propiedades que tienen isColumn="true". Este atributo solo es útil cuando inInvertedIndex es "true" en Windows Vista o cuando isColumn es "true" en Windows 7. Si los usuarios tienden a ordenar la propiedad con frecuencia, se debe especificar este atributo. El valor predeterminado de Windows Vista es "NotIndexed". El valor predeterminado de Windows 7 es "OnDemand". Los valores siguientes son válidos.<ul><li><strong>NotIndexed:</strong>nunca cree un índice de valor.</li><li><strong>OnDisk:</strong>compile un índice de valor de forma predeterminada para esta propiedad.</li><li><strong>OnDiskAll</strong> (Windows 7 y versiones posteriores): compile un índice de valor de forma predeterminada para esta propiedad y, si es una propiedad de vector, también un índice de valor para todos los valores de vector concatenados.</li><li><strong>OnDiskVector</strong> (Windows 7 y versiones posteriores): cree un índice de valor de forma predeterminada para los valores de vector concatenados.</li><li><strong>OnDemand</strong> (Windows 7 y versiones posteriores): solo se crean índices de valor por demanda, es decir, solo la primera vez que se usan para una consulta.</li></ul> | 
| Maxsize | Público. Opcional. Tamaño máximo, en bytes, permitido para una determinada propiedad que se almacena en la base de Windows de búsqueda. El valor predeterminado es:<ul><li><strong>Windows Vista:</strong>128 bytes</li><li><strong>Windows 7 y versiones posteriores:</strong>512 bytes</li></ul>Tenga en cuenta que este tamaño máximo se mide en bytes, no en caracteres. El número máximo de caracteres depende de su codificación.<br /> | 
| teclas de acceso | <strong>Windows 7 y versiones posteriores.</strong> Público. Opcional. Lista de valores mnemotécnicos que se pueden usar para hacer referencia a la propiedad en las consultas de búsqueda. La lista está delimitada por '|Carácter '. | 




 

 

 

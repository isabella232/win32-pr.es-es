---
description: Especifica cómo se muestran las etiquetas de la propiedad.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: labelInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d2d358270bfdf231f990feee54d90f6f39f16fa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475101"
---
# <a name="labelinfo"></a>labelInfo

Especifica cómo se muestran las etiquetas de la propiedad. Solo debe haber un [elemento labelInfo]() para cada [elemento propertyDescription.](./propdesc-schema-propertydescription.md)

Si hay varios elementos, se usa el último. Si no se proporciona ningún elemento [labelInfo,]() no se muestra la etiqueta de la propiedad; sin embargo, esto suele ser un defecto.

## <a name="syntax"></a>Syntax


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                   | Elementos secundarios |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | Ninguno           |



 

## <a name="attributes"></a>Atributos




| Atributo | Descripción | 
|-----------|-------------|
| label | Público. Opcional. Etiqueta tal como se muestra en la interfaz de usuario (por ejemplo, la etiqueta de columna de detalles o el panel de vista previa). La sintaxis permite una cadena de presentación directa o una referencia de cadena de presentación indirecta. Use la cadena de presentación indirecta porque se puede localizar. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription::GetDisplayName devuelve</strong></a> el nombre para mostrar resuelto. | 
| sortDescription | Opcional. Especifica las cadenas que se ofrecen como opciones de ordenación. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription::GetSortDescription devuelve</strong></a> esta descripción de ordenación. Los valores siguientes proporcionan las cadenas de interfaz de usuario correspondientes.<ul><li>General: "Sort going up" / "Sort going down"</li><li>AToZ: "A en la parte superior" / "Z en la parte superior"</li><li>LowestHighest: "Lowest on top" / "Highest on top"</li><li>OldestNewest: "Oldest on top" / "Newest on top"</li><li>SmallestLargest: "Smallest on top" / "Largest on top"</li></ul> | 
| invitationText | Opcional. Texto de la cadena de ayuda que se muestra como una instrucción al usuario para el control o la información sobre herramientas (por ejemplo, "Escriba el nombre del autor"). La sintaxis permite una cadena de presentación directa o una referencia de cadena de presentación indirecta. Use la cadena de presentación indirecta porque se puede localizar. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription::GetEditInvitation devuelve</strong></a> el texto de invitación resuelto. | 
| hideLabel | Opcional. El valor predeterminado es "false". Indica si la etiqueta está oculta. | 




 

 

 

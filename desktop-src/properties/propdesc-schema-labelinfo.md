---
description: Especifica cómo se muestran las etiquetas de la propiedad.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: labelInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cc0cfc417fae49527bcee50ac5043b1f07f309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666861"
---
# <a name="labelinfo"></a>labelInfo

Especifica cómo se muestran las etiquetas de la propiedad. Solo debe haber un elemento [labelInfo]() para cada elemento [propertyDescription](./propdesc-schema-propertydescription.md) .

Si hay varios elementos, se usa el último. Si no se proporciona ningún elemento [labelInfo]() , no se muestra la etiqueta de la propiedad; sin embargo, esto suele ser un defecto.

## <a name="syntax"></a>Sintaxis


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
<td>etiqueta</td>
<td>Público. Opcional. La etiqueta tal como se muestra en la interfaz de usuario (por ejemplo, la etiqueta de la columna de detalles o el panel de vista previa). La sintaxis permite una cadena de presentación directa o una referencia de cadena de presentación indirecta. Use la cadena de presentación indirecta porque se puede localizar. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription:: getDisplayName</strong></a> devuelve el nombre para mostrar resuelto.</td>
</tr>
<tr class="even">
<td>sortDescription</td>
<td>Opcional. Especifica las cadenas que se ofrecen como opciones de ordenación. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription:: GetSortDescription</strong></a> devuelve esta descripción de ordenación. Los valores siguientes proporcionan las cadenas de interfaz de usuario correspondientes.
<ul>
<li>General: orden de marcha en orden &quot; &quot;  /  &quot; descendente&quot;</li>
<li>AToZ: a &quot; en la parte superior &quot;  /  &quot; Z en la parte superior&quot;</li>
<li>LowestHighest: &quot; más &quot;  /  &quot; alto en la parte superior superior&quot;</li>
<li>OldestNewest: &quot; más antiguo en la parte superior &quot;  /  &quot; más reciente&quot;</li>
<li>SmallestLargest: más pequeño en la parte superior &quot; &quot;  /  &quot; más grande&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td>invitationText</td>
<td>Opcional. El texto de la cadena de ayuda que se muestra como una instrucción al usuario para el control o la información sobre herramientas (por ejemplo, &quot; Escriba el nombre del autor &quot; ). La sintaxis permite una cadena de presentación directa o una referencia de cadena de presentación indirecta. Use la cadena de presentación indirecta porque se puede localizar. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription:: GetEditInvitation</strong></a> devuelve el texto de la invitación resuelta.</td>
</tr>
<tr class="even">
<td>hideLabel</td>
<td>Opcional. El valor predeterminado es &quot;false&quot;. Indica si la etiqueta está oculta.</td>
</tr>
</tbody>
</table>



 

 

 

---
description: Especifica el control que se va a usar al mostrar simplemente la propiedad.
ms.assetid: 0fb8afc4-d16b-4c2e-80b3-da9935b11bb5
title: drawControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5318fdebc995ff45932f75b4000ceda6e74068e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082422"
---
# <a name="drawcontrol"></a>drawControl

Especifica el control que se va a usar al mostrar simplemente la propiedad. Solo debe haber un elemento [drawControl]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .

Si hay varios elementos, se usa el último. Si no se proporciona ningún elemento [drawControl]() , los valores de atributo predeterminados se aplican a la descripción de la propiedad.

Este formulario del control no permite la edición de propiedades.

## <a name="syntax"></a>Sintaxis


```
<!-- drawControl -->
<xs:element name="drawControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="PercentBar"/>
                    <xs:enumeration value="ProgressBar"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="StaticText"/>
                    <xs:enumeration value="IconList"/>
                    <xs:enumeration value="BooleanCheckMark"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                   | Elementos secundarios |
|--------------------------------------------------|----------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | None           |



 

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
<td>control</td>
<td>Público. Opcional. El valor predeterminado es &quot; default &quot; . Estos son los valores válidos. 
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valor predeterminado</td>
<td>Predeterminada. Utiliza el control predeterminado, basado en el <typeInfo type=&quot;&quot;> atributo. El tipo predeterminado es &quot; String &quot; (varios valores) y el control predeterminado es &quot; MultiValueText &quot; . Cualquier otro tipo da como resultado el uso del &quot; &quot; control StaticText.</td>
</tr>
<tr class="even">
<td>MultiLineText</td>
<td>Usa el control de texto de varias líneas.</td>
</tr>
<tr class="odd">
<td>MultiValueText</td>
<td>Usa el control de texto de varios valores.</td>
</tr>
<tr class="even">
<td>PercentBar</td>
<td>Usa el control de barra de porcentaje.</td>
</tr>
<tr class="odd">
<td>ProgressBar</td>
<td>Usa el control de barra de progreso.</td>
</tr>
<tr class="even">
<td>Rating</td>
<td>Usa el control de clasificación de 5 estrellas.</td>
</tr>
<tr class="odd">
<td>StaticText</td>
<td>Usa <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription:: FormatForDisplay</strong></a> para mostrar el valor de propiedad.</td>
</tr>
<tr class="even">
<td>IconList</td>
<td><strong>Windows 7 y versiones posteriores.</strong> Una enumeración de iconos.</td>
</tr>
<tr class="odd">
<td>BooleanCheckMark</td>
<td><strong>Windows 7 y versiones posteriores.</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 

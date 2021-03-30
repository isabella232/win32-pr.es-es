---
description: Especifica el control que se va a usar al editar la propiedad.
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: editControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966f9742082fd6b5f939941a956eaae1ac4e427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002046"
---
# <a name="editcontrol"></a>editControl

Especifica el control que se va a usar al editar la propiedad. Solo debe haber un elemento [editControl]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .

Si hay varios elementos, se usa el último. Si no se proporciona ningún elemento [editControl]() , los valores de atributo predeterminados se aplican a la descripción de la propiedad.

Si <typeInfo isInnate="true"> es, este elemento se omite porque no se puede editar una propiedad innate.

## <a name="syntax"></a>Sintaxis


```
<!-- editControl -->
<xs:element name="editControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                    <xs:enumeration value="IconList"/>
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
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valor predeterminado</td>
<td>Predeterminada. Utiliza el control predeterminado, basado en el <typeInfo type=&quot;&quot;> atributo. A continuación se enumeran los tipos predeterminados. Cualquier otro tipo da como resultado el uso del &quot; control de texto &quot; . 
<table>
<thead>
<tr class="header">
<th>Tipo</th>
<th>Control</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>Texto</td>
</tr>
<tr class="even">
<td>Cadena (varios valores)</td>
<td>MultiValueText</td>
</tr>
<tr class="odd">
<td>DateTime</td>
<td>Calendario</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Calendario</td>
<td>Usa el control de calendario.</td>
</tr>
<tr class="odd">
<td>CheckboxDropList</td>
<td>Utiliza el control de lista con las casillas.</td>
</tr>
<tr class="even">
<td>Plegable</td>
<td>Utiliza el control de lista desplegable.</td>
</tr>
<tr class="odd">
<td>MultiLineText</td>
<td>Usa el control de edición de texto de varias líneas.</td>
</tr>
<tr class="even">
<td>MultiValueText</td>
<td>Usa el control de edición de texto de varios valores.</td>
</tr>
<tr class="odd">
<td>Rating</td>
<td>Usa el control de clasificación de 5 estrellas.</td>
</tr>
<tr class="even">
<td>Texto</td>
<td>Usa el control de edición de texto.</td>
</tr>
<tr class="odd">
<td>IconList</td>
<td><strong>Windows 7 y versiones posteriores.</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 

---
description: Especifica qué control se va a usar al editar la propiedad.
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: editControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213d6fba3f03f90e0d5a2702226dd8596462b289
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626821"
---
# <a name="editcontrol"></a>editControl

Especifica qué control se va a usar al editar la propiedad. Solo debe haber un [elemento editControl]() para cada [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Si hay varios elementos, se usa el último. Si no [se proporciona ningún elemento editControl,]() la configuración predeterminada del atributo se aplica a la descripción de la propiedad.

Si es , este elemento se omite porque no se puede editar una <typeInfo isInnate="true"> propiedad innate.

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
<col  />
<col  />
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
<td>Público. Opcional. El valor predeterminado &quot; es Default &quot; . Estos son los valores válidos. 
<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Predeterminado</td>
<td>Predeterminada. Usa el control predeterminado, basado en el <typeInfo type=&quot;&quot;> atributo . A continuación se enumeran los tipos predeterminados. Cualquier otro tipo da como resultado el uso del &quot; &quot; control Texto. 
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
<td>Usa el control de lista con casillas.</td>
</tr>
<tr class="even">
<td>DropList</td>
<td>Usa el control de lista desplegable.</td>
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



 

 

 

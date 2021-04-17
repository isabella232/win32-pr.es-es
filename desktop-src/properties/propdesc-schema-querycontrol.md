---
description: No se admite en Windows 7 y versiones posteriores. Especifica el control que se va a usar en el generador de consultas.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: Consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448b47038f82afb9f860209bfe89eb9e6eecb890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666856"
---
# <a name="querycontrol"></a>Consulta

No se admite en Windows 7 y versiones posteriores. Especifica el control que se va a usar en el generador de consultas. Solo debe haber un elemento [consulta]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .

Si hay varios elementos, se usa el último. Si no se proporciona ningún elemento [consulta]() , los valores de atributo predeterminados se aplican a la descripción de la propiedad.

## <a name="syntax"></a>Sintaxis


```
<!-- queryControl -->
<xs:element name="queryControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="NumericText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
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
<th>ConditionType</th>
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
<td>Número o tamaño</td>
<td>NumericText</td>
</tr>
<tr class="even">
<td>Número o tamaño (enumeración)</td>
<td>List</td>
</tr>
<tr class="odd">
<td>DateTime</td>
<td>Calendario</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Boolean</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Utiliza el control booleano.</td>
</tr>
<tr class="odd">
<td>Calendario</td>
<td>Usa el control de calendario desplegable.</td>
</tr>
<tr class="even">
<td>CheckboxDropList</td>
<td>Utiliza el control de lista con las casillas.</td>
</tr>
<tr class="odd">
<td>Plegable</td>
<td>Utiliza el control de lista desplegable.</td>
</tr>
<tr class="even">
<td>MultiValueText</td>
<td>Usa el control de edición de texto de varios valores.</td>
</tr>
<tr class="odd">
<td>NumericText</td>
<td>Usa el control de edición de texto numérico.</td>
</tr>
<tr class="even">
<td>Rating</td>
<td>Usa el control de clasificación de 5 estrellas.</td>
</tr>
<tr class="odd">
<td>Texto</td>
<td>Usa el control de edición de texto.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 

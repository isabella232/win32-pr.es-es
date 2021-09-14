---
description: No se admite en Windows 7 y versiones posteriores. Especifica qué control se va a usar en el generador de consultas.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: queryControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3652a46d403bc258226de5a48f34ae16960ff517
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262980"
---
# <a name="querycontrol"></a>queryControl

No se admite en Windows 7 y versiones posteriores. Especifica qué control se va a usar en el generador de consultas. Solo debe haber un [elemento queryControl]() para cada [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Si hay varios elementos, se usa el último. Si no se proporciona ningún elemento [queryControl,]() la configuración de atributo predeterminada se aplica a la descripción de la propiedad.

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
<td>Público. Opcional. El valor predeterminado &quot; es &quot; Default. Estos son los valores válidos. 
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
<td>Valor predeterminado</td>
<td>Predeterminada. Usa el control predeterminado, basado en el <typeInfo type=&quot;&quot;> atributo . Los tipos predeterminados se enumeran a continuación. Cualquier otro tipo da como resultado el uso del &quot; &quot; control Texto. 
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
<td>Usa el control booleano .</td>
</tr>
<tr class="odd">
<td>Calendario</td>
<td>Usa el control de calendario desplegable.</td>
</tr>
<tr class="even">
<td>CheckboxDropList</td>
<td>Usa el control de lista con casillas.</td>
</tr>
<tr class="odd">
<td>DropList</td>
<td>Usa el control de lista desplegable.</td>
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



 

 

 

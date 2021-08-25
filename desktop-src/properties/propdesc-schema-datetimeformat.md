---
description: Especifica cómo IPropertyDescription::FormatForDisplay debe dar formato al valor de la propiedad como una cadena. Esto solo es aplicable si <displayInfo displayType=&\#0034;DateTime&\#0034;> .
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950f10106d7850f4a5b58aeb165e8cb4cc9ffcd4
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629177"
---
# <a name="datetimeformat"></a>dateTimeFormat

Especifica cómo [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) debe dar formato al valor de la propiedad como una cadena. Esto solo es aplicable si <displayInfo displayType="DateTime"> . Solo debe haber un [elemento dateTimeFormat]() para cada [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Si hay varios elementos, se usa el último. Si no [se proporciona ningún elemento dateTimeFormat,]() la configuración de atributo predeterminada se aplica a la descripción de la propiedad.

## <a name="syntax"></a>Sintaxis


```
      <!-- dateTimeFormat -->
      <xs:element name="dateTimeFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Month"/>
                <xs:enumeration value="YearMonth"/>
                <xs:enumeration value="Year"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatTimeAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortTime"/>
                <xs:enumeration value="LongTime"/>
                <xs:enumeration value="HideTime"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDateAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="ShortDate"/>
                <xs:enumeration value="LongDate"/>
                <xs:enumeration value="HideDate"/>
                <xs:enumeration value="RelativeShortDate"/>
                <xs:enumeration value="RelativeLongDate"/>
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
<td>formatAs</td>
<td>Público. Opcional. El valor predeterminado &quot; es &quot; General. Estos son los valores válidos. 
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>General</td>
<td>Predeterminada. Da formato al valor de fecha y hora <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>mediante SHFormatDateTime.</strong></a> Use los <em>atributos formatTimeAs</em> <em>y formatDateAs</em> para especificar cómo se formatea la hora y la fecha. Requiere que el tipo de propiedad sea DateTime.</td>
</tr>
<tr class="even">
<td>Month (Mes)</td>
<td>Da formato al valor como uno de los meses del año. Requiere que el tipo de propiedad sea Int32. El valor debe almacenarse como un valor numérico con 1 que represente el primer mes del año.</td>
</tr>
<tr class="odd">
<td>YearMonth</td>
<td>Da formato al valor &quot; como Año - Mes &quot; . Requiere que el tipo de propiedad sea Int32. El valor debe almacenarse de forma que los dos bytes más altos especifiquen el año y los dos bytes inferiores especifiquen el mes.</td>
</tr>
<tr class="even">
<td>Year</td>
<td>Da formato al valor como una cadena simple.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formatTimeAs</td>
<td>Público. Opcional. El valor predeterminado &quot; es &quot; ShortTime. Especifica el formato en el que se va a mostrar la hora. Se aplica cuando <strong>formatAs= &quot; General &quot; </strong>. Estos son los valores válidos. 
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShortTime</td>
<td>Predeterminada. Muestre la hora como &quot; 7:48 p. &quot; m.</td>
</tr>
<tr class="even">
<td>Largo</td>
<td>Muestre la hora como &quot; 7:48:33 p. &quot; m.</td>
</tr>
<tr class="odd">
<td>HideTime</td>
<td>No muestre la parte de hora de la fecha.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>formatDateAs</td>
<td>Público. Opcional. El valor predeterminado &quot; es &quot; ShortDate. Especifica el formato en el que se va a mostrar la fecha. Se aplica cuando <strong>formatAs= &quot; General &quot; </strong>. Estos son los valores válidos. 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Ejemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShortDate</td>
<td>Predeterminada. Muestre la fecha como &quot; 5/13/59 &quot; .</td>
</tr>
<tr class="even">
<td>LongDate</td>
<td>Muestre la fecha como &quot; miércoles, 13 de mayo de 1959. &quot;</td>
</tr>
<tr class="odd">
<td>HideDate</td>
<td>No muestre la parte de la fecha.</td>
</tr>
<tr class="even">
<td>RelativeShortDate</td>
<td>Muestre la fecha como &quot; &quot; ShortDate, pero use descripciones relativas, como &quot; &quot; ayer, siempre que sea posible.</td>
</tr>
<tr class="odd">
<td>RelativeLongDate</td>
<td>Muestre la fecha como &quot; &quot; LongDate, pero use descripciones relativas, como &quot; &quot; ayer, siempre que sea posible.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 

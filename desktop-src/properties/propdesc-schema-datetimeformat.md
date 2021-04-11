---
description: 'Especifica cómo IPropertyDescription:: FormatForDisplay debe formatear el valor de la propiedad como una cadena. Esto solo es aplicable si <displayInfo displayType=&\#0034;DateTime&\#0034;> .'
ms.assetid: c290fb2e-ef5b-4dea-ba42-7c9e273a89dc
title: dateTimeFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091898f77f4dcc37bbe65515f8606104a4d968bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276205"
---
# <a name="datetimeformat"></a>dateTimeFormat

Especifica cómo [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) debe formatear el valor de la propiedad como una cadena. Esto solo es aplicable si <displayInfo displayType="DateTime"> . Solo debe haber un elemento [DateTimeFormat]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .

Si hay varios elementos, se usa el último. Si no se proporciona ningún elemento [DateTimeFormat]() , se aplica la configuración de atributo predeterminada a la descripción de la propiedad.

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
<td>formatas</td>
<td>Público. Opcional. El valor predeterminado es &quot; General &quot; . Estos son los valores válidos. 
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
<td>Predeterminada. Da formato al valor de fecha y hora mediante <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shformatdatetimea"><strong>SHFormatDateTime</strong></a>. Use los atributos <em>formatTimeAs</em> y <em>formatDateAs</em> para especificar cómo se da formato a la fecha y hora. Requiere que el tipo de propiedad sea DateTime.</td>
</tr>
<tr class="even">
<td>Mes</td>
<td>Da formato al valor como uno de los meses del año. Requiere que el tipo de propiedad sea Int32. El valor debe almacenarse como un valor numérico con 1 que representa el primer mes del año.</td>
</tr>
<tr class="odd">
<td>YearMonth</td>
<td>Da formato al valor como &quot; año-mes &quot; . Requiere que el tipo de propiedad sea Int32. El valor se debe almacenar de forma que los dos bytes más altos especifiquen el año y los dos bytes inferiores especifiquen el mes.</td>
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
<td>Público. Opcional. El valor predeterminado es &quot; ShortTime &quot; . Especifica el formato en el que se va a mostrar la hora. Se aplica cuando <strong>formatas &quot; = &quot; General</strong>. Estos son los valores válidos. 
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
<td>Predeterminada. Mostrar la hora como &quot; 7:48 PM &quot; .</td>
</tr>
<tr class="even">
<td>Sido</td>
<td>Mostrar la hora como &quot; 7:48:33 PM &quot; .</td>
</tr>
<tr class="odd">
<td>HideTime</td>
<td>No muestra la parte de hora de la fecha.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>formatDateAs</td>
<td>Público. Opcional. El valor predeterminado es &quot; fechacorta &quot; . Especifica el formato en el que se va a mostrar la fecha. Se aplica cuando <strong>formatas &quot; = &quot; General</strong>. Estos son los valores válidos. 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Ejemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Fechacorta</td>
<td>Predeterminada. Muestra la fecha como &quot; 5/13/59 &quot; .</td>
</tr>
<tr class="even">
<td>LongDate</td>
<td>Mostrar la fecha como el &quot; miércoles, 13 de mayo de 1959 &quot; .</td>
</tr>
<tr class="odd">
<td>HideDate</td>
<td>No mostrar la parte de la fecha.</td>
</tr>
<tr class="even">
<td>RelativeShortDate</td>
<td>Muestre la fecha como &quot; fechacorta &quot; , pero use descripciones relativas, como &quot; ayer &quot; , siempre que sea posible.</td>
</tr>
<tr class="odd">
<td>RelativeLongDate</td>
<td>Muestre la fecha como &quot; LongDate &quot; , pero use descripciones relativas, como &quot; ayer &quot; , siempre que sea posible.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 

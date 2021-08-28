---
description: Especifica cómo IPropertyDescription::FormatForDisplay debe dar formato al valor de la propiedad como una cadena. Esto solo es aplicable si <displayInfo displayType=&\#0034;Number&\#0034;> .
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: numberFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e9db77cc68dab7038a1b5b9c50d49f5381ee948
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883658"
---
# <a name="numberformat"></a>numberFormat

Especifica cómo [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) debe dar formato al valor de la propiedad como una cadena. Esto solo es aplicable si <displayInfo displayType="Number"> . Solo debe haber un [elemento numberFormat]() para cada [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Si hay varios elementos, se usa el último. Si no se proporciona ningún elemento [numberFormat,]() la configuración de atributo predeterminada se aplica a la descripción de la propiedad.

## <a name="syntax"></a>Syntax


```
      <!-- numberFormat -->
      <xs:element name="numberFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="General"/>
                <xs:enumeration value="Percentage"/>
                <xs:enumeration value="ByteSize"/>
                <xs:enumeration value="KBSize"/>
                <xs:enumeration value="SampleSize"/>
                <xs:enumeration value="Bitrate"/>
                <xs:enumeration value="SampleRate"/>
                <xs:enumeration value="FrameRate"/>
                <xs:enumeration value="Pixels"/>
                <xs:enumeration value="DPI"/>
                <xs:enumeration value="Duration"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
          <xs:attribute name="formatDurationAs">
              <xs:restriction base="xs:string">
                <xs:enumeration value="hh:mm"/>
                <xs:enumeration value="hh:mm:ss"/>
                <xs:enumeration value="hh:mm:ss.fff"/>
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
<td>Público. Opcional. El valor predeterminado &quot; es &quot; General. Especifica el formato de presentación. Estos son los valores válidos. 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>General</td>
<td>Predeterminada. Muestra el valor como un número sin formato.</td>
</tr>
<tr class="even">
<td>Porcentaje</td>
<td>Da formato al valor como un porcentaje. Requiere que la propiedad sea UInt32.</td>
</tr>
<tr class="odd">
<td>ByteSize</td>
<td>Da formato al valor como byte, &quot; &quot; KB, &quot; MB o GB según &quot; &quot; &quot; corresponda. Requiere que la propiedad sea UInt64.</td>
</tr>
<tr class="even">
<td>KBSize</td>
<td>Da formato al valor como &quot; &quot; KB, independientemente de cuál sea el valor. Requiere que la propiedad sea UInt64.</td>
</tr>
<tr class="odd">
<td>SampleSize</td>
<td>Da formato al valor como un número de bits. Requiere que la propiedad sea UInt32.</td>
</tr>
<tr class="even">
<td>Velocidad de bits</td>
<td>Da formato al valor en &quot; Kbps &quot; . Requiere que la propiedad sea UInt32. El valor debe almacenarse en &quot; unidades de bits por &quot; segundo.</td>
</tr>
<tr class="odd">
<td>SampleRate</td>
<td>Da formato al valor &quot; en &quot; KHz. Requiere que la propiedad sea UInt32. El valor debe almacenarse en unidades &quot; de &quot; Hertz.</td>
</tr>
<tr class="even">
<td>FrameRate</td>
<td>Da formato al valor en fotogramas/segundo. Requiere que la propiedad sea UInt32. El valor debe almacenarse en &quot; unidades de kilo fotogramas por &quot; segundo.</td>
</tr>
<tr class="odd">
<td>píxeles</td>
<td>Da formato al valor en unidades de píxeles. Requiere que la propiedad sea UInt32.</td>
</tr>
<tr class="even">
<td>ppp</td>
<td>Da formato al valor en puntos por pulgada. Requiere que la propiedad sea UInt32.</td>
</tr>
<tr class="odd">
<td>Duration</td>
<td>Da formato al valor como una duración. Use &lt; formatDurationAs &gt; para especificar el formato de duración. Requiere que la propiedad sea UInt64.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formatDurationAs</td>
<td>Público. Opcional. El valor &quot; predeterminado es hh:mm:ss. &quot; Solo se aplica si <em>formatAs= &quot; Duration &quot; </em>. Requiere que la propiedad sea UInt64. Estos son los valores válidos. 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>hh:mm</td>
<td>Da formato al valor en horas y minutos.</td>
</tr>
<tr class="even">
<td>hh:mm:ss</td>
<td>Predeterminada. Da formato al valor en horas, minutos y segundos.</td>
</tr>
<tr class="odd">
<td>hh:mm:ss.fff</td>
<td>Da formato al valor en horas, minutos, segundos y milisegundos.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 

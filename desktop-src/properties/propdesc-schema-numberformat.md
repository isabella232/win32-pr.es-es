---
description: 'Especifica cómo IPropertyDescription:: FormatForDisplay debe formatear el valor de la propiedad como una cadena. Esto solo es aplicable si <displayInfo displayType=&\#0034;Number&\#0034;> .'
ms.assetid: 9e8cfe5c-e17a-40d6-958f-a1bd1130c699
title: Numérico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6750a9fb4dcf6a7a56c350fccf80241644b956da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666860"
---
# <a name="numberformat"></a>Numérico

Especifica cómo [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) debe formatear el valor de la propiedad como una cadena. Esto solo es aplicable si <displayInfo displayType="Number"> . Solo debe haber un elemento [NumberFormat]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .

Si hay varios elementos, se usa el último. Si no se proporciona ningún elemento [NumberFormat]() , se aplica la configuración de atributo predeterminada a la descripción de la propiedad.

## <a name="syntax"></a>Sintaxis


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
<td>Público. Opcional. El valor predeterminado es &quot; General &quot; . Especifica el formato de presentación. Estos son los valores válidos. 
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
<td>Predeterminada. Muestra el valor como un número sin formato.</td>
</tr>
<tr class="even">
<td>Porcentaje</td>
<td>Da formato al valor como un porcentaje. Requiere que la propiedad sea UInt32.</td>
</tr>
<tr class="odd">
<td>ByteSize</td>
<td>Da formato al valor como un byte, &quot; KB &quot; , &quot; MB &quot; o &quot; GB &quot; según corresponda. Requiere que la propiedad sea UInt64.</td>
</tr>
<tr class="even">
<td>KBSize</td>
<td>Da formato a un valor de &quot; KB &quot; , independientemente de cuál sea el valor. Requiere que la propiedad sea UInt64.</td>
</tr>
<tr class="odd">
<td>SampleSize</td>
<td>Da formato al valor como un número de bits. Requiere que la propiedad sea UInt32.</td>
</tr>
<tr class="even">
<td>Velocidad de bits</td>
<td>Da formato al valor en &quot; Kbps &quot; . Requiere que la propiedad sea UInt32. El valor debe almacenarse en &quot; unidades de bits por segundo &quot; .</td>
</tr>
<tr class="odd">
<td>SampleRate</td>
<td>Da formato al valor en &quot; kHz &quot; . Requiere que la propiedad sea UInt32. El valor debe almacenarse en &quot; unidades de hercios &quot; .</td>
</tr>
<tr class="even">
<td>FrameRate</td>
<td>Da formato al valor en fotogramas/segundo. Requiere que la propiedad sea UInt32. El valor debe almacenarse en &quot; unidades de kilo-fotogramas por segundo &quot; .</td>
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
<td>Da formato al valor como una duración. <formatDurationAs>Se usa para especificar el formato de duración. Requiere que la propiedad sea UInt64.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>formatDurationAs</td>
<td>Público. Opcional. El valor predeterminado es &quot; HH: mm: SS &quot; . Solo se aplica si <em>formatas &quot; = &quot; Duration</em>. Requiere que la propiedad sea UInt64. Estos son los valores válidos. 
<table>
<thead>
<tr class="header">
<th>Value</th>
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
<td>HH: mm: SS. FFF</td>
<td>Da formato al valor en horas, minutos, segundos y milisegundos.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 

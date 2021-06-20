---
description: Especifica cómo IPropertyDescription::FormatForDisplay debe dar formato al valor de la propiedad booleanFormat como una cadena.
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 528458d9c31d54ef43eca8325b1daeef4eee1195
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405968"
---
# <a name="booleanformat"></a>booleanFormat

Especifica cómo [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) debe dar formato al valor de la propiedad como una cadena. Esto solo es aplicable si <displayInfo displayType="String"> . Solo debe haber un elemento [booleanFormat]() para cada [elemento displayInfo.](./propdesc-schema-displayinfo.md)

Si hay varios elementos, se usa el último. Si no se proporciona ningún elemento [booleanFormat,]() la configuración de atributo predeterminada se aplica a la descripción de la propiedad.

## <a name="syntax"></a>Sintaxis


```
      <!-- booleanFormat -->
      <xs:element name="booleanFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="YesNo"/>
                <xs:enumeration value="OnOff"/>
                <xs:enumeration value="TrueFalse"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                   | Elementos secundarios |
|--------------------------------------------------|----------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | Ninguno           |



 

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
<td>formatAs</td>
<td>Público. Opcional. El valor predeterminado &quot; es &quot; SíNo. Estos son los valores válidos. 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SíNo</td>
<td>Predeterminada. Da formato al valor &quot; como Sí &quot; o &quot; &quot; No. Requiere que el tipo de propiedad sea booleano.</td>
</tr>
<tr class="even">
<td>OnOff</td>
<td>Da formato al valor &quot; como On &quot; o &quot; &quot; Off. Requiere que el tipo de propiedad sea booleano.</td>
</tr>
<tr class="odd">
<td>TrueFalse</td>
<td>Da formato al valor como &quot; True &quot; o &quot; &quot; False. Requiere que el tipo de propiedad sea booleano.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 

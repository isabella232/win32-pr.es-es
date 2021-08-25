---
description: Especifica cómo IPropertyDescription::FormatForDisplay debe dar formato al valor de la propiedad booleanFormat como una cadena.
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6ed13194fa18ba558c9c7fbac8fb7cd4317b67
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623721"
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
<td>Público. Opcional. El valor predeterminado &quot; es &quot; SíNo. Estos son los valores válidos. 
<table>
<thead>
<tr class="header">
<th>Value</th>
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



 

 

 

---
description: 'Especifica cómo IPropertyDescription:: FormatForDisplay debe formatear el valor de la propiedad como una cadena. Esto solo es aplicable si <displayInfo displayType=&\#0034;String&\#0034;> .'
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec05a6eedf1734c1d62c0503027810ad05916160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666851"
---
# <a name="stringformat"></a>stringFormat

Especifica cómo [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) debe formatear el valor de la propiedad como una cadena. Esto solo es aplicable si <displayInfo displayType="String"> . Solo debe haber un elemento [StringFormat]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .

Si hay varios elementos, se usa el último. Si no se proporciona ningún elemento [StringFormat]() , se aplica la configuración de atributo predeterminada a la descripción de la propiedad.

## <a name="syntax"></a>Sintaxis


```
<!-- stringFormat -->
<xs:element name="stringFormat"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="formatAs">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="FileName"/>
                    <xs:enumeration value="FilePath"/>
                    <xs:enumeration value="Hyperlink"/>
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
<td>Predeterminada. Devuelve el valor como una cadena sin formato.</td>
</tr>
<tr class="even">
<td>FileName</td>
<td>Da formato al valor como un nombre de archivo. Oculta la extensión según la configuración del usuario. Requiere que el tipo de propiedad sea una cadena.</td>
</tr>
<tr class="odd">
<td>FilePath</td>
<td>Da formato al valor como una ruta de acceso de archivo. Oculta la extensión según la configuración del usuario. Requiere que el tipo de propiedad sea una cadena.</td>
</tr>
<tr class="even">
<td>Hyperlink</td>
<td>Da formato al valor como un hipervínculo.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 

---
description: Especifica el control que se va a usar en el menú de filtro de encabezado.
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: filterControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c0de28eaa349b9a999ba39c1bad47aa01d43d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666863"
---
# <a name="filtercontrol"></a>filterControl

Especifica el control que se va a usar en el menú de filtro de encabezado. Solo debe haber un elemento [filterControl]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .

Si hay varios elementos, se usa el último. Si no se proporciona ningún elemento [filterControl]() , los valores de atributo predeterminados se aplican a la descripción de la propiedad.

## <a name="syntax"></a>Sintaxis


```
      <!-- filterControl -->
      <xs:element name="filterControl"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="control">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="Default"/>
                <xs:enumeration value="Calendar"/>
                <xs:enumeration value="Rating"/>
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
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valor predeterminado</td>
<td>Predeterminada. Utiliza el control predeterminado, basado en el <typeInfo type=&quot;&quot;> atributo. El tipo predeterminado es &quot; DateTime &quot; y el control predeterminado es &quot; Calendar &quot; . Cualquier otro tipo da como resultado un control de filtro especial.</td>
</tr>
<tr class="even">
<td>Calendario</td>
<td>Usa el control de calendario.</td>
</tr>
<tr class="odd">
<td>Rating</td>
<td>Usa el control de clasificación de 5 estrellas.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 

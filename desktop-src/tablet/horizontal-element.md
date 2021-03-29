---
description: Contiene información de formato para las líneas horizontales utilizadas para el diseño de fondo de una nota de Journal.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Elemento horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e380ca35f86ce1012084d31de732cd66c79363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810070"
---
# <a name="horizontal-element"></a>Elemento horizontal

Contiene información de formato para las líneas horizontales utilizadas para el diseño de fondo de una nota de Journal.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos primarios

[**LineLayout**](linelayout-element.md)

## <a name="child-elements"></a>Elementos secundarios

Ninguno.

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Tipo</th>
<th>Obligatorio</th>
<th>Descripción</th>
<th>Valores posibles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Estilo</strong></td>
<td>SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a></td>
<td>Obligatorio</td>
<td>Especifica el tipo de línea que se va a dibujar.</td>
<td><ul>
<li>None</li>
<li>Sólido</li>
<li>Guión</li>
<li>Punto</li>
<li>DashDot</li>
<li>DashDotDot</li>
<li>Doble</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Color</strong></td>
<td>SimpleType de <a href="colortype-simple-type.md"><strong>ColorType</strong></a></td>
<td>Opcionales</td>
<td>Color del elemento.</td>
<td>Valor RGB hexadecimal. Coincide con la siguiente expresión regular: # [0-9-9 a-Z-Z] {6} . Por ejemplo, #4a79B5.<br/></td>
</tr>
<tr class="odd">
<td><strong>SpacingBefore</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Opcionales</td>
<td>Espaciado antes del elemento.</td>
<td>Cualquier entero no negativo.</td>
</tr>
<tr class="even">
<td><strong>SpacingBetween</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Opcionales</td>
<td>Espaciado entre este elemento y los elementos circundantes.</td>
<td>Cualquier entero no negativo.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Información de elemento



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| Tipo de elemento | [**HorizontalType complexType**](horizontaltype-complex-type.md) |
| Espacio de nombres    | urn: schemas-microsoft-com: TabletPC: richink                        |
| Nombre del esquema  | Lector de diario                                                    |



 

 

 





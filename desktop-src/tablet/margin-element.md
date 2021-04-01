---
description: Define las líneas de margen dibujadas en la página.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Margin, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0500d4db165012393cb600c1e118089b68c76695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279167"
---
# <a name="margin-element"></a>Margin, elemento

Define las líneas de margen dibujadas en la página.

## <a name="definition"></a>Definición

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a>Elementos primarios

Ninguno.

## <a name="child-elements"></a>Elementos secundarios

Ninguno...

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
<td><strong>Tipo</strong></td>
<td>SimpleType <a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a></td>
<td>Opcionales</td>
<td>Indica el margen izquierdo o derecho.</td>
<td><ul>
<li>Left</li>
<li>Right</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Espaciado</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Opcionales</td>
<td>Espaciado entre el borde de la página y el margen.</td>
<td>Cualquier entero no negativo.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Información de elemento



|              |                                                           |
|--------------|-----------------------------------------------------------|
| Tipo de elemento | [**MarginType**](margintype-complex-type.md) complexType |
| Espacio de nombres    | urn: schemas-microsoft-com: TabletPC: richink                |
| Nombre del esquema  | Lector de diario                                            |



 

 

 





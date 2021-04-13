---
description: Contiene la información que describe el componente vertical de las líneas del diseño de fondo usado por la nota de Journal. Se utiliza, por ejemplo, cuando la nota tiene líneas de cuadrícula.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Elemento vertical
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 191a9c5cb3190cff9b1e379a68dbfab49ddc25a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360253"
---
# <a name="vertical-element"></a>Elemento vertical

Contiene la información que describe el componente vertical de las líneas del diseño de fondo usado por la nota de Journal. Se utiliza, por ejemplo, cuando la nota tiene líneas de cuadrícula.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
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



|              |                                                               |
|--------------|---------------------------------------------------------------|
| Tipo de elemento | [**VerticalType**](verticaltype-complex-type.md) complexType |
| Espacio de nombres    | urn: schemas-microsoft-com: TabletPC: richink                    |
| Nombre del esquema  | Lector de diario                                                |



 

 

 





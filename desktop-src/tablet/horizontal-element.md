---
description: Contiene información de formato para las líneas horizontales usadas para la papelería en una nota de diario.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Elemento Horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de08008d0243d27f8a8c5f64d6aeac5ddbcc1c
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432387"
---
# <a name="horizontal-element"></a>Elemento Horizontal

Contiene información de formato para las líneas horizontales usadas para la papelería en una nota de diario.

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
<th>Requerido</th>
<th>Descripción</th>
<th>Valores posibles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Estilo</strong></td>
<td><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</td>
<td>Requerido</td>
<td>Especifica el tipo de línea que se va a dibujar.</td>
<td><ul>
<li>Ninguno</li>
<li>Sólido</li>
<li>Guión</li>
<li>Punto</li>
<li>DashDot</li>
<li>DashDotDot</li>
<li>Double</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Color</strong></td>
<td><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</td>
<td>Opcionales</td>
<td>Color del elemento.</td>
<td>Valor RGB hexadecimal. Coincide con la siguiente expresión regular: #[0-9a-zA-Z] {6} . Por ejemplo, #4a79B5.<br/></td>
</tr>
<tr class="odd">
<td><strong>SpacingBefore</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Opcionales</td>
<td>Espaciado delante del elemento.</td>
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



|  Elemento     | Value                                                     |
|--------------|-------------------------------------------------------------------|
| Tipo de elemento | [**HorizontalType complexType**](horizontaltype-complex-type.md) |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink                        |
| Nombre del esquema  | Lector de diario                                                    |



 

 

 





---
description: Contiene información de título sobre la nota de diario.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Elemento Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef687f809aae5c3722cdad84ee63d79c7bfcfb21
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432227"
---
# <a name="title-element"></a>Elemento Title

Contiene información de título sobre la nota de diario.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Diseño de fondo**](stationery-element.md)

## <a name="child-elements"></a>Elementos secundarios

[**TitleArea**](titlearea-element.md)

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
<td><strong>xs:string</strong></td>
<td>Requerido</td>
<td>Especifica el tipo de borde que rodea el título de la nota.</td>
<td><ul>
<li>Ninguno</li>
<li>SolidSquare</li>
<li>OutlineSquare</li>
<li>SolidRoundRect</li>
<li>OutlineRoundRect</li>
<li>SolidRoundRectDottedBaseline</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>DateStyle</strong></td>
<td><strong>xs:string</strong></td>
<td>Requerido</td>
<td>Define si el título incluye una fecha o no.</td>
<td><ul>
<li>Ninguno</li>
<li>Short</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Color</strong></td>
<td><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></td>
<td>Opcionales</td>
<td>Especifica el color del fondo.</td>
<td>Vea <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Información de elemento



| Elemento      | Value                                                   |
|--------------|---------------------------------------------------------|
| Tipo de elemento | [**TitleType**](titletype-complex-type.md) complexType |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink              |
| Nombre del esquema  | Lector de diario                                          |



 

 

 




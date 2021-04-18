---
description: Contiene el fondo de un elemento JournalDocument o un elemento JournalPage.
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Background (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e58a836c7cfd13130779c1cd6b017105bcaa6321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716591"
---
# <a name="background-element"></a>Background (elemento)

Contiene el fondo de un elemento [**JournalDocument**](journaldocument-element.md) o un elemento [**JournalPage**](journalpage-element.md) .

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Diseño de fondo**](stationery-element.md)

## <a name="child-elements"></a>Elementos secundarios

[**Impresión**](image-element.md)

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
<td><strong>xs:string</strong></td>
<td>Obligatorio</td>
<td>Especifica el estilo del fondo.</td>
<td><ul>
<li>None</li>
<li>Sólido</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Color</strong></td>
<td>SimpleType de <a href="colortype-simple-type.md"><strong>ColorType</strong></a></td>
<td>Opcionales</td>
<td>Especifica el color del fondo.</td>
<td>Consulte <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Información de elemento



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| Tipo de elemento | [**BackgroundType**](backgroundtype-complex-type.md) complexType |
| Espacio de nombres    | urn: schemas-microsoft-com: TabletPC: richink                        |
| Nombre del esquema  | Lector de diario                                                    |



 

 

 




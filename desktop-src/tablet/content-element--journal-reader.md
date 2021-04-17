---
description: Incluye el contenido de una página de diario.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Content (elemento) [Journal Reader]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b5a7c9631cd69d38b8db54e2a2f8e69636f7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697380"
---
# <a name="content-element-journal-reader"></a>Lector del diario de elementos de contenido \[\]

Incluye el contenido de una página de diario.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementos primarios

[**JournalPage**](journalpage-element.md)

## <a name="child-elements"></a>Elementos secundarios

[**Groupnode BizTalk**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**Dibujo**](drawing-element.md)

[**Texto**](text-element.md)

[**Impresión**](image-element.md)

[**Marca**](flag-element.md)

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
<th>PossibleValues</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Tipo</strong></td>
<td><a href="contenttype-complex-type.md"><strong>ComplexType de ContentType</strong></a></td>
<td>Obligatorio</td>
<td>Si el tipo es &quot; inerte &quot; , no se puede modificar el contenido.<br/></td>
<td><ul>
<li>Normal</li>
<li>Inert</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Información de elemento



|              |                                                             |
|--------------|-------------------------------------------------------------|
| Tipo de elemento | ComplexType de [**ContentType**](contenttype-complex-type.md) |
| Espacio de nombres    | urn: schemas-microsoft-com: TabletPC: richink                  |
| Nombre del esquema  | Lector de diario                                              |



 

 

 





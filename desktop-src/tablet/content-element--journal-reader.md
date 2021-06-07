---
description: Contiene el contenido de una página De diario.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Elemento Content [Lector de diario]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fec59601a91d63b09c703557b7c6cd28fd11620
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432157"
---
# <a name="content-element-journal-reader"></a>Lector del diario \[ de elementos content\]

Contiene el contenido de una página De diario.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementos primarios

[**JournalPage**](journalpage-element.md)

## <a name="child-elements"></a>Elementos secundarios

[**GroupNode**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**Dibujo**](drawing-element.md)

[**Texto**](text-element.md)

[**Imagen**](image-element.md)

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
<th>Requerido</th>
<th>Descripción</th>
<th>PossibleValues</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Tipo</strong></td>
<td><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></td>
<td>Requerido</td>
<td>Si el tipo es &quot; Inert &quot; , no se puede modificar el contenido.<br/></td>
<td><ul>
<li>Normal</li>
<li>Inerte</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Información de elemento



|  Elemento     | Value                                                     |
|--------------|-------------------------------------------------------------|
| Tipo de elemento | [**ContentType**](contenttype-complex-type.md) complexType |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink                  |
| Nombre del esquema  | Lector de diario                                              |



 

 

 





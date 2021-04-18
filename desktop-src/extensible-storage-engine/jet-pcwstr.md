---
description: 'Más información acerca de: JET_PCWSTR'
title: JET_PCWSTR
TOCTitle: JET_PCWSTR
ms:assetid: fef64bb9-c2e0-4cfb-8138-c98ae6f50952
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294145(v=EXCHG.10)
ms:contentKeyID: 32765759
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51cd0dab17096fb8f7371a01ebabfca3abc595be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707375"
---
# <a name="jet_pcwstr"></a>JET_PCWSTR


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_pcwstr"></a>JET_PCWSTR

El tipo de datos **JET_PCWSTR** contiene una cadena **Unicode** constante terminada en null (char \* ).

**Windows Vista: JET_PCWSTR** se incorpora en Windows Vista.

```cpp
    typedef __nullterminated const WCHAR * JET_PCWSTR;
```

### <a name="data-types"></a>Tipo de datos

JET_PCWSTR

Cadena Unicode constante (Char) terminada en NULL \* .

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


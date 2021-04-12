---
description: 'Más información acerca de: JET_PFNREALLOC función de devolución de llamada'
title: JET_PFNREALLOC función de devolución de llamada
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
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
ms.openlocfilehash: 032c1edcfd18166b79f4c8b2868d53d0b84434d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279400"
---
# <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC función de devolución de llamada


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC función de devolución de llamada

La función JET_PFNREALLOC es una devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) usada por [JetEnumerateColumns](./jetenumeratecolumns-function.md) para asignar memoria para sus búferes de salida.

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a>Parámetros

*pvContext*

El puntero de contexto dado a [JetEnumerateColumns](./jetenumeratecolumns-function.md). Este puntero de contexto se puede usar para transmitir el estado del llamador de [JetEnumerateColumns](./jetenumeratecolumns-function.md) a la implementación de esta devolución de llamada.

*FV*

Si no es NULL, especifica un puntero a un bloque de memoria asignado previamente por esta devolución de llamada. Si es NULL, se asignará un nuevo bloque de memoria del tamaño solicitado.

*CB*

Nuevo tamaño del bloque de memoria en bytes. Si este parámetro es 0 (cero) y se especifica un bloque de memoria, el bloque de memoria se liberará.

### <a name="return-value"></a>Valor devuelto

El sistema puede generar códigos de éxito o error como resultado de una llamada a esta función. Para obtener información sobre cómo devolver estos códigos como valores HRESULT, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código devuelto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Correcto</p></td>
<td><p>Si se especificó un bloque de memoria asignado previamente y se especificó un nuevo tamaño de cero, se liberará ese bloque y se devolverá NULL. Si se especificó un bloque de memoria asignado previamente y se especificó un nuevo tamaño distinto de cero, se devuelve el bloque de memoria reasignado. Si no se especificó ningún bloque de memoria, se devuelve un bloque de memoria recién asignado del tamaño especificado.</p></td>
</tr>
<tr class="even">
<td><p>Error</p></td>
<td><p>Se devolverá NULL. Si se proporcionó un bloque de memoria asignado previamente, ese bloque permanecerá asignado.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JetEnumerateColumns](./jetenumeratecolumns-function.md)

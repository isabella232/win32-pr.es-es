---
description: 'Más información acerca de: JetCloseTable (función)'
title: JetCloseTable función)
TOCTitle: JetCloseTable Function
ms:assetid: c8975145-e48a-4029-9522-1509263019ae
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294087(v=EXCHG.10)
ms:contentKeyID: 32765702
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b38ba9b14c34d20b01b6530f2ed3406e55b3bc3f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104548158"
---
# <a name="jetclosetable-function"></a>JetCloseTable función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetclosetable-function"></a>JetCloseTable función)

La función **JetCloseTable** cierra una tabla abierta en una base de datos. La tabla puede ser una tabla temporal o una tabla normal.

```cpp
JET_ERR JET_API JetCloseTable(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid
);
```

### <a name="parameters"></a>Parámetros

*sesid*

Identifica el contexto de la sesión de base de datos que se utilizará para la llamada API.

*TABLEID*

Identifica la tabla que se va a cerrar.

Establezca *TABLEID* en JET_tableidNil para liberar memoria.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

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
<td><p>JET_errSuccess</p></td>
<td><p>La operación se ha completado correctamente.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Observaciones

Se debe llamar a esta función en todas las tablas abiertas con [JetOpenTable](./jetopentable-function.md).

La excepción a esta regla se produce cuando se llama a [JetOpenTable](./jetopentable-function.md) en una transacción y se revierte la transacción (con [JetRollback](./jetrollback-function.md)). Cuando se revierte una transacción, la tabla se cierra automáticamente. En este caso, es un error cerrar la tabla con **JetCloseTable**.

#### <a name="requirements"></a>Requisitos

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
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTable](./jetopentable-function.md)  
[JetRollback](./jetrollback-function.md)

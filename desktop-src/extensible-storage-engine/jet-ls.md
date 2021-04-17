---
description: 'Más información acerca de: JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
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
ms.openlocfilehash: 3300fd88c0dd1e1fca55722bf58350e28f3c3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716531"
---
# <a name="jet_ls"></a>JET_LS


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_ls"></a>JET_LS

El tipo de datos **JET_LS** contiene un identificador de contexto para el almacenamiento local (LS). Este identificador puede estar asociado a un cursor o una tabla y puede hacer referencia a recursos asignados dinámicamente.

**Windows XP: JET_LS** se presenta en Windows XP.

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a>Tipo de datos

JET_LS

Un valor de JET_LSNil indica un identificador de contexto no válido.

### <a name="remarks"></a>Observaciones

Un identificador de contexto se asocia inicialmente con el tipo de datos **JET_LS** , mediante [JetSetLS](./jetsetls-function.md). El identificador de contexto se puede recuperar desde el tipo de datos **JET_LS** , mediante [JetGetLS](./jetgetls-function.md).

El identificador de contexto se puede desasociar explícitamente del tipo de datos **JET_LS** mediante [JetGetLS](./jetgetls-function.md) con JET_bitLSReset. También se puede desasociar implícitamente el identificador de contexto del tipo de datos **JET_LS** cuando el motor de base de datos libera el objeto subyacente como resultado de una acción directa o indirecta de la aplicación. En el caso implícito, se emite una devolución de llamada en tiempo de ejecución a la aplicación para que pueda limpiar el identificador de contexto. Para obtener más información sobre la desasociación implícita del tipo de datos **JET_LS** , vea [JetSetLS](./jetsetls-function.md).

Las siguientes marcas están asociadas al tipo de datos JET_LS.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Término</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>El identificador de contexto se ha desasociado del objeto.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSCursor</p></td>
<td><p>Establezca o recupere el almacenamiento local asociado a un cursor de tabla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSTable</p></td>
<td><p>Establezca o recupere el almacenamiento local asociado a una tabla.</p></td>
</tr>
<tr class="even">
<td><p>JET_LSNil</p></td>
<td><p>El identificador de contexto no es válido.</p></td>
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
<td><p>Requiere Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JetSetLS](./jetsetls-function.md)  
[JetGetLS](./jetgetls-function.md)

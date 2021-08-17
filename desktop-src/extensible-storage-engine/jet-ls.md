---
description: 'Más información sobre: JET_LS'
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
ms.openlocfilehash: 38ddb306ee6fdcbd1eb792b2c29ca367adc0f4b88cc25dfcbdde22c2638258d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765059"
---
# <a name="jet_ls"></a>JET_LS


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_ls"></a>JET_LS

El **JET_LS** de datos contiene un identificador de contexto para el almacenamiento local (LS). Este identificador podría estar asociado a un cursor o una tabla y podría hacer referencia a recursos asignados dinámicamente.

**Windows XP: JET_LS** se introduce en Windows XP.

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a>Tipo de datos

JET_LS

Un valor de JET_LSNil indica un identificador de contexto no válido.

### <a name="remarks"></a>Comentarios

Un identificador de contexto se asocia inicialmente al **tipo JET_LS** datos, mediante [JetSetLS](./jetsetls-function.md). El identificador de contexto se puede recuperar del **tipo JET_LS** datos, mediante [JetGetLS.](./jetgetls-function.md)

El identificador de contexto se puede desasociar explícitamente del **tipo JET_LS** de datos mediante [JetGetLS](./jetgetls-function.md) con JET_bitLSReset. Como alternativa, el identificador de contexto se puede desasociar implícitamente del tipo de datos **JET_LS** cuando el motor de base de datos libera el objeto subyacente como resultado de una acción directa o indirecta por parte de la aplicación. En el caso implícito, se emite una devolución de llamada en tiempo de ejecución a la aplicación para que pueda limpiar el identificador de contexto. Para obtener más información sobre la desasociación implícita del **tipo JET_LS** datos, vea [JetSetLS](./jetsetls-function.md).

Las marcas siguientes están asociadas al tipo JET_LS datos.

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
<td><p>El identificador de contexto se desasocia del objeto .</p></td>
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
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JetSetLS](./jetsetls-function.md)  
[JetGetLS](./jetgetls-function.md)

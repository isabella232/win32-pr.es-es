---
description: 'Más información acerca de: JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35120be9a26dcbdc8d012cd12c871ddcf8f71555
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105718579"
---
# <a name="jet_err"></a>JET_ERR


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_err"></a>JET_ERR

El tipo de datos **JET_ERR** contiene un [código de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md).

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a>Tipo de datos

JET_ERR

Un valor de cero (correspondiente a JET_errSuccess) indica que la llamada se realizó correctamente. Un valor positivo advierte de una condición no irrecuperable que se produjo durante una llamada correcta de otro modo. Un valor negativo indica que se produjo un error en la llamada.

### <a name="remarks"></a>Observaciones

Para obtener información sobre cómo devolver los errores como valores HRESULT, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md). Para obtener información acerca de las marcas para configurar la base de datos para controlar los errores, consulte [parámetros de control de errores](./error-handling-parameters.md).

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

[Errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md)  
[Códigos de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md)  
[Parámetros de control de errores](./error-handling-parameters.md)

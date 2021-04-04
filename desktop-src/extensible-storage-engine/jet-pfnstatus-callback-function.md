---
description: 'Más información acerca de: JET_PFNSTATUS función de devolución de llamada'
title: JET_PFNSTATUS función de devolución de llamada
TOCTitle: JET_PFNSTATUS Callback Function
ms:assetid: 8b0cf5bf-a4ee-4d8f-8dd7-556c35cd269d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269326(v=EXCHG.10)
ms:contentKeyID: 32765616
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
ms.openlocfilehash: c5f3eb374580dc6bed752900434706b66c6623b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277863"
---
# <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS función de devolución de llamada


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS función de devolución de llamada

La función de devolución de llamada **JET_PFNSTATUS** recibe información sobre el progreso de las operaciones de ejecución prolongada, como la desfragmentación, la copia de seguridad o las operaciones de restauración. Durante estas operaciones, el motor de base de datos llama a esta función de devolución de llamada para proporcionar una actualización en el progreso de la operación.

```cpp
    JET_ERR JET_API JET_PFNSTATUS(
                           JET_SESID  sesid,
                           JET_SNP snp,
                           JET_SNT snt,
                           void* pv
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión de tipo [JET_SESID](./jet-sesid.md) con la que se llamó a la función de ejecución prolongada.

*SNP*

El tipo de operación tal y como se especifica en [JET_SNP](./jet-snp.md). Entre los tipos de operaciones se incluyen reparación, compactación, restauración, copia de seguridad, actualización, limpieza y actualización del formato de registro.

*SNT*

Estado de una operación. Los tipos de estado incluyen Inicio, en curso, finalización o error. El estado se especificará con el tercer parámetro de tipo [JET_SNT](./jet-snt.md).

*FV*

Puntero opcional a una estructura de tipo [JET_SNPROG](./jet-snprog-structure.md).

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de información [JET_ERR](./jet-err.md) con uno de los [códigos de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md). Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

Si se ejecuta correctamente, la operación que emitió la devolución de llamada puede continuar con normalidad. En algunos casos, la devolución de llamada podría devolver una advertencia que influye en esa operación.

En caso de error, la operación que emitió la devolución de llamada podría continuar normalmente o producir un error.

### <a name="remarks"></a>Observaciones

Esta función de devolución de llamada se usará en una notificación de progreso en la que la estructura indicará el estado actual del progreso. Tenga en cuenta que es posible que se llame varias veces a la función de devolución de llamada para el progreso de la operación.

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

[Códigos de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md)  
[Errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md)  
[JET_SESID](./jet-sesid.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)

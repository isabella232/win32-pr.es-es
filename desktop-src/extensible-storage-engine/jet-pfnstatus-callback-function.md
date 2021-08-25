---
description: 'Más información sobre: función JET_PFNSTATUS de devolución de llamada'
title: JET_PFNSTATUS de devolución de llamada
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
ms.openlocfilehash: d10de8491379a3e19217bcdb4a28f3546ebc009f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482921"
---
# <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS de devolución de llamada


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS de devolución de llamada

La **JET_PFNSTATUS** de devolución de llamada recibe información sobre el progreso de las operaciones de ejecución larga, como las operaciones de desfragmentación, copia de seguridad o restauración. Durante estas operaciones, el motor de base de datos llama a esta función de devolución de llamada para proporcionar una actualización sobre el progreso de la operación.

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

Sesión de tipo [JET_SESID](./jet-sesid.md) con la que se llamó a la función de ejecución larga.

*Snp*

Tipo de operación tal como se especifica [en JET_SNP](./jet-snp.md). Los tipos de operaciones incluyen reparación, compactación, restauración, copia de seguridad, actualización, limpieza y actualización del formato de registro.

*Snt*

Estado de una operación. Los tipos de estado incluyen inicio, en curso, finalización o error. El estado se especificará con el tercer parámetro de tipo [JET_SNT](./jet-snt.md).

*Pv*

Puntero opcional a una estructura de tipo [JET_SNPROG](./jet-snprog-structure.md).

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [tipo JET_ERR](./jet-err.md) con uno de los códigos de [error extensibles Storage engine](./extensible-storage-engine-error-codes.md). Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).

Si se ejecuta correctamente, la operación que emitió la devolución de llamada puede continuar con normalidad. En algunos casos, la devolución de llamada podría devolver una advertencia que influye en esa operación.

En caso de error, la operación que emitió la devolución de llamada podría continuar con normalidad o podría producir un error.

### <a name="remarks"></a>Comentarios

Esta función de devolución de llamada se usará en una notificación de progreso en la que la estructura indicará el estado actual del progreso. Tenga en cuenta que la función de devolución de llamada podría llamarse varias veces para el progreso de la operación.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[Códigos de error Storage motor extensibles](./extensible-storage-engine-error-codes.md)  
[Errores extensibles Storage motor de ejecución](./extensible-storage-engine-errors.md)  
[JET_SESID](./jet-sesid.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)

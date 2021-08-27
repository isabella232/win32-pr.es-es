---
description: 'Más información sobre: JetOSSnapshotThaw (Función)'
title: JetOSSnapshotThaw (Función)
TOCTitle: JetOSSnapshotThaw Function
ms:assetid: 3b001113-6299-4082-ab15-461f2e33e996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269229(v=EXCHG.10)
ms:contentKeyID: 32765531
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotThaw
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9be4bcff435fe30186b3b7585c79e3066987cc5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479061"
---
# <a name="jetossnapshotthaw-function"></a>JetOSSnapshotThaw (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetossnapshotthaw-function"></a>JetOSSnapshotThaw (Función)

La **función JetOSSnapshotThaw** notifica al motor que puede reanudar las operaciones normales de E/S después de un período de inmovilización y una instantánea correcta.

**Windows XP:****JetOSSnapshotThaw** se presenta en Windows XP.  

```cpp
    JET_ERR JET_API JetOSSnapshotThaw(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*snapId*

Identificador de la sesión de instantánea.

*grbit*

Este parámetro está reservado para uso futuro y el único valor válido admitido es 0.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInvalidParameter</p> | <p>La sesión de instantánea no es válida o <em>el parámetro grbit</em> no es válido.</p> | 
| <p>JET_errOSSnapshotTimeOut</p> | <p>La sesión de instantánea tenía un tiempo de espera interno antes de que se produjese esta llamada. Por lo tanto, las operaciones de E/S han vuelto a la normalidad antes de realizar esta llamada.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>El identificador de la sesión de instantánea no es válido.</p> | 



Si esta función se realiza correctamente, finaliza una sesión de instantánea y se reanuda el comportamiento normal del motor. Más adelante se puede iniciar una nueva sesión de instantáneas.

Si se produce un error en esta función, finaliza la sesión de instantánea actual, pero la inmovilización de las E/S durante el período de instantánea no se respeta internamente.

#### <a name="remarks"></a>Comentarios

Las entradas del registro de eventos se generarán para los distintos pasos de la instantánea.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)

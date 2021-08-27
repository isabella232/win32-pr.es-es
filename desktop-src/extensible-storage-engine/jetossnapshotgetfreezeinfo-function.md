---
description: 'Más información sobre: JetOSSnapshotGetFreezeInfo (Función)'
title: JetOSSnapshotGetFreezeInfo (Función)
TOCTitle: JetOSSnapshotGetFreezeInfo Function
ms:assetid: b94eaf91-7407-4c62-ab1e-3249ad076c1a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294070(v=EXCHG.10)
ms:contentKeyID: 32765685
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotGetFreezeInfo
- JetOSSnapshotGetFreezeInfoA
- JetOSSnapshotGetFreezeInfoW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e737d6fe31dde43eeba7526e740ec096db20abc9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466212"
---
# <a name="jetossnapshotgetfreezeinfo-function"></a>JetOSSnapshotGetFreezeInfo (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetossnapshotgetfreezeinfo-function"></a>JetOSSnapshotGetFreezeInfo (Función)

La **función JetOSSnapshotGetFreezeInfo** recupera la lista de instancias y bases de datos que forman parte de la sesión de instantáneas en un momento dado.

**Windows Vista:****JetOSSnapshotGetFreezeInfo** se presenta en Windows Vista.  

```cpp
    JET_ERR JET_API JetOSSnapshotGetFreezeInfo(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*snapId*

Identificador de la sesión de instantánea que se va a iniciar.

*pcInstanceInfo*

Número de instancias que se ejecutan actualmente que forman parte de la sesión de instantáneas.

*paInstanceInfo*

Matriz de estructuras, una para cada instancia en ejecución, que describe la instancia y las bases de datos que forman parte de ella.

*grbit*

Opciones para esta llamada. Este parámetro se reserva para uso futuro. El único valor válido es 0 (cero).

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Error en la función debido a una condición de memoria fuera de memoria.</p> | 
| <p>JET_errInvalidParameter</p> | <p><em>pcInstanceInfo</em> o <em>paInstanceInfo</em> es <strong>NULL.</strong></p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>El identificador de la sesión de instantánea no es válido.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Una sesión de instantánea no está en curso.</p> | 



Si esta función se realiza correctamente, la información de la instancia se rellena correctamente y se debe liberar más adelante llamando a [JetFreeBuffer](./jetfreebuffer-function.md) con el puntero a la matriz de información de instancia que se devolvió.

Si se produce un error en esta función, no se produce ningún cambio en el estado del motor.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) y <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[Parámetros de control de errores](./error-handling-parameters.md)  
[Errores extensibles Storage motor de datos](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)

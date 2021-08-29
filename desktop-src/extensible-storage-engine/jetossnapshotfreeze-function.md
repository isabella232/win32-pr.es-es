---
description: 'Más información sobre: JetOSSnapshotFreeze (Función)'
title: Función JetOSSnapshotFreeze
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d133f0bc66da7c4f249676dc46ecbf92f2677aa6
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988478"
---
# <a name="jetossnapshotfreeze-function"></a>Función JetOSSnapshotFreeze


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetossnapshotfreeze-function"></a>Función JetOSSnapshotFreeze

La **función JetOSSnapshotFreeze** inicia una instantánea. Mientras la instantánea está en curso, el motor no puede realizar ninguna actividad de escritura en disco.

**Windows XP:****JetOSSnapshotFreeze** se introdujo en Windows XP.  

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*snapId*

Identificador de la sesión de instantánea.

*pcInstanceInfo*

Número de instancias que se ejecutan actualmente en el motor que forman parte de la sesión de instantáneas.

*paInstanceInfo*

Matriz de estructuras, una para cada instancia en ejecución que forma parte de la sesión de instantánea, que describe la instancia y las bases de datos que forman parte de ella.

*grbit*

Opciones de esta llamada. Este parámetro está reservado para uso futuro y el único valor válido admitido es 0.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Los punteros proporcionados para los parámetros de salida son NULL, la sesión de instantánea no es válida o el <em>parámetro grbit</em> no es válido.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>La sesión de instantánea no está en el estado adecuado para iniciar una inmovilización (por ejemplo, una inmovilización anterior no se pudo realizar en esta sesión).</p> | 
| <p>JET_errOSSnapshotNotAllowed</p> | <p>El motor no está en un estado en el que se puede realizar una instantánea. Una o varias copias de seguridad de streaming ya están en curso o una o varias instancias están pasando por pasos de recuperación o terminación.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>El identificador de la sesión de instantánea no es válido.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Error de la función debido a una condición de memoria fuera de memoria.</p> | 
| <p>JET_errOutOfThreads</p> | <p>Error en la función porque no se pudo iniciar un nuevo subproceso que está realizando la inmovilización.</p> | 



Si esta función se realiza correctamente, no habrá ninguna E/S de escritura emitida para los archivos de base de datos ni para los archivos de registro que forman parte de instancias inmovilizadas. Además, la información de instancia se rellenará correctamente y se debe liberar más adelante mediante una llamada a [JetFreeBuffer](./jetfreebuffer-function.md) con el puntero a la matriz de información de instancia que se devolvió.

Si se produce un error en esta función, el motor seguirá ejecutándose con normalidad con las E/S que se producen como de costumbre. No es necesario llamar a [JetOSSnapshotThaw si](./jetossnapshotthaw-function.md) se produce un error en la inmovilización. Además, la información de la instancia no se rellenará, por lo que no es necesario liberar este recurso.

#### <a name="remarks"></a>Observaciones

Durante el período de inmovilización, no habrá ninguna E/S de escritura emitida para las bases de datos adjuntas o los registros de transacciones, aunque es posible que haya E/S de escritura emitidas en las bases de datos temporales o los archivos de streaming.

El estado en el que las bases de datos y los archivos de registro estarán durante la inmovilización (el estado en el que los archivos estarían en una imagen de instantánea de volumen) será tal que será posible una recuperación normal si esos archivos se restauran más adelante.

Dado que no hay ninguna operación de escritura durante el período de inmovilización, es posible que las llamadas API normales al motor se detendrán durante ese intervalo. La aplicación cliente debe ser capaz de controlar las llamadas API que pueden tardar más tiempo en normalizarse si se produce una inmovilización.

Debido a los posibles efectos descritos anteriormente, hay un tiempo de espera interno después del cual la sesión de instantáneas detendrá la fase de inmovilización incluso si no se llamó a las API que realizaron la descongelización o anulación. El valor del tiempo de espera se puede cambiar mediante el [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) parámetro del sistema. Tenga en cuenta que el intervalo de inmovilización típico está en el intervalo de 10 segundos con el tiempo de espera predeterminado en torno a 60 segundos.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetOSSnapshotFreezeW</strong> (Unicode) y <strong>JetOSSnapshotFreezeA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)

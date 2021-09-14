---
description: 'Más información sobre: JetOSSnapshotPrepare (Función)'
title: Función JetOSSnapshotPrepare
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c667ec1a4e78972a941eb42dd88649e39d133a86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126882740"
---
# <a name="jetossnapshotprepare-function"></a>Función JetOSSnapshotPrepare


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetossnapshotprepare-function"></a>Función JetOSSnapshotPrepare

La **función JetOSSnapshotPrepare** comienza los preparativos para una sesión de instantánea. Una sesión de instantánea es un breve intervalo de tiempo en el que el motor no emite ninguna E/S de escritura en el disco, de modo que el motor pueda participar en una sesión de instantáneas de volumen (cuando está controlado por un escritor de instantáneas).

**Windows XP:****JetOSSnapshotPrepare** se introduce en Windows XP.  

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*psnapId*

Identificador de la sesión de instantánea que se va a iniciar.

*grbit*

Opciones para esta llamada. Este parámetro puede tener una combinación de los valores siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>0</p> | <p>Instantánea normal.</p> | 
| <p>JET_bitIncrementalSnapshot</p> | <p>Solo se tomarán los archivos de registro.</p> | 
| <p>JET_bitCopySnapshot</p> | <p>Instantánea de copia (normal o incremental) sin truncamiento del registro.</p> | 
| <p>JET_bitContinueAfterThaw</p> | <p>La sesión de instantánea se produce después <a href="gg269229(v=exchg.10).md">de JetOSSnapshotThaw</a> y requerirá una llamada a la función <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd.</a></p> | 
| <p>JET_bitExplicitPrepare</p> | <p>No se preparará ninguna instancia de forma predeterminada.</p><p><strong>Windows 7:</strong>  JET_bitExplicitPrepare se introdujo en Windows 7.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInvalidParameter</p> | <p>El puntero de identificador de instantánea es NULL o <em>el parámetro grbit</em> no es válido.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Una sesión de instantáneas ya está en curso y la operación no puede tener más de una sesión de instantáneas en un momento dado.</p> | 



Si esta función se realiza correctamente, una sesión de instantánea podrá iniciarse en cualquier momento con la fase de inmovilización de E/S. Se devolverá el identificador de la sesión y se debe usar en las llamadas posteriores para la sesión de instantánea.

Las instancias en ejecución del motor ahora se considerarán parte de la sesión de instantáneas.

**Windows Vista:**  Para especificar un subconjunto diferente de instancias, se puede llamar a [JetOSSnapshotPrepareInstance.](./jetossnapshotprepareinstance-function.md)

La llamada de secuencia de API normal es: **JetOSSnapshotPrepare**, seguida opcionalmente de una o varias llamadas a [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)y, a continuación, seguida de [JetOSSnapshotFreeze.](./jetossnapshotfreeze-function.md) Una vez iniciada la inmovilización, se puede finalizar [con JetOSSnapshotThaw](./jetossnapshotthaw-function.md). En cualquier momento después de la preparación, la sesión de instantánea se puede finalizar repentinamente [con JetOSSnapshotAbort.](./jetossnapshotabort-function.md)

Si JET_bitContinueAfterThaw se especifica después de [JetOSSnapshotThaw](./jetossnapshotthaw-function.md), la sesión de instantánea permanecerá (aunque se reanudará la E/S). Esto habilitará una comprobación de la instantánea y, si es necesario, habilitará el truncamiento del registro [mediante JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) y requerirá una llamada a [JetOSSnapshotEnd](./jetossnapshotend-function.md).

Si se produce un error en esta función, no se produce ningún cambio en el estado del motor.

#### <a name="remarks"></a>Observaciones

Las entradas del registro de eventos se generarán para los distintos pasos de la instantánea.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)  
[JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md)

---
description: 'Más información sobre: JetEndExternalBackup (Función)'
title: Función JetEndExternalBackup
TOCTitle: JetEndExternalBackup Function
ms:assetid: 058f903b-14b7-44b3-9ec7-7c05c9ec6363
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269176(v=EXCHG.10)
ms:contentKeyID: 32765479
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec39e95bb3dae2b77d52df40bcc416cef3d13eab
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983748"
---
# <a name="jetendexternalbackup-function"></a>Función JetEndExternalBackup


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetendexternalbackup-function"></a>Función JetEndExternalBackup

La **función JetEndExternalBackup** finaliza una sesión de copia de seguridad externa. Esta función es el último elemento de API de una serie de elementos de API a los que se debe llamar para ejecutar una copia de seguridad correcta en línea (no basada en VSS).

```cpp
    JET_ERR JET_API JetEndExternalBackup(void);
```

### <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errNotInitialized</p> | <p>La operación no se puede completar porque todavía no se ha inicializado la instancia asociada a la sesión.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p><strong>Windows XP:</strong> Este valor devuelto se introduce en Windows XP</p><p>La operación no se puede completar porque la instancia asociada a la sesión encontró un error irrevocado que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errNoBackup</p> | <p>Error en la operación porque no hay ninguna copia de seguridad externa en curso.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p><strong>Windows Server 2003:</strong> Este valor devuelto se introduce en Windows Server 2003.</p><p>Error en la operación porque una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>anuló la copia de seguridad externa actual.</p> | 
| <p>errBackupAbortByCaller</p> | <p><strong>Windows XP:</strong> Este valor devuelto se introduce en Windows XP.</p><p>El autor de la llamada finalizó una copia de seguridad en medio de la secuencia de copia de seguridad sin indicar la intención <a href="gg294067(v=exchg.10).md">con JetStopBackup</a>. Este error es el resultado de un error en el cliente de copia de seguridad en Windows Server 2003 y versiones posteriores. En Windows XP, este error se devuelve para una terminación intencionada de la secuencia de copia de seguridad externa.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Error en la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad Windows 2000) donde solo se admite una instancia, cuando de hecho ya existen varias instancias.</p> | 



Si esta función se realiza correctamente, la copia de seguridad externa se ha hecho correctamente. Correcto indica que todos los archivos (por ejemplo, bases de datos y registros) que son adecuados para el tipo de copia de seguridad (especificado en [JetBeginExternalBackup)](./jetbeginexternalbackup-function.md)se recuperaron del motor de copia de seguridad. Los archivos de copia de seguridad se pueden recuperar con recuperación en disco[(JetExternalRestore).](./jetexternalrestore-function.md)

Si se produce un error en esta función, normalmente finaliza la copia de seguridad externa. Un error significa que la copia de seguridad no es válida debido a un cliente o a un error de uso de la aplicación. Es importante comprobar el código de retorno de esta API para comprobar que la secuencia de copia de seguridad se ha realizado correctamente.

#### <a name="remarks"></a>Observaciones

Si el motor está configurado para registrar eventos, se registra un evento para indicar la resolución de la copia de seguridad externa.

Si la secuencia de copia de seguridad no se completa en orden y con una llamada correcta a **JetEndExternalBackup,** las copias de seguridad incrementales posteriores pueden contener más datos de los previstos por la aplicación.

Para obtener más información sobre la secuencia de API de copia de seguridad externa, [vea JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

Antes Windows Vista, si no se ha realizado el truncamiento del registro, el motor consideró que la copia de seguridad era una copia de seguridad de copia. Sin embargo, la copia de seguridad puede ser una copia de seguridad normal para la que no se ha realizado el truncamiento (por ejemplo, si hay bases de datos desasociadas). La JET_bitBackupTruncateDone se puede usar para informar al motor sobre esto y permitir las modificaciones de encabezado de base de datos adecuadas.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[Parámetros de control de errores](./error-handling-parameters.md)  
[Errores extensibles Storage motor de ejecución](./extensible-storage-engine-errors.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JET_ERR](./jet-err.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)

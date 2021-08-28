---
description: 'Más información sobre: JetEndExternalBackupInstance (Función)'
title: JetEndExternalBackupInstance (Función)
TOCTitle: JetEndExternalBackupInstance Function
ms:assetid: 2256f63e-91f5-44ad-b67e-506dd71ffa94
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269204(v=EXCHG.10)
ms:contentKeyID: 32765507
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f82af0be3185db36498d9a5888da190e92314184
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479181"
---
# <a name="jetendexternalbackupinstance-function"></a>JetEndExternalBackupInstance (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetendexternalbackupinstance-function"></a>JetEndExternalBackupInstance (Función)

La **función JetEndExternalBackupInstance** finaliza una sesión de copia de seguridad externa. Esta API es la última API de una serie de API a las que se debe llamar para ejecutar una copia de seguridad correcta en línea (no basada en VSS).

**Windows XP: JetEndExternalBackupInstance** se introdujo en Windows XP.

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parámetros

*Ejemplo*

Instancia de que se va a usar para esta llamada.

**Windows 2000:** Por Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia. En este caso, el uso de esta instancia global está implícito.

**Windows XP:** Para Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (Windows modo de compatibilidad 2000) donde solo se admite una instancia. De lo contrario, se producirá un error en la operación JET_errRunningInMultiInstanceMode.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBackupAbortByCaller</p> | <p><strong>Windows XP:</strong> Este valor devuelto se introduce en Windows XP.</p><p>El autor de la llamada finalizó una copia de seguridad en medio de la secuencia de copia de seguridad sin indicar la intención <a href="gg294067(v=exchg.10).md">con JetStopBackup</a>. Este error es el resultado de un error en el cliente de copia de seguridad en Windows Server 2003 y versiones posteriores. En Windows XP, este error se devuelve para una terminación intencionada de la secuencia de copia de seguridad externa.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p><strong>Windows Server 2003:</strong> Este valor devuelto se introduce en Windows Server 2003.</p><p>Error en la operación porque una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>anuló la copia de seguridad externa actual.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p><strong>Windows XP:</strong> Este valor devuelto se introduce en Windows XP.</p><p>La operación no se puede completar porque la instancia de asociada a la sesión encontró un error irrevocado que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p> | 
| <p>JET_errNoBackup</p> | <p>Error en la operación porque no hay ninguna copia de seguridad externa en curso.</p> | 
| <p>JET_errNotInitialized</p> | <p>La operación no se puede completar porque todavía no se ha inicializado la instancia asociada a la sesión.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Error en la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad Windows 2000) donde solo se admite una instancia, cuando de hecho ya existen varias instancias.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque se está cerrando la instancia asociada a la sesión.</p> | 



Si la función se realiza correctamente, la copia de seguridad externa se ha hecho correctamente. Correcto indica que todos los archivos (por ejemplo, bases de datos y registros) que son adecuados para el tipo de copia de seguridad (especificado en [JetBeginExternalBackup)](./jetbeginexternalbackup-function.md)se recuperaron del motor de copia de seguridad. Los archivos de copia de seguridad se pueden recuperar con recuperación en disco[(JetExternalRestore).](./jetexternalrestore-function.md)

Si se produce un error en esta función, normalmente finaliza la copia de seguridad externa. Un error significa que la copia de seguridad no es válida debido a un cliente o a un error de uso de la aplicación. Es importante comprobar el código de retorno de esta API para comprobar que la secuencia de copia de seguridad se ha realizado correctamente.

#### <a name="remarks"></a>Comentarios

Si el motor está configurado para registrar eventos, se registra un evento para indicar la resolución de la copia de seguridad externa.

Si la secuencia de copia de seguridad no se completa en orden y con una llamada correcta a [JetEndExternalBackup,](./jetendexternalbackup-function.md)las copias de seguridad incrementales posteriores pueden contener más datos de los previstos por la aplicación.

Para obtener más información sobre la secuencia de API de copia de seguridad externa, [vea JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

Antes Windows Vista, si no se realizaba el truncamiento del registro, el motor consideró que la copia de seguridad era una copia de seguridad de copia. Sin embargo, la copia de seguridad puede ser una copia de seguridad normal para la que no se ha realizado el truncamiento (por ejemplo, si hay bases de datos desasociadas). La JET_bitBackupTruncateDone se puede usar para informar al motor sobre esto y permitir las modificaciones de encabezado de base de datos adecuadas.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[Parámetros de control de errores](./error-handling-parameters.md)  
[Errores extensibles Storage motor de datos](./extensible-storage-engine-errors.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JET_ERR](./jet-err.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)

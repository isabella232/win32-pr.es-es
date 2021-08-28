---
description: 'Más información sobre: JetBeginExternalBackup (Función)'
title: JetBeginExternalBackup (Función)
TOCTitle: JetBeginExternalBackup Function
ms:assetid: 702e6cbf-4648-40f2-b2eb-6194759d4cde
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269292(v=EXCHG.10)
ms:contentKeyID: 32765584
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8d0e47a117c044899a8b078290be622cfecdae91
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482911"
---
# <a name="jetbeginexternalbackup-function"></a>JetBeginExternalBackup (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetbeginexternalbackup-function"></a>JetBeginExternalBackup (Función)

La **función JetBeginExternalBackup** inicia una copia de seguridad externa mientras el motor y la base de datos están en línea y activos. **JetBeginExternalBackup** es el primero de una serie de funciones a las que se debe llamar para ejecutar una copia de seguridad correcta en línea (no basada en VSS).

Se puede usar una copia de seguridad externa para implementar copias de seguridad completas, incrementales o diferenciales.

La copia de seguridad será aproximada, ya que la copia de seguridad será coherente con un único punto en el tiempo en el historial de transacciones, pero no es posible controlar el momento exacto en el tiempo.

```cpp
    JET_ERR JET_API JetBeginExternalBackup(
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*grbit*

Grupo de bits que especifican cero o más de las siguientes opciones.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Esta marca está en desuso. El uso de este bit dará lugar a la JET_errInvalidgrbit se devolverá.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Crea una copia de seguridad incremental en lugar de una copia de seguridad completa. Esto significa que solo se realizará una copia de seguridad de los archivos de registro desde la última copia de seguridad completa o incremental.</p> | 
| <p>JET_bitBackupSnapshot</p> | <p>Reservado para uso futuro. Se define para Windows XP.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Si ya hay una copia de seguridad externa o una copia de seguridad de instantáneas en proceso, se devolverá este error hasta que se llame a <strong>JetBeginExternalBackup</strong> (o a una de las variantes de la misma). ESE solo permite una copia de seguridad en línea a la vez.</p> | 
| <p>JET_errBackupNotAllowedYet</p> | <p>La instancia o el motor de base de datos se encuentra en fase de recuperación o en fase de apagado o finalización.</p> | 
| <p>JET_errCheckpointCorrupt</p> | <p>En una copia de seguridad completa, no se pudo leer el archivo de punto de comprobación o no se pudo comprobar el archivo.</p> | 
| <p>JET_errCheckpointFileNotFound</p> | <p>En una copia de seguridad completa, no se encontró el archivo de punto de comprobación.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>La operación no se puede completar porque la instancia asociada a la sesión ha encontrado un error irrevocado que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong> Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errInvalidBackup</p> | <p>El registro circular está habilitado y el tipo de copia de seguridad especificado JET_bitBackupIncremental. Consulte <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> los errores del <strong>registro de transacciones</strong> para obtener información sobre cómo controlar el registro circular o no circular.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Uno o varios de los <em>miembros grbit</em> no son válidos.</p> | 
| <p>JET_errLoggingDisabled</p> | <p>La recuperación o el registro están deshabilitados. No puede realizar una copia de seguridad en línea si el registro está deshabilitado. Para obtener más información sobre el registro y la recuperación, <a href="gg269235(v=exchg.10).md">vea JET_paramRecovery</a>.</p> | 
| <p>JET_errLogWriteFail</p> | <p>El motor ha dejado de escribir en la unidad de registro, debido a que el registro está lleno o a errores de E/S de disco.</p> | 
| <p>JET_errMissingFullBackup</p> | <p>Se especificó la copia de seguridad incremental (con JET_bitBackupIncremental) y nunca se ha realizado una copia de seguridad completa para una de las bases de datos adjuntas para el conjunto de registro.</p> | 
| <p>JET_errNotInitialized</p> | <p>La operación no se puede completar porque todavía no se ha inicializado la instancia asociada a la sesión.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Error en la operación porque no se pudo asignar suficiente memoria para completarla.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Error en la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad Windows 2000), donde solo se admite una instancia cuando en realidad ya existen varias instancias.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque se está cerrando la instancia asociada a la sesión.</p> | 



Si la función se realiza correctamente, se inicia una copia de seguridad externa y se inicializa el motor de estado de copia de seguridad. Ahora se puede llamar a las API posteriores para completar la secuencia de copia de seguridad externa y transmitir o leer el archivo de base de datos, el archivo de revisión de base de datos (si se admite) y el archivo de registro. Se puede registrar un evento en el que se ha iniciado una copia de seguridad externa.

Si se produce un error en la función, no se iniciará la sesión de copia de seguridad. Si hay otra sesión de copia de seguridad en curso, no se cancelará.

#### <a name="remarks"></a>Comentarios

El proceso de copia de seguridad externo (iniciado por **JetBeginExternalBackup)** está diseñado para permitir una copia de seguridad en línea de transacciones aproximadas de toda la instancia en un dispositivo de destino como una secuencia. La copia de seguridad contendrá todos los archivos de base de datos asociados a la instancia mediante [JetAttachDatabase](./jetattachdatabase-function.md) (para una copia de seguridad completa), seguidos de sus archivos de revisión de base de datos asociados (si se admiten) y, por último, de los archivos de registro de transacciones que se generaron durante el proceso de copia de seguridad. El resultado final será un conjunto de archivos que se pueden restaurar desde la secuencia, posiblemente combinados con los archivos de registro y base de datos existentes y, por último, recuperarse a un estado coherente.

El orden general de las operaciones para una copia de seguridad completa consta de las siguientes llamadas. En primer lugar, **se llama a JetBeginExternalBackup** para iniciar el proceso de copia de seguridad. A [continuación, se llama a JetGetAttachInfo](./jetgetattachinfo-function.md) para obtener la lista de bases de datos adjuntas a la instancia de de la que se debe realizar una copia de seguridad. Para cada una de estas bases de datos, se llama a [JetOpenFile,](./jetopenfile-function.md) seguido de varias llamadas a [JetReadFile](./jetreadfile-function.md) y, a continuación, de una llamada a [JetCloseFile.](./jetclosefile-function.md) A continuación, se llama a [JetGetLogInfo](./jetgetloginfo-function.md) para obtener una lista de los archivos de registro y revisión de base de datos de los que se va a realizar una copia de seguridad. Para cada uno de estos archivos, se realiza otra secuencia de [llamadas a JetOpenFile,](./jetopenfile-function.md) [JetReadFile](./jetreadfile-function.md)y [JetCloseFile.](./jetclosefile-function.md) A continuación, los archivos de registro de transacciones no deseados se eliminan [mediante JetTruncateLog](./jettruncatelog-function.md). Por último, la copia de seguridad finaliza mediante una llamada a [JetEndExternalBackup](./jetendexternalbackup-function.md).

También es posible modificar este conjunto de pasos para realizar una copia de seguridad incremental de la instancia. Una copia de seguridad incremental enumera y hace una copia de seguridad de los archivos de registro. Las copias de seguridad incrementales solo son posibles si el registro circular no está habilitado.

También es posible modificar este conjunto de pasos para permitir que se realicen copias de seguridad diferenciales posteriores de la instancia. Para realizar una copia de seguridad diferencial, no llame a [JetTruncateLog](./jettruncatelog-function.md) en la copia de seguridad completa o incremental anterior. Al no llamar a [JetTruncateLog,](./jettruncatelog-function.md)permite que las copias de seguridad posteriores sean diferenciales con respecto a la última copia de seguridad completa o incremental. Las copias de seguridad diferenciales solo son posibles si el registro circular no está habilitado.

El archivo de revisión de base de datos es un archivo auxiliar especial que se usa para almacenar imágenes de página de base de datos en determinadas circunstancias durante la copia de seguridad. Este archivo debe estar presente en la misma ubicación que la base de datos asociada durante una operación de restauración. Este archivo solo se usa en Windows 2000. Como resultado, cualquier aplicación escrita para funcionar con Windows 2000 y otras versiones debe admitir archivos de revisión de base de datos, si están presentes, pero no debe producirse un error si no están presentes.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetEndExternalBackup](./jetendexternalbackup-function.md)  
[JetEndExternalBackupInstance2](./jetendexternalbackupinstance2-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)

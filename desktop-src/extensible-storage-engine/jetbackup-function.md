---
description: 'Más información sobre: JetBackup (Función)'
title: Función JetBackup
TOCTitle: JetBackup Function
ms:assetid: afff995f-378a-4e67-b522-d5eafcbad57e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294058(v=EXCHG.10)
ms:contentKeyID: 32765673
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupA
- JetBackup
- JetBackupW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3cd4eb8c36e48de9ba2e1d715d7aed585fed34c6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472681"
---
# <a name="jetbackup-function"></a>Función JetBackup


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetbackup-function"></a>Función JetBackup

La **función JetBackup** crea una copia de seguridad de la base de datos mientras la base de datos está en línea. Esta función es principalmente para la compatibilidad con versiones anteriores con Windows 2000 y motores de base de datos anteriores, donde solo se permite una instancia de una base de datos. En este caso, la instancia activa es la instancia de la que se hace una copia de seguridad.

```cpp
    JET_ERR JET_API JetBackup(
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>Parámetros

*szBackupPath*

Directorio donde se almacena la copia de seguridad. Si la ruta de acceso de copia de seguridad es NULL, la función truncará los registros, si es posible.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Crea una copia de seguridad completa de la base de datos. Esto permite conservar una copia de seguridad existente en el mismo directorio si se produce un error en la nueva copia de seguridad.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Crea una copia de seguridad incremental en lugar de una copia de seguridad completa. Esto significa que solo se realizará una copia de seguridad de los archivos de registro desde la última copia de seguridad completa o incremental.</p> | 



*pfnStatus*

Puntero a la [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) de devolución de llamada, que proporciona información de notificación sobre el progreso de la operación de copia de seguridad.

### <a name="return-value"></a>Valor devuelto

La función devuelve uno de [los](./jet-err.md) JET_ERR de error. Los siguientes son los que se devuelven con más comúnmente. (Para obtener una lista completa de los errores de esta API, consulte Códigos de error [extensibles Storage engine).](./extensible-storage-engine-error-codes.md)


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Ya hay una copia de seguridad en curso para la misma instancia. No se permiten varias copias de seguridad al mismo tiempo.</p> | 
| <p>JET_errBackupNotAllowedYet</p> | <p>La instancia aún no está lista para la copia de seguridad, ya que se está inicializando.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>La operación no se puede completar porque la instancia asociada a la sesión ha encontrado un error irrevocado que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong> Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errInvalidBackup</p> | <p>No se permite una copia de seguridad incremental si el registro circular está habilitado.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Las opciones especificadas no son válidas.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Se pasó un parámetro no válido a la API.</p> | 
| <p>JET_errInvalidPath</p> | <p>La ruta de acceso de destino no existe.</p> | 
| <p>JET_errLoggingDisabled</p> | <p>La instancia se ejecuta sin registro. No se permite ninguna copia de seguridad.</p> | 
| <p>JET_errLogReadVerifyFailure</p> | <p>Se produjo un error de comprobación de suma de comprobación en un archivo de registro.</p> | 
| <p>JET_errLogWriteFail</p> | <p>El registro de la instancia es temporal o está deshabilitado permanentemente debido a un error inesperado.</p> | 
| <p>JET_errNotInitialized</p> | <p>La operación no se puede completar porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errReadVerifyFailure</p> | <p>Se produjo un error de comprobación de suma de comprobación en una página de base de datos.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p><strong>Windows XP:</strong> Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque se está cerrando la instancia asociada a la sesión.</p> | 



Si la función se realiza correctamente, todos los archivos necesarios para una restauración hasta el momento de la copia de seguridad se incluirán en el directorio de copia de seguridad. Si se trata de una copia de seguridad completa, los archivos serán los archivos de base de datos y los archivos de registro necesarios para que la base de datos tenga un estado coherente. Si se trata de una copia de seguridad incremental, solo se agregarán archivos de registro a los directorios, pero los archivos ya existentes (bases de datos y archivos de registro), junto con los nuevos archivos de registro, se podrán restaurar para que la base de datos vuelva al estado en el que se encontraba en el momento en que se inició la copia de seguridad.

Como efecto secundario de la copia de seguridad, se truncarán los archivos de registro que ya no son necesarios.

Al mismo tiempo, los encabezados de base de datos se actualizarán con la información cuando se realizó la última copia de seguridad.

Si se produce un error en la función, no habrá ningún archivo en el destino del directorio de copia de seguridad, por lo que no será posible realizar ninguna restauración. Al mismo tiempo, los archivos de registro actuales no se truncarán.

#### <a name="remarks"></a>Comentarios

Los distintos pasos de la copia de seguridad tendrán entradas del registro de eventos generadas, incluidos los nombres de archivo, el truncamiento del registro y el resultado final de la copia de seguridad.

Las copias de seguridad incrementales solo son posibles después de realizar una copia de seguridad completa. Además, las copias de seguridad incrementales solo son posibles si el registro circular está desactivado. Se recomienda que el directorio de copia de seguridad no contenga ningún archivo distinto del utilizado en la copia de seguridad o agregado por una copia de seguridad correcta anterior.

El directorio de copia de seguridad debe existir a menos que se *JET_paramCreatePathIfNotExist* parámetro para la instancia. Para obtener información, vea [Parámetros del sistema](./extensible-storage-engine-system-parameters.md).

La copia de seguridad realizará una comprobación de suma de comprobación en todas las páginas de base de datos usadas y a partir de Windows Server 2003, también en los archivos de registro. Esto ofrece la oportunidad de calcular el estado de la base de datos, incluso para las páginas que no se leen durante las operaciones normales. Si se produce algún daño de este tipo, se producirá un error en la copia de seguridad.

Durante la copia de seguridad, se finalizará el archivo de registro actual y se generará un nuevo registro. De este modo, todos los archivos de registro necesarios pueden ser copias, ya que el registro actual ya no estará en uso.

Se recomienda encarecidamente que la copia de seguridad no se utilice para ningún propósito que no sea la copia de seguridad y restauración en el nivel de motor. Esto minimizará la posibilidad de obtener errores durante las operaciones de copia de seguridad y restauración.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetBackupW</strong> (Unicode) y <strong>JetBackupA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[Archivos extensibles Storage engine](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)

---
description: 'Más información sobre: JetRestore2 (Función)'
title: Función JetRestore2
TOCTitle: JetRestore2 Function
ms:assetid: 7f7fc2e3-727a-43e4-8497-64ff56d92b9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269313(v=EXCHG.10)
ms:contentKeyID: 32765603
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore2
- JetRestore2A
- JetRestore2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 464fbc228acc1d73b50253b2312edd3889289e2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126962756"
---
# <a name="jetrestore2-function"></a>Función JetRestore2


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetrestore2-function"></a>Función JetRestore2

**JetRestore2 restaura y** recupera una copia de seguridad de streaming de una instancia, incluidas todas las bases de datos adjuntas. Esta función es principalmente para la compatibilidad con versiones anteriores con Windows 2000 y motores de base de datos anteriores, donde solo se permite una instancia de una base de datos. En este caso, la instancia activa es la instancia que se restaura.

```cpp
    JET_ERR JET_API JetRestore2(
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Parámetros

*Sz*

Carpeta donde se encuentra la copia de seguridad. La copia de seguridad debe haber sido generada mediante las [API de JetBackup.](./jetbackup-function.md)

*szDest*

Nombre de la carpeta donde se copiarán y recuperarán los archivos de base de datos del conjunto de copia de seguridad. Si se establece en NULL (que es el caso de [jetRestore](./jetrestore-function.md)heredado), los archivos de base de datos se copiarán y recuperarán en su ubicación original.

*pfn*

Puntero opcional a la función a la que se llamará como información de notificación sobre el progreso de la operación de restauración.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>Error en la operación porque el motor ya está inicializado para esta instancia.</p> | 
| <p>JET_errInvalidLogSequence</p> | <p>El conjunto de archivos de registro del conjunto de copia de seguridad y de la ruta de acceso del registro actual no coinciden.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> devolverá este error cuando el motor esté en modo de varias instancias y pinstance haga referencia a una instancia no válida Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidPath</p> | <p>Error en la operación porque algunas de las rutas de acceso proporcionadas no son válidas (la ruta de acceso de copia de seguridad, la ruta de acceso de destino, el registro o la ruta de acceso del sistema para la instancia).</p> | 
| <p>JET_errPageSizeMismatch</p> | <p>Error en la operación porque el motor está configurado para usar un tamaño de página de base de datos (mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para JET_paramDatabasePageSize ) que no coincide con el tamaño de página de la base de datos utilizado para crear los archivos de registro de transacciones o las bases de datos asociadas <a href="gg269337(v=exchg.10).md">a</a>los archivos de registro de transacciones.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Error en la operación porque los parámetros implícitos en modo de instancia única (Windows modo de compatibilidad 2000) y el motor ya está en modo de instancias múltiples.</p> | 



Si se ejecuta correctamente, los archivos de base de datos del conjunto de copia de seguridad se restaurarán en su ubicación y la recuperación se ejecutará de forma que las bases de datos se encontrarán en un estado de coherencia transaccional limpia. La recuperación reproducirá los archivos de registro del conjunto de copia de seguridad y los archivos de registro de la ruta de acceso del registro si estos archivos existen. Esta recuperación dará lugar a cambios en el archivo de punto de comprobación, los archivos de registro de transacciones y las bases de datos a las que hacen referencia esos archivos de registro de transacciones.

En caso de error, la instancia permanece en un estado no inicializado. El estado de los archivos de registro de transacciones y las bases de datos a las que hacen referencia esos archivos de registro de transacciones probablemente se habrán cambiado al intentar inicializar la restauración y recuperar las bases de datos.

#### <a name="remarks"></a>Observaciones

El proceso de recuperación reconstruirá las bases de datos asociadas a la instancia durante la copia de seguridad y guardará los cambios en los archivos de base de datos. El resultado serán bases de datos coherentes con las transacciones. Si es posible, también guardará en la base de datos los cambios realizados desde que se hizo la copia de seguridad hasta el cambio más reciente encontrado en los registros de transacciones. Esto sería posible si los registros de transacciones generados desde que se tomó la copia de seguridad siguen estando presentes en el directorio del registro de transacciones. Tenga en cuenta que si se ha habilitado el registro circular para la instancia, los registros de transacciones generados se reutilizan de forma que la recuperación podrá guardar los cambios que se realizaron hasta el momento de la copia de seguridad. En cualquier caso, este proceso puede tardar bastante tiempo si el número de archivos de registro de transacciones que se va a reproducir en las bases de datos es grande.

Se debe llamar a las funciones de [JetRestore](./jetrestore-function.md) en una instancia antes [de llamar a JetInit](./jetinit-function.md) para esa instancia.

Dado que durante la recuperación se usará un número significativo de páginas de base de datos y registros de transacciones, hay una serie completa de errores que estas funciones pueden devolver. Estos errores pueden ser desde errores temporales de asignación de recursos como Jet_errOutOfMemory a errores que representan daños físicos como JET_errReadVerifyFailure, JET_errLogFileCorrupt o JET_errBadPageLink. Estos errores casi siempre se deben a problemas de hardware y, por tanto, no se pueden evitar. La administración de archivos se manifesta con más frecuencia JET_errMissingLogFile, JET_errAttachedDatabaseMismatch, JET_errDatabaseSharingViolation o JET_errInvalidLogSequence. La aplicación puede evitar estos errores. La aplicación debe tener cuidado de proteger el repositorio de estos archivos de la manipulación por parte de fuerzas externas, como el usuario u otras aplicaciones. Si la aplicación desea destruir una instancia por completo, se deben eliminar todos los archivos asociados a la instancia. Estos incluyen el archivo de punto de comprobación, los archivos de registro de transacciones y los archivos de base de datos asociados a la instancia.

Los distintos pasos de la recuperación tendrán entradas del registro de eventos generadas, incluido el progreso de la reproducción del registro de transacciones y el resultado final de la restauración.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa <strong>como JetRestore2W</strong> (Unicode) y <strong>JetRestore2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBackup](./jetbackup-function.md)  
[JetBackupInstance](./jetbackupinstance-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)

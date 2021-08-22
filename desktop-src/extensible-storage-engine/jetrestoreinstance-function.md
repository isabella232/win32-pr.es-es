---
description: 'Más información sobre: JetRestoreInstance (Función)'
title: Función JetRestoreInstance
TOCTitle: JetRestoreInstance Function
ms:assetid: 7ba2b6ee-96f5-44c5-9842-5e58580f60f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269306(v=EXCHG.10)
ms:contentKeyID: 32765597
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestoreInstanceW
- JetRestoreInstance
- JetRestoreInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 638ec789417dcd35e63758263227245f6c22d65b3c7bb7dff775420c0bac2d66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978855"
---
# <a name="jetrestoreinstance-function"></a>Función JetRestoreInstance


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetrestoreinstance-function"></a>Función JetRestoreInstance

La **función JetRestoreInstance** restaura y recupera una copia de seguridad de streaming de una instancia, incluidas todas las bases de datos adjuntas. Está diseñado para funcionar con una copia de seguridad creada con la [función JetBackupInstance.](./jetbackupinstance-function.md) Se trata de la función de restauración más sencilla y encapsulada.

**Windows XP:****JetRestoreInstance** se introdujo en Windows XP.  

```cpp
    JET_ERR JET_API JetRestoreInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Parámetros

*Ejemplo*

Especifica la instancia que se va a usar para esta llamada.

Para Windows XP y versiones posteriores, el uso de este parámetro depende del modo de funcionamiento del motor. Si el motor funciona en modo heredado (modo de compatibilidad Windows 2000) donde solo se admite una instancia, este parámetro puede ser NULL o puede establecerse en un búfer de salida válido que contenga NULL o JET_instanceNil que devolverá el identificador de instancia global creado como efecto secundario de la inicialización. Este identificador de instancia se puede pasar a cualquier otra API que tome una instancia. Si el motor funciona en modo de varias instancias, este parámetro debe establecerse en un búfer de entrada válido que contenga el identificador de instancia devuelto por [JetCreateInstance](./jetcreateinstance-function.md) que se está inicializando.

*Sz*

Carpeta donde se encuentra la copia de seguridad. La copia de seguridad se debe haber generado mediante las [API de JetBackup.](./jetbackup-function.md)

*szDest*

Nombre de la carpeta donde se copiarán y recuperarán los archivos de base de datos del conjunto de copia de seguridad. Si se establece en NULL (que es el caso del [jetRestore](./jetrestore-function.md)heredado), los archivos de base de datos se copiarán y recuperarán en su ubicación original.

*pfn*

Puntero opcional a la función a la que se llamará como información de notificación sobre el progreso de la operación de restauración.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código devuelto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>La operación se ha completado correctamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>Error en la operación porque el motor ya está inicializado para esta instancia.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLogSequence</p></td>
<td><p>El conjunto de archivos de registro del conjunto de copia de seguridad y de la ruta de acceso del registro actual no coinciden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. <strong>JetRestoreInstance</strong> devolverá este error cuando el motor esté en modo de varias instancias y pinstance haga referencia a una instancia no válida Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Error en la operación porque algunas de las rutas de acceso proporcionadas no son válidas (la ruta de acceso de copia de seguridad, la ruta de acceso de destino, el registro o la ruta de acceso del sistema para la instancia).</p></td>
</tr>
<tr class="even">
<td><p>JET_errPageSizeMismatch</p></td>
<td><p>Error en la operación porque el motor está configurado para usar un tamaño de página de base de datos (mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize)</a>que no coincide con el tamaño de página de la base de datos utilizado para crear los archivos de registro de transacciones o las bases de datos asociadas a los archivos de registro de transacciones.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Error en la operación porque los parámetros implican el modo de instancia única (Windows modo de compatibilidad 2000) y el motor ya está en modo de varias instancias.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, los archivos de base de datos del conjunto de copia de seguridad se restaurarán en su ubicación y la recuperación se ejecutará de forma que las bases de datos se encontrarán en un estado de coherencia transaccional limpio. La recuperación reproducirá los archivos de registro del conjunto de copia de seguridad y los archivos de registro de la ruta de acceso del registro si estos archivos existen. Esta recuperación dará lugar a cambios en el archivo de punto de comprobación, los archivos de registro de transacciones y las bases de datos a las que hacen referencia esos archivos de registro de transacciones.

En caso de error, la instancia permanece en un estado sin inicializar. El estado de los archivos de registro de transacciones y las bases de datos a las que hacen referencia esos archivos de registro de transacciones probablemente se habrán cambiado al intentar inicializar la restauración y recuperar las bases de datos.

#### <a name="remarks"></a>Comentarios

El proceso de recuperación reconstruirá las bases de datos adjuntas a la instancia durante la copia de seguridad y guardará los cambios en los archivos de base de datos. El resultado serán bases de datos coherentes con las transacciones. Si es posible, también guardará en la base de datos los cambios realizados desde que se hizo la copia de seguridad hasta el cambio más reciente encontrado en los registros de transacciones. Esto sería posible si los registros de transacciones generados desde que se tomó la copia de seguridad siguen estando presentes en el directorio del registro de transacciones. Tenga en cuenta que si se ha habilitado el registro circular para la instancia, los registros de transacciones generados se reutilizan de modo que la recuperación pueda guardar los cambios que se realizaron hasta el momento de la copia de seguridad. En cualquier caso, este proceso puede tardar bastante tiempo si el número de archivos de registro de transacciones que se va a reproducir en las bases de datos es grande.

**Se debe llamar a JetRestoreInstance** en una instancia de que ya se creó [mediante JetCreateInstance](./jetcreateinstance-function.md).

Dado que durante la recuperación se usará un número significativo de páginas de base de datos y registros de transacciones, hay una serie completa de errores que estas funciones podrían devolver. Estos errores pueden ser desde errores temporales de asignación de recursos como Jet_errOutOfMemory a errores que representan daños físicos, como JET_errReadVerifyFailure, JET_errLogFileCorrupt o JET_errBadPageLink. Estos errores casi siempre se deben a problemas de hardware y, por tanto, no se pueden evitar. La administración errónea de archivos se manifesta con más frecuencia JET_errMissingLogFile o JET_errAttachedDatabaseMismatch, JET_errDatabaseSharingViolation o JET_errInvalidLogSequence. La aplicación puede evitar estos errores. La aplicación debe tener cuidado de proteger el repositorio de estos archivos frente a la manipulación por parte de fuerzas externas, como el usuario u otras aplicaciones. Si la aplicación desea destruir una instancia por completo, se deben eliminar todos los archivos asociados a la instancia. Estos incluyen el archivo de punto de comprobación, los archivos de registro de transacciones y los archivos de base de datos asociados a la instancia.

Los distintos pasos de la recuperación tendrán entradas del registro de eventos generadas, incluido el progreso de la reproducción del registro de transacciones y el resultado final de la restauración.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JetRestoreInstanceW</strong> (Unicode) y <strong>JetRestoreInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBackup](./jetbackup-function.md)  
[JetBackupInstance](./jetbackupinstance-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)

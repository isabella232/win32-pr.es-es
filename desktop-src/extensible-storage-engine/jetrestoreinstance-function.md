---
description: 'Más información acerca de: JetRestoreInstance (función)'
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
ms.openlocfilehash: bb7af096a63880a88496631999ddbc26a975cac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278936"
---
# <a name="jetrestoreinstance-function"></a>Función JetRestoreInstance


_**Se aplica a:** Windows | Windows Server_

## <a name="jetrestoreinstance-function"></a>Función JetRestoreInstance

La función **JetRestoreInstance** restaura y recupera una copia de seguridad de streaming de una instancia de, incluidas todas las bases de datos adjuntas. Está diseñado para trabajar con una copia de seguridad creada con la función [JetBackupInstance](./jetbackupinstance-function.md) . Esta es la función de restauración más sencilla y más encapsulada.

**Windows XP:**  **JetRestoreInstance** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetRestoreInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Parámetros

*repetición*

Especifica la instancia de que se va a usar para esta llamada.

En Windows XP y versiones posteriores, el uso de este parámetro depende del modo de funcionamiento del motor. Si el motor está funcionando en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, este parámetro puede ser NULL o se puede establecer en un búfer de salida válido que contenga NULL o JET_instanceNil que devolverá el identificador de instancia global creado como un efecto secundario de la inicialización. Este identificador de instancia se puede pasar a cualquier otra API que toma una instancia. Si el motor está funcionando en modo de varias instancias, este parámetro debe establecerse en un búfer de entrada válido que contenga el identificador de instancia devuelto por [JetCreateInstance](./jetcreateinstance-function.md) que se está inicializando.

*SZ*

La carpeta donde se encuentra la copia de seguridad. La copia de seguridad debe haberse generado mediante las API de [JetBackup](./jetbackup-function.md) .

*szDest*

Nombre de la carpeta donde se copiarán y recuperarán los archivos de base de datos del conjunto de copia de seguridad. Si se establece en NULL (que es el caso del [JetRestore](./jetrestore-function.md)heredado), los archivos de la base de datos se copiarán y recuperarán en su ubicación original.

*pfn*

Puntero opcional a la función que se llamará como información de notificación sobre el progreso de la operación de restauración.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

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
<td><p>No se pudo realizar la operación porque el motor ya está inicializado para esta instancia.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLogSequence</p></td>
<td><p>El conjunto de archivos de registro del conjunto de copia de seguridad y de la ruta de acceso del registro actual no coincide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro. Este error lo devolverá <strong>JetRestoreInstance</strong> cuando el motor está en modo de varias instancias y pinstance hace referencia a una instancia no válida de Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>No se pudo realizar la operación porque algunas de las rutas de acceso proporcionadas no son válidas (ruta de acceso de copia de seguridad, ruta de acceso de destino, registro o ruta de acceso del sistema para la instancia).</p></td>
</tr>
<tr class="even">
<td><p>JET_errPageSizeMismatch</p></td>
<td><p>Se produjo un error en la operación porque el motor está configurado para usar un tamaño de página de base de datos (con <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) que no coincide con el tamaño de página de la base de datos utilizado para crear los archivos de registro de transacciones o las bases de datos asociadas a los archivos de registro de transacciones.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>No se pudo realizar la operación porque los parámetros modo de instancia única implícita (modo de compatibilidad de Windows 2000) y el motor ya están en modo de varias instancias.</p></td>
</tr>
</tbody>
</table>


En caso de éxito, los archivos de base de datos del conjunto de copia de seguridad se restaurarán a su ubicación y la recuperación se ejecutará de forma que las bases de datos estén en un estado de coherencia transaccional limpio. La recuperación reproducirá los archivos de registro del conjunto de copia de seguridad y los archivos de registro de la ruta de acceso del registro si estos archivos existen. Esta recuperación producirá cambios en el archivo de punto de comprobación, en los archivos de registro de transacciones y en cualquier base de datos a la que hagan referencia esos archivos de registro de transacciones.

En caso de error, la instancia permanece en un estado no inicializado. Es probable que se haya cambiado el estado de los archivos de registro de transacciones y cualquier base de datos a la que hagan referencia los archivos de registro de transacciones al intentar inicializar la restauración y recuperar las bases de datos.

#### <a name="remarks"></a>Observaciones

El proceso de recuperación volverá a construir las bases de datos adjuntas a la instancia durante la copia de seguridad y guardará los cambios en los archivos de base de datos. El resultado serán las bases de datos que son coherentes con las transacciones. Si es posible, también guardará en la base de datos los cambios realizados desde que se realizó la copia de seguridad hasta que se haya producido el cambio más reciente en los registros de transacciones. Esto sería posible si los registros de transacciones generados desde que se realizó la copia de seguridad siguen presentes en el directorio del registro de transacciones. Tenga en cuenta que si se ha habilitado el registro circular para la instancia, los registros de transacciones generados se reutilizan de forma que la recuperación pueda guardar los cambios que tuvieron lugar en el momento de la copia de seguridad. En cualquier caso, es posible que este proceso tarde bastante tiempo si el número de archivos de registro de transacciones que se van a reproducir en las bases de datos es grande.

Se debe llamar a **JetRestoreInstance** en una instancia de que ya se haya creado con [JetCreateInstance](./jetcreateinstance-function.md).

Dado que durante la recuperación se usará un número significativo de páginas de base de datos y registros de transacciones, hay una serie de errores completa que podrían ser devueltos por estas funciones. Estos errores pueden ser de errores de asignación de recursos temporales como Jet_errOutOfMemory a errores que representan daños físicos como JET_errReadVerifyFailure, JET_errLogFileCorrupt o JET_errBadPageLink. Estos errores casi siempre están causados por problemas de hardware y, por tanto, no se pueden evitar. La administración de archivos indebidos se manifestará normalmente como JET_errMissingLogFile o JET_errAttachedDatabaseMismatch o JET_errDatabaseSharingViolation o JET_errInvalidLogSequence. Estos errores son impidebles por la aplicación. La aplicación debe tener cuidado de proteger el repositorio de estos archivos contra la manipulación de las fuerzas externas, como el usuario u otras aplicaciones. Si la aplicación desea destruir una instancia por completo, se deben eliminar todos los archivos asociados a la instancia. Entre ellos se incluyen el archivo de punto de comprobación, los archivos de registro de transacciones y cualquier archivo de base de datos asociado a la instancia.

Los distintos pasos de la recuperación tendrán entradas del registro de eventos generadas que incluyen el progreso de la reproducción del registro de transacciones y el resultado final de la restauración.

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
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
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

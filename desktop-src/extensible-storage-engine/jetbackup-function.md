---
description: 'Más información acerca de: JetBackup (función)'
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
ms.openlocfilehash: f225053df36ebe98bc890a8e036d84ee31b6b154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717169"
---
# <a name="jetbackup-function"></a>Función JetBackup


_**Se aplica a:** Windows | Windows Server_

## <a name="jetbackup-function"></a>Función JetBackup

La función **JetBackup** crea una copia de seguridad de la base de datos mientras la base de datos está en línea. Esta función es principalmente para la compatibilidad con versiones anteriores de Windows 2000 y los motores de base de datos anteriores, donde solo se permite una instancia de una base de datos. En este caso, la instancia activa es la instancia de la que se realiza una copia de seguridad.

```cpp
    JET_ERR JET_API JetBackup(
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>Parámetros

*szBackupPath*

Directorio en el que se almacena la copia de seguridad. Si la ruta de acceso de copia de seguridad es NULL, la función truncará los registros, si es posible.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitBackupAtomic</p></td>
<td><p>Crea una copia de seguridad completa de la base de datos. Esto permite conservar una copia de seguridad existente en el mismo directorio si se produce un error en la nueva copia de seguridad.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>Crea una copia de seguridad incremental en lugar de una copia de seguridad completa. Esto significa que solo se realizará una copia de seguridad de los archivos de registro desde la última copia de seguridad completa o incremental.</p></td>
</tr>
</tbody>
</table>


*pfnStatus*

Puntero a la función de devolución de llamada [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , que proporciona información de notificación sobre el progreso de la operación de copia de seguridad.

### <a name="return-value"></a>Valor devuelto

La función devuelve uno de los códigos de error de [JET_ERR](./jet-err.md) . A continuación se muestran los elementos que se devuelven con más frecuencia. (Para obtener una lista completa de los errores de esta API, consulte [códigos de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md)).

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
<td><p>JET_errBackupInProgress</p></td>
<td><p>Ya hay una copia de seguridad en curso para la misma instancia. No se permiten varias copias de seguridad al mismo tiempo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupNotAllowedYet</p></td>
<td><p>La instancia todavía no está lista para la copia de seguridad mientras se está inicializando.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No se puede completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No se puede completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBackup</p></td>
<td><p>No se permite una copia de seguridad incremental si el registro circular está activado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Las opciones especificadas no son válidas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Se pasó un parámetro no válido a la API.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>La ruta de acceso de destino no existe.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLoggingDisabled</p></td>
<td><p>La instancia se está ejecutando sin registro. No se permite ninguna copia de seguridad.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>Se produjo un error de comprobación de la suma de comprobación en un archivo de registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogWriteFail</p></td>
<td><p>El registro de la instancia es temporal o está deshabilitado permanentemente debido a un error inesperado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No se puede completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>Se produjo un error de comprobación de la suma de comprobación en una página de base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No se puede completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si la función se ejecuta correctamente, todos los archivos necesarios para una restauración hasta el momento de la copia de seguridad se incluirán en el directorio de copia de seguridad. Si se trata de una copia de seguridad completa, los archivos serán los archivos de base de datos y los archivos de registro necesarios para poner la base de datos en un estado coherente. Si se trata de una copia de seguridad incremental, solo se agregarán archivos de registro a los directorios, pero los archivos ya existentes (archivos de registro y bases de datos), junto con los nuevos archivos de registro, se podrán restaurar para devolver la base de datos al estado en que se encontraba en el momento en que comenzó la copia de seguridad.

Como efecto secundario de la copia de seguridad, se truncarán los archivos de registro que ya no sean necesarios.

Al mismo tiempo, los encabezados de la base de datos se actualizarán con la información cuando se realizó la última copia de seguridad.

Si se produce un error en la función, no habrá ningún archivo en el destino del directorio de copia de seguridad, por lo que no será posible realizar ninguna restauración. Al mismo tiempo, los archivos de registro actuales no se truncarán.

#### <a name="remarks"></a>Observaciones

Los distintos pasos de la copia de seguridad tendrán entradas del registro de eventos generadas, incluidos los nombres de archivo, el truncamiento del registro y el resultado final de la copia de seguridad.

Las copias de seguridad incrementales solo son posibles después de realizar una copia de seguridad completa. Además, solo se pueden realizar copias de seguridad incrementales si el registro circular está desactivado. Se recomienda que el directorio de copia de seguridad no contenga ningún archivo que no sea el utilizado en la copia de seguridad o que haya agregado una copia de seguridad correcta anterior.

El directorio de copia de seguridad debe existir a menos que se establezca el parámetro *JET_paramCreatePathIfNotExist* para la instancia. Para obtener más información, vea [parámetros del sistema](./extensible-storage-engine-system-parameters.md).

La copia de seguridad realizará una comprobación de suma de comprobación en todas las páginas de base de datos usadas y, a partir de Windows Server 2003, también en los archivos de registro. Esto ofrece una oportunidad para estimar el estado de la base de datos, incluso para las páginas que no se leen durante las operaciones normales. Si se encuentra algún daño de este tipo, se producirá un error en la copia de seguridad.

Durante la copia de seguridad, se completará el archivo de registro actual y se generará un nuevo registro. De esta manera, todos los archivos de registro necesarios se pueden copiar, ya que el registro actual ya no estará en uso.

Se recomienda encarecidamente que la copia de seguridad no se use para ningún propósito que no sea la copia de seguridad y restauración en el nivel de motor. Esto minimizará la posibilidad de obtener errores durante las operaciones de copia de seguridad y restauración.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
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
<td><p>Se implementa como <strong>JetBackupW</strong> (Unicode) y <strong>JetBackupA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[Archivos del motor de almacenamiento extensible](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)

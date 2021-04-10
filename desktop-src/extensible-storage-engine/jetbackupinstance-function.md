---
description: 'Más información acerca de: JetBackupInstance (función)'
title: Función JetBackupInstance
TOCTitle: JetBackupInstance Function
ms:assetid: 82486441-5037-440b-8632-038e953ad870
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269318(v=EXCHG.10)
ms:contentKeyID: 32765608
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupInstanceW
- JetBackupInstanceA
- JetBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fab20676267333ae8f60e4fe4f07d98a8b45e88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153775"
---
# <a name="jetbackupinstance-function"></a>Función JetBackupInstance


_**Se aplica a:** Windows | Windows Server_

## <a name="jetbackupinstance-function"></a>Función JetBackupInstance

La función **JetBackupInstance** realiza una copia de seguridad de secuencias de una instancia, incluidas todas las bases de datos adjuntas, en un directorio. Con varios métodos de copia de seguridad admitidos por el motor de, esta es la función más sencilla y encapsulada.

**Windows XP: JetBackupInstance** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>Parámetros

*repetición*

Instancia de la base de datos que se va a copiar.

*szBackupPath*

Directorio en el que se almacena la copia de seguridad. Si la ruta de acceso de copia de seguridad es NULL para usar la función, truncará los registros, si es posible.

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
<td><p>Crea una copia de seguridad incremental en lugar de una copia de seguridad completa. Esto significa que solo se realizará una copia de seguridad de los archivos de registro creados desde la última copia de seguridad completa o incremental.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>Reservado para uso futuro.</p></td>
</tr>
</tbody>
</table>


*pfnStatus*

Puntero a la función de devolución de llamada [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , que proporciona información de notificación sobre el progreso de la operación de copia de seguridad.

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
<td><p>JET_errBackupInProgress</p></td>
<td><p>Ya hay una copia de seguridad en curso para la misma instancia. No se permiten varias copias de seguridad al mismo tiempo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupNotAllowedYet</p></td>
<td><p>La instancia todavía no está lista para la copia de seguridad mientras se está inicializando.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No se puede completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</p></td>
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


Una vez que la función devuelve un resultado correcto, se mostrarán todos los archivos necesarios para una restauración hasta el momento de la copia de seguridad. Si se trata de una copia de seguridad completa, los archivos serán los archivos de base de datos y los archivos de registro necesarios para poner la base de datos en un estado coherente. Si se trata de una copia de seguridad incremental, solo se agregarán los archivos de registro a los directorios, pero los archivos ya existentes (archivos de registro y bases de datos) junto con los nuevos archivos de registro se podrán restaurar y volver a poner la base de datos al estado en el momento de la copia de seguridad.

Como efecto secundario de la copia de seguridad, se truncarán los archivos de registro que ya no sean necesarios.

Al mismo tiempo, los encabezados de la base de datos se actualizarán con la información cuando se realizó la última copia de seguridad.

En caso de error, no habrá ningún archivo en el destino del directorio de copia de seguridad, por lo que no será posible realizar ninguna restauración. Al mismo tiempo, los archivos de registro actuales no se truncarán.

#### <a name="remarks"></a>Observaciones

Los distintos pasos de la copia de seguridad tendrán entradas del registro de eventos generadas, incluidos los nombres de archivo, el truncamiento del registro y el resultado final de la copia de seguridad.

La copia de seguridad incremental solo es posible después de realizar una copia de seguridad completa. Además, solo se pueden realizar copias de seguridad incrementales si el registro circular está desactivado. Se recomienda que el directorio de copia de seguridad no contenga otros archivos, el implicado en la copia de seguridad o que se agregaron mediante una copia de seguridad correcta anterior.

El directorio de copia de seguridad debe existir a menos que se establezca el parámetro *JET_paramCreatePathIfNotExist* para la instancia. Para obtener más información, vea [parámetros del sistema](./extensible-storage-engine-system-parameters.md).

La copia de seguridad realizará la comprobación de la suma de comprobación en todas las páginas de base de datos usadas y, a partir de Windows Server 2003, también en los archivos de registro. Esto ofrece una oportunidad para estimar el estado de la base de datos incluso para las páginas que no se leen durante las operaciones normales. Si se encuentra algún daño de este tipo, se producirá un error en la copia de seguridad.

Durante la copia de seguridad, el archivo de registro actual finalizará y se iniciará una nueva generación de registros. Esto permitirá copiar los archivos de registro necesarios porque ya no se utilizará el último que sea necesario.

Se recomienda encarecidamente que la copia de seguridad no se use para otras otras, y que se restaure en el nivel de motor. Esto minimizará el cambio de obtención de errores durante las operaciones de copia de seguridad y restauración.

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
<td><p>Se implementa como <strong>JetBackupInstanceW</strong> (Unicode) y <strong>JetBackupInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetStopServiceInstance](./jetstopserviceinstance-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)

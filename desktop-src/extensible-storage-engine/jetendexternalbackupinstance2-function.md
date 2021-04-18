---
description: 'Más información acerca de: JetEndExternalBackupInstance2 (función)'
title: JetEndExternalBackupInstance2 función)
TOCTitle: JetEndExternalBackupInstance2 Function
ms:assetid: a30961f7-a1fb-44fe-881a-d46bf8f743b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294047(v=EXCHG.10)
ms:contentKeyID: 32765646
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e719885cc61ff3f3193046b632e9969b8d660f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706711"
---
# <a name="jetendexternalbackupinstance2-function"></a>JetEndExternalBackupInstance2 función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetendexternalbackupinstance2-function"></a>JetEndExternalBackupInstance2 función)

La función **JetEndExternalBackupInstance2** finaliza una sesión de copia de seguridad externa. Esta API es la última API en una serie de API a las que se debe llamar para ejecutar una copia de seguridad en línea (no basada en VSS) correcta.

**Windows XP: JetEndExternalBackupInstance2** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*repetición*

Instancia de que se va a usar para esta llamada.

**Windows 2000:** En Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia. En este caso, se implica el uso de esta instancia global.

**Windows XP:** En Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia. De lo contrario, se producirá un error en la operación con JET_errRunningInMultiInstanceMode.

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
<td><p>JET_bitBackupEndAbort<br />
0x0002</p></td>
<td><p>La aplicación cliente está anulando la copia de seguridad.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupEndNormal<br />
0x0001</p></td>
<td><p>La aplicación cliente finalizó la copia de seguridad por completo y termina normalmente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupTruncateDone<br />
0x0100</p></td>
<td><p><strong>Windows Vista:  </strong> JET_bitBackupTruncateDone se introduce en Windows Vista.</p>
<p>El motor puede marcar los encabezados de la base de datos según corresponda (por ejemplo, una copia de seguridad completa completada), aunque no se haya completado la llamada a TRUNCATE.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errBackupAbortByCaller</p></td>
<td><p><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</p>
<p>El autor de la llamada finalizó una copia de seguridad en medio de la secuencia de copia de seguridad sin señalar la intención con <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. Este error se debe a un error en el cliente de copia de seguridad en Windows Server 2003 y versiones posteriores. En Windows XP, este error se devuelve para una terminación intencionada de la secuencia de copia de seguridad externa.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p><strong>Windows Server 2003:  </strong> Este valor devuelto se introduce en Windows Server 2003.</p>
<p>No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</p>
<p>No se puede completar la operación porque la instancia asociada a la sesión encontró un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup</p></td>
<td><p>No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, cuando en realidad existen varias instancias.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si la función se ejecuta correctamente, la copia de seguridad externa era correcta. Success indica que todos los archivos (por ejemplo, bases de datos y registros) que son adecuados para el tipo de copia de seguridad (especificado en [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) se recuperaron del motor de copia de seguridad. Los archivos de copia de seguridad se pueden recuperar con recuperación de hardware ([JetExternalRestore](./jetexternalrestore-function.md)).

Si se produce un error en esta función, normalmente finaliza la copia de seguridad externa. El error significa que la copia de seguridad no es válida debido a un error de uso del cliente o de la aplicación. Es importante comprobar el código de retorno de esta API para comprobar que la secuencia de copia de seguridad se ha realizado correctamente.

#### <a name="remarks"></a>Observaciones

Si el motor está configurado para registrar eventos, se registra un evento para indicar la resolución de la copia de seguridad externa.

Si la secuencia de copia de seguridad no se completa en orden y con una llamada correcta a [JetEndExternalBackup](./jetendexternalbackup-function.md), las copias de seguridad incrementales subsiguientes podrían contener más datos de los esperados por la aplicación.

Para obtener más información sobre la secuencia de API de copia de seguridad externa, vea [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

Antes de Windows Vista, si no se realizó el truncamiento del registro, el motor consideró que la copia de seguridad era una copia de seguridad de copia. Sin embargo, la copia de seguridad puede ser una copia de seguridad normal para la que no se ha realizado el truncamiento (por ejemplo, si hay bases de datos desasociadas). La opción JET_bitBackupTruncateDone se puede usar para informar al motor sobre esto y permitir las modificaciones de encabezado de base de datos apropiadas.

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
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[Parámetros de control de errores](./error-handling-parameters.md)  
[Errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)

---
description: 'Más información acerca de: JetBeginExternalBackupInstance (función)'
title: JetBeginExternalBackupInstance función)
TOCTitle: JetBeginExternalBackupInstance Function
ms:assetid: f1c5a73d-b1cc-4ee4-942b-b5e4ef51bc2f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294132(v=EXCHG.10)
ms:contentKeyID: 32765746
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bab2fa3d9faa7f81abea278e3d9fcf4a4022c24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496936"
---
# <a name="jetbeginexternalbackupinstance-function"></a>JetBeginExternalBackupInstance función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetbeginexternalbackupinstance-function"></a>JetBeginExternalBackupInstance función)

La función **JetBeginExternalBackupInstance** inicia una copia de seguridad externa mientras el motor y la base de datos están en línea y activos.

**Windows XP: JetBeginExternalBackupInstance** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*repetición*

Instancia de base de datos que se va a usar para esta llamada.

En Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia. En este caso, se implica el uso de esta instancia global.

En Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia. De lo contrario, se producirá un error en la operación con JET_errRunningInMultiInstanceMode.

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
<td><p>Esta marca está en desuso. El uso de este bit producirá JET_errInvalidgrbit devuelto.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>Crea una copia de seguridad incremental en lugar de una copia de seguridad completa. Esto significa que solo se realizará una copia de seguridad de los archivos de registro desde la última copia de seguridad completa o incremental.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>Reservado para uso futuro. Definido para Windows XP.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

El sistema puede generar códigos de éxito o error como resultado de una llamada a esta función. Para obtener una lista completa de los errores de esta API, consulte [códigos de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md).

Vea [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

#### <a name="remarks"></a>Observaciones

**JetBeginExternalBackupInstance** es la primera función de una serie de funciones a las que se debe llamar para ejecutar una copia de seguridad en línea (no basada en VSS) correcta. Vea también [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) y [JetStopBackupInstance](./jetstopbackupinstance-function.md).

Se puede utilizar una copia de seguridad externa para implementar copias de seguridad completas, incrementales o diferenciales.

La copia de seguridad será aproximada, en la que la copia de seguridad será coherente con un único punto en el tiempo en el historial de transacciones, pero no es posible controlar el punto exacto en el tiempo en este momento.

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
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetEndExternalBackup](./jetendexternalbackup-function.md)  
[JetEndExternalBackupInstance2](./jetendexternalbackupinstance2-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)

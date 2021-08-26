---
description: 'Más información sobre: JetBeginExternalBackupInstance (Función)'
title: JetBeginExternalBackupInstance (Función)
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
ms.openlocfilehash: 53583a1d51de390b0c84143dcb59f3327b7c91bb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479301"
---
# <a name="jetbeginexternalbackupinstance-function"></a>JetBeginExternalBackupInstance (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetbeginexternalbackupinstance-function"></a>JetBeginExternalBackupInstance (Función)

La **función JetBeginExternalBackupInstance** inicia una copia de seguridad externa mientras el motor y la base de datos están en línea y activos.

**Windows XP: JetBeginExternalBackupInstance** se introdujo en Windows XP.

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*Ejemplo*

Instancia de base de datos que se va a usar para esta llamada.

Por Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia. En este caso, el uso de esta instancia global está implícito.

Para Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (modo de compatibilidad Windows 2000), donde solo se admite una instancia. De lo contrario, se producirá un error en la operación JET_errRunningInMultiInstanceMode.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Esta marca está en desuso. El uso de este bit dará lugar a la JET_errInvalidgrbit se devolverá.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Crea una copia de seguridad incremental en lugar de una copia de seguridad completa. Esto significa que solo se realizará una copia de seguridad de los archivos de registro desde la última copia de seguridad completa o incremental.</p> | 
| <p>JET_bitBackupSnapshot</p> | <p>Reservado para uso futuro. Se define para Windows XP.</p> | 



### <a name="return-value"></a>Valor devuelto

El sistema puede generar códigos correctos o de error como resultado de una llamada a esta función. Para obtener una lista completa de los errores de esta API, consulte Extensible Storage Engine Error Codes (Códigos de error del [motor de aplicaciones extensibles).](./extensible-storage-engine-error-codes.md)

Consulte [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

#### <a name="remarks"></a>Comentarios

**JetBeginExternalBackupInstance** es la primera función de una serie de funciones a las que se debe llamar para ejecutar una copia de seguridad correcta en línea (no basada en VSS). Consulte también [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) y [JetStopBackupInstance.](./jetstopbackupinstance-function.md)

Se puede usar una copia de seguridad externa para implementar copias de seguridad completas, incrementales o diferenciales.

La copia de seguridad será aproximada, ya que la copia de seguridad será coherente con un único momento en el tiempo en el historial de transacciones, pero no es posible controlar el momento exacto en el tiempo en este momento.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



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

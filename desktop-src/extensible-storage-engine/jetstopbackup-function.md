---
description: 'Más información sobre: JetStopBackup (Función)'
title: Función JetStopBackup
TOCTitle: JetStopBackup Function
ms:assetid: b7545284-2fdb-4470-8466-fc2109ad63c5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294067(v=EXCHG.10)
ms:contentKeyID: 32765682
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd5f7fe7096b0562aa9fc4ce8d15f77a4ccf205f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469702"
---
# <a name="jetstopbackup-function"></a>Función JetStopBackup


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetstopbackup-function"></a>Función JetStopBackup

La **función JetStopBackup** impide que cualquier actividad relacionada con la copia de seguridad de streaming continúe en una instancia en ejecución específica, lo que finaliza la copia de seguridad de streaming de una manera predecible.

**Windows XP:**  Esta función se introduce en Windows XP.

[JetStopService es](./jetstopservice-function.md) la llamada heredada cuando solo se permite una instancia. En este caso, la única instancia activa es la que se prepara para la terminación.

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>No está claro qué instancia prepararse para la terminación cuando se <a href="gg269240(v=exchg.10).md">usa JetStopService</a> con el modo de varias instancias.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 



Si esta función se realiza correctamente, la instancia comenzará a dar error a las nuevas API de copia de seguridad de streaming.

Si se produce un error en esta función, no se realizará ningún paso para preparar la finalización de la copia de seguridad en la instancia y no se producirá ningún cambio en el estado de la instancia.

#### <a name="remarks"></a>Comentarios

Normalmente, la copia de seguridad se desencadena mediante un evento fuera del mecanismo de proceso y, al usar esta API, la propia aplicación ESENT realizará más llamadas a las API de copia de seguridad de streaming para que no se realicen errores. La mayoría de las API de copia de seguridad de streaming comenzarán a dar error con JET_errBackupAbortByServer. Por lo tanto, cualquier progreso de la copia de seguridad de streaming [(como JetReadFileInstance)](./jetreadfileinstance-function.md)devolverá un error. Todavía se permitirán las operaciones de copia de seguridad que forman parte de la terminación de la copia de seguridad (como [JetEndExternalBackupInstance).](./jetendexternalbackupinstance-function.md)

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)

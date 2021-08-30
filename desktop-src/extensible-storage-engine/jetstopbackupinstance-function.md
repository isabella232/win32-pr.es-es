---
description: 'Más información sobre: JetStopBackupInstance (Función)'
title: Función JetStopBackupInstance
TOCTitle: JetStopBackupInstance Function
ms:assetid: 7d008eac-2a32-402b-91ef-965ed3c3b0de
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269309(v=EXCHG.10)
ms:contentKeyID: 32765599
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52dfbae29c9d45206c36015788d20f9b7ac610dd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481181"
---
# <a name="jetstopbackupinstance-function"></a>Función JetStopBackupInstance


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetstopbackupinstance-function"></a>Función JetStopBackupInstance

La **función JetStopBackupInstance** impide que la actividad relacionada con la copia de seguridad de streaming continúe en una instancia en ejecución específica, lo que finaliza la copia de seguridad de streaming de una manera predecible.

**Windows XP:****JetStopBackupInstance** se introdujo en Windows XP.  

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parámetros

*Ejemplo*

Identifica la instancia en ejecución que se usará para la llamada API.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInvalidParameter</p> | <p>El parámetro de instancia especificado tiene un valor no válido (no una instancia que se está ejecutando actualmente).</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 



Si esta función se realiza correctamente, la instancia especificada comenzará a dar error a las nuevas API de copia de seguridad de streaming.

Si se produce un error en esta función, no se realizará ningún paso para preparar la finalización de la copia de seguridad en la instancia y no se producirá ningún cambio en el estado de la instancia.

#### <a name="remarks"></a>Comentarios

Normalmente, la copia de seguridad se desencadena mediante un evento fuera del mecanismo de proceso y, al usar esta API, la propia aplicación ESENT realizará más llamadas a las API de copia de seguridad de streaming para que no se realicen errores. La mayoría de las API de copia de seguridad de streaming comenzarán a dar error con JET_errBackupAbortByServer. Por lo tanto, cualquier progreso de la copia de seguridad de streaming [(como JetReadFileInstance)](./jetreadfileinstance-function.md)devolverá un error. Todavía se permitirán las operaciones de copia de seguridad que forman parte de la terminación de la copia de seguridad (como [JetEndExternalBackupInstance).](./jetendexternalbackupinstance-function.md)

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)

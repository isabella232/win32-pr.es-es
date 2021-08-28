---
description: 'Más información sobre: JetStopBackupInstance (Función)'
title: JetStopBackupInstance (Función)
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
ms.openlocfilehash: c4dae676cfbbb0f2509a7d86fbb6507b8e2110f1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987248"
---
# <a name="jetstopbackupinstance-function"></a>JetStopBackupInstance (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetstopbackupinstance-function"></a>JetStopBackupInstance (Función)

La **función JetStopBackupInstance** impide que la actividad relacionada con la copia de seguridad de streaming continúe en una instancia en ejecución específica, finalizando así la copia de seguridad de streaming de una manera predecible.

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

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInvalidParameter</p> | <p>El parámetro de instancia especificado tiene un valor no válido (no una instancia que se está ejecutando actualmente).</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 



Si esta función se realiza correctamente, la instancia especificada empezará a dar error a las nuevas API de copia de seguridad de streaming.

Si se produce un error en esta función, no se realizará ningún paso para preparar la finalización de la copia de seguridad en la instancia y no se producirá ningún cambio en el estado de la instancia.

#### <a name="remarks"></a>Observaciones

Normalmente, la copia de seguridad se desencadena mediante un evento fuera del mecanismo de proceso y, mediante esta API, la propia aplicación ESENT realizará cualquier otra llamada a las API de copia de seguridad de streaming para producir un error. La mayoría de las API de copia de seguridad de streaming comenzarán a dar error con JET_errBackupAbortByServer. Por lo tanto, cualquier progreso de la copia de seguridad de streaming [(como JetReadFileInstance)](./jetreadfileinstance-function.md)devolverá un error. Todavía se permitirán las operaciones de copia de seguridad que forman parte de la terminación de copia de seguridad (como [JetEndExternalBackupInstance).](./jetendexternalbackupinstance-function.md)

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)

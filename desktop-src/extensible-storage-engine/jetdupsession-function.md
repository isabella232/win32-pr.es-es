---
description: 'Más información sobre: JetDupSession (Función)'
title: JetDupSession (Función)
TOCTitle: JetDupSession Function
ms:assetid: fa8fbaca-fe48-401e-9700-1303f4842ad9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294141(v=EXCHG.10)
ms:contentKeyID: 32765755
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupSession
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c22be08630c446f6c5ba106b38be6bc24415325
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466632"
---
# <a name="jetdupsession-function"></a>JetDupSession (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetdupsession-function"></a>JetDupSession (Función)

La **función JetDupSession** inicia una sesión e inicializa y devuelve un identificador de sesión ese ([JET_SESID](./jet-sesid.md)). Las sesiones controlan todo el acceso a la base de datos y se usan para controlar el ámbito de las transacciones. La sesión se puede usar para iniciar, confirmar o anular transacciones. La sesión también se usa para adjuntar, crear o abrir una base de datos. La sesión se usa como contexto para todas las operaciones DDL y DML. Para aumentar la simultaneidad y el acceso paralelo a la base de datos, se pueden iniciar varias sesiones.

**Nota** Esta API actuará de todas las maneras como se llama a [JetBeginSession](./jetbeginsession-function.md) en la instancia de la sesión pasada. Esta función no se recomienda, [se prefiere JetBeginSession.](./jetbeginsession-function.md)

```cpp
    JET_ERR JET_API JetDupSession(
      __in          JET_SESID sesid,
      __out         JET_SESID* psesid
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se usará como origen para duplicar o iniciar la sesión.

*psesid*

Puntero a la variable que el identificador de sesión inicializa al devolverse correctamente.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Error en la operación porque no se pudo asignar memoria.</p> | 
| <p>JET_errOutOfSessions</p> | <p>El número de sesiones que el motor permitirá que el cliente inicie es limitado. Este valor se puede cambiar mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <em>la JET_paramMaxSessions</em> constante. El número predeterminado de sesiones es 16. Consulte <a href="gg294139(v=exchg.10).md">Parámetros del sistema</a> para obtener más información <em>JET_paramMaxSessions</em>.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, se inicializa el identificador de sesión y se puede usar para las operaciones de base de datos.

En caso de error, no hay sesiones disponibles o no se pudo inicializar una nueva sesión.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_SESID](./jet-sesid.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)

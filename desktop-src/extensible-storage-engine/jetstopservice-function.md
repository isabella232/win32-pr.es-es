---
description: 'Más información sobre: JetStopService (Función)'
title: Función JetStopService
TOCTitle: JetStopService Function
ms:assetid: 46aeb9ed-ee72-49cc-99e3-791a51a55b02
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269240(v=EXCHG.10)
ms:contentKeyID: 32765542
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopService
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75e8622d79f2757bee8ab3041250b2ba78499194
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480311"
---
# <a name="jetstopservice-function"></a>Función JetStopService


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetstopservice-function"></a>Función JetStopService

La **función JetStopService** prepara una instancia para la terminación.

**JetStopService es** la llamada heredada cuando solo se permite una instancia. En este caso, la única instancia activa es la que se prepara para la terminación.

```cpp
    JET_ERR JET_API JetStopService(void);
```

### <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>No está claro qué instancia prepararse para la terminación cuando se <strong>usa JetStopService</strong> con el modo de varias instancias.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 



Si esta función se realiza correctamente, se prepara para una terminación futura. Los pasos necesarios para prepararse para una terminación incluyen los siguientes:

  - Detenga la desfragmentación en línea si se está ejecutando.

  - Inicie una limpieza del almacén de versiones.

  - Para reducir la profundidad del punto de control, empiece a vaciar las páginas desatendcidas en el administrador de búferes.

  - Evitar llamadas futuras a la mayoría de las funciones de esa instancia.

Si se produce un error en esta función, no se realizará ninguno de los pasos para prepararse para la terminación de una instancia, por lo que no se producirá ningún cambio en el estado de la instancia.

#### <a name="remarks"></a>Comentarios

Esta función reduce el trabajo que tendrá que realizar la instancia cuando finalice, pero no finalizará la instancia. Como resultado, esta función es simplemente una optimización y no es obligatoria de usar. Tenga en cuenta que la cantidad de trabajo realizado en preparación fue menor en Windows 2000 y Windows XP. Una vez que la función se realiza correctamente, la llamada a funciones que ya no se permiten devolverá JET_errClientRequestToStopJetService. Las funciones que todavía se permiten después de esta llamada son: [JetRollback,](./jetrollback-function.md) [JetCloseTable,](./jetclosetable-function.md) [JetEndSession,](./jetendsession-function.md) [JetCloseDatabase,](./jetclosedatabase-function.md) [JetDetachDatabase](./jetdetachdatabase-function.md) y [JetResetSessionContext.](./jetresetsessioncontext-function.md)

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)

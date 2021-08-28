---
description: 'Más información sobre: JetCloseTable (Función)'
title: JetCloseTable (Función)
TOCTitle: JetCloseTable Function
ms:assetid: c8975145-e48a-4029-9522-1509263019ae
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294087(v=EXCHG.10)
ms:contentKeyID: 32765702
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe7f3c084a52faa9b5f011474bd0b502aebd277b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989068"
---
# <a name="jetclosetable-function"></a>JetCloseTable (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetclosetable-function"></a>JetCloseTable (Función)

La **función JetCloseTable** cierra una tabla abierta en una base de datos. La tabla puede ser una tabla temporal o una tabla normal.

```cpp
JET_ERR JET_API JetCloseTable(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid
);
```

### <a name="parameters"></a>Parámetros

*sesid*

Identifica el contexto de sesión de base de datos que se usará para la llamada API.

*tableid*

Identifica la tabla que se va a cerrar.

Establezca *tableid en* JET_tableidNil liberar memoria.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 



#### <a name="remarks"></a>Observaciones

Se debe llamar a esta función en todas las tablas abiertas [con JetOpenTable](./jetopentable-function.md).

La excepción a esta regla se produce cuando se llama a [JetOpenTable](./jetopentable-function.md) en una transacción y la transacción se revierte [(con JetRollback](./jetrollback-function.md)). Al revertir una transacción, la tabla se cierra automáticamente. En este caso, es un error cerrar la tabla con **JetCloseTable**.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTable](./jetopentable-function.md)  
[JetRollback](./jetrollback-function.md)

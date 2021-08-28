---
description: 'Más información sobre: JetDeleteColumn (Función)'
title: JetDeleteColumn (Función)
TOCTitle: JetDeleteColumn Function
ms:assetid: b2f4be8c-7ea9-4f66-925b-4e9c14d9d475
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294062(v=EXCHG.10)
ms:contentKeyID: 32765677
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumnA
- JetDeleteColumnW
- JetDeleteColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c7c73c5a6fd3249a8779526f6655992ad545372
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985918"
---
# <a name="jetdeletecolumn-function"></a>JetDeleteColumn (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetdeletecolumn-function"></a>JetDeleteColumn (Función)

La **función JetDeleteColumn** elimina una columna de una tabla de base de datos ESE.

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*tableid*

Tabla de la que se va a eliminar la columna.

*szColumnName*

Nombre de la columna que se va a eliminar.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errColumnInUse</p> | <p>La columna está actualmente en uso. Un índice la puede usar actualmente.</p> | 
| <p>JET_errFixedDDL</p> | <p>Se intentó modificar el DDL fijo.</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>La columna denominada <em>en szColumnName existe</em> en la tabla de plantillas y no se puede modificar el DDL de una tabla de plantilla.</p> | 
| <p>JET_errInvalidName</p> | <p>Esto se puede devolver si se ha dado un nombre no bueno <em>para szColumnName.</em></p> | 
| <p>JET_errPermissionDenied</p> | <p>La tabla no se puede escribir. Esto puede devolverse si la base de datos se abrió en modo de solo lectura.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La transacción es una transacción de solo lectura.</p> | 



#### <a name="remarks"></a>Observaciones

Llamar **a JetDeleteColumn** es idéntico a llamar [a JetDeleteColumn2](./jetdeletecolumn2-function.md) con *grbit* establecido en cero (0).

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa <strong>como JetDeleteColumnW</strong> (Unicode) y <strong>JetDeleteColumnA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)

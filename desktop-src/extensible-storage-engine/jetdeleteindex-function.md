---
description: 'Más información sobre: JetDeleteIndex (Función)'
title: JetDeleteIndex (Función)
TOCTitle: JetDeleteIndex Function
ms:assetid: c540503b-d5a6-47f2-9113-9650891c4b6d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294081(v=EXCHG.10)
ms:contentKeyID: 32765696
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteIndexW
- JetDeleteIndexA
- JetDeleteIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a934581754477f336415926716a9a8c7e6097d81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126887297"
---
# <a name="jetdeleteindex-function"></a>JetDeleteIndex (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetdeleteindex-function"></a>JetDeleteIndex (Función)

La **función JetDeleteIndex** elimina un índice de una tabla.

```cpp
    JET_ERR JET_API JetDeleteIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*tableid*

Tabla que contiene la columna que se va a eliminar.

*szIndexName*

Nombre del índice que se va a eliminar.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errFixedDDL</p> | <p>Se intentó eliminar un índice de una tabla fija (por ejemplo, uno creado con JET_bitTableCreateFixedDDL).</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>Se intentó eliminar un índice de una tabla de plantillas. Una tabla de plantillas tiene DDL fijo.</p> | 
| <p>JET_errIndexNotFound</p> | <p>No se encontró el índice denominado <em>en szIndexName.</em></p> | 
| <p>JET_errPermissionDenied</p> | <p>La tabla no se puede actualizar porque se abrió de solo lectura.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Varios subprocesos intentaron usar la misma sesión de base de datos.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La transacción se abrió como una transacción de solo lectura.</p> | 



#### <a name="remarks"></a>Observaciones

Cuando se realiza correctamente, el índice se elimina y, por tanto, no se puede usar posteriormente. No debe haber ninguna transacción activa mediante el índice.

Si se ejecuta correctamente, la moneda se establece antes del primer registro.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetDeleteIndexW</strong> (Unicode) y <strong>JetDeleteIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)

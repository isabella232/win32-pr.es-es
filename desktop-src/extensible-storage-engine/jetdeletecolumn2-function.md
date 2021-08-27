---
description: 'Más información sobre: JetDeleteColumn2 (Función)'
title: JetDeleteColumn2 (Función)
TOCTitle: JetDeleteColumn2 Function
ms:assetid: 840b5acd-8bbf-4524-9741-5d74e3427329
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269320(v=EXCHG.10)
ms:contentKeyID: 32765610
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumn2
- JetDeleteColumn2A
- JetDeleteColumn2W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 87e9506048094b77674e85f76f6c1718def44cae
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467172"
---
# <a name="jetdeletecolumn2-function"></a>JetDeleteColumn2 (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetdeletecolumn2-function"></a>JetDeleteColumn2 (Función)

La **función JetDeleteColumn2** elimina una columna de una tabla de base de datos ESE y permite establecer una opción *grbit.*

**Windows XP: JetDeleteColumn2** se introdujo en Windows XP.

```cpp
    JET_ERR JET_API JetDeleteColumn2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szColumnName,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*tableid*

Tabla que contiene la columna que se va a eliminar.

*szColumnName*

Nombre de la columna que se va a eliminar.

*grbit*

Grupo de bits que especifica cero o más de las siguientes opciones.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitDeleteColumnIgnoreTemplateColumns</p> | <p>Si JET_bitDeleteColumIgnoreTemplateColumns, la API solo intentará eliminar columnas de la tabla derivada. Si existe una columna con ese nombre en la tabla base, se omitirá.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errColumnInUse</p> | <p>La columna está actualmente en uso. Un índice la puede usar actualmente.</p> | 
| <p>JET_errFixedDDL</p> | <p>Se intentó modificar el DDL fijo.</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>La columna denominada <em>en szColumnName existe</em> en la tabla de plantillas y no se puede modificar el DDL de una tabla de plantillas.</p> | 
| <p>JET_errInvalidName</p> | <p>Esto se puede devolver si se ha dado un nombre no bueno <em>para szColumnName.</em></p> | 
| <p>JET_errPermissionDenied</p> | <p>La tabla no se puede escribir. Esto puede devolverse si la base de datos se abrió en modo de solo lectura.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La transacción es una transacción de solo lectura.</p> | 



#### <a name="remarks"></a>Comentarios

Llamar [a JetDeleteColumn](./jetdeletecolumn-function.md) es idéntico a llamar **a JetDeleteColumn2** con *grbit* establecido en cero (0).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa <strong>como JetDeleteColumn2W</strong> (Unicode) y <strong>JetDeleteColumn2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)

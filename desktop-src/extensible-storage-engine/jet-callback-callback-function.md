---
description: 'Más información sobre: JET_CALLBACK de devolución de llamada'
title: JET_CALLBACK de devolución de llamada
TOCTitle: JET_CALLBACK Callback Function
ms:assetid: d15d4f84-8378-4b4b-9b8b-e89a56be5ead
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294098(v=EXCHG.10)
ms:contentKeyID: 32765713
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8a49c63a948cd25abe97dfc58e10a97720eae248
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986168"
---
# <a name="jet_callback-callback-function"></a>JET_CALLBACK de devolución de llamada


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_callback-callback-function"></a>JET_CALLBACK de devolución de llamada

La **JET_CALLBACK** es una función de devolución de llamada multipropósito que usa el motor de base de datos para informar a la aplicación de un evento que implica desfragmentación en línea y notificaciones de estado de cursor.

Consulte [JET_CBTYP](./jet-cbtyp.md) configuración específica que se usará para los parámetros de esta función, ya que esta configuración variará en función de la opción **JET_CBTYP** seleccionada para su uso en el *parámetro cbtyp.*

```cpp
    JET_ERR JET_API* JET_CALLBACK(
      [in]                 JET_SESID sesid,
      [in]                 JET_DBID dbid,
      [in]                 JET_TABLEID tableid,
      [in]                 JET_CBTYP cbtyp,
      [in, out]            void* pvArg1,
      [in, out]            void* pvArg2,
      [in]                 void* pvContext,
      [in]                 JET_API_PTR ulUnused
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión para la que se realiza la devolución de llamada.

*Dbid*

Base de datos para la que se realiza la devolución de llamada.

*tableid*

Cursor para el que se realiza la devolución de llamada.

*cbtyp*

Punto de la operación en la que se realiza la devolución de llamada. Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener una lista de valores y el significado de los parámetros siguientes en cada caso.

*pvArg1*

Parámetro que se usa para comunicarse con la aplicación mediante la devolución de llamada. Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso de este parámetro para cada devolución de llamada compatible con el motor de base de datos.

*pvArg2*

Parámetro que se usa para comunicarse con la aplicación mediante la devolución de llamada. Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso de este parámetro para cada devolución de llamada compatible con el motor de base de datos.

*pvContext*

Parámetro que se usa para comunicarse con la aplicación mediante la devolución de llamada. Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso de este parámetro para cada devolución de llamada compatible con el motor de base de datos.

*ulUnused*

Parámetro que se usa para comunicarse con la aplicación mediante la devolución de llamada. Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso de este parámetro para cada devolución de llamada compatible con el motor de base de datos.

#### <a name="return-value"></a>Valor devuelto

La función devuelve uno de los códigos de [error extensibles Storage Engine](./extensible-storage-engine-error-codes.md). Para obtener información sobre cómo devolver estos códigos como HSULT, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md). Si se ejecuta correctamente, la operación que emitió la devolución de llamada puede continuar con normalidad. En algunos casos, la devolución de llamada puede devolver una advertencia que influye en esa operación. Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso de estas advertencias por la operación.

En caso de error, la operación que emitió la devolución de llamada puede continuar con normalidad o puede producir un error. Vea [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso del código de error por la operación.

#### <a name="remarks"></a>Observaciones

Si la devolución de llamada pasa un cursor a la aplicación, es importante saber que este cursor se limita intencionadamente a un conjunto más pequeño de funcionalidades para evitar la recursividad y otras características. Se permiten las siguientes operaciones:

  - [JetDupCursor](./jetdupcursor-function.md)

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetCurrentIndex](./jetgetcurrentindex-function.md)

  - [JetGetCursorInfo](./jetgetcursorinfo-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordPosition](./jetgetrecordposition-function.md)

  - [JetGetSecondaryIndexBookmark](./jetgetsecondaryindexbookmark-function.md)

  - [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)

  - [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetRegisterCallback](./jetregistercallback-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetSetLS](./jetsetls-function.md)

  - [JetUnregisterCallback](./jetunregistercallback-function.md)

Al diseñar la devolución de llamada, tiene en cuenta que, incluso con estas restricciones, todavía es posible que se pueda producir un error en la devolución de llamada.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_API_PTR](./jet-api-ptr.md)  
[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_CBTYP](./jet-cbtyp.md)

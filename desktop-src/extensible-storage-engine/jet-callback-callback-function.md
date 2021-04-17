---
description: 'Más información acerca de: JET_CALLBACK función de devolución de llamada'
title: JET_CALLBACK función de devolución de llamada
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
ms.openlocfilehash: 5e6d26bd5e347757fce270d5f2c78ab471755c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677500"
---
# <a name="jet_callback-callback-function"></a>JET_CALLBACK función de devolución de llamada


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_callback-callback-function"></a>JET_CALLBACK función de devolución de llamada

La función **JET_CALLBACK** es una función de devolución de llamada de varios propósitos utilizada por el motor de base de datos para informar a la aplicación de un evento que implique las notificaciones de estado de cursor y desfragmentación en línea.

Vea [JET_CBTYP](./jet-cbtyp.md) para ver la configuración específica para los parámetros de esta función, ya que estas opciones variarán en función de la opción **JET_CBTYP** seleccionada para su uso en el parámetro *CBTYP* .

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

*DBID*

La base de datos para la que se realiza la devolución de llamada.

*TABLEID*

Cursor para el que se realiza la devolución de llamada.

*cbtyp*

Punto de la operación en el que se realiza la devolución de llamada. Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener una lista de valores y el significado de los parámetros siguientes en cada caso.

*pvArg1*

Parámetro que se usa para comunicarse con la aplicación mediante la devolución de llamada. Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso de este parámetro para cada devolución de llamada admitida por el motor de base de datos.

*pvArg2*

Parámetro que se usa para comunicarse con la aplicación mediante la devolución de llamada. Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso de este parámetro para cada devolución de llamada admitida por el motor de base de datos.

*pvContext*

Parámetro que se usa para comunicarse con la aplicación mediante la devolución de llamada. Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso de este parámetro para cada devolución de llamada admitida por el motor de base de datos.

*ulUnused*

Parámetro que se usa para comunicarse con la aplicación mediante la devolución de llamada. Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso de este parámetro para cada devolución de llamada admitida por el motor de base de datos.

#### <a name="return-value"></a>Valor devuelto

La función devuelve uno de los [códigos de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md). Para obtener información sobre cómo devolver estos códigos como valores HRESULT, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md). Si se ejecuta correctamente, la operación que emitió la devolución de llamada puede continuar con normalidad. En algunos casos, la devolución de llamada puede devolver una advertencia que influye en esa operación. Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso de estas advertencias en la operación.

En caso de error, la operación que ha emitido la devolución de llamada puede continuar normalmente o puede producir un error. Consulte [JET_CBTYP](./jet-cbtyp.md) para obtener información sobre el uso del código de error en la operación.

#### <a name="remarks"></a>Observaciones

Si la devolución de llamada pasa un cursor a la aplicación, es importante saber que este cursor está limitado intencionadamente a un conjunto más pequeño de funciones para evitar la recursividad y otros ugliness. Se permiten las siguientes operaciones:

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

Al diseñar la devolución de llamada, tenga en cuenta que incluso con estas restricciones, todavía es posible que se produzca un error en la devolución de llamada.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_API_PTR](./jet-api-ptr.md)  
[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_CBTYP](./jet-cbtyp.md)

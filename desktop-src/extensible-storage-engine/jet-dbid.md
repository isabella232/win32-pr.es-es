---
description: 'Más información acerca de: JET_DBID'
title: JET_DBID
TOCTitle: JET_DBID
ms:assetid: 516acb79-aa75-4609-81b6-3b2e4e0c95af
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269248(v=EXCHG.10)
ms:contentKeyID: 32765550
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
ms.openlocfilehash: fe3a8ccd813ececcb42388c7d577f78e9055d5b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809680"
---
# <a name="jet_dbid"></a>JET_DBID


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_dbid"></a>JET_DBID

El tipo de datos **JET_DBID** contiene el identificador de la base de datos. Un identificador de base de datos se utiliza para administrar el esquema de una base de datos. También se puede usar para administrar las tablas dentro de esa base de datos.

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a>Tipo de datos

JET_DBID

Identificador de la base de datos.

Un valor de JET_dbidNil indica que el identificador no es válido.

### <a name="remarks"></a>Observaciones

Un identificador de base de datos se crea mediante una llamada a [JetCreateDatabase](./jetcreatedatabase-function.md) o [JetOpenDatabase](./jetopendatabase-function.md).

Un identificador de base de datos se puede cerrar explícitamente con [JetCloseDatabase](./jetclosedatabase-function.md) o cerrarse implícitamente mediante [JetEndSession](./jetendsession-function.md) o [JetTerm](./jetterm-function.md).

Un identificador de base de datos solo se puede usar dentro de la sesión en la que se creó. La existencia de un identificador de base de datos corresponde al abierto lógico de una base de datos. Una apertura lógica es diferente de la abierta física de una base de datos, que se produce cuando se adjunta una base de datos al sistema.

### <a name="requirements"></a>Requisitos

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

[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetEndSession](./jetendsession-function.md)

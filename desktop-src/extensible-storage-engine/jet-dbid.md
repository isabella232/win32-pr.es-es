---
description: 'Más información sobre: JET_DBID'
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
ms.openlocfilehash: 988dd14ca96a5818254602b5ab6dcaeab4952669
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470911"
---
# <a name="jet_dbid"></a>JET_DBID


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_dbid"></a>JET_DBID

El **JET_DBID** tipo de datos contiene el identificador de la base de datos. Un identificador de base de datos se usa para administrar el esquema de una base de datos. También se puede usar para administrar las tablas dentro de esa base de datos.

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a>Tipo de datos

JET_DBID

Identificador de la base de datos.

Un valor de JET_dbidNil indica que el identificador no es válido.

### <a name="remarks"></a>Comentarios

Un identificador de base de datos se crea mediante una llamada a [JetCreateDatabase](./jetcreatedatabase-function.md) o [JetOpenDatabase.](./jetopendatabase-function.md)

[JetCloseDatabase](./jetclosedatabase-function.md) puede cerrar explícitamente un identificador de base de datos o cerrarlo implícitamente [JetEndSession](./jetendsession-function.md) [o JetTerm.](./jetterm-function.md)

Un identificador de base de datos solo se puede usar dentro de la sesión en la que se creó. La existencia de un identificador de base de datos corresponde a la apertura lógica de una base de datos. Una apertura lógica es diferente de la apertura física de una base de datos, lo que sucede cuando una base de datos está asociada al sistema.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetEndSession](./jetendsession-function.md)

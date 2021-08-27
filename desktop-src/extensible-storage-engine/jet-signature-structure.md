---
description: 'Más información sobre: JET_SIGNATURE estructura'
title: JET_SIGNATURE estructura
TOCTitle: JET_SIGNATURE Structure
ms:assetid: 90d3fd56-be65-4126-b50c-b53e3c3f38f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269340(v=EXCHG.10)
ms:contentKeyID: 32765629
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
ms.openlocfilehash: da4684872358d9d6751812b2adb2b2bea819a2e3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476481"
---
# <a name="jet_signature-structure"></a>JET_SIGNATURE estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_signature-structure"></a>JET_SIGNATURE estructura

La **JET_SIGNATURE** contiene información que identifica de forma única una base de datos.

```cpp
    typedef struct {
      unsigned long ulRandom;
      JET_LOGTIME logtimeCreate;
      char szComputerName[JET_MAX_COMPUTERNAME_LENGTH + 1];
    } JET_SIGNATURE;
```

### <a name="members"></a>Miembros

**ulRandom**

Número asignado aleatoriamente.

**logtimeCreate**

El [JET_LOGTIME](./jet-logtime-structure.md) en el momento de [ejecutar JetCreateDatabase.](./jetcreatedatabase-function.md)

**szComputerName**

Valor de cadena opcional del nombre NetBIOS del equipo. Este valor no se puede establecer.

### <a name="remarks"></a>Comentarios

Se puede encontrar como un elemento de [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)

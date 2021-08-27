---
description: 'Más información sobre: JET_SIGNATURE structure'
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
ms.openlocfilehash: 456eadecbaba7295753a18ec2ca739f5e3fc8391
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987828"
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

Valor de cadena opcional del nombre NetBIOS del equipo. Es posible que no se establezca este valor.

### <a name="remarks"></a>Observaciones

Se puede encontrar como un elemento de [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)

---
description: 'Más información sobre: JET_LGPOS estructura'
title: JET_LGPOS estructura
TOCTitle: JET_LGPOS Structure
ms:assetid: dbce1a60-b32b-40c1-a215-e93bb77cd8c1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294113(v=EXCHG.10)
ms:contentKeyID: 32765727
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
ms.openlocfilehash: e3e83786236a95cf2b0c4d77e26e6987334a5b00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964300"
---
# <a name="jet_lgpos-structure"></a>JET_LGPOS estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_lgpos-structure"></a>JET_LGPOS estructura

La **JET_LGPOS** contiene datos internos del mecanismo de registro del motor de base de datos. Esta estructura se considera interna.

```cpp
    typedef struct {
      unsigned short ib;
      unsigned short isec;
      long lGeneration;
    } JET_LGPOS;
```

### <a name="members"></a>Members

**Ib**

Admite la infraestructura ese y no se puede usar desde el código.

**Isec**

Admite la infraestructura ese y no se puede usar desde el código.

**lGeneration**

Admite la infraestructura ese y no se puede usar desde el código.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)

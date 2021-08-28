---
description: 'Más información sobre: JET_BKINFO estructura'
title: JET_BKINFO estructura
TOCTitle: JET_BKINFO Structure
ms:assetid: dfaf1d72-1d5f-4777-91c1-6affb735b092
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294120(v=EXCHG.10)
ms:contentKeyID: 32765734
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
ms.openlocfilehash: e859d34a610ddcff0431b7395d11c72b01fb8bb7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985288"
---
# <a name="jet_bkinfo-structure"></a>JET_BKINFO estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_bkinfo-structure"></a>JET_BKINFO estructura

La **JET_BKINFO** contiene una colección de datos sobre un evento de copia de seguridad específico.

```cpp
    typedef struct {
      JET_LGPOS lgposMark;
      union {
        JET_LOGTIME logtimeMark;
        JET_BKLOGTIME bklogtimeMark;
      };
      unsigned long genLow;
      unsigned long genHigh;
    } JET_BKINFO;
```

### <a name="members"></a>Miembros

**lgposMark**

Identificador de esta copia de seguridad.

**logtimeMark**

Hora de este evento de copia de seguridad.

**bklogtimeMark**

Hora de este evento de copia de seguridad, con bits adicionales para indicar una copia de seguridad de instantáneas.

**Windows Vista: bklogtimeMark** se presenta en Windows Vista.

**genLow**

Número de generación de registros bajo asociado a este evento de copia de seguridad.

**genHigh**

Número de generación de registros alto asociado a este evento de copia de seguridad.

### <a name="remarks"></a>Observaciones

Esta estructura se usa dentro de la estructura [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) para representar datos sobre el evento de copia de seguridad de la base de datos.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_BKLOGTIME](./jet-bklogtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)

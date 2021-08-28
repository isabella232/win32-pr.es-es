---
description: 'Más información sobre: JET_OSSNAPID'
title: JET_OSSNAPID
TOCTitle: JET_OSSNAPID
ms:assetid: 89b15492-674a-46e4-8aea-991df4f22a6f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269325(v=EXCHG.10)
ms:contentKeyID: 32765615
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
ms.openlocfilehash: 82be9a4aa00f1880493d81dbcd53d1d8d76cc46a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983808"
---
# <a name="jet_ossnapid"></a>JET_OSSNAPID


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_ossnapid"></a>JET_OSSNAPID

El **JET_OSSNAPID** de datos contiene un identificador para una instantánea de la base de datos.

```cpp
    typedef JET_API_PTR JET_OSSNAPID;
```

### <a name="data-types"></a>Tipo de datos

JET_OSSNAPID

Identificador de una instantánea de la base de datos. Este identificador se usa en elementos de la API jet que están implicados en la copia de seguridad de instantáneas.

**NULL** se puede usar para indicar un identificador no válido.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



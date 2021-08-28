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
ms.openlocfilehash: d6185f17c16cbdb2a45e172a14af346c3519aa12
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468372"
---
# <a name="jet_ossnapid"></a>JET_OSSNAPID


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_ossnapid"></a>JET_OSSNAPID

El **JET_OSSNAPID** tipo de datos contiene un identificador para una instantánea de la base de datos.

```cpp
    typedef JET_API_PTR JET_OSSNAPID;
```

### <a name="data-types"></a>Tipo de datos

JET_OSSNAPID

Identificador de una instantánea de la base de datos. Este identificador se usa en los elementos de la API de JET que están implicados en la copia de seguridad de instantáneas.

**NULL** se puede usar para indicar un identificador no válido.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



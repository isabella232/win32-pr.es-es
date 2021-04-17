---
description: Miembros de CMSPCallMultiGraph
ms.assetid: 49451585-3084-4426-8617-79b60eb77518
title: Miembros de CMSPCallMultiGraph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ee556efbbdaf679e292b6b3a33b4b0a0b6616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677946"
---
# <a name="cmspcallmultigraph-members"></a>Miembros de CMSPCallMultiGraph

``` syntax
CMSPArray <THREADPOOLWAITBLOCK>     m_ThreadPoolWaitBlocks;
```

Los bloques de espera almacenan la información sobre la espera registrada en el grupo de subprocesos. Incluye los identificadores de espera devueltos por la llamada [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) y un puntero a la estructura de contexto. Cada bloque de la matriz es para un gráfico en uno de los objetos de secuencia. El desplazamiento de un bloque en esta matriz es el mismo que el desplazamiento de la secuencia que posee el gráfico.

 

 

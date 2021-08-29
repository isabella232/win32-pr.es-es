---
title: Afinidad del procesador en WOW64
description: Los procesadores de 32 Windows admiten un máximo de 32 procesadores. Por lo tanto, funciones como GetProcessAffinityMask simulan un equipo con 32 procesadores cuando se llama en WOW64.
ms.assetid: f50a03e8-1c23-4eb0-a1ff-471c28d6b611
keywords:
- afinidad de procesador de 64 bits Windows programación
- WOW64 64 bits de programación Windows , afinidad de procesador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09cfb3aaaa676bf14d8810a6d73b210236a8fba39ad8274d1e04538dd743e2b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643325"
---
# <a name="processor-affinity-under-wow64"></a>Afinidad del procesador en WOW64

Los procesadores de 32 Windows admiten un máximo de 32 procesadores. Por lo tanto, funciones como [**GetProcessAffinityMask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) simulan un equipo con 32 procesadores cuando se llama en WOW64.

La máscara de afinidad se obtiene realizando una operación OR bit a bit de los 32 bits superiores de la máscara con los 32 bits inferiores. Por lo tanto, si un subproceso tiene afinidad para los procesadores 0, 1 y 32, WOW64 notifica la afinidad como 0 y 1, porque el procesador 32 se asigna al procesador 0. Las funciones que establecen la afinidad del procesador, [**como SetThreadAffinityMask,**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask)restringen los procesadores a los primeros 32 procesadores en WOW64.

Para obtener más información sobre la afinidad de procesador, vea [Varios procesadores.](/windows/desktop/ProcThread/multiple-processors)

 

 
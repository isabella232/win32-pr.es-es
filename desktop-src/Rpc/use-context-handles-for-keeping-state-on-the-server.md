---
title: Usar identificadores de contexto para mantener el estado en el servidor
description: Usar identificadores de contexto para mantener el estado en el servidor
ms.assetid: ee511745-04cf-445d-a02b-41734aabc193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90bf14632ed1821a1a097a64951f6ca9aef751d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268834"
---
# <a name="use-context-handles-for-keeping-state-on-the-server"></a><span data-ttu-id="d22e9-103">Usar identificadores de contexto para mantener el estado en el servidor</span><span class="sxs-lookup"><span data-stu-id="d22e9-103">Use Context Handles for Keeping State on the Server</span></span>

<span data-ttu-id="d22e9-104">**Procedimiento recomendado:** Cuando el estado se mantiene en el servidor entre llamadas, use los identificadores de contexto.</span><span class="sxs-lookup"><span data-stu-id="d22e9-104">**Best practice:** Whenever state is kept on the server between calls, use context handles.</span></span>

<span data-ttu-id="d22e9-105">Los identificadores de contexto suelen intimidar a los nuevos programadores de RPC y es posible que la sobrecarga de los identificadores de contexto de aprendizaje no parezca inicialmente merecente del esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="d22e9-105">Context handles are often intimidating for new RPC programmers, and the overhead of learning context handles may not initially appear worth the effort.</span></span> <span data-ttu-id="d22e9-106">Merece la pena porque los identificadores de contexto tienen soluciones integradas para muchos problemas comunes que se producen en la programación de red que, de lo contrario, tendrían que implementarse desde el principio.</span><span class="sxs-lookup"><span data-stu-id="d22e9-106">It is worth it because context handles have built-in solutions for many common pitfalls encountered in network programming that otherwise would have to be implemented from scratch.</span></span> <span data-ttu-id="d22e9-107">La descripción de los identificadores de contexto paga los dividendos más adelante.</span><span class="sxs-lookup"><span data-stu-id="d22e9-107">Understanding context handles pays dividends later.</span></span>

 

 





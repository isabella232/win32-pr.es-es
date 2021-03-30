---
title: Usar variación natural
description: Usar variación natural
ms.assetid: 5d5750e4-cf30-43dc-9419-7e6bbdb9aa5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd2d35afeb168dc8839ba259f0079434b487c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148773"
---
# <a name="use-natural-variation"></a><span data-ttu-id="7a605-103">Usar variación natural</span><span class="sxs-lookup"><span data-stu-id="7a605-103">Use Natural Variation</span></span>

<span data-ttu-id="7a605-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7a605-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="7a605-105">Mientras que la coherencia de la presentación en la interfaz convencional de la aplicación, como los menús y los cuadros de diálogo, hace que la interfaz sea más predecible, varíe la animación y la salida de voz en la interfaz del carácter.</span><span class="sxs-lookup"><span data-stu-id="7a605-105">While consistency of presentation in your application's conventional interface, such as menus and dialog boxes, makes the interface more predictable, vary the animation and spoken output in the character's interface.</span></span> <span data-ttu-id="7a605-106">La variación adecuada de las respuestas del carácter proporciona una interfaz más natural.</span><span class="sxs-lookup"><span data-stu-id="7a605-106">Appropriately varying the character's responses provides a more natural interface.</span></span> <span data-ttu-id="7a605-107">Si un carácter siempre dirige exactamente al usuario de la misma manera; por ejemplo, siempre diciendo las mismas palabras, es probable que el usuario tenga en cuenta el carácter aburrido, disinterested o, incluso, a la fuerza.</span><span class="sxs-lookup"><span data-stu-id="7a605-107">If a character always addresses the user exactly the same way; for example, always saying the same words, the user is likely to consider the character boring, disinterested, or even rude.</span></span> <span data-ttu-id="7a605-108">La comunicación humana rara vez implica una repetición precisa.</span><span class="sxs-lookup"><span data-stu-id="7a605-108">Human communication rarely involves precise repetition.</span></span> <span data-ttu-id="7a605-109">Incluso cuando se repite algo en una situación similar, podríamos cambiar el texto, gestos o expresiones faciales.</span><span class="sxs-lookup"><span data-stu-id="7a605-109">Even when repeating something in a similar situation, we may change wording, gestures, or facial expression.</span></span>

<span data-ttu-id="7a605-110">El agente de Microsoft le permite compilar en una variación de un carácter.</span><span class="sxs-lookup"><span data-stu-id="7a605-110">Microsoft Agent enables you to build in some variation for a character.</span></span> <span data-ttu-id="7a605-111">Al definir animaciones de un carácter, puede usar las probabilidades de bifurcación en cualquier fotograma de animación para cambiar una animación cuando se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="7a605-111">When defining a character's animations, you can use branching probabilities on any animation frame to change an animation when it plays.</span></span> <span data-ttu-id="7a605-112">También puede asignar varias animaciones a cada Estado.</span><span class="sxs-lookup"><span data-stu-id="7a605-112">You can also assign multiple animations to each state.</span></span> <span data-ttu-id="7a605-113">El agente de Microsoft elige aleatoriamente una de las animaciones asignadas cada vez que inicia un estado.</span><span class="sxs-lookup"><span data-stu-id="7a605-113">Microsoft Agent randomly chooses one of the assigned animations each time it initiates a state.</span></span> <span data-ttu-id="7a605-114">En el caso de la salida de voz, también puede incluir caracteres de barra vertical en el texto de salida para modificar automáticamente el texto que se habla.</span><span class="sxs-lookup"><span data-stu-id="7a605-114">For speech output, you can also include vertical bar characters in your output text to automatically vary the text spoken.</span></span> <span data-ttu-id="7a605-115">Por ejemplo, el agente de Microsoft seleccionará aleatoriamente una de las instrucciones siguientes al procesar este texto como parte del método [**Speak**](speak-method.md) :</span><span class="sxs-lookup"><span data-stu-id="7a605-115">For example, Microsoft Agent will randomly select one of the following statements when processing this text as part of the [**Speak**](speak-method.md) method:</span></span>

<span data-ttu-id="7a605-116">"Puedo decir esto. \| Lo puedo decir. \| Puedo decir algo más ".</span><span class="sxs-lookup"><span data-stu-id="7a605-116">"I can say this.\|I can say that.\|I can say something else."</span></span>

 

 





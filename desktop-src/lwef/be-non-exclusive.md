---
title: No es exclusivo
description: No es exclusivo
ms.assetid: 7a44840d-6bf9-4c12-ba14-66d7067a984d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b637bcf0860ccc4917b1af344664f9828b0da8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418532"
---
# <a name="be-non-exclusive"></a><span data-ttu-id="92eae-103">No es exclusivo</span><span class="sxs-lookup"><span data-stu-id="92eae-103">Be Non-Exclusive</span></span>

<span data-ttu-id="92eae-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="92eae-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="92eae-105">Los caracteres interactivos se pueden emplear en la interfaz de usuario como asistentes, guías, artistas, narradores, agentes de ventas o en otros roles.</span><span class="sxs-lookup"><span data-stu-id="92eae-105">Interactive characters can be employed in the user interface as assistants, guides, entertainers, storytellers, sales agents, or in a variety of other roles.</span></span> <span data-ttu-id="92eae-106">Un carácter que realice automáticamente o que ayude no debe diseñarse de forma contraria al principio de diseño de mantener el control del usuario.</span><span class="sxs-lookup"><span data-stu-id="92eae-106">A character that automatically performs or assists should not be designed contrary to the design principle of keeping the user in control.</span></span> <span data-ttu-id="92eae-107">Al agregar un carácter a la interfaz de un sitio web o aplicación convencional, use el carácter como una mejora, en lugar de reemplazar la interfaz principal.</span><span class="sxs-lookup"><span data-stu-id="92eae-107">When adding a character to the interface of a website or conventional application, use the character as an enhancement, rather than a replacement of, the primary interface.</span></span> <span data-ttu-id="92eae-108">Evite implementar cualquier característica u operación que requiera exclusivamente un carácter.</span><span class="sxs-lookup"><span data-stu-id="92eae-108">Avoid implementing any feature or operation that exclusively requires a character.</span></span>

<span data-ttu-id="92eae-109">Del mismo modo, permita que el usuario elija Cuándo desea interactuar con el carácter.</span><span class="sxs-lookup"><span data-stu-id="92eae-109">Similarly, let the user choose when they want to interact with your character.</span></span> <span data-ttu-id="92eae-110">Un usuario debe poder descartar el carácter y hacer que se devuelva solo con el permiso del usuario.</span><span class="sxs-lookup"><span data-stu-id="92eae-110">A user should be able to dismiss the character and have it return only with the user's permission.</span></span> <span data-ttu-id="92eae-111">Forzar la interacción de los caracteres en los usuarios puede tener un efecto negativo grave.</span><span class="sxs-lookup"><span data-stu-id="92eae-111">Forcing character interaction on users can have a serious negative effect.</span></span> <span data-ttu-id="92eae-112">Para admitir el control de usuario de la interacción de caracteres, Microsoft Agent incluye automáticamente comandos para ocultar y mostrar.</span><span class="sxs-lookup"><span data-stu-id="92eae-112">To support user control of character interaction, Microsoft Agent automatically includes Hide and Show commands.</span></span> <span data-ttu-id="92eae-113">La API de Microsoft Agent también admite estos métodos, por lo que puede incluir compatibilidad con estas funciones en su propia interfaz.</span><span class="sxs-lookup"><span data-stu-id="92eae-113">The Microsoft Agent API also supports these methods, so you can include support for these functions in your own interface.</span></span> <span data-ttu-id="92eae-114">Además, la interfaz de usuario de Microsoft Agent incluye propiedades globales que permiten al usuario invalidar ciertas opciones de salida de caracteres.</span><span class="sxs-lookup"><span data-stu-id="92eae-114">In addition, Microsoft Agent's user interface includes global properties that enable the user to override certain character output options.</span></span> <span data-ttu-id="92eae-115">Para asegurarse de que se mantienen las preferencias del usuario, estas propiedades no se pueden invalidar a través de la API.</span><span class="sxs-lookup"><span data-stu-id="92eae-115">To ensure that the user's preferences are maintained, these properties cannot be overridden through the API.</span></span>

 

 





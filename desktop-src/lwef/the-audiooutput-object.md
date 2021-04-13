---
title: El objeto AudioOutput
description: El objeto AudioOutput
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919b435edf31b6ae24a8b5c6977d5aed542efac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420710"
---
# <a name="the-audiooutput-object"></a><span data-ttu-id="e4983-103">El objeto AudioOutput</span><span class="sxs-lookup"><span data-stu-id="e4983-103">The AudioOutput Object</span></span>

<span data-ttu-id="e4983-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e4983-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="e4983-105">Este objeto proporciona acceso a las propiedades de salida de audio mantenidas por el servidor.</span><span class="sxs-lookup"><span data-stu-id="e4983-105">This object provides access to audio output properties maintained by the server.</span></span> <span data-ttu-id="e4983-106">Las propiedades son de solo lectura, pero el usuario puede cambiarlas en la hoja de propiedades de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e4983-106">The properties are read-only, but the user can change them in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="e4983-107">Si declara una variable de objeto de tipo [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), no podrá tener acceso a todas las propiedades del objeto [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) .</span><span class="sxs-lookup"><span data-stu-id="e4983-107">If you declare an object variable of type [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), you will not be able to access all properties for the [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) object.</span></span> <span data-ttu-id="e4983-108">Aunque el agente también admite [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), esta última interfaz se proporciona solo para la compatibilidad con versiones anteriores y solo admite esas propiedades en versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="e4983-108">While Agent also supports [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), this latter interface is provided only for backward compatibility and supports only those properties in previous releases.</span></span>

-   [<span data-ttu-id="e4983-109">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="e4983-109">**Enabled**</span></span>](enabled-property-ao.md)
-   [<span data-ttu-id="e4983-110">**SoundEffects**</span><span class="sxs-lookup"><span data-stu-id="e4983-110">**SoundEffects**</span></span>](soundeffects-property.md)
-   [<span data-ttu-id="e4983-111">**Status**</span><span class="sxs-lookup"><span data-stu-id="e4983-111">**Status**</span></span>](status-property.md)

 

 
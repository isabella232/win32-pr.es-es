---
title: El objeto SpeechInput
description: El objeto SpeechInput
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1671a3f3e37b0de16b42129921337ee855b58c14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994382"
---
# <a name="the-speechinput-object"></a><span data-ttu-id="0a8ad-103">El objeto SpeechInput</span><span class="sxs-lookup"><span data-stu-id="0a8ad-103">The SpeechInput Object</span></span>

<span data-ttu-id="0a8ad-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0a8ad-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="0a8ad-105">El objeto [**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) proporciona acceso a las propiedades de entrada de voz mantenidas por el servidor del agente.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-105">The [**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) object provides access to the speech input properties maintained by the Agent server.</span></span> <span data-ttu-id="0a8ad-106">Las propiedades son de solo lectura para las aplicaciones cliente, pero el usuario puede cambiarlas en la hoja de propiedades de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-106">The properties are read-only for client applications, but the user can change them in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="0a8ad-107">El servidor solo devuelve valores si se ha instalado un motor de voz compatible y está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-107">The server returns values only if a compatible speech engine has been installed and is enabled.</span></span>

<span data-ttu-id="0a8ad-108">Ya no se admiten las propiedades [**Engine**](https://www.bing.com/search?q=**Engine**), [**installed**](https://www.bing.com/search?q=**Installed**)y [**Language**](https://www.bing.com/search?q=**Language**) , pero (por compatibilidad con versiones anteriores) devuelven valores NULL si se consultan.</span><span class="sxs-lookup"><span data-stu-id="0a8ad-108">The [**Engine**](https://www.bing.com/search?q=**Engine**), [**Installed**](https://www.bing.com/search?q=**Installed**), and [**Language**](https://www.bing.com/search?q=**Language**) properties are no longer supported, but (for backward compatibility) return null values if queried.</span></span> <span data-ttu-id="0a8ad-109">Para consultar o establecer el modo de reconocimiento de voz, use la propiedad [**SRModeID**](srmodeid-property.md) .</span><span class="sxs-lookup"><span data-stu-id="0a8ad-109">To query or set a speech recognition's mode, use the [**SRModeID**](srmodeid-property.md) property.</span></span>

-   [<span data-ttu-id="0a8ad-110">Propiedades de SpeechInput</span><span class="sxs-lookup"><span data-stu-id="0a8ad-110">SpeechInput Properties</span></span>](speechinput-properties.md)

 

 





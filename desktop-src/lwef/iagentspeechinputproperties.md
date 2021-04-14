---
title: IAgentSpeechInputProperties
description: IAgentSpeechInputProperties
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c6a83ed488d3ff95914c25fd518862740951ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418324"
---
# <a name="iagentspeechinputproperties"></a><span data-ttu-id="65354-103">IAgentSpeechInputProperties</span><span class="sxs-lookup"><span data-stu-id="65354-103">IAgentSpeechInputProperties</span></span>

<span data-ttu-id="65354-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="65354-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="65354-105">IAgentSpeechInputProperties proporciona acceso a las propiedades de entrada de voz mantenidas por el servidor.</span><span class="sxs-lookup"><span data-stu-id="65354-105">IAgentSpeechInputProperties provides access to the speech input properties maintained by the server.</span></span> <span data-ttu-id="65354-106">La mayoría de las propiedades son de solo lectura para las aplicaciones cliente, pero el usuario puede cambiarlas en la hoja de propiedades de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="65354-106">Most of the properties are read-only for client applications, but the user can change them in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="65354-107">El servidor de agente de Microsoft solo devuelve valores si se ha instalado un motor de voz compatible y está habilitado.</span><span class="sxs-lookup"><span data-stu-id="65354-107">The Microsoft Agent server returns values only if a compatible speech engine has been installed and is enabled.</span></span> <span data-ttu-id="65354-108">Al consultar estas propiedades se intenta iniciar el motor de voz.</span><span class="sxs-lookup"><span data-stu-id="65354-108">Querying these properties attempts to start the speech engine.</span></span>

<span data-ttu-id="65354-109">**Métodos en orden de Vtable**</span><span class="sxs-lookup"><span data-stu-id="65354-109">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="65354-110">Métodos IAgentSpeechInputProperties</span><span class="sxs-lookup"><span data-stu-id="65354-110">IAgentSpeechInputProperties Methods</span></span>                                     | <span data-ttu-id="65354-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="65354-111">Description</span></span>                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="65354-112">**GetEnabled**</span><span class="sxs-lookup"><span data-stu-id="65354-112">**GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)           | <span data-ttu-id="65354-113">Devuelve si el motor de reconocimiento de voz está habilitado.</span><span class="sxs-lookup"><span data-stu-id="65354-113">Returns whether the speech recognition engine is enabled.</span></span> |
| [<span data-ttu-id="65354-114">**GetHotKey**</span><span class="sxs-lookup"><span data-stu-id="65354-114">**GetHotKey**</span></span>](iagentspeechinputproperties--gethotkey.md)             | <span data-ttu-id="65354-115">Devuelve la asignación de clave actual de la clave de escucha.</span><span class="sxs-lookup"><span data-stu-id="65354-115">Returns the current key assignment of the Listening key.</span></span>  |
| [<span data-ttu-id="65354-116">**GetListeningTip**</span><span class="sxs-lookup"><span data-stu-id="65354-116">**GetListeningTip**</span></span>](iagentspeechinputproperties--getlisteningtip.md) | <span data-ttu-id="65354-117">Devuelve si la sugerencia de escucha está habilitada.</span><span class="sxs-lookup"><span data-stu-id="65354-117">Returns whether the Listening Tip is enabled.</span></span>             |



 

<span data-ttu-id="65354-118">Los métodos [**GetInstalled**](https://www.bing.com/search?q=**GetInstalled**), [**GetLCID**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**)y [**SetEngine**](https://www.bing.com/search?q=**SetEngine**) (que se admiten en versiones anteriores de Microsoft Agent) todavía se admiten por razones de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="65354-118">[**GetInstalled**](https://www.bing.com/search?q=**GetInstalled**), [**GetLCID**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**), and [**SetEngine**](https://www.bing.com/search?q=**SetEngine**) methods (supported in earlier versions of Microsoft Agent) are still supported for backward compatibility.</span></span> <span data-ttu-id="65354-119">Sin embargo, los métodos no tienen stub y no devuelven valores útiles.</span><span class="sxs-lookup"><span data-stu-id="65354-119">However, the methods are not stubbed and do not return useful values.</span></span> <span data-ttu-id="65354-120">Use [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) y [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) para consultar y establecer el motor de reconocimiento de voz que se va a usar con el carácter.</span><span class="sxs-lookup"><span data-stu-id="65354-120">Use [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) and [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) to query and set the speech recognition engine to be used with the character.</span></span> <span data-ttu-id="65354-121">Tenga en cuenta que el motor debe coincidir con la configuración de idioma actual del carácter.</span><span class="sxs-lookup"><span data-stu-id="65354-121">Keep in mind that the engine must match the character's current language setting.</span></span>

 

 





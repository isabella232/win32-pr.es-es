---
title: IAgentCharacterEx GetActive
description: IAgentCharacterEx GetActive
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1dab89ee9ba89c5982e34844917334d97169b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903730"
---
# <a name="iagentcharacterexgetactive"></a><span data-ttu-id="f9384-103">IAgentCharacterEx::GetActive</span><span class="sxs-lookup"><span data-stu-id="f9384-103">IAgentCharacterEx::GetActive</span></span>

<span data-ttu-id="f9384-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f9384-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

<span data-ttu-id="f9384-105">Recupera si la aplicación cliente es el cliente activo del carácter y si el carácter es superior.</span><span class="sxs-lookup"><span data-stu-id="f9384-105">Retrieves whether your client application is the active client of the character and whether the character is topmost.</span></span>

-   <span data-ttu-id="f9384-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f9384-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f9384-107"><span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*</span><span class="sxs-lookup"><span data-stu-id="f9384-107"><span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*</span></span>
</dt> <dd>

<span data-ttu-id="f9384-108">Dirección de una variable que recibe uno de los siguientes valores para la configuración de estado:</span><span class="sxs-lookup"><span data-stu-id="f9384-108">Address of a variable that receives one of the following values for the state setting:</span></span>



| <span data-ttu-id="f9384-109">Value</span><span class="sxs-lookup"><span data-stu-id="f9384-109">Value</span></span>                                                              | <span data-ttu-id="f9384-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9384-110">Description</span></span>                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="f9384-111">**const unsigned short** **Activate \_ = 0;**</span><span class="sxs-lookup"><span data-stu-id="f9384-111">**const unsigned short** **ACTIVATE\_NOTACTIVE = 0;**</span></span><br/>   | <span data-ttu-id="f9384-112">El cliente no es el cliente activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="f9384-112">Your client is not the active client of the character.</span></span>                |
| <span data-ttu-id="f9384-113">**const unsigned short** **Activate \_ Active = 1;**</span><span class="sxs-lookup"><span data-stu-id="f9384-113">**const unsigned short** **ACTIVATE\_ACTIVE = 1;**</span></span><br/>      | <span data-ttu-id="f9384-114">El cliente es el cliente activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="f9384-114">Your client is the active client of the character.</span></span>                    |
| <span data-ttu-id="f9384-115">**const unsigned short** **Active \_ INPUTACTIVE = 2;**</span><span class="sxs-lookup"><span data-stu-id="f9384-115">**const unsigned short** **ACTIVATE\_INPUTACTIVE = 2;**</span></span><br/> | <span data-ttu-id="f9384-116">El cliente es de entrada-activo (cliente activo del carácter superior).</span><span class="sxs-lookup"><span data-stu-id="f9384-116">Your client is input-active (active client of the topmost character).</span></span> |



 

</dd> </dl>

<span data-ttu-id="f9384-117">Esta configuración le permite saber si es el cliente activo del carácter o si el carácter es el carácter activo de entrada.</span><span class="sxs-lookup"><span data-stu-id="f9384-117">This setting lets you know whether you are the active client of the character or whether your character is the input active character.</span></span> <span data-ttu-id="f9384-118">Cuando varias aplicaciones cliente comparten el mismo carácter, el cliente activo del carácter recibe la entrada del mouse (por ejemplo, eventos de clic o arrastre de control del agente de Microsoft).</span><span class="sxs-lookup"><span data-stu-id="f9384-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="f9384-119">Del mismo modo, cuando se muestran varios caracteres, el cliente activo del carácter superior (también conocido como cliente de entrada-activo) recibe los eventos [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="f9384-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events.</span></span>

<span data-ttu-id="f9384-120">Use el método [**Activate**](iagentcharacter--activate.md) para establecer si la aplicación es el cliente activo del carácter o para convertir la aplicación en el cliente activo de entrada (que también hace que el carácter sea más alto).</span><span class="sxs-lookup"><span data-stu-id="f9384-120">Use the [**Activate**](iagentcharacter--activate.md) method to set whether your application is the active client of the character or to make your application the input active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="f9384-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f9384-121">See Also</span></span>

<span data-ttu-id="f9384-122">[**IAgentCharacter:: Activate**](iagentcharacter--activate.md), [ **IAgentNotifySinkEx:: ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)</span><span class="sxs-lookup"><span data-stu-id="f9384-122">[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentNotifySinkEx::ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)</span></span>


 

 






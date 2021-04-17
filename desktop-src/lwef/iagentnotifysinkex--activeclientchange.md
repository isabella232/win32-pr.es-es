---
title: IAgentNotifySinkEx ActiveClientChange
description: IAgentNotifySinkEx ActiveClientChange
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96988f80d8a1799bf46f12bd38906e9357453f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704673"
---
# <a name="iagentnotifysinkexactiveclientchange"></a><span data-ttu-id="1d840-103">IAgentNotifySinkEx::ActiveClientChange</span><span class="sxs-lookup"><span data-stu-id="1d840-103">IAgentNotifySinkEx::ActiveClientChange</span></span>

<span data-ttu-id="1d840-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1d840-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ActiveClientChange(
...long dwCharID,  // character ID
   long lStatus    // active state flag
);
```

<span data-ttu-id="1d840-105">Notifica a una aplicación cliente si su cliente activo ya no es el cliente activo de un carácter.</span><span class="sxs-lookup"><span data-stu-id="1d840-105">Notifies a client application if its active client is no longer the active client of a character.</span></span>

-   <span data-ttu-id="1d840-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1d840-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="1d840-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="1d840-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="1d840-108">Identificador del carácter para el que cambió el estado de cliente activo.</span><span class="sxs-lookup"><span data-stu-id="1d840-108">Identifier of the character for which active client status changed.</span></span>

</dd> <dt>

<span data-ttu-id="1d840-109"><span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*</span><span class="sxs-lookup"><span data-stu-id="1d840-109"><span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*</span></span>
</dt> <dd>

<span data-ttu-id="1d840-110">Cambio de estado activo del cliente, que puede ser una combinación de cualquiera de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="1d840-110">Active state change of the client, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="1d840-111">Value</span><span class="sxs-lookup"><span data-stu-id="1d840-111">Value</span></span>                                                              | <span data-ttu-id="1d840-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d840-112">Description</span></span>                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="1d840-113">**const unsigned short** **Activate \_ = 0;**</span><span class="sxs-lookup"><span data-stu-id="1d840-113">**const unsigned short** **ACTIVATE\_NOTACTIVE = 0;**</span></span><br/>   | <span data-ttu-id="1d840-114">El cliente no es el cliente activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="1d840-114">Your client is not the active client of the character.</span></span>                |
| <span data-ttu-id="1d840-115">**const unsigned short** **Activate \_ Active = 1;**</span><span class="sxs-lookup"><span data-stu-id="1d840-115">**const unsigned short** **ACTIVATE\_ACTIVE = 1;**</span></span><br/>      | <span data-ttu-id="1d840-116">El cliente es el cliente activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="1d840-116">Your client is the active client of the character.</span></span>                    |
| <span data-ttu-id="1d840-117">**const unsigned short** **Active \_ INPUTACTIVE = 2;**</span><span class="sxs-lookup"><span data-stu-id="1d840-117">**const unsigned short** **ACTIVATE\_INPUTACTIVE = 2;**</span></span><br/> | <span data-ttu-id="1d840-118">El cliente es de entrada-activo (cliente activo del carácter superior).</span><span class="sxs-lookup"><span data-stu-id="1d840-118">Your client is input-active (active client of the topmost character).</span></span> |



 

</dd> </dl>

<span data-ttu-id="1d840-119">Cuando varias aplicaciones cliente comparten el mismo carácter, el cliente activo del carácter recibe la entrada del mouse (por ejemplo, eventos de clic o arrastre de control del agente de Microsoft).</span><span class="sxs-lookup"><span data-stu-id="1d840-119">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="1d840-120">Del mismo modo, cuando se muestran varios caracteres, el cliente activo del carácter superior (también conocido como cliente de entrada-activo) recibe los eventos [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="1d840-120">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events.</span></span>

<span data-ttu-id="1d840-121">Cuando el cliente activo de un carácter cambia, este evento devuelve el identificador de ese carácter y **es true** si la aplicación se convierte en el cliente activo del carácter o en **false** si ya no es el cliente activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="1d840-121">When the active client of a character changes, this event passes back the ID of that character and **True** if your application has become the active client of the character or **False** if it is no longer the active client of the character.</span></span>

<span data-ttu-id="1d840-122">Una aplicación cliente puede recibir este evento cuando el usuario selecciona la entrada de otra aplicación cliente en el menú emergente del carácter o mediante el comando Voice, la aplicación cliente cambia su estado activo u otra aplicación cliente cierra su conexión con Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="1d840-122">A client application may receive this event when the user selects another client application's entry in character's pop-up menu or by voice command, the client application changes its active status, or another client application quits its connection to Microsoft Agent.</span></span> <span data-ttu-id="1d840-123">El agente envía este evento solo a las aplicaciones cliente que se ven afectadas directamente: aquellas que se convierten en el cliente activo o dejan de ser el cliente activo.</span><span class="sxs-lookup"><span data-stu-id="1d840-123">Agent sends this event only to the client applications that are directly affected-those that either become the active client or stop being the active client.</span></span>

<span data-ttu-id="1d840-124">Puede usar el método [**Activate**](iagentcharacter--activate.md) para establecer si la aplicación es el cliente activo del carácter o para que la aplicación sea el cliente activo de entrada (que también hace que el carácter sea más alto).</span><span class="sxs-lookup"><span data-stu-id="1d840-124">You can use the [**Activate**](iagentcharacter--activate.md) method to set whether your application is the active client of the character or to make your application the input-active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="1d840-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1d840-125">See Also</span></span>

<span data-ttu-id="1d840-126">[**IAgentCharacter:: Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx:: GetActive**](iagentcharacterex--getactive.md), [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md)</span><span class="sxs-lookup"><span data-stu-id="1d840-126">[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx::GetActive**](iagentcharacterex--getactive.md), [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md)</span></span>


 

 






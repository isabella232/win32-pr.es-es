---
title: IAgentCharacter activar
description: IAgentCharacter activar
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e86d2c094da484f528750d433e0fb6608790e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532506"
---
# <a name="iagentcharacteractivate"></a><span data-ttu-id="0f3c6-103">IAgentCharacter:: Activate</span><span class="sxs-lookup"><span data-stu-id="0f3c6-103">IAgentCharacter::Activate</span></span>

<span data-ttu-id="0f3c6-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0f3c6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

<span data-ttu-id="0f3c6-105">Establece si un cliente está activo o un carácter es el nivel superior.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-105">Sets whether a client is active or a character is topmost.</span></span>

-   <span data-ttu-id="0f3c6-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="0f3c6-107">Devuelve S \_ false para indicar que la operación no se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-107">Returns S\_FALSE to indicate the operation was not successful.</span></span>

<dl> <dt>

<span data-ttu-id="0f3c6-108"><span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*</span><span class="sxs-lookup"><span data-stu-id="0f3c6-108"><span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*</span></span>
</dt> <dd>

<span data-ttu-id="0f3c6-109">Puede especificar los siguientes valores para este parámetro:</span><span class="sxs-lookup"><span data-stu-id="0f3c6-109">You can specify the following values for this parameter:</span></span>



| <span data-ttu-id="0f3c6-110">Value</span><span class="sxs-lookup"><span data-stu-id="0f3c6-110">Value</span></span> | <span data-ttu-id="0f3c6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f3c6-111">Description</span></span>                   |
|-------|-------------------------------|
| <span data-ttu-id="0f3c6-112">0</span><span class="sxs-lookup"><span data-stu-id="0f3c6-112">0</span></span>     | <span data-ttu-id="0f3c6-113">Se establece como no es el cliente activo.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-113">Set as not the active client.</span></span> |
| <span data-ttu-id="0f3c6-114">1</span><span class="sxs-lookup"><span data-stu-id="0f3c6-114">1</span></span>     | <span data-ttu-id="0f3c6-115">Establezca como el cliente activo.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-115">Set as the active client.</span></span>     |
| <span data-ttu-id="0f3c6-116">2</span><span class="sxs-lookup"><span data-stu-id="0f3c6-116">2</span></span>     | <span data-ttu-id="0f3c6-117">Cree el carácter más alto.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-117">Make the topmost character.</span></span>   |



 

</dd> </dl>

<span data-ttu-id="0f3c6-118">Cuando hay varios caracteres visibles, solo uno de los caracteres recibe la entrada de voz a la vez.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-118">When multiple characters are visible, only one of the characters receives speech input at a time.</span></span> <span data-ttu-id="0f3c6-119">Del mismo modo, cuando varias aplicaciones cliente comparten el mismo carácter, solo uno de los clientes recibe la entrada de mouse (por ejemplo, eventos de clic o arrastre de control del agente de Microsoft) a la vez.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-119">Similarly, when multiple client applications share the same character, only one of the clients receives mouse input (for example, Microsoft Agent control click or drag events) at a time.</span></span> <span data-ttu-id="0f3c6-120">El juego de caracteres para recibir entrada de mouse y voz es el carácter más alto y el cliente que recibe la entrada es el cliente activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-120">The character set to receive mouse and speech input is the topmost character and the client that receives input is the character's active client.</span></span> <span data-ttu-id="0f3c6-121">(La ventana del carácter superior también aparece en la parte superior del orden z de la ventana de caracteres). Normalmente, el usuario determina qué carácter es el nivel superior seleccionándolo explícitamente.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-121">(The topmost character's window also appears at the top of the character window's z-order.) Typically, the user determines which character is topmost by explicitly selecting it.</span></span> <span data-ttu-id="0f3c6-122">Sin embargo, la activación de nivel superior también cambia cuando se muestra o se oculta un carácter (el carácter se vuelve o ya no es más alto, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="0f3c6-122">However, topmost activation also changes when a character is shown or hidden (the character becomes or is no longer topmost, respectively.)</span></span>

<span data-ttu-id="0f3c6-123">También puede usar este método para administrar explícitamente cuando el cliente recibe entradas dirigidas al carácter, como cuando la propia aplicación se activa.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-123">You can also use this method to explicitly manage when your client receives input directed to the character, such as when your application itself becomes active.</span></span> <span data-ttu-id="0f3c6-124">Por ejemplo, establecer el **Estado** en 2 hace que el carácter sea más alto y el cliente recibe todos los eventos de entrada del mouse y voz generados a partir de la interacción del usuario con el carácter.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-124">For example, setting **State** to 2 makes the character topmost, and your client receives all mouse and speech input events generated from user interaction with the character.</span></span> <span data-ttu-id="0f3c6-125">Por lo tanto, también convierte al cliente en el cliente de entrada y activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-125">Therefore, it also makes your client the input-active client of the character.</span></span> <span data-ttu-id="0f3c6-126">Sin embargo, también puede establecer el cliente activo para un carácter sin hacer que el carácter sea más alto, estableciendo el **Estado** en 1.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-126">However, you can also set the active client for a character without making the character topmost, by setting **State** to 1.</span></span> <span data-ttu-id="0f3c6-127">Esto permite que el cliente reciba entradas dirigidas a ese carácter cuando el carácter se vuelve más alto.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-127">This enables your client to receive input directed to that character when the character becomes topmost.</span></span> <span data-ttu-id="0f3c6-128">Del mismo modo, puede configurar el cliente para que no sea el cliente activo (para no recibir entradas) cuando el carácter se convierta en el nivel más alto, estableciendo el **Estado** en 0.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-128">Similarly, you can set your client to not be the active client (to not receive input) when the character becomes topmost, by setting **State** to 0.</span></span> <span data-ttu-id="0f3c6-129">Puede determinar si un carácter tiene otros clientes actuales mediante [**IAgentCharacter:: HasOtherClients**](iagentcharacter--hasotherclients.md).</span><span class="sxs-lookup"><span data-stu-id="0f3c6-129">You can determine if a character has other current clients using [**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md).</span></span>

<span data-ttu-id="0f3c6-130">Evite llamar a este método directamente después de un método [**Show**](iagentcharacter--show.md) .</span><span class="sxs-lookup"><span data-stu-id="0f3c6-130">Avoid calling this method directly after a [**Show**](iagentcharacter--show.md) method.</span></span> <span data-ttu-id="0f3c6-131">**Mostrar** establece automáticamente el cliente de entrada-activo.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-131">**Show** automatically sets the input-active client.</span></span> <span data-ttu-id="0f3c6-132">Cuando se oculta el carácter, se puede producir un error en la llamada a **Activate** si se procesa antes de que se complete el método **Show** .</span><span class="sxs-lookup"><span data-stu-id="0f3c6-132">When the character is hidden, the **Activate** call may fail, if it gets processed before the **Show** method completes.</span></span>

<span data-ttu-id="0f3c6-133">Se producirá un error al intentar llamar a este método con el parámetro de **Estado** establecido en 2 (si el carácter especificado está oculto).</span><span class="sxs-lookup"><span data-stu-id="0f3c6-133">Attempting to call this method with the **State** parameter set to 2 (when the specified character is hidden) will fail.</span></span> <span data-ttu-id="0f3c6-134">De forma similar, si establece **State** en 0 y la aplicación es el único cliente, se produce un error en esta llamada.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-134">Similarly, if you set **State** to 0, and your application is the only client, this call fails.</span></span> <span data-ttu-id="0f3c6-135">Un carácter siempre debe tener un cliente superior.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-135">A character must always have a topmost client.</span></span>

> [!Note]  
> <span data-ttu-id="0f3c6-136">La llamada a este método con el **Estado** establecido en 1 no suele generar un evento [**AgentNotifySink:: ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) a menos que no se hayan cargado otros caracteres o que la aplicación ya sea de entrada-activa.</span><span class="sxs-lookup"><span data-stu-id="0f3c6-136">Calling this method with **State** set to 1 does not typically generate an [**AgentNotifySink::ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) event unless there are no other characters loaded or your application is already input-active.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="0f3c6-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0f3c6-137">See Also</span></span>

[<span data-ttu-id="0f3c6-138">**IAgentCharacter::HasOtherClients**</span><span class="sxs-lookup"><span data-stu-id="0f3c6-138">**IAgentCharacter::HasOtherClients**</span></span>](iagentcharacter--hasotherclients.md)


 

 





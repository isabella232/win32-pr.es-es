---
title: Interrupción IAgentCharacter
description: Interrupción IAgentCharacter
ms.assetid: ae05d317-e2d9-4d11-a6df-f9b25e43467a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c9f19f716b15a48ec3cdb064aa4c0fdbbd1774
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995118"
---
# <a name="iagentcharacterinterrupt"></a><span data-ttu-id="5f5f3-103">IAgentCharacter:: Interrupt</span><span class="sxs-lookup"><span data-stu-id="5f5f3-103">IAgentCharacter::Interrupt</span></span>

<span data-ttu-id="5f5f3-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5f5f3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Interrupt(
   long dwReqID,    // request ID to interrupt
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="5f5f3-105">Interrumpe la animación especificada (solicitud) de otro carácter.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-105">Interrupts the specified animation (request) of another character.</span></span>

-   <span data-ttu-id="5f5f3-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="5f5f3-107">Cuando la función devuelve, *pdwReqID* contiene el identificador de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="5f5f3-108"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span><span class="sxs-lookup"><span data-stu-id="5f5f3-108"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="5f5f3-109">IDENTIFICADOR de la solicitud que se va a interrumpir.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-109">An ID of the request to interrupt.</span></span>

</dd> <dt>

<span data-ttu-id="5f5f3-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="5f5f3-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="5f5f3-111">Dirección de una variable que recibe el identificador de la solicitud de **interrupción** .</span><span class="sxs-lookup"><span data-stu-id="5f5f3-111">Address of a variable that receives the **Interrupt** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="5f5f3-112">Si carga varios caracteres, puede utilizar este método para sincronizar la animación entre los caracteres.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-112">If you load multiple characters, you can use this method to sync up animation between characters.</span></span> <span data-ttu-id="5f5f3-113">Por ejemplo, si hay otro carácter en una animación de bucle, este método detendrá la animación en bucle e iniciará la siguiente animación en la cola del carácter.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-113">For example, if another character is in a looping animation, this method will stop the looping animation and start the next animation in the character's queue.</span></span>

<span data-ttu-id="5f5f3-114">La **interrupción** detiene la animación existente, pero no vacía la cola de animaciones del carácter.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-114">**Interrupt** halts the existing animation, but does not flush the character's animation queue.</span></span> <span data-ttu-id="5f5f3-115">Inicia la siguiente animación en la cola del carácter.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-115">It starts the next animation in the character's queue.</span></span> <span data-ttu-id="5f5f3-116">Para detener y vaciar la cola de un carácter, utilice el método [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) .</span><span class="sxs-lookup"><span data-stu-id="5f5f3-116">To halt and flush a character's queue, use the [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) method.</span></span>

<span data-ttu-id="5f5f3-117">No puede usar este método para tener una interrupción de carácter en sí porque el servidor de agente de Microsoft pone en cola el método de **interrupción** en la cola de animaciones del carácter.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-117">You cannot use this method to have a character interrupt itself because the Microsoft Agent server queues the **Interrupt** method in the character's animation queue.</span></span> <span data-ttu-id="5f5f3-118">Por lo tanto, solo puede usar la **interrupción** para detener la animación de otro carácter que haya cargado.</span><span class="sxs-lookup"><span data-stu-id="5f5f3-118">Therefore, you can only use **Interrupt** to halt the animation of another character you have loaded.</span></span>

 

 
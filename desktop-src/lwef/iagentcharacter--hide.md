---
title: Ocultar IAgentCharacter
description: Ocultar IAgentCharacter
ms.assetid: a8128fe8-9a3b-41a3-bfe3-82ace1baff6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd0ef91eb4d2738f19fb594ac1ab186efaec6e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077675"
---
# <a name="iagentcharacterhide"></a><span data-ttu-id="99287-103">IAgentCharacter:: Hide</span><span class="sxs-lookup"><span data-stu-id="99287-103">IAgentCharacter::Hide</span></span>

<span data-ttu-id="99287-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="99287-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Hide(
   long bFast,      // play Hiding state animation flag
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="99287-105">Oculta el carácter.</span><span class="sxs-lookup"><span data-stu-id="99287-105">Hides the character.</span></span>

-   <span data-ttu-id="99287-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="99287-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="99287-107">Cuando la función devuelve, *pdwReqID* contiene el identificador de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="99287-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="99287-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span><span class="sxs-lookup"><span data-stu-id="99287-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span></span>
</dt> <dd>

<span data-ttu-id="99287-109">**Ocultar** marca de animación de estado.</span><span class="sxs-lookup"><span data-stu-id="99287-109">**Hiding** state animation flag.</span></span> <span data-ttu-id="99287-110">Si este parámetro es **true**, la animación de **ocultación** no se reproduce antes de que se oculte el marco de caracteres; Si **es false**, la animación se reproduce.</span><span class="sxs-lookup"><span data-stu-id="99287-110">If this parameter is **True**, the **Hiding** animation does not play before the character frame is hidden; if **False**, the animation plays.</span></span>

</dd> <dt>

<span data-ttu-id="99287-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="99287-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="99287-112">Dirección de una variable que recibe el identificador de solicitud de **ocultación** .</span><span class="sxs-lookup"><span data-stu-id="99287-112">Address of a variable that receives the **Hide** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="99287-113">El servidor pone en cola la animación asociada al método **Hide** en la cola del carácter.</span><span class="sxs-lookup"><span data-stu-id="99287-113">The server queues the animation associated with the **Hide** method in the character's queue.</span></span> <span data-ttu-id="99287-114">Esto le permite usarlo para ocultar el carácter después de una secuencia de otras animaciones.</span><span class="sxs-lookup"><span data-stu-id="99287-114">This allows you to use it to hide the character after a sequence of other animations.</span></span> <span data-ttu-id="99287-115">Puede reproducir la acción inmediatamente mediante el método [**Stop**](iagentcharacter--stop.md) antes de llamar al método **Hide** .</span><span class="sxs-lookup"><span data-stu-id="99287-115">You can play the action immediately by using the [**Stop**](iagentcharacter--stop.md) method before calling the **Hide** method.</span></span>

<span data-ttu-id="99287-116">Al usar el protocolo HTTP para tener acceso a los datos de animación y de caracteres, utilice el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantizar la disponibilidad de la animación de **ocultación** de estado antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="99287-116">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Hiding** state animation before calling this method.</span></span>

<span data-ttu-id="99287-117">Ocultar un carácter también puede producir el desencadenamiento del evento [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md) de otro carácter visible.</span><span class="sxs-lookup"><span data-stu-id="99287-117">Hiding a character can also result in triggering the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md) event of another visible character.</span></span>

<span data-ttu-id="99287-118">Los caracteres ocultos no pueden tener acceso al canal de audio.</span><span class="sxs-lookup"><span data-stu-id="99287-118">Hidden characters cannot access the audio channel.</span></span> <span data-ttu-id="99287-119">El servidor devolverá un estado de error en el evento [**RequestComplete**](iagentnotifysink--requestcomplete.md) si genera una solicitud de animación y el carácter está oculto.</span><span class="sxs-lookup"><span data-stu-id="99287-119">The server will pass back a failure status in the [**RequestComplete**](iagentnotifysink--requestcomplete.md) event if you generate an animation request and the character is hidden.</span></span>

## <a name="see-also"></a><span data-ttu-id="99287-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="99287-120">See Also</span></span>

[<span data-ttu-id="99287-121">**IAgentCharacter:: show**</span><span class="sxs-lookup"><span data-stu-id="99287-121">**IAgentCharacter::Show**</span></span>](iagentcharacter--show.md)


 

 
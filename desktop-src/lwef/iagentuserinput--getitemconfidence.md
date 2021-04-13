---
title: IAgentUserInput GetItemConfidence
description: IAgentUserInput GetItemConfidence
ms.assetid: 7d1ca2f0-416c-43c3-99a8-9f287cb88de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846e1fca9ea1245a62fc68330d68263b63fb7cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356653"
---
# <a name="iagentuserinputgetitemconfidence"></a><span data-ttu-id="c6084-103">IAgentUserInput::GetItemConfidence</span><span class="sxs-lookup"><span data-stu-id="c6084-103">IAgentUserInput::GetItemConfidence</span></span>

<span data-ttu-id="c6084-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c6084-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemConfidence(
   long dwItemIndex,    // index of Command alternative
   long * plConfidence  // address of confidence value for Command 
);
```

<span data-ttu-id="c6084-105">Recupera el valor de confianza para un [**comando**](command-event.md) que se pasa a una devolución de llamada de [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="c6084-105">Retrieves the confidence value for a [**Command**](command-event.md) passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="c6084-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c6084-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c6084-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span><span class="sxs-lookup"><span data-stu-id="c6084-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="c6084-108">Índice de una alternativa de [**comando**](command-event.md) que se pasa a la devolución de llamada de [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="c6084-108">The index of a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="c6084-109"><span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plConfidence*</span><span class="sxs-lookup"><span data-stu-id="c6084-109"><span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plConfidence*</span></span>
</dt> <dd>

<span data-ttu-id="c6084-110">Dirección de una variable que recibe la puntuación de confianza para una alternativa de [**comando**](command-event.md) que se pasa a la devolución de llamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="c6084-110">Address of a variable that receives the confidence score for a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> </dl>

<span data-ttu-id="c6084-111">Si la entrada de voz no era el origen del comando, por ejemplo, si el usuario selecciona el comando en el menú emergente del carácter, el servidor de agente de Microsoft devuelve el valor de confianza de la mejor coincidencia como 100 y los valores de confianza para todas las demás alternativas como cero (0).</span><span class="sxs-lookup"><span data-stu-id="c6084-111">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, the Microsoft Agent server returns the confidence value of the best match as 100 and the confidence values for all other alternatives as zero (0).</span></span>

## <a name="see-also"></a><span data-ttu-id="c6084-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c6084-112">See Also</span></span>

<span data-ttu-id="c6084-113">[**IAgentUserInput:: GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput:: GetAllItemData**](iagentuserinput--getallitemdata.md), [**IAgentUserInput:: GetItemText**](iagentuserinput--getitemtext.md)</span><span class="sxs-lookup"><span data-stu-id="c6084-113">[**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md)</span></span>


 

 





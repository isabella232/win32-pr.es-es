---
title: IAgentUserInput GetItemText
description: IAgentUserInput GetItemText
ms.assetid: 69653806-c001-4015-bd05-3c261a312ede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7010172147f86282903641c46aa5137ce69c80be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104074984"
---
# <a name="iagentuserinputgetitemtext"></a><span data-ttu-id="690ca-103">IAgentUserInput::GetItemText</span><span class="sxs-lookup"><span data-stu-id="690ca-103">IAgentUserInput::GetItemText</span></span>

<span data-ttu-id="690ca-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="690ca-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemText(
   Long dwItemIndex,  // index of Command alternative
   BSTR * pbszText    // address of voice text for Command 
);
```

<span data-ttu-id="690ca-105">Recupera el texto de la voz de una alternativa de [**comando**](command-event.md) que se pasa a la devolución de llamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="690ca-105">Retrieves the voice text for a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="690ca-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="690ca-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="690ca-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span><span class="sxs-lookup"><span data-stu-id="690ca-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="690ca-108">Índice de una alternativa de [**comando**](command-event.md) que se pasa a la devolución de llamada de [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="690ca-108">The index of a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="690ca-109"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span><span class="sxs-lookup"><span data-stu-id="690ca-109"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span></span>
</dt> <dd>

<span data-ttu-id="690ca-110">Dirección de un BSTR que recibe el valor del texto de la voz para el [**comando**](command-event.md).</span><span class="sxs-lookup"><span data-stu-id="690ca-110">Address of a BSTR that receives the value of the voice text for the [**Command**](command-event.md).</span></span>

</dd> </dl>

<span data-ttu-id="690ca-111">Si la entrada de voz no era el origen del comando, por ejemplo, si el usuario selecciona el comando en el menú emergente del carácter, el servidor devuelve **null** para el texto de la voz del [**comando**](command-event.md).</span><span class="sxs-lookup"><span data-stu-id="690ca-111">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, the server returns **NULL** for the [**Command**](command-event.md)'s voice text.</span></span>

## <a name="see-also"></a><span data-ttu-id="690ca-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="690ca-112">See Also</span></span>

<span data-ttu-id="690ca-113">[**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput:: GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput:: GetAllItemData**](iagentuserinput--getallitemdata.md)</span><span class="sxs-lookup"><span data-stu-id="690ca-113">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)</span></span>


 

 





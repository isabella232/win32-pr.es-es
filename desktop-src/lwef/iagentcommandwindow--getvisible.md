---
title: IAgentCommandWindow GetVisible
description: IAgentCommandWindow GetVisible
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66c6d7bf2ee59512f478fd8daa7cee882515690
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714149"
---
# <a name="iagentcommandwindowgetvisible"></a><span data-ttu-id="7005c-103">IAgentCommandWindow:: GetVisible</span><span class="sxs-lookup"><span data-stu-id="7005c-103">IAgentCommandWindow::GetVisible</span></span>

<span data-ttu-id="7005c-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7005c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for Visible setting for 
);                   // Voice Commands Window
```

<span data-ttu-id="7005c-105">Determina si la ventana comandos de voz está visible u oculta.</span><span class="sxs-lookup"><span data-stu-id="7005c-105">Determines whether the Voice Commands Window is visible or hidden.</span></span>

-   <span data-ttu-id="7005c-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7005c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7005c-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="7005c-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="7005c-108">Dirección de una variable que recibe **true** si la ventana comandos de voz está visible o **false** si está oculta.</span><span class="sxs-lookup"><span data-stu-id="7005c-108">Address of a variable that receives **True** if the Voice Commands Window is visible, or **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="7005c-109">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7005c-109">See Also</span></span>

[<span data-ttu-id="7005c-110">**IAgentCommandWindow:: SetVisible**</span><span class="sxs-lookup"><span data-stu-id="7005c-110">**IAgentCommandWindow::SetVisible**</span></span>](iagentcommandwindow--setvisible.md)


 

 





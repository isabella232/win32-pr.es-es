---
title: IAgentCharacterEx SetAutoPopupMenu
description: IAgentCharacterEx SetAutoPopupMenu
ms.assetid: f2402b1f-a39b-4fd5-a046-c0a3245d2af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcfd1bd7ea0b02f226ed6f0365b466577807a193
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994286"
---
# <a name="iagentcharacterexsetautopopupmenu"></a><span data-ttu-id="64a39-103">IAgentCharacterEx::SetAutoPopupMenu</span><span class="sxs-lookup"><span data-stu-id="64a39-103">IAgentCharacterEx::SetAutoPopupMenu</span></span>

<span data-ttu-id="64a39-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="64a39-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetAutoPopupMenu(
   long bAutoPopupMenu,  // auto pop-up menu display setting
);
```

<span data-ttu-id="64a39-105">Establece si el servidor muestra automáticamente el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="64a39-105">Sets whether the server automatically displays the character's pop-up menu.</span></span>

-   <span data-ttu-id="64a39-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="64a39-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="64a39-107"><span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*</span><span class="sxs-lookup"><span data-stu-id="64a39-107"><span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*</span></span>
</dt> <dd>

<span data-ttu-id="64a39-108">Marca de visualización automática del menú emergente.</span><span class="sxs-lookup"><span data-stu-id="64a39-108">The automatic pop-up menu display flag.</span></span> <span data-ttu-id="64a39-109">Si este parámetro es **true**, el agente de Microsoft muestra automáticamente el menú emergente del carácter cuando el usuario hace clic con el botón secundario en el icono de la barra de tareas del carácter o del carácter.</span><span class="sxs-lookup"><span data-stu-id="64a39-109">If this parameter is **True**, Microsoft Agent automatically displays the character's pop-up menu when the user right-clicks the character or character's taskbar icon.</span></span>

</dd> </dl>

<span data-ttu-id="64a39-110">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="64a39-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="64a39-111">Al establecer esta propiedad en **false**, puede crear su propio comportamiento de control de menús.</span><span class="sxs-lookup"><span data-stu-id="64a39-111">By setting this property to **False**, you can create your own menu-handling behavior.</span></span> <span data-ttu-id="64a39-112">Para mostrar el menú después de establecer esta propiedad en **false**, use el método [**IAgentCharacterEx:: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="64a39-112">To display the menu after setting this property to **False**, use the [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="64a39-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="64a39-113">See Also</span></span>

<span data-ttu-id="64a39-114">[**IAgentCharacterEx:: GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [ **IAgentCharacterEx:: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span><span class="sxs-lookup"><span data-stu-id="64a39-114">[**IAgentCharacterEx::GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span></span>


 

 





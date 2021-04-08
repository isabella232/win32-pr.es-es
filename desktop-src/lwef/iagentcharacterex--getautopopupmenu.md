---
title: IAgentCharacterEx GetAutoPopupMenu
description: IAgentCharacterEx GetAutoPopupMenu
ms.assetid: c29bfd6e-c7eb-426e-be38-2fa0bdb13211
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c7a3b8d1075c596f27af17df34c7cb94d8a1ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994430"
---
# <a name="iagentcharacterexgetautopopupmenu"></a><span data-ttu-id="96161-103">IAgentCharacterEx::GetAutoPopupMenu</span><span class="sxs-lookup"><span data-stu-id="96161-103">IAgentCharacterEx::GetAutoPopupMenu</span></span>

<span data-ttu-id="96161-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="96161-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAutoPopupMenu(
   long * pbAutoPopupMenu  // address of auto pop-up menu display setting
);
```

<span data-ttu-id="96161-105">Recupera si el servidor muestra automáticamente el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="96161-105">Retrieves whether the server automatically displays the character's pop-up menu.</span></span>

-   <span data-ttu-id="96161-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="96161-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="96161-107"><span id="pbAutoPopupMenu"></span><span id="pbautopopupmenu"></span><span id="PBAUTOPOPUPMENU"></span>*pbAutoPopupMenu*</span><span class="sxs-lookup"><span data-stu-id="96161-107"><span id="pbAutoPopupMenu"></span><span id="pbautopopupmenu"></span><span id="PBAUTOPOPUPMENU"></span>*pbAutoPopupMenu*</span></span>
</dt> <dd>

<span data-ttu-id="96161-108">Dirección de una variable que recibe **true** si el servidor de agente de Microsoft controla automáticamente la visualización del menú emergente del carácter y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="96161-108">Address of a variable that receives **True** if the Microsoft Agent server automatically handles displaying the character's pop-up menu and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="96161-109">Cuando esta propiedad está establecida en **false**, la aplicación debe mostrar el menú emergente con el método [**IAgentCharacterEx:: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="96161-109">When this property is set to **False**, your application must display the pop-up menu using [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) method.</span></span>

<span data-ttu-id="96161-110">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="96161-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="96161-111">Consulte también</span><span class="sxs-lookup"><span data-stu-id="96161-111">See Also</span></span>

<span data-ttu-id="96161-112">[**IAgentCharacterEx:: SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md), [ **IAgentCharacterEx:: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span><span class="sxs-lookup"><span data-stu-id="96161-112">[**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md), [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span></span>


 

 





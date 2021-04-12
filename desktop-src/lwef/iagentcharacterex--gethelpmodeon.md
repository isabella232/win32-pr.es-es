---
title: IAgentCharacterEx GetHelpModeOn
description: IAgentCharacterEx GetHelpModeOn
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072f657ba5ac93d057474f062f73101f2559aed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269285"
---
# <a name="iagentcharacterexgethelpmodeon"></a><span data-ttu-id="220c3-103">IAgentCharacterEx::GetHelpModeOn</span><span class="sxs-lookup"><span data-stu-id="220c3-103">IAgentCharacterEx::GetHelpModeOn</span></span>

<span data-ttu-id="220c3-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="220c3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

<span data-ttu-id="220c3-105">Recupera si el modo de ayuda contextual está activado para el carácter.</span><span class="sxs-lookup"><span data-stu-id="220c3-105">Retrieves whether context-sensitive Help mode is on for the character.</span></span>

-   <span data-ttu-id="220c3-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="220c3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="220c3-107"><span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*</span><span class="sxs-lookup"><span data-stu-id="220c3-107"><span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*</span></span>
</dt> <dd>

<span data-ttu-id="220c3-108">Dirección de una variable que recibe **true** si el modo de ayuda está activado para el carácter y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="220c3-108">Address of a variable that receives **True** if Help mode is on for the character and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="220c3-109">Cuando esta propiedad se establece en **true**, el puntero del mouse cambia a la imagen de ayuda contextual cuando se mueve sobre el carácter o sobre el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="220c3-109">When this property is set to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="220c3-110">Cuando el usuario hace clic o arrastra el carácter o hace clic en un elemento del menú emergente del carácter, el servidor desencadena el evento [**IAgentNotifySinkEx:: HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) y sale del modo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="220c3-110">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**IAgentNotifySinkEx::HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) event and exits Help mode.</span></span>

<span data-ttu-id="220c3-111">En el modo de ayuda, el servidor no envía los eventos [**IAgentNotifySink:: click**](iagentnotifysink--click.md), [**IAgentNotifySink::D ragstart**](iagentnotifysink--dragstart.md), [**IAgentNotifySink::D Ragcomplete**](iagentnotifysink--dragcomplete.md)y [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) , a menos que la propiedad [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) devuelva **true**.</span><span class="sxs-lookup"><span data-stu-id="220c3-111">In Help mode, the server does not send the [**IAgentNotifySink::Click**](iagentnotifysink--click.md), [**IAgentNotifySink::DragStart**](iagentnotifysink--dragstart.md), [**IAgentNotifySink::DragComplete**](iagentnotifysink--dragcomplete.md), and [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events, unless [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) property returns **True**.</span></span> <span data-ttu-id="220c3-112">En ese caso, el servidor enviará el evento **IAgentNotifySink:: click** (no abandona el modo de ayuda), sino solo el botón secundario del mouse para que pueda mostrar el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="220c3-112">In that case, the server will send the **IAgentNotifySink::Click** event (does not exit Help mode), but only for the right mouse button to enable you to display the pop-up menu.</span></span>

<span data-ttu-id="220c3-113">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="220c3-113">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="220c3-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="220c3-114">See Also</span></span>

[<span data-ttu-id="220c3-115">**IAgentCharacterEx::SetHelpModeOn**</span><span class="sxs-lookup"><span data-stu-id="220c3-115">**IAgentCharacterEx::SetHelpModeOn**</span></span>](iagentcharacterex--sethelpmodeon.md)


 

 





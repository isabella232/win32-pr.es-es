---
title: IAgentCharacterEx SetHelpModeOn
description: IAgentCharacterEx SetHelpModeOn
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674fc8dcca3bca2f44c0928474d8684e77fc6e9b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149202"
---
# <a name="iagentcharacterexsethelpmodeon"></a><span data-ttu-id="183c9-103">IAgentCharacterEx::SetHelpModeOn</span><span class="sxs-lookup"><span data-stu-id="183c9-103">IAgentCharacterEx::SetHelpModeOn</span></span>

<span data-ttu-id="183c9-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="183c9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpModeOn(
   long bHelpModeOn  // help mode setting
);
```

<span data-ttu-id="183c9-105">Establece el modo de ayuda contextual en para el carácter.</span><span class="sxs-lookup"><span data-stu-id="183c9-105">Sets context-sensitive Help mode on for the character.</span></span>

-   <span data-ttu-id="183c9-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="183c9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="183c9-107"><span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*</span><span class="sxs-lookup"><span data-stu-id="183c9-107"><span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*</span></span>
</dt> <dd>

<span data-ttu-id="183c9-108">Marca de modo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="183c9-108">Help mode flag.</span></span> <span data-ttu-id="183c9-109">Si este parámetro es **true**, el agente de Microsoft activa el modo de ayuda para el carácter.</span><span class="sxs-lookup"><span data-stu-id="183c9-109">If this parameter is **True**, Microsoft Agent turns on Help mode for the character.</span></span>

</dd> </dl>

<span data-ttu-id="183c9-110">Cuando se establece esta propiedad en **true**, el puntero del mouse cambia a la imagen de ayuda contextual cuando se mueve sobre el carácter o sobre el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="183c9-110">When you set this property to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="183c9-111">Cuando el usuario hace clic o arrastra el carácter o hace clic en un elemento del menú emergente del carácter, el servidor desencadena el evento [**IAgentNotifySinkEx:: HelpComplete**](iagentnotifysinkex--helpcomplete.md) y sale del modo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="183c9-111">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md) event and exits Help mode.</span></span>

<span data-ttu-id="183c9-112">En el modo de ayuda, el servidor no envía los eventos [**click**](click-event.md), [**DragStart**](/windows/desktop/lwef/dragstart-event), [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)y [**Command**](command-event.md) , a menos que la propiedad [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) devuelva **true**.</span><span class="sxs-lookup"><span data-stu-id="183c9-112">In Help mode, the server does not send the [**Click**](click-event.md), [**DragStart**](/windows/desktop/lwef/dragstart-event), [**DragComplete**](https://www.bing.com/search?q=**DragComplete**), and [**Command**](command-event.md) events, unless the [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) property returns **True**.</span></span> <span data-ttu-id="183c9-113">En ese caso, el servidor enviará el evento de **clic** (no saldrá del modo de ayuda), sino solo para el botón secundario del mouse para que pueda mostrar el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="183c9-113">In that case, the server will send the **Click** event (does not exit Help mode), but only for the right mouse button so you can display the pop-up menu.</span></span>

<span data-ttu-id="183c9-114">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="183c9-114">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="183c9-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="183c9-115">See Also</span></span>

<span data-ttu-id="183c9-116">[**IAgentCharacterEx:: GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [ **IAgentNotifySinkEx:: HelpComplete**](iagentnotifysinkex--helpcomplete.md)</span><span class="sxs-lookup"><span data-stu-id="183c9-116">[**IAgentCharacterEx::GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md)</span></span>


 

 
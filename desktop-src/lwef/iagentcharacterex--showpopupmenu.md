---
title: IAgentCharacterEx ShowPopupMenu
description: IAgentCharacterEx ShowPopupMenu
ms.assetid: f93c4c9e-5ef8-42d1-8f22-d6625af7978f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535a86496f3553e0927ebe67d2c9823b738fb901
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903641"
---
# <a name="iagentcharacterexshowpopupmenu"></a><span data-ttu-id="15266-103">IAgentCharacterEx::ShowPopupMenu</span><span class="sxs-lookup"><span data-stu-id="15266-103">IAgentCharacterEx::ShowPopupMenu</span></span>

<span data-ttu-id="15266-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="15266-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ShowPopupMenu(
   short x,  // x-coordinate of pop-up menu
   short y   // y-coordinate of pop-up menu
);
```

<span data-ttu-id="15266-105">Muestra el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="15266-105">Displays the pop-up menu for the character.</span></span>

-   <span data-ttu-id="15266-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="15266-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="15266-107"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="15266-107"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="15266-108">La coordenada x del menú emergente del carácter, en píxeles, con respecto al origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="15266-108">The x-coordinate of the character's pop-up menu in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="15266-109"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="15266-109"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="15266-110">Coordenada y del menú emergente del carácter, en píxeles, con respecto al origen de la pantalla (parte superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="15266-110">The y-coordinate of the character's pop-up menu in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="15266-111">Al establecer [**IAgentCharacterEx:: SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) en **false**, el servidor ya no muestra automáticamente el menú cuando se hace clic con el botón derecho en el carácter o el icono de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="15266-111">When you set [**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) to **False**, the server no longer automatically displays the menu when the character or its taskbar icon is right-clicked.</span></span> <span data-ttu-id="15266-112">Puede utilizar este método para mostrar el menú.</span><span class="sxs-lookup"><span data-stu-id="15266-112">You can use this method to display the menu.</span></span>

<span data-ttu-id="15266-113">El menú se muestra hasta que el usuario selecciona un comando o muestra otro menú.</span><span class="sxs-lookup"><span data-stu-id="15266-113">The menu displays until the user selects a command or displays another menu.</span></span> <span data-ttu-id="15266-114">Solo se puede mostrar un menú emergente a la vez; por lo tanto, las llamadas a este método cancelarán (quitará) el menú anterior.</span><span class="sxs-lookup"><span data-stu-id="15266-114">Only one pop-up menu can be displayed at a time; therefore, calls to this method will cancel (remove) the former menu.</span></span>

<span data-ttu-id="15266-115">Solo se debe llamar a este método cuando la aplicación cliente es el cliente activo del carácter; en caso contrario, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="15266-115">This method should only be called when your client application is the active client of the character; otherwise it fails.</span></span>

[<span data-ttu-id="15266-116">**IAgentCharacterEx::SetAutoPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="15266-116">**IAgentCharacterEx::SetAutoPopupMenu**</span></span>](iagentcharacterex--setautopopupmenu.md)

 

 





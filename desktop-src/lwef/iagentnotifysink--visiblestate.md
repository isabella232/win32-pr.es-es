---
title: IAgentNotifySink VisibleState
description: IAgentNotifySink VisibleState
ms.assetid: b0346296-74e9-448f-aa6d-a9fb1e645f05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3525c079ecd1b566ac2230f06e3effa1ceb7a694
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704761"
---
# <a name="iagentnotifysinkvisiblestate"></a><span data-ttu-id="44bbd-103">IAgentNotifySink::VisibleState</span><span class="sxs-lookup"><span data-stu-id="44bbd-103">IAgentNotifySink::VisibleState</span></span>

<span data-ttu-id="44bbd-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="44bbd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT VisibleState(
   long dwCharID,  // character ID
   long bVisible,  // visibility flag
   long dwCause,   // cause of visible state
);                          
```

<span data-ttu-id="44bbd-105">Notifica a una aplicación cliente cuando cambia el estado de visibilidad del carácter.</span><span class="sxs-lookup"><span data-stu-id="44bbd-105">Notifies a client application when the visibility state of the character changes.</span></span>

-   <span data-ttu-id="44bbd-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="44bbd-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="44bbd-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="44bbd-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="44bbd-108">Identificador del carácter cuyo estado de visibilidad se cambia.</span><span class="sxs-lookup"><span data-stu-id="44bbd-108">Identifier of the character whose visibility state is changed.</span></span>

</dd> <dt>

<span data-ttu-id="44bbd-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="44bbd-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="44bbd-110">Marca de visibilidad.</span><span class="sxs-lookup"><span data-stu-id="44bbd-110">Visibility flag.</span></span> <span data-ttu-id="44bbd-111">Este valor booleano es **true** cuando el carácter se vuelve visible y **false** cuando se oculta el carácter.</span><span class="sxs-lookup"><span data-stu-id="44bbd-111">This Boolean value is **True** when character becomes visible and **False** when the character becomes hidden.</span></span>

</dd> <dt>

<span data-ttu-id="44bbd-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="44bbd-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="44bbd-113">Causa del último cambio en el estado de visibilidad del carácter.</span><span class="sxs-lookup"><span data-stu-id="44bbd-113">Cause of last change to the character's visibility state.</span></span> <span data-ttu-id="44bbd-114">El parámetro puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="44bbd-114">The parameter may be one of the following:</span></span>



| <span data-ttu-id="44bbd-115">Value</span><span class="sxs-lookup"><span data-stu-id="44bbd-115">Value</span></span>                                                                   | <span data-ttu-id="44bbd-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="44bbd-116">Description</span></span>                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="44bbd-117">**const unsigned short** **NeverShown = 0;**</span><span class="sxs-lookup"><span data-stu-id="44bbd-117">**const unsigned short** **NeverShown = 0;**</span></span><br/>                 | <span data-ttu-id="44bbd-118">No se ha mostrado el carácter.</span><span class="sxs-lookup"><span data-stu-id="44bbd-118">Character has not been shown.</span></span>                                                               |
| <span data-ttu-id="44bbd-119">**const unsigned short** **UserHid = 1;**</span><span class="sxs-lookup"><span data-stu-id="44bbd-119">**const unsigned short** **UserHid = 1;**</span></span><br/>                    | <span data-ttu-id="44bbd-120">El usuario ocultó el carácter con el menú emergente del icono de la barra de tareas del carácter o con entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="44bbd-120">User hid the character with the character's taskbar icon pop-up menu or with speech input..</span></span> |
| <span data-ttu-id="44bbd-121">**const unsigned short** **UserShowed = 2;**</span><span class="sxs-lookup"><span data-stu-id="44bbd-121">**const unsigned short** **UserShowed = 2;**</span></span><br/>                 | <span data-ttu-id="44bbd-122">El usuario mostró el carácter.</span><span class="sxs-lookup"><span data-stu-id="44bbd-122">User showed the character.</span></span>                                                                  |
| <span data-ttu-id="44bbd-123">**const unsigned short** **ProgramHid = 3;**</span><span class="sxs-lookup"><span data-stu-id="44bbd-123">**const unsigned short** **ProgramHid = 3;**</span></span><br/>                 | <span data-ttu-id="44bbd-124">La aplicación ocultó el carácter.</span><span class="sxs-lookup"><span data-stu-id="44bbd-124">Your application hid the character.</span></span>                                                         |
| <span data-ttu-id="44bbd-125">**const unsigned short** **ProgramShowed = 4;**</span><span class="sxs-lookup"><span data-stu-id="44bbd-125">**const unsigned short** **ProgramShowed = 4;**</span></span><br/>              | <span data-ttu-id="44bbd-126">La aplicación mostró el carácter.</span><span class="sxs-lookup"><span data-stu-id="44bbd-126">Your application showed the character.</span></span>                                                      |
| <span data-ttu-id="44bbd-127">**const unsigned short** **OtherProgramHid = 5;**</span><span class="sxs-lookup"><span data-stu-id="44bbd-127">**const unsigned short** **OtherProgramHid = 5;**</span></span><br/>            | <span data-ttu-id="44bbd-128">Otra aplicación ocultó el carácter.</span><span class="sxs-lookup"><span data-stu-id="44bbd-128">Another application hid the character.</span></span>                                                      |
| <span data-ttu-id="44bbd-129">**const unsigned short** **OtherProgramShowed = 6;**</span><span class="sxs-lookup"><span data-stu-id="44bbd-129">**const unsigned short** **OtherProgramShowed = 6;**</span></span><br/>         | <span data-ttu-id="44bbd-130">Otra aplicación mostró el carácter.</span><span class="sxs-lookup"><span data-stu-id="44bbd-130">Another application showed the character.</span></span>                                                   |
| <span data-ttu-id="44bbd-131">**const unsigned short** **UserHidViaCharacterMenu = 7**</span><span class="sxs-lookup"><span data-stu-id="44bbd-131">**const unsigned short** **UserHidViaCharacterMenu = 7**</span></span><br/>     | <span data-ttu-id="44bbd-132">El usuario ocultó el carácter con el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="44bbd-132">User hid the character with the character's pop-up menu.</span></span>                                    |
| <span data-ttu-id="44bbd-133">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span><span class="sxs-lookup"><span data-stu-id="44bbd-133">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span></span><br/> | <span data-ttu-id="44bbd-134">El usuario ocultó el carácter con el menú emergente del icono de la barra de tareas del carácter o con la entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="44bbd-134">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="44bbd-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="44bbd-135">See Also</span></span>

<span data-ttu-id="44bbd-136">[**IAgentCharacter:: GetVisible**](iagentcharacter--getvisible.md), [ **IAgentCharacter:: GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)</span><span class="sxs-lookup"><span data-stu-id="44bbd-136">[**IAgentCharacter::GetVisible**](iagentcharacter--getvisible.md), [**IAgentCharacter::GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)</span></span>


 

 






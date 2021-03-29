---
title: IAgentCharacter GetVisibilityCause
description: IAgentCharacter GetVisibilityCause
ms.assetid: 46f681de-1c99-4f90-a3fe-aae04bb75339
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6013385144b82b79a0f17ae6443b094a9d9c8a4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419202"
---
# <a name="iagentcharactergetvisibilitycause"></a><span data-ttu-id="82c50-103">IAgentCharacter::GetVisibilityCause</span><span class="sxs-lookup"><span data-stu-id="82c50-103">IAgentCharacter::GetVisibilityCause</span></span>

<span data-ttu-id="82c50-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="82c50-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisibilityCause(
   long * pdwCause  // address of variable for cause of character visible state
);
```

<span data-ttu-id="82c50-105">Recupera la causa del estado visible del carácter.</span><span class="sxs-lookup"><span data-stu-id="82c50-105">Retrieves the cause of the character's visible state.</span></span>

-   <span data-ttu-id="82c50-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="82c50-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="82c50-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span><span class="sxs-lookup"><span data-stu-id="82c50-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="82c50-108">Dirección de una variable que recibe la causa del último cambio de estado de visibilidad del carácter y será uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="82c50-108">Address of a variable that receives the cause of the character's last visibility state change and will be one of the following:</span></span>



| <span data-ttu-id="82c50-109">Value</span><span class="sxs-lookup"><span data-stu-id="82c50-109">Value</span></span>                                                                   | <span data-ttu-id="82c50-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="82c50-110">Description</span></span>                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="82c50-111">**const unsigned short** **NeverShown = 0;**</span><span class="sxs-lookup"><span data-stu-id="82c50-111">**const unsigned short** **NeverShown = 0;**</span></span><br/>                 | <span data-ttu-id="82c50-112">No se ha mostrado el carácter.</span><span class="sxs-lookup"><span data-stu-id="82c50-112">Character has not been shown.</span></span>                                                               |
| <span data-ttu-id="82c50-113">**const unsigned short** **UserHid = 1;**</span><span class="sxs-lookup"><span data-stu-id="82c50-113">**const unsigned short** **UserHid = 1;**</span></span><br/>                    | <span data-ttu-id="82c50-114">El usuario ocultó el carácter con el menú emergente del icono de la barra de tareas del carácter o con la entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="82c50-114">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |
| <span data-ttu-id="82c50-115">**const unsigned short** **UserShowed = 2;**</span><span class="sxs-lookup"><span data-stu-id="82c50-115">**const unsigned short** **UserShowed = 2;**</span></span><br/>                 | <span data-ttu-id="82c50-116">El usuario mostró el carácter.</span><span class="sxs-lookup"><span data-stu-id="82c50-116">User showed the character.</span></span>                                                                  |
| <span data-ttu-id="82c50-117">**const unsigned short** **ProgramHid = 3;**</span><span class="sxs-lookup"><span data-stu-id="82c50-117">**const unsigned short** **ProgramHid = 3;**</span></span><br/>                 | <span data-ttu-id="82c50-118">La aplicación ocultó el carácter.</span><span class="sxs-lookup"><span data-stu-id="82c50-118">Your application hid the character.</span></span>                                                         |
| <span data-ttu-id="82c50-119">**const unsigned short** **ProgramShowed = 4;**</span><span class="sxs-lookup"><span data-stu-id="82c50-119">**const unsigned short** **ProgramShowed = 4;**</span></span><br/>              | <span data-ttu-id="82c50-120">La aplicación mostró el carácter.</span><span class="sxs-lookup"><span data-stu-id="82c50-120">Your application showed the character.</span></span>                                                      |
| <span data-ttu-id="82c50-121">**const unsigned short** **OtherProgramHid = 5;**</span><span class="sxs-lookup"><span data-stu-id="82c50-121">**const unsigned short** **OtherProgramHid = 5;**</span></span><br/>            | <span data-ttu-id="82c50-122">Otra aplicación ocultó el carácter.</span><span class="sxs-lookup"><span data-stu-id="82c50-122">Another application hid the character.</span></span>                                                      |
| <span data-ttu-id="82c50-123">**const unsigned short** **OtherProgramShowed = 6;**</span><span class="sxs-lookup"><span data-stu-id="82c50-123">**const unsigned short** **OtherProgramShowed = 6;**</span></span><br/>         | <span data-ttu-id="82c50-124">Otra aplicación mostró el carácter.</span><span class="sxs-lookup"><span data-stu-id="82c50-124">Another application showed the character.</span></span>                                                   |
| <span data-ttu-id="82c50-125">**const unsigned short** **UserHidViaCharacterMenu = 7**</span><span class="sxs-lookup"><span data-stu-id="82c50-125">**const unsigned short** **UserHidViaCharacterMenu = 7**</span></span><br/>     | <span data-ttu-id="82c50-126">El usuario ocultó el carácter con el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="82c50-126">User hid the character with the character's pop-up menu.</span></span>                                    |
| <span data-ttu-id="82c50-127">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span><span class="sxs-lookup"><span data-stu-id="82c50-127">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span></span><br/> | <span data-ttu-id="82c50-128">El usuario ocultó el carácter con el menú emergente del icono de la barra de tareas del carácter o con la entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="82c50-128">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="82c50-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="82c50-129">See Also</span></span>

[<span data-ttu-id="82c50-130">**IAgentNotifySink::VisibleState**</span><span class="sxs-lookup"><span data-stu-id="82c50-130">**IAgentNotifySink::VisibleState**</span></span>](iagentnotifysink--visiblestate.md)


 

 






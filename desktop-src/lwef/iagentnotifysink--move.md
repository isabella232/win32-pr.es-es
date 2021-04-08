---
title: Movimiento de IAgentNotifySink
description: Movimiento de IAgentNotifySink
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52563ff3838348b7bf8e6a2bcdfdf20a51c79723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994532"
---
# <a name="iagentnotifysinkmove"></a><span data-ttu-id="cf8a9-103">IAgentNotifySink:: Move</span><span class="sxs-lookup"><span data-stu-id="cf8a9-103">IAgentNotifySink::Move</span></span>

<span data-ttu-id="cf8a9-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cf8a9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Move(
   long dwCharID,  // character ID
   long x,         // x-coordinate of new location
   long y,         // y-coordinate of new location
   long dwCause    // cause of move state
);                          
```

<span data-ttu-id="cf8a9-105">Notifica a una aplicación cliente cuando se ha cambiado el carácter.</span><span class="sxs-lookup"><span data-stu-id="cf8a9-105">Notifies a client application when the character has been moved.</span></span>

-   <span data-ttu-id="cf8a9-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cf8a9-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="cf8a9-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="cf8a9-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="cf8a9-108">Identificador del carácter que se ha despasado.</span><span class="sxs-lookup"><span data-stu-id="cf8a9-108">Identifier of the character that has been moved.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a9-109"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="cf8a9-109"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="cf8a9-110">Coordenada x de la nueva posición en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="cf8a9-110">The x-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="cf8a9-111">La ubicación de un carácter se basa en la esquina superior izquierda de su fotograma de animación.</span><span class="sxs-lookup"><span data-stu-id="cf8a9-111">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a9-112"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="cf8a9-112"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="cf8a9-113">Coordenada y de la nueva posición en píxeles, con respecto al origen de la pantalla (superior izquierda).</span><span class="sxs-lookup"><span data-stu-id="cf8a9-113">The y-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="cf8a9-114">La ubicación de un carácter se basa en la esquina superior izquierda de su fotograma de animación.</span><span class="sxs-lookup"><span data-stu-id="cf8a9-114">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a9-115"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="cf8a9-115"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="cf8a9-116">Causa del movimiento del carácter.</span><span class="sxs-lookup"><span data-stu-id="cf8a9-116">The cause of the character move.</span></span> <span data-ttu-id="cf8a9-117">El parámetro puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="cf8a9-117">The parameter may be one of the following:</span></span>



| <span data-ttu-id="cf8a9-118">Value</span><span class="sxs-lookup"><span data-stu-id="cf8a9-118">Value</span></span>                                                          | <span data-ttu-id="cf8a9-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf8a9-119">Description</span></span>                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cf8a9-120">**const unsigned short** **NeverMoved = 0;**</span><span class="sxs-lookup"><span data-stu-id="cf8a9-120">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="cf8a9-121">No se ha despasado el carácter.</span><span class="sxs-lookup"><span data-stu-id="cf8a9-121">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="cf8a9-122">**const unsigned short** **UserMoved = 1;**</span><span class="sxs-lookup"><span data-stu-id="cf8a9-122">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="cf8a9-123">El usuario arrastró el carácter.</span><span class="sxs-lookup"><span data-stu-id="cf8a9-123">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="cf8a9-124">**const unsigned short** **ProgramMoved = 2;**</span><span class="sxs-lookup"><span data-stu-id="cf8a9-124">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="cf8a9-125">La aplicación ha cambiado el carácter.</span><span class="sxs-lookup"><span data-stu-id="cf8a9-125">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="cf8a9-126">**const unsigned short** **OtherProgramMoved = 3;**</span><span class="sxs-lookup"><span data-stu-id="cf8a9-126">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="cf8a9-127">Otra aplicación ha cambiado el carácter.</span><span class="sxs-lookup"><span data-stu-id="cf8a9-127">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="cf8a9-128">**const unsigned short** **SystemMoved = 4**</span><span class="sxs-lookup"><span data-stu-id="cf8a9-128">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="cf8a9-129">El servidor ha quitado el carácter para mantenerlo en la pantalla después de un cambio en la resolución de pantalla.</span><span class="sxs-lookup"><span data-stu-id="cf8a9-129">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

<span data-ttu-id="cf8a9-130">Este evento se envía a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="cf8a9-130">This event is sent to all clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf8a9-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cf8a9-131">See Also</span></span>

<span data-ttu-id="cf8a9-132">[**IAgentCharacter:: GetMoveCause**](iagentcharacter--getmovecause.md), [ **IAgentCharacter:: moveTo**](iagentcharacter--moveto.md)</span><span class="sxs-lookup"><span data-stu-id="cf8a9-132">[**IAgentCharacter::GetMoveCause**](iagentcharacter--getmovecause.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md)</span></span>


 

 






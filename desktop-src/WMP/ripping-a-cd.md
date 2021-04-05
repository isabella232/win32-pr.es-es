---
title: Copia desde CD
description: Copia desde CD
ms.assetid: f5c1b5bf-d616-48cb-8690-e0237c56e402
keywords:
- Windows Media Player, copia desde CD
- Modelo de objetos de Windows Media Player, copia desde CD
- modelo de objetos, copia desde CD
- Control ActiveX de Windows Media Player, copia desde CD
- Control ActiveX, copiar CD
- Control ActiveX móvil de Windows Media Player, copia desde CD
- Windows Media Player Mobile, copia desde CD
- CD, acerca de
- copiar CDs, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767734b3449fd0a64b31c8f351406bbf9f6c805b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903688"
---
# <a name="ripping-a-cd"></a><span data-ttu-id="94b9e-112">Copia desde CD</span><span class="sxs-lookup"><span data-stu-id="94b9e-112">Ripping a CD</span></span>

<span data-ttu-id="94b9e-113">Hay dos maneras de copiar un CD mediante el control Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="94b9e-113">There are two ways to rip a CD by using the Windows Media Player control.</span></span> <span data-ttu-id="94b9e-114">Windows Media Player 9 puede copiar CDs mediante **IWMPPlayerServices:: setTaskPane**.</span><span class="sxs-lookup"><span data-stu-id="94b9e-114">Windows Media Player 9 can rip CDs by using **IWMPPlayerServices::setTaskPane**.</span></span> <span data-ttu-id="94b9e-115">Windows Media Player 11 presenta la interfaz de **IWMPCdromRip** para copiar CDs.</span><span class="sxs-lookup"><span data-stu-id="94b9e-115">Windows Media Player 11 introduces the **IWMPCdromRip** interface for ripping CDs.</span></span> <span data-ttu-id="94b9e-116">Esta interfaz proporciona más funcionalidad que **IWMPPlayerServices:: setTaskPane** y se recomienda usar **IWMPCdromRip** si está disponible.</span><span class="sxs-lookup"><span data-stu-id="94b9e-116">This interface provides more functionality than **IWMPPlayerServices::setTaskPane**, and it is recommended that you use **IWMPCdromRip** if it is available.</span></span>

<span data-ttu-id="94b9e-117">En las secciones siguientes se describe cómo copiar un CD mediante Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="94b9e-117">The following sections describe how to rip a CD by using Windows Media Player.</span></span>

-   [<span data-ttu-id="94b9e-118">Copia desde CD mediante la interfaz IWMPCdromRip</span><span class="sxs-lookup"><span data-stu-id="94b9e-118">Ripping by Using the IWMPCdromRip Interface</span></span>](ripping-by-using-the-iwmpcdromrip-interface.md)
-   [<span data-ttu-id="94b9e-119">Copiar mediante IWMPPlayerServices:: setTaskPane</span><span class="sxs-lookup"><span data-stu-id="94b9e-119">Ripping by Using IWMPPlayerServices::setTaskPane</span></span>](ripping-by-using-iwmpplayerservices--settaskpane.md)

## <a name="related-topics"></a><span data-ttu-id="94b9e-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="94b9e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94b9e-121">**Guía de control del reproductor**</span><span class="sxs-lookup"><span data-stu-id="94b9e-121">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 





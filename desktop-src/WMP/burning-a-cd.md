---
title: Grabación de un CD
description: Grabación de un CD
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Windows Media Player, grabación de CD
- Modelo de objetos de Windows Media Player, grabación de CD
- modelo de objetos, grabación de CD
- Control ActiveX de Windows Media Player, grabación de CD
- Control ActiveX, grabación de CD
- Control ActiveX móvil de Windows Media Player, grabación de CD
- Windows Media Player Mobile, grabación de CD
- Grabación de CD, acerca de
- grabar CDs, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007b7808ff375ab0673592d0d016f8e713321d1a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149090"
---
# <a name="burning-a-cd"></a><span data-ttu-id="a10a6-112">Grabación de un CD</span><span class="sxs-lookup"><span data-stu-id="a10a6-112">Burning a CD</span></span>

<span data-ttu-id="a10a6-113">En esta sección se describe cómo usar la interfaz [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) para grabar música en un CD.</span><span class="sxs-lookup"><span data-stu-id="a10a6-113">This section describes how to use the [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface to burn music to a CD.</span></span> <span data-ttu-id="a10a6-114">La interfaz **IWMPCdromBurn** proporciona funcionalidad para grabar listas de reproducción en CDs como datos o pistas de audio, así como para borrar CD-RW.</span><span class="sxs-lookup"><span data-stu-id="a10a6-114">The **IWMPCdromBurn** interface provides functionality for burning playlists to CDs as either data or audio tracks, as well as erasing CD-RWs.</span></span>

<span data-ttu-id="a10a6-115">Uso del código</span><span class="sxs-lookup"><span data-stu-id="a10a6-115">Code Usage</span></span>

<span data-ttu-id="a10a6-116">En los ejemplos de código de esta sección se usan las clases Active Template Library (ATL), como **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="a10a6-116">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

<span data-ttu-id="a10a6-117">Encabezados incluidos</span><span class="sxs-lookup"><span data-stu-id="a10a6-117">Included Headers</span></span>

<span data-ttu-id="a10a6-118">Para usar el código de esta sección, incluya los encabezados siguientes:</span><span class="sxs-lookup"><span data-stu-id="a10a6-118">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



<span data-ttu-id="a10a6-119">Punteros de interfaz</span><span class="sxs-lookup"><span data-stu-id="a10a6-119">Interface Pointers</span></span>

<span data-ttu-id="a10a6-120">Las interfaces para Media Player de Windows se almacenan en las siguientes variables miembro:</span><span class="sxs-lookup"><span data-stu-id="a10a6-120">The interfaces for Windows Media Player are stored in the following member variables:</span></span>


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromBurn>          m_spCdromBurn;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



<span data-ttu-id="a10a6-121">En los temas siguientes se describe cómo usar la API de grabación de CD.</span><span class="sxs-lookup"><span data-stu-id="a10a6-121">The following topics describe how to use the CD burning API.</span></span>

-   [<span data-ttu-id="a10a6-122">Recuperación de la interfaz de grabación de CD</span><span class="sxs-lookup"><span data-stu-id="a10a6-122">Retrieving the CD Burning Interface</span></span>](retrieving-the-cd-burning-interface.md)
-   [<span data-ttu-id="a10a6-123">Iniciar el proceso de grabación</span><span class="sxs-lookup"><span data-stu-id="a10a6-123">Starting the Burn Process</span></span>](starting-the-burn-process.md)
-   [<span data-ttu-id="a10a6-124">Borrado de un CD regrabable</span><span class="sxs-lookup"><span data-stu-id="a10a6-124">Erasing a Rewritable CD</span></span>](erasing-a-rewritable-cd.md)
-   [<span data-ttu-id="a10a6-125">Recuperación de la unidad y el estado del disco</span><span class="sxs-lookup"><span data-stu-id="a10a6-125">Retrieving the Drive and Disc Status</span></span>](retrieving-the-drive-and-disc-status.md)
-   [<span data-ttu-id="a10a6-126">Recuperación del estado de la grabación</span><span class="sxs-lookup"><span data-stu-id="a10a6-126">Retrieving the Burn Status</span></span>](retrieving-the-burn-status.md)

## <a name="related-topics"></a><span data-ttu-id="a10a6-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a10a6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a10a6-128">**Guía de control del reproductor**</span><span class="sxs-lookup"><span data-stu-id="a10a6-128">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 





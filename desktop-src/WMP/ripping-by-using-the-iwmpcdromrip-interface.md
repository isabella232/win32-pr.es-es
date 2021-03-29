---
title: Copia desde CD mediante la interfaz IWMPCdromRip
description: Copia desde CD mediante la interfaz IWMPCdromRip
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
keywords:
- Windows Media Player, copia desde CD
- Modelo de objetos de Windows Media Player, copia desde CD
- modelo de objetos, copia desde CD
- Control ActiveX de Windows Media Player, copia desde CD
- Control ActiveX, copiar CD
- Control ActiveX móvil de Windows Media Player, copia desde CD
- Windows Media Player Mobile, copia desde CD
- Copia desde CD, interfaz de IWMPCdromRip
- copia desde CD, interfaz de IWMPCdromRip
- Interfaz IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf2e959d10385365075bb20e1c04c2d796ad2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103904412"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a><span data-ttu-id="c7139-113">Copia desde CD mediante la interfaz IWMPCdromRip</span><span class="sxs-lookup"><span data-stu-id="c7139-113">Ripping by Using the IWMPCdromRip Interface</span></span>

<span data-ttu-id="c7139-114">En esta sección se describe cómo usar la interfaz [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) para copiar música desde un CD.</span><span class="sxs-lookup"><span data-stu-id="c7139-114">This section describes how to use the [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) interface to rip music from a CD.</span></span>

<span data-ttu-id="c7139-115">La copia desde CD mediante la interfaz **IWMPCdromRip** tiene el mismo efecto que la copia de música mediante la interfaz de usuario de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c7139-115">Ripping a CD by using the **IWMPCdromRip** interface has the same effect as ripping music by using the Windows Media Player user interface.</span></span> <span data-ttu-id="c7139-116">El contenido copiado se agrega automáticamente a la biblioteca según las preferencias del usuario.</span><span class="sxs-lookup"><span data-stu-id="c7139-116">Ripped content is automatically added to the library according to the user's preferences.</span></span> <span data-ttu-id="c7139-117">Para obtener más información acerca de la copia de CD, consulte la sección acerca de la copia de música desde CDs en la ayuda de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c7139-117">For more information about CD ripping, see "Ripping music from CDs" in Windows Media Player Help.</span></span>

<span data-ttu-id="c7139-118">En los ejemplos de código de esta sección se usan las clases Active Template Library (ATL), como **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="c7139-118">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

## <a name="included-headers"></a><span data-ttu-id="c7139-119">Encabezados incluidos</span><span class="sxs-lookup"><span data-stu-id="c7139-119">Included Headers</span></span>

<span data-ttu-id="c7139-120">Para usar el código de esta sección, incluya los encabezados siguientes:</span><span class="sxs-lookup"><span data-stu-id="c7139-120">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



## <a name="interface-pointers"></a><span data-ttu-id="c7139-121">Punteros de interfaz</span><span class="sxs-lookup"><span data-stu-id="c7139-121">Interface Pointers</span></span>

<span data-ttu-id="c7139-122">Las interfaces de Media Player de Windows se almacenan en las siguientes variables de miembro.</span><span class="sxs-lookup"><span data-stu-id="c7139-122">The interfaces for Windows Media Player are stored in the following member variables.</span></span>


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromRip>           m_spCdromRip;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



<span data-ttu-id="c7139-123">En las secciones siguientes se describe cómo usar la interfaz IWMPCdromRip</span><span class="sxs-lookup"><span data-stu-id="c7139-123">The Following Sections Describe How to Use the IWMPCdromRip Interface</span></span>

-   [<span data-ttu-id="c7139-124">Recuperación de la interfaz de copia desde CD</span><span class="sxs-lookup"><span data-stu-id="c7139-124">Retrieving the Ripping Interface</span></span>](retrieving-the-ripping-interface.md)
-   [<span data-ttu-id="c7139-125">Inicio del proceso RIP</span><span class="sxs-lookup"><span data-stu-id="c7139-125">Starting the Rip Process</span></span>](starting-the-rip-process.md)
-   [<span data-ttu-id="c7139-126">Recuperación del estado de RIP</span><span class="sxs-lookup"><span data-stu-id="c7139-126">Retrieving the Rip Status</span></span>](retrieving-the-rip-status.md)
-   [<span data-ttu-id="c7139-127">Seleccionar elementos para copiar desde CD</span><span class="sxs-lookup"><span data-stu-id="c7139-127">Selecting Items for Ripping</span></span>](selecting-items-for-ripping.md)

 

 





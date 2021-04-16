---
title: Inicio del proceso RIP
description: Inicio del proceso RIP
ms.assetid: 82ffc114-ddad-41be-af80-6c1bd29cb0d4
keywords:
- Windows Media Player, copia desde CD
- Modelo de objetos de Windows Media Player, copia desde CD
- modelo de objetos, copia desde CD
- Control ActiveX de Windows Media Player, copia desde CD
- Control ActiveX, copiar CD
- Control ActiveX móvil de Windows Media Player, copia desde CD
- Windows Media Player Mobile, copia desde CD
- Copiar CD, iniciar el proceso RIP
- copiar CDs, iniciar el proceso RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2107b053abf8747d7add8fcedc26a2386ae5fd84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695538"
---
# <a name="starting-the-rip-process"></a><span data-ttu-id="b2786-112">Inicio del proceso RIP</span><span class="sxs-lookup"><span data-stu-id="b2786-112">Starting the Rip Process</span></span>

<span data-ttu-id="b2786-113">Una vez que haya recuperado la interfaz de copia desde CD como se explicó en la sección anterior, inicie el proceso de copia desde CD llamando a [IWMPCdromRip:: startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span><span class="sxs-lookup"><span data-stu-id="b2786-113">After you have retrieved the ripping interface as explained in the previous section, start the ripping process by calling [IWMPCdromRip::startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span></span>


```C++
// Start ripping.
HRESULT hr = m_spCdromRip->startRip();

```



<span data-ttu-id="b2786-114">Puede detener la operación de copia desde CD llamando a [IWMPCdromRip:: stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span><span class="sxs-lookup"><span data-stu-id="b2786-114">You can stop the ripping operation by calling [IWMPCdromRip::stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span></span>


```C++
// Stop ripping.
HRESULT hr = m_spCdromRip->stopRip();

```



## <a name="related-topics"></a><span data-ttu-id="b2786-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2786-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2786-116">**Copia desde CD**</span><span class="sxs-lookup"><span data-stu-id="b2786-116">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="b2786-117">**Recuperación de la interfaz de copia desde CD**</span><span class="sxs-lookup"><span data-stu-id="b2786-117">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="b2786-118">**Recuperación del estado de RIP**</span><span class="sxs-lookup"><span data-stu-id="b2786-118">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> <dt>

[<span data-ttu-id="b2786-119">**Seleccionar elementos para copiar desde CD**</span><span class="sxs-lookup"><span data-stu-id="b2786-119">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> </dl>

 

 





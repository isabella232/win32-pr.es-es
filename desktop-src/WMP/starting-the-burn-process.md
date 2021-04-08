---
title: Iniciar el proceso de grabación
description: Iniciar el proceso de grabación
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- Windows Media Player, grabación de CD
- Modelo de objetos de Windows Media Player, grabación de CD
- modelo de objetos, grabación de CD
- Control ActiveX de Windows Media Player, grabación de CD
- Control ActiveX, grabación de CD
- Control ActiveX móvil de Windows Media Player, grabación de CD
- Windows Media Player Mobile, grabación de CD
- Grabación de CD, iniciar proceso de grabación
- grabar CDs, iniciar el proceso de grabación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a35f473eebe35bffd48ac802dcfe79082689de
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994960"
---
# <a name="starting-the-burn-process"></a><span data-ttu-id="81c22-112">Iniciar el proceso de grabación</span><span class="sxs-lookup"><span data-stu-id="81c22-112">Starting the Burn Process</span></span>

<span data-ttu-id="81c22-113">Antes de que pueda comenzar la grabación, debe asignar una lista de reproducción para grabarla.</span><span class="sxs-lookup"><span data-stu-id="81c22-113">Before burning can begin, you must assign a playlist to be burned.</span></span> <span data-ttu-id="81c22-114">Use [IWMPCdromBurn::p UT \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) para especificar una lista de reproducción para la grabación.</span><span class="sxs-lookup"><span data-stu-id="81c22-114">Use [IWMPCdromBurn::put\_burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) to specify a playlist for burning.</span></span>


```C++
HRESULT CMainDlg::PutPlaylist (void)
{
    // Specify the burn playlist.   
    HRESULT hr = m_spCdromBurn->put_burnPlaylist(m_spPlaylist);

    // Update the status information.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromBurn->refreshStatus();
    }

    return hr;
}

```



<span data-ttu-id="81c22-115">Para obtener información sobre el uso de listas de reproducción, vea [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).</span><span class="sxs-lookup"><span data-stu-id="81c22-115">For information about using playlists, see [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).</span></span>

<span data-ttu-id="81c22-116">Para iniciar la operación de grabación, llame a [IWMPCdromBurn:: startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).</span><span class="sxs-lookup"><span data-stu-id="81c22-116">To start the burning operation, call [IWMPCdromBurn::startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).</span></span>


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



<span data-ttu-id="81c22-117">Puede detener la operación de grabación llamando a [IWMPCdromBurn:: stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).</span><span class="sxs-lookup"><span data-stu-id="81c22-117">You can stop the burning operation by calling [IWMPCdromBurn::stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).</span></span>


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a><span data-ttu-id="81c22-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81c22-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81c22-119">**Grabación de un CD**</span><span class="sxs-lookup"><span data-stu-id="81c22-119">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="81c22-120">**Recuperación de la interfaz de grabación de CD**</span><span class="sxs-lookup"><span data-stu-id="81c22-120">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="81c22-121">**Borrado de un CD regrabable**</span><span class="sxs-lookup"><span data-stu-id="81c22-121">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="81c22-122">**Recuperación de la unidad y el estado del disco**</span><span class="sxs-lookup"><span data-stu-id="81c22-122">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="81c22-123">**Recuperación del estado de la grabación**</span><span class="sxs-lookup"><span data-stu-id="81c22-123">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 





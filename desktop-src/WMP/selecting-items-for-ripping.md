---
title: Seleccionar elementos para copiar desde CD
description: Seleccionar elementos para copiar desde CD
ms.assetid: 94bc765a-8318-4715-82e0-e7a9b93e99e0
keywords:
- Windows Media Player, copia desde CD
- Modelo de objetos de Windows Media Player, copia desde CD
- modelo de objetos, copia desde CD
- Control ActiveX de Windows Media Player, copia desde CD
- Control ActiveX, copiar CD
- Control ActiveX móvil de Windows Media Player, copia desde CD
- Windows Media Player Mobile, copia desde CD
- Copiar CD, seleccionar elementos
- copiar CDs, seleccionar elementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc18ded43b609be6c7ac1f16833b0c8a33505ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994361"
---
# <a name="selecting-items-for-ripping"></a><span data-ttu-id="585a7-112">Seleccionar elementos para copiar desde CD</span><span class="sxs-lookup"><span data-stu-id="585a7-112">Selecting Items for Ripping</span></span>

<span data-ttu-id="585a7-113">A veces, un usuario no desea copiar todas las pistas de un CD.</span><span class="sxs-lookup"><span data-stu-id="585a7-113">Sometimes a user does not want to rip every track on a CD.</span></span> <span data-ttu-id="585a7-114">Windows Media Player proporciona una interfaz para especificar las pistas que se seleccionan para copiar desde CD.</span><span class="sxs-lookup"><span data-stu-id="585a7-114">Windows Media Player provides an interface for specifying which tracks are selected for ripping.</span></span> <span data-ttu-id="585a7-115">Normalmente, en una aplicación de copia de CD hay una interfaz de usuario que permite al usuario seleccionar casillas en una lista de pistas del CD.</span><span class="sxs-lookup"><span data-stu-id="585a7-115">Typically in a CD ripping application there is a user interface that lets the user select check boxes in a list of tracks on the CD.</span></span>

<span data-ttu-id="585a7-116">Es posible que no se seleccionen algunas pistas para copiar de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="585a7-116">Some tracks might not be selected for ripping by default.</span></span> <span data-ttu-id="585a7-117">Si ya hay una pista en la biblioteca de Media Player de Windows, no se seleccionará automáticamente para la copia.</span><span class="sxs-lookup"><span data-stu-id="585a7-117">If a track is already in the Windows Media Player library, it will not be automatically selected for ripping.</span></span> <span data-ttu-id="585a7-118">En el segundo ejemplo de código de esta sección se muestra cómo omitir el valor predeterminado y seleccionar manualmente una pista para copiar si ya se ha copiado.</span><span class="sxs-lookup"><span data-stu-id="585a7-118">The second code example in this section demonstrates how to bypass the default value and manually select a track for ripping if it has already been ripped.</span></span>

<span data-ttu-id="585a7-119">En el ejemplo de código siguiente se muestra cómo determinar si se ha seleccionado una pista para copiar desde CD:</span><span class="sxs-lookup"><span data-stu-id="585a7-119">The following code example demonstrates how to determine whether a track is selected for ripping:</span></span>


```C++
HRESULT CMainDlg::IsTrackSelected(long lIndex, bool &bSelected)
{
    // The track is selected unless the
    // "SelectedForRip" attribute is true.
    bSelected = true;

    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Check whether it is selected for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(
            bstrItemName,
            &bstrVal);
    }
    if (SUCCEEDED(hr))
    {
        // If getItemInfo("SelectedForRip") is not "True"
        // then the track is not selected.
        if (wcscmp(bstrVal.m_str, L"True"))
            bSelected = false;
    }

    return hr;
}

```



<span data-ttu-id="585a7-120">En el ejemplo de código siguiente se muestra cómo especificar si se ha seleccionado una pista para copiar desde CD.</span><span class="sxs-lookup"><span data-stu-id="585a7-120">The following code example demonstrates how to specify whether a track is selected for ripping.</span></span>


```C++
HRESULT CMainDlg::SelectTrack (long lIndex, bool bSelected)
{
    // bstrItemName and bstrVal are used for setItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Select the track for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        if (bSelected)
        {
            hr = bstrVal.Append("True");
        }
        else
        {
            hr = bstrVal.Append("False");
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->setItemInfo(
            bstrItemName,
            bstrVal);
    }

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="585a7-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="585a7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="585a7-122">**Copia desde CD**</span><span class="sxs-lookup"><span data-stu-id="585a7-122">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="585a7-123">**Recuperación de la interfaz de copia desde CD**</span><span class="sxs-lookup"><span data-stu-id="585a7-123">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="585a7-124">**Inicio del proceso RIP**</span><span class="sxs-lookup"><span data-stu-id="585a7-124">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="585a7-125">**Recuperación del estado de RIP**</span><span class="sxs-lookup"><span data-stu-id="585a7-125">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> </dl>

 

 





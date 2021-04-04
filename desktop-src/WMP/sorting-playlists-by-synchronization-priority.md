---
title: Ordenar listas de reproducción por prioridad de sincronización
description: Ordenar listas de reproducción por prioridad de sincronización
ms.assetid: 0f7f1ed3-0639-47bf-bf8e-52ae0a1d7ab2
keywords:
- Windows Media Player, listas de reproducción de sincronización
- Modelo de objetos de Windows Media Player, listas de reproducción de sincronización
- modelo de objetos, listas de reproducción de sincronización
- Windows Media Player Mobile, listas de reproducción de sincronización
- Control ActiveX de Windows Media Player, listas de reproducción de sincronización
- Control ActiveX móvil de Windows Media Player, listas de reproducción de sincronización
- Control ActiveX, listas de reproducción de sincronización
- listas de reproducción, sincronización
- listas de reproducción de metarchivos, sincronización
- Listas de reproducción de metarchivos de Windows Media, sincronización
- dispositivos portátiles, ordenar listas de reproducción de sincronización
- listas de reproducción de sincronización, ordenar
- listas de reproducción de sincronización, prioridades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90624e8e1cab715e8a26e33f40a444d53ab35def
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103904410"
---
# <a name="sorting-playlists-by-synchronization-priority"></a><span data-ttu-id="cd6b7-116">Ordenar listas de reproducción por prioridad de sincronización</span><span class="sxs-lookup"><span data-stu-id="cd6b7-116">Sorting Playlists by Synchronization Priority</span></span>

<span data-ttu-id="cd6b7-117">El siguiente código realiza una simple ordenación de listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="cd6b7-117">The following code performs a simple sort of playlists.</span></span> <span data-ttu-id="cd6b7-118">Puede ver cómo se usa esta función en el código de ejemplo en [enumerar listas de reproducción de sincronización](enumerating-synchronization-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="cd6b7-118">You can see how this function is used in the example code in [Enumerating Synchronization Playlists](enumerating-synchronization-playlists.md).</span></span> <span data-ttu-id="cd6b7-119">La función toma los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="cd6b7-119">The function takes the following parameters:</span></span>

-   <span data-ttu-id="cd6b7-120">*pPlaylist*.</span><span class="sxs-lookup"><span data-stu-id="cd6b7-120">*pPlaylist*.</span></span> <span data-ttu-id="cd6b7-121">Puntero a la lista de reproducción de Windows Media Player que se va a ordenar.</span><span class="sxs-lookup"><span data-stu-id="cd6b7-121">The pointer to the Windows Media Player playlist to sort.</span></span> <span data-ttu-id="cd6b7-122">Los elementos multimedia de la lista de reproducción deben apuntar a otras listas de reproducción, no a archivos de medios digitales individuales.</span><span class="sxs-lookup"><span data-stu-id="cd6b7-122">The media items in the playlist must point to other playlists, not individual digital media files.</span></span>
-   <span data-ttu-id="cd6b7-123">*bstrSyncAttribute*.</span><span class="sxs-lookup"><span data-stu-id="cd6b7-123">*bstrSyncAttribute*.</span></span> <span data-ttu-id="cd6b7-124">BSTR que contiene el nombre del atributo de Perfil de sincronización para el dispositivo actual ("Sync01", "Sync02", etc.).</span><span class="sxs-lookup"><span data-stu-id="cd6b7-124">A BSTR containing the name of the synchronization partnership attribute for the current device ("Sync01", "Sync02", and so on).</span></span>
-   <span data-ttu-id="cd6b7-125">*plSelected*.</span><span class="sxs-lookup"><span data-stu-id="cd6b7-125">*plSelected*.</span></span> <span data-ttu-id="cd6b7-126">Puntero a una variable **larga** que recibe el recuento de listas de reproducción de sincronización.</span><span class="sxs-lookup"><span data-stu-id="cd6b7-126">Pointer to a **long** variable that receives the count of synchronization playlists.</span></span>

<span data-ttu-id="cd6b7-127">La función inspecciona el atributo de Asociación de sincronización para cada elemento multimedia (que representa una lista de reproducción) en la lista de reproducción especificada por *pPlaylist*.</span><span class="sxs-lookup"><span data-stu-id="cd6b7-127">The function inspects the synchronization partnership attribute for each media item (representing a playlist) in the playlist specified by *pPlaylist*.</span></span> <span data-ttu-id="cd6b7-128">Si el atributo tiene un valor distinto de cero, el código mueve el elemento multimedia al principio de la lista de reproducción y lo inserta en orden de prioridad.</span><span class="sxs-lookup"><span data-stu-id="cd6b7-128">If the attribute has a nonzero value, the code moves the media item to the beginning of the playlist and inserts it in priority order.</span></span>

<span data-ttu-id="cd6b7-129">Cuando finaliza, la función devuelve el recuento de elementos multimedia (listas de reproducción de sincronización) que tenían un valor distinto de cero para el atributo de Perfil de sincronización.</span><span class="sxs-lookup"><span data-stu-id="cd6b7-129">When finished, the function returns the count of media items (synchronization playlists) that had a nonzero value for the synchronization partnership attribute.</span></span>


```C++
STDMETHODIMP CSyncSettings::SortPlaylist(IWMPPlaylist *pPlaylist, BSTR bstrSyncAttribute, long *plSelected)
{
    HRESULT hr = S_OK;
    long lSyncItemCount = 0;

    ATLASSERT (pPlaylist);
    ATLASSERT (plSelected);

    // Local copies of the parameters.
    CComPtr<IWMPPlaylist> spPlaylist(pPlaylist);
    CComBSTR bstrAttribute(bstrSyncAttribute);

    ATLASSERT (bstrAttribute.Length());

    // Get the count of playlist media items.
    long lCount = 0;
    spPlaylist->get_count(&lCount);

    // Walk the playlist.
    for(long i = 0; i < lCount; i++)
    {
        CComPtr<IWMPMedia> spMedia;                 
        CComBSTR bstrVal;            
        long lPriority = 0;
        
        hr = spPlaylist->get_item(i, &spMedia);

        if(SUCCEEDED(hr) && spMedia)
        {      
            // Get the sync priority value as a string.
            hr = spMedia->getItemInfo(bstrAttribute, &bstrVal);
        }

        if(SUCCEEDED(hr) && spMedia)
        {
            // Convert sync priority to a long number.
            lPriority = _wtol(bstrVal);
        }

        // Sort the playlist.
        // Only move the current item if it has a
        // sync priority value.
        if(lPriority > 0)
        {
            lSyncItemCount++;

            // Walk down the list and insert the item
            // in ascending order.
            for(long j = 0; j < lCount; j++)
            {
                CComPtr<IWMPMedia> spMediaCompare;
                CComBSTR bstrValCompare;
                long lPriorityTest = 0;

                hr = spPlaylist->get_item(j, &spMediaCompare);

                if(SUCCEEDED(hr) && spMediaCompare.p)
                {
                    hr = spMediaCompare->getItemInfo(bstrAttribute, &bstrValCompare);
                }
                if(SUCCEEDED(hr) && spMediaCompare.p)
                {
                    lPriorityTest = _wtol(bstrValCompare);
                    
                    if(lPriority <= lPriorityTest || 
                        0 == lPriorityTest)
                    {
                        hr = spPlaylist->moveItem(i, j);
                        break;                            
                    }                        
                } 
            } // for j                       
        } // if(lPriority > 0)          
    } // for i  
  
    // Return the sync item count.
    *plSelected = lSyncItemCount;

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="cd6b7-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cd6b7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd6b7-131">**IWMPMedia:: getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="cd6b7-131">**IWMPMedia::getItemInfo**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[<span data-ttu-id="cd6b7-132">**IWMPPlaylist:: get \_ Item**</span><span class="sxs-lookup"><span data-stu-id="cd6b7-132">**IWMPPlaylist::get\_item**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_item)
</dt> <dt>

[<span data-ttu-id="cd6b7-133">**IWMPPlaylist:: moveItem**</span><span class="sxs-lookup"><span data-stu-id="cd6b7-133">**IWMPPlaylist::moveItem**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-moveitem)
</dt> <dt>

[<span data-ttu-id="cd6b7-134">**Administrar listas de reproducción de sincronización**</span><span class="sxs-lookup"><span data-stu-id="cd6b7-134">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="cd6b7-135">**Atributos de sincronización**</span><span class="sxs-lookup"><span data-stu-id="cd6b7-135">**Sync Attributes**</span></span>](sync-attributes.md)
</dt> </dl>

 

 





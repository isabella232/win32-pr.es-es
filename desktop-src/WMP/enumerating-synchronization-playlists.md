---
title: Enumerar listas de reproducción de sincronización
description: Enumerar listas de reproducción de sincronización
ms.assetid: 830c3ea5-2937-48b5-b89f-ef68a6649ca3
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
- listas de reproducción de sincronización, enumeración
- dispositivos portátiles, enumeración
- enumeraciones, listas de reproducción de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29679380cec1844e9a790ac4ff047bfa4bf05288
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695547"
---
# <a name="enumerating-synchronization-playlists"></a><span data-ttu-id="b4938-116">Enumerar listas de reproducción de sincronización</span><span class="sxs-lookup"><span data-stu-id="b4938-116">Enumerating Synchronization Playlists</span></span>

<span data-ttu-id="b4938-117">En el código de ejemplo siguiente se crea una función que rellena un control ListView con listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="b4938-117">The following example code creates a function that fills a ListView control with playlists.</span></span> <span data-ttu-id="b4938-118">Las listas de reproducción de sincronización aparecen en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="b4938-118">Synchronization playlists appear first.</span></span> <span data-ttu-id="b4938-119">Las listas de reproducción de sincronización para el dispositivo seleccionado actualmente se marcan con una marca de verificación y se ordenan en orden de prioridad de sincronización.</span><span class="sxs-lookup"><span data-stu-id="b4938-119">Synchronization playlists for the currently selected device are marked with a check mark and are sorted in synchronization priority order.</span></span> <span data-ttu-id="b4938-120">Todas las demás listas de reproducción están desactivadas.</span><span class="sxs-lookup"><span data-stu-id="b4938-120">All other playlists are unchecked.</span></span>

<span data-ttu-id="b4938-121">El control ListView se configuró para la selección única.</span><span class="sxs-lookup"><span data-stu-id="b4938-121">The ListView control was configured for single selection.</span></span> <span data-ttu-id="b4938-122">El orden de las listas de reproducción en el control ListView determina su prioridad de sincronización.</span><span class="sxs-lookup"><span data-stu-id="b4938-122">The order of playlists in the ListView control determines their synchronization priority.</span></span> <span data-ttu-id="b4938-123">El estado activado de una lista de reproducción individual determina si se trata de una lista de reproducción de sincronización para el dispositivo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="b4938-123">The checked state of an individual playlist determines whether it is a synchronization playlist for the currently selected device.</span></span>

<span data-ttu-id="b4938-124">El parámetro *lPSIndex* especifica el índice de Asociación para el dispositivo portátil seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="b4938-124">The parameter *lPSIndex* specifies the partnership index for the currently selected portable device.</span></span>


```C++
STDMETHODIMP CSyncSettings::ShowPlaylists(long lPSIndex)
{ 
    HRESULT hr = S_OK; 
    ATLASSERT(m_pMainDlg);
   
    CComPtr<IWMPMediaCollection> spMediaCollection;
    CComPtr<IWMPPlaylist> spPlaylist; // Contains a playlist of all playlists.
    long lSyncItemCount= 0; // Count of items selected for synchronization. 

    ListView_DeleteAllItems(m_hPlView);

    m_spPlaylist.Release();
   
    if(lPSIndex == 0)
    {
        return S_OK;
    } 

    HCURSOR hCursor = LoadCursor(NULL, IDC_WAIT);
    HCURSOR hCursorOld = SetCursor(hCursor);

    if(SUCCEEDED(hr))
    {
        // Retrieve a pointer to IWMPMediaCollection.
        hr = m_spPlayer->get_mediaCollection(&spMediaCollection);
    }

    if(SUCCEEDED(hr) && spMediaCollection)
    {
        // Retrieve a playlist filled with IWMPMedia items.
        // Each IWMPMedia represents an individual playlist 
        // in the library.
        hr = spMediaCollection->getByAttribute(CComBSTR("MediaType"), CComBSTR("playlist"), &spPlaylist);
    }
 
    if(SUCCEEDED(hr) && spPlaylist)
    {  
        // Get the sync attribute name for the current device.
        CComBSTR bstrAttribute(g_szSyncAttributeNames[lPSIndex]);

        // Sort the playlist.
        // lSyncItemCount is the count of synchronization playlists.
        hr = SortPlaylist(spPlaylist, bstrAttribute, &lSyncItemCount);
     
        if(SUCCEEDED(hr))
        {
            m_spPlaylist = spPlaylist;  // Cache the playlist.

            long lCount = 0;
            spPlaylist->get_count(&lCount);
             
            // Fill the ListView control.
            for(long i = 0; i < lCount; i++)
            {
                CComPtr<IWMPMedia> spMedia;
                CComBSTR bstrPlaylistName;
                CComBSTR bstrVal; // Value of the SyncXX attribute.

                // Retrieve a playlist.
                hr = spPlaylist->get_item(i, &spMedia);

                if(SUCCEEDED(hr) && spMedia)
                {
                    // Get the name.
                    hr = spMedia->get_name(&bstrPlaylistName);
                }  
                if(SUCCEEDED(hr) && spMedia)
                {      
                    // Get the SyncXX attribute value.
                    hr = spMedia->getItemInfo(bstrAttribute, &bstrVal);
                }

                if(SUCCEEDED(hr) && bstrPlaylistName.Length())
                {
                    // Insert the item in the ListView control.
                    LVITEM lvI;
                    ZeroMemory(&lvI, sizeof(LVITEM));
                    lvI.mask = LVIF_TEXT; 
                    lvI.lParam = _wtol(bstrVal);
                    lvI.iItem = ListView_GetItemCount(m_hPlView);
                    lvI.pszText = "";
                    ListView_InsertItem(m_hPlView, &lvI);

                    // If this is a sync playlist, mark the check box.
                    if(i < lSyncItemCount)
                    {
                        ListView_SetCheckState(m_hPlView, i, TRUE);
                    }

                    // Display the playlist name.
                    lvI.iSubItem = 1;
                    lvI.pszText = COLE2T(bstrPlaylistName);
                    ListView_SetItem(m_hPlView, &lvI);
                }
            }
        }        
    }

    SetCursor(hCursorOld);
    return hr;
}
```



<span data-ttu-id="b4938-125">Para la implementación de la función SortPlaylist, consulte [Ordenar listas de reproducción por prioridad de sincronización](sorting-playlists-by-synchronization-priority.md).</span><span class="sxs-lookup"><span data-stu-id="b4938-125">For the implementation of the SortPlaylist function, see [Sorting Playlists by Synchronization Priority](sorting-playlists-by-synchronization-priority.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4938-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b4938-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4938-127">**IWMPMedia:: getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="b4938-127">**IWMPMedia::getItemInfo**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[<span data-ttu-id="b4938-128">**IWMPMediaCollection::getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="b4938-128">**IWMPMediaCollection::getByAttribute**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyattribute)
</dt> <dt>

[<span data-ttu-id="b4938-129">**Administrar listas de reproducción de sincronización**</span><span class="sxs-lookup"><span data-stu-id="b4938-129">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="b4938-130">**Atributos de sincronización**</span><span class="sxs-lookup"><span data-stu-id="b4938-130">**Sync Attributes**</span></span>](sync-attributes.md)
</dt> </dl>

 

 





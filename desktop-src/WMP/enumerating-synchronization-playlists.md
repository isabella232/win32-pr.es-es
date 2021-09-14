---
title: Enumeración de listas de reproducción de sincronización
description: Enumeración de listas de reproducción de sincronización
ms.assetid: 830c3ea5-2937-48b5-b89f-ef68a6649ca3
keywords:
- Reproductor de Windows Media,listas de reproducción de sincronización
- Reproductor de Windows Media de objetos, listas de reproducción de sincronización
- modelo de objetos, listas de reproducción de sincronización
- Reproductor de Windows Media Móvil, listas de reproducción de sincronización
- Reproductor de Windows Media ActiveX control, listas de reproducción de sincronización
- Reproductor de Windows Media Control de ActiveX móviles, listas de reproducción de sincronización
- ActiveX control, listas de reproducción de sincronización
- listas de reproducción, sincronización
- listas de reproducción de metarchivo, sincronización
- Windows Listas de reproducción de metarchivo multimedia, sincronización
- listas de reproducción de sincronización, enumeración
- dispositivos portátiles, enumeración
- enumeraciones, listas de reproducción de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29679380cec1844e9a790ac4ff047bfa4bf05288
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243249"
---
# <a name="enumerating-synchronization-playlists"></a>Enumeración de listas de reproducción de sincronización

En el código de ejemplo siguiente se crea una función que rellena un control ListView con listas de reproducción. Las listas de reproducción de sincronización aparecen primero. Las listas de reproducción de sincronización para el dispositivo seleccionado actualmente se marcan con una marca de verificación y se ordenan en orden de prioridad de sincronización. Todas las demás listas de reproducción están desactivadas.

El control ListView se configuró para una selección única. El orden de las listas de reproducción en el control ListView determina su prioridad de sincronización. El estado comprobado de una lista de reproducción individual determina si se trata de una lista de reproducción de sincronización para el dispositivo seleccionado actualmente.

El parámetro *lPSIndex* especifica el índice de asociación para el dispositivo portátil seleccionado actualmente.


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



Para la implementación de la función SortPlaylist, vea [Ordenar listas de reproducción por prioridad de sincronización.](sorting-playlists-by-synchronization-priority.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMPMedia::getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[**IWMPMediaCollection::getByAttribute**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyattribute)
</dt> <dt>

[**Administración de listas de reproducción de sincronización**](managing-synchronization-playlists.md)
</dt> <dt>

[**Atributos de sincronización**](sync-attributes.md)
</dt> </dl>

 

 





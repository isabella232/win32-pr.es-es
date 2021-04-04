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
# <a name="sorting-playlists-by-synchronization-priority"></a>Ordenar listas de reproducción por prioridad de sincronización

El siguiente código realiza una simple ordenación de listas de reproducción. Puede ver cómo se usa esta función en el código de ejemplo en [enumerar listas de reproducción de sincronización](enumerating-synchronization-playlists.md). La función toma los parámetros siguientes:

-   *pPlaylist*. Puntero a la lista de reproducción de Windows Media Player que se va a ordenar. Los elementos multimedia de la lista de reproducción deben apuntar a otras listas de reproducción, no a archivos de medios digitales individuales.
-   *bstrSyncAttribute*. BSTR que contiene el nombre del atributo de Perfil de sincronización para el dispositivo actual ("Sync01", "Sync02", etc.).
-   *plSelected*. Puntero a una variable **larga** que recibe el recuento de listas de reproducción de sincronización.

La función inspecciona el atributo de Asociación de sincronización para cada elemento multimedia (que representa una lista de reproducción) en la lista de reproducción especificada por *pPlaylist*. Si el atributo tiene un valor distinto de cero, el código mueve el elemento multimedia al principio de la lista de reproducción y lo inserta en orden de prioridad.

Cuando finaliza, la función devuelve el recuento de elementos multimedia (listas de reproducción de sincronización) que tenían un valor distinto de cero para el atributo de Perfil de sincronización.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMPMedia:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[**IWMPPlaylist:: get \_ Item**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_item)
</dt> <dt>

[**IWMPPlaylist:: moveItem**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-moveitem)
</dt> <dt>

[**Administrar listas de reproducción de sincronización**](managing-synchronization-playlists.md)
</dt> <dt>

[**Atributos de sincronización**](sync-attributes.md)
</dt> </dl>

 

 





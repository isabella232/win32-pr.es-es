---
title: Cambiar la prioridad de sincronización
description: Cambiar la prioridad de sincronización
ms.assetid: 992781cb-5018-4b88-aa93-2f8a86468a42
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
- dispositivos portátiles, cambiar las prioridades de la lista de reproducción
- listas de reproducción de sincronización, prioridades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327f211282e2e3b35c21dce721a17f99dcb6583d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788847"
---
# <a name="changing-synchronization-priority"></a><span data-ttu-id="0d9d1-115">Cambiar la prioridad de sincronización</span><span class="sxs-lookup"><span data-stu-id="0d9d1-115">Changing Synchronization Priority</span></span>

<span data-ttu-id="0d9d1-116">En el ejemplo de código siguiente se especifica un valor de prioridad para cada elemento del control ListView identificado por IDC \_ PLVIEW.</span><span class="sxs-lookup"><span data-stu-id="0d9d1-116">The following example code specifies a priority value for each item in the ListView control identified by IDC\_PLVIEW.</span></span> <span data-ttu-id="0d9d1-117">A los elementos marcados con una marca de verificación se les asigna un valor de prioridad en función de su orden en la lista.</span><span class="sxs-lookup"><span data-stu-id="0d9d1-117">Items that are marked with a check mark are assigned a priority value based on their order in the list.</span></span> <span data-ttu-id="0d9d1-118">A los elementos que no se comprueban se les asigna un valor de prioridad de cero.</span><span class="sxs-lookup"><span data-stu-id="0d9d1-118">Items that are not checked are assigned a priority value of zero.</span></span>


```C++
void CSyncSettings::SetPriorities()
{
    ATLASSERT(m_spPlaylist.p);
    
    long lCount = 0;
    CComBSTR bstrAttribute(g_szSyncAttributeNames[m_lCurrentPSIndex]); 
    long lPriorityCount = 0; // Tracks the next priority value to be assigned.
    long lNewPriority = 0; // Contains the new priority value for the playlist.

    HRESULT hr = m_spPlaylist->get_count(&lCount);

    if(SUCCEEDED(hr) && lCount > 0)
    {
        HCURSOR hCursor = LoadCursor(NULL, IDC_WAIT);
        HCURSOR hCursorOld = SetCursor(hCursor);

        // Walk the list.
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spMedia;
            BOOL bChecked = ListView_GetCheckState(m_hPlView, i);

            if(TRUE == bChecked)
            {
                // Assign a priority value.
                lNewPriority = ++lPriorityCount;
            }
            else
            {
                // Not a sync playlist.
                lNewPriority = 0;
            }

            // Set the attribute on the playlist.
            hr = m_spPlaylist->get_item(i, &spMedia);

            if(SUCCEEDED(hr))
            {     
                WCHAR buffer[30];
                _ltow(lNewPriority, buffer, 10);
                CComBSTR bstrPriority(buffer);
                hr = spMedia->setItemInfo(bstrAttribute, bstrPriority);
            }
        }
        SetCursor(hCursorOld);
    }       
}
```



## <a name="related-topics"></a><span data-ttu-id="0d9d1-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0d9d1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d9d1-120">**Interfaz IWMPMedia**</span><span class="sxs-lookup"><span data-stu-id="0d9d1-120">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="0d9d1-121">**Interfaz IWMPPlaylist**</span><span class="sxs-lookup"><span data-stu-id="0d9d1-121">**IWMPPlaylist Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[<span data-ttu-id="0d9d1-122">**Administrar listas de reproducción de sincronización**</span><span class="sxs-lookup"><span data-stu-id="0d9d1-122">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> </dl>

 

 





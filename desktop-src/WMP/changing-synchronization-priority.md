---
title: Cambiar la prioridad de sincronización
description: Cambiar la prioridad de sincronización
ms.assetid: 992781cb-5018-4b88-aa93-2f8a86468a42
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
- dispositivos portátiles, cambiar las prioridades de la lista de reproducción de sincronización
- listas de reproducción de sincronización, prioridades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1513679bcde31893cd7c4f456bc0e99404bb5dc66de37976f2053ae1559a4cdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997665"
---
# <a name="changing-synchronization-priority"></a>Cambiar la prioridad de sincronización

El código de ejemplo siguiente especifica un valor de prioridad para cada elemento del control ListView identificado por IDC \_ PLVIEW. A los elementos marcados con una marca de verificación se les asigna un valor de prioridad en función de su orden en la lista. A los elementos que no están activados se les asigna un valor de prioridad de cero.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMPMedia (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPPlaylist (Interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Administración de listas de reproducción de sincronización**](managing-synchronization-playlists.md)
</dt> </dl>

 

 





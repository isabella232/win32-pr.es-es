---
title: Administración de listas de reproducción de sincronización
description: Administración de listas de reproducción de sincronización
ms.assetid: 5891ada0-37a6-4256-9885-8aa9dbe98b7c
keywords:
- Reproductor de Windows Media dispositivos portátiles
- Reproductor de Windows Media de objetos, dispositivos portátiles
- modelo de objetos, dispositivos portátiles
- Reproductor de Windows Media ActiveX, dispositivos portátiles
- ActiveX, dispositivos portátiles
- Reproductor de Windows Media Control ActiveX dispositivos móviles, dispositivos portátiles
- Reproductor de Windows Media Dispositivos móviles y portátiles
- dispositivos portátiles, administración de listas de reproducción de sincronización
- sincronización de dispositivos, listas de reproducción
- sincronizar dispositivos, listas de reproducción
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
- listas de reproducción de sincronización, administración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10253d7f08c618d62079ccc1767fdaf85560861eae68d39cd897e7959eaffcad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996375"
---
# <a name="managing-synchronization-playlists"></a>Administración de listas de reproducción de sincronización

Reproductor de Windows Media 10 o posterior usa listas de reproducción para sincronizar archivos multimedia digitales con dispositivos portátiles. En esta sección se explica cómo trabajar con listas de reproducción de sincronización.

El código de ejemplo de esta sección usa dos controles ListView para mostrar información. El primer control ListView (IDC PLVIEW) muestra todas las listas de reproducción de la biblioteca Reproductor de Windows Media, y las listas de reproducción de sincronización \_ aparecen primero. Las listas de reproducción de sincronización para el dispositivo seleccionado actualmente se marcan con una marca de verificación y se ordenan en orden de prioridad de sincronización. Todas las demás listas de reproducción están desactivadas. El control ListView se configuró para una selección única. El orden de las listas de reproducción en el control ListView determina su prioridad de sincronización. El estado comprobado de una lista de reproducción individual determina si se trata de una lista de reproducción de sincronización para el dispositivo seleccionado actualmente.

El segundo control ListView (IDC \_ MEDIAVIEW) muestra los elementos multimedia en la lista de reproducción seleccionada. Dos columnas adicionales muestran texto que indica si el archivo multimedia digital se copió en el dispositivo y, en caso de error, si se ha producido un error en la copia porque el archivo multimedia digital no cabe.

El código de ejemplo siguiente muestra cómo se inicializan los controles ListView:


```C++
STDMETHODIMP CSyncSettings::InitListView()
{
    m_hPlView = GetDlgItem(IDC_PLVIEW);
    m_hMediaView = GetDlgItem(IDC_MEDIAVIEW); 

    ATLASSERT(m_hPlView);
    ATLASSERT(m_hMediaView);

    // Sync playlist information.
    // Selection highlights all rows.
    // Show checkboxes.
    ListView_SetExtendedListViewStyleEx(m_hPlView, 0, LVS_EX_CHECKBOXES | LVS_EX_FULLROWSELECT);
   
    // Add headers.
    LVCOLUMN lvc;
    ZeroMemory(&lvc, sizeof(LVCOLUMN));
    lvc.mask = LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM; 
    lvc.iSubItem = 0;
    
    lvc.pszText = _T("Sync");
    lvc.cx = 40;
    ListView_InsertColumn(m_hPlView, lvc.iSubItem, &lvc);

    lvc.iSubItem++;
    lvc.pszText = _T("Playlist Name");
    lvc.cx = 300;
    ListView_InsertColumn(m_hPlView, lvc.iSubItem, &lvc); 

    // Media information.
    // Selection highlights all rows.
    ListView_SetExtendedListViewStyleEx(m_hMediaView, 0, LVS_EX_FULLROWSELECT);

    // Add headers
    ZeroMemory(&lvc, sizeof(LVCOLUMN));
    lvc.mask = LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM; 
    lvc.iSubItem = 0;
    
    lvc.pszText = _T("Media name");
    lvc.cx = 150;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);

    lvc.iSubItem++;
    lvc.pszText = _T("On Device");
    lvc.cx = 69;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);  

    lvc.iSubItem++;
    lvc.pszText = _T("Fit?");
    lvc.cx = 40;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);  
   
    return S_OK;
}
```



La siguiente matriz de cadenas contiene los nombres de los atributos de sincronización utilizados en los ejemplos:


```C++
static const TCHAR *g_szSyncAttributeNames[17] = {
        _T("Not used"), // Do not access this one.
        _T("Sync01"),
        _T("Sync02"),
        _T("Sync03"),
        _T("Sync04"),
        _T("Sync05"),
        _T("Sync06"),
        _T("Sync07"),
        _T("Sync08"),
        _T("Sync09"),
        _T("Sync10"),
        _T("Sync11"),
        _T("Sync12"),
        _T("Sync13"),
        _T("Sync14"),
        _T("Sync15"),
        _T("Sync16")};
```



La siguiente variable miembro contiene una lista de reproducción que contiene todas las listas de reproducción de la Reproductor de Windows Media lista de reproducción. Cada lista de reproducción se representa como un elemento multimedia.


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



En las secciones siguientes se proporciona código de ejemplo:

-   [Enumeración de listas de reproducción de sincronización](enumerating-synchronization-playlists.md)
-   [Ordenar listas de reproducción por prioridad de sincronización](sorting-playlists-by-synchronization-priority.md)
-   [Enumeración de los elementos multimedia](enumerating-the-media-items.md)
-   [Determinar el estado de sincronización de la lista de reproducción](determining-playlist-synchronization-state.md)
-   [Cambiar la prioridad de sincronización](changing-synchronization-priority.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con dispositivos portátiles**](working-with-portable-devices.md)
</dt> </dl>

 

 





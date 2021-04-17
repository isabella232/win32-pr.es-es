---
title: Administrar listas de reproducción de sincronización
description: Administrar listas de reproducción de sincronización
ms.assetid: 5891ada0-37a6-4256-9885-8aa9dbe98b7c
keywords:
- Windows Media Player, dispositivos portátiles
- Modelo de objetos de Windows Media Player, dispositivos portátiles
- modelo de objetos, dispositivos portátiles
- Control ActiveX de Windows Media Player, dispositivos portátiles
- Control ActiveX, dispositivos portátiles
- Control ActiveX móvil de Windows Media Player, dispositivos portátiles
- Windows Media Player dispositivos móviles y portátiles
- dispositivos portátiles, administrar listas de reproducción de sincronización
- sincronización de dispositivos, listas de reproducción
- sincronizar dispositivos, listas de reproducción
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
- listas de reproducción de sincronización, administrar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be0fe084918c0b69b827dbb941388246cbd177ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704812"
---
# <a name="managing-synchronization-playlists"></a><span data-ttu-id="6e138-124">Administrar listas de reproducción de sincronización</span><span class="sxs-lookup"><span data-stu-id="6e138-124">Managing Synchronization Playlists</span></span>

<span data-ttu-id="6e138-125">Windows Media Player 10 o posterior usa listas de reproducción para sincronizar archivos multimedia digitales con dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="6e138-125">Windows Media Player 10 or later uses playlists to synchronize digital media files with portable devices.</span></span> <span data-ttu-id="6e138-126">En esta sección se explica cómo trabajar con listas de reproducción de sincronización.</span><span class="sxs-lookup"><span data-stu-id="6e138-126">This section explains how to work with synchronization playlists.</span></span>

<span data-ttu-id="6e138-127">En el código de ejemplo de esta sección se usan dos controles ListView para mostrar información.</span><span class="sxs-lookup"><span data-stu-id="6e138-127">The example code in this section uses two ListView controls to display information.</span></span> <span data-ttu-id="6e138-128">El primer control ListView (IDC \_ PLVIEW) muestra todas las listas de reproducción de la biblioteca de Windows Media Player, donde las listas de reproducción de sincronización aparecen en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="6e138-128">The first ListView control (IDC\_PLVIEW) displays all of the playlists in the Windows Media Player library, with synchronization playlists appearing first.</span></span> <span data-ttu-id="6e138-129">Las listas de reproducción de sincronización para el dispositivo seleccionado actualmente se marcan con una marca de verificación y se ordenan en orden de prioridad de sincronización.</span><span class="sxs-lookup"><span data-stu-id="6e138-129">Synchronization playlists for the currently selected device are marked with a check mark and are sorted in synchronization priority order.</span></span> <span data-ttu-id="6e138-130">Todas las demás listas de reproducción están desactivadas.</span><span class="sxs-lookup"><span data-stu-id="6e138-130">All other playlists are unchecked.</span></span> <span data-ttu-id="6e138-131">El control ListView se configuró para la selección única.</span><span class="sxs-lookup"><span data-stu-id="6e138-131">The ListView control was configured for single selection.</span></span> <span data-ttu-id="6e138-132">El orden de las listas de reproducción en el control ListView determina su prioridad de sincronización.</span><span class="sxs-lookup"><span data-stu-id="6e138-132">The order of playlists in the ListView control determines their synchronization priority.</span></span> <span data-ttu-id="6e138-133">El estado activado de una lista de reproducción individual determina si se trata de una lista de reproducción de sincronización para el dispositivo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="6e138-133">The checked state of an individual playlist determines whether it is a synchronization playlist for the currently selected device.</span></span>

<span data-ttu-id="6e138-134">El segundo control ListView (IDC \_ MEDIAVIEW) muestra los elementos multimedia en la lista de reproducción seleccionada.</span><span class="sxs-lookup"><span data-stu-id="6e138-134">The second ListView control (IDC\_MEDIAVIEW) displays the media items in the selected playlist.</span></span> <span data-ttu-id="6e138-135">Dos columnas adicionales muestran texto que indica si el archivo multimedia digital se copió en el dispositivo y, en caso de error, si se produjo un error en la copia porque el archivo multimedia digital no se ajustaba.</span><span class="sxs-lookup"><span data-stu-id="6e138-135">Two additional columns display text indicating whether the digital media file was copied to the device and, in the case of a failure, whether the copy failed because the digital media file did not fit.</span></span>

<span data-ttu-id="6e138-136">En el ejemplo de código siguiente se muestra cómo se inicializan los controles ListView:</span><span class="sxs-lookup"><span data-stu-id="6e138-136">The following example code shows how the ListView controls are initialized:</span></span>


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



<span data-ttu-id="6e138-137">La siguiente matriz de cadenas contiene los nombres de los atributos de sincronización usados en los ejemplos:</span><span class="sxs-lookup"><span data-stu-id="6e138-137">The following array of strings contains the names of the synchronization attributes used in the examples:</span></span>


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



<span data-ttu-id="6e138-138">La siguiente variable miembro contiene una lista de reproducción que contiene todas las listas de reproducción de la biblioteca de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6e138-138">The following member variable contains a playlist containing all playlists in the Windows Media Player library.</span></span> <span data-ttu-id="6e138-139">Cada lista de reproducción se representa como un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="6e138-139">Each playlist is represented as a media item.</span></span>


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



<span data-ttu-id="6e138-140">En las secciones siguientes se proporciona código de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6e138-140">The following sections provide example code:</span></span>

-   [<span data-ttu-id="6e138-141">Enumerar listas de reproducción de sincronización</span><span class="sxs-lookup"><span data-stu-id="6e138-141">Enumerating Synchronization Playlists</span></span>](enumerating-synchronization-playlists.md)
-   [<span data-ttu-id="6e138-142">Ordenar listas de reproducción por prioridad de sincronización</span><span class="sxs-lookup"><span data-stu-id="6e138-142">Sorting Playlists by Synchronization Priority</span></span>](sorting-playlists-by-synchronization-priority.md)
-   [<span data-ttu-id="6e138-143">Enumerar los elementos multimedia</span><span class="sxs-lookup"><span data-stu-id="6e138-143">Enumerating the Media Items</span></span>](enumerating-the-media-items.md)
-   [<span data-ttu-id="6e138-144">Determinar el estado de sincronización de la lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="6e138-144">Determining Playlist Synchronization State</span></span>](determining-playlist-synchronization-state.md)
-   [<span data-ttu-id="6e138-145">Cambiar la prioridad de sincronización</span><span class="sxs-lookup"><span data-stu-id="6e138-145">Changing Synchronization Priority</span></span>](changing-synchronization-priority.md)

## <a name="related-topics"></a><span data-ttu-id="6e138-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6e138-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e138-147">**Trabajar con dispositivos portátiles**</span><span class="sxs-lookup"><span data-stu-id="6e138-147">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 





---
title: Recuperación del estado de RIP
description: Recuperación del estado de RIP
ms.assetid: 9907bfdd-eae7-4ca2-b488-5a6ad11416f5
keywords:
- Windows Media Player, copia desde CD
- Modelo de objetos de Windows Media Player, copia desde CD
- modelo de objetos, copia desde CD
- Control ActiveX de Windows Media Player, copia desde CD
- Control ActiveX, copiar CD
- Control ActiveX móvil de Windows Media Player, copia desde CD
- Windows Media Player Mobile, copia desde CD
- Copiar CD, recuperar el estado de RIP
- copiar CDs, recuperar el estado de RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be1fce1a46f9cc2d8477cabcc12a3a1b5bd159d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077356"
---
# <a name="retrieving-the-rip-status"></a><span data-ttu-id="b5c58-112">Recuperación del estado de RIP</span><span class="sxs-lookup"><span data-stu-id="b5c58-112">Retrieving the Rip Status</span></span>

<span data-ttu-id="b5c58-113">Puede supervisar el progreso de la operación de copia desde CD llamando periódicamente a [IWMPCdromRip:: get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span><span class="sxs-lookup"><span data-stu-id="b5c58-113">You can monitor the progress of the ripping operation by periodically calling [IWMPCdromRip::get\_ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span></span> <span data-ttu-id="b5c58-114">Este método recupera un valor de progreso para toda la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="b5c58-114">This method retrieves a progress value for the entire ripping operation.</span></span> <span data-ttu-id="b5c58-115">El valor recuperado es un número que representa el porcentaje de copia completada, de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="b5c58-115">The value retrieved is a number that represents the percentage of ripping completed, from 0 to 100.</span></span>

<span data-ttu-id="b5c58-116">El valor de progreso representa el porcentaje completado de todo el proceso de copia.</span><span class="sxs-lookup"><span data-stu-id="b5c58-116">The progress value represents the completed percentage of the entire ripping process.</span></span> <span data-ttu-id="b5c58-117">Para determinar el progreso de una pista concreta, use [IWMPMedia:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) con "RipProgress" como nombre de atributo.</span><span class="sxs-lookup"><span data-stu-id="b5c58-117">To determine the progress of a specific track, use [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) with "RipProgress" as the attribute name.</span></span> <span data-ttu-id="b5c58-118">Para determinar el índice de la pista que se está copiando actualmente, llame a **IWMPPlaylist:: getItemInfo** con "CurrentRipTrackIndex" como nombre de atributo.</span><span class="sxs-lookup"><span data-stu-id="b5c58-118">To determine the index of the track currently being ripped, call **IWMPPlaylist::getItemInfo** with "CurrentRipTrackIndex" as the attribute name.</span></span>

<span data-ttu-id="b5c58-119">Puede supervisar el estado de la operación de copia desde CD llamando periódicamente a [IWMPCdromRip:: get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span><span class="sxs-lookup"><span data-stu-id="b5c58-119">You can monitor the state of the ripping operation by periodically calling [IWMPCdromRip::get\_ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span></span> <span data-ttu-id="b5c58-120">Este método recupera un valor de enumeración [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) que indica si la operación está en curso o detenido.</span><span class="sxs-lookup"><span data-stu-id="b5c58-120">This method retrieves a [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) enumeration value that indicates whether the operation is in progress or stopped.</span></span> <span data-ttu-id="b5c58-121">También puede supervisar el estado de la operación de copia desde CD mediante el control del evento [IWMPEvents3:: CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) .</span><span class="sxs-lookup"><span data-stu-id="b5c58-121">You can also monitor the state of the ripping operation by handling the [IWMPEvents3::CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) event.</span></span> <span data-ttu-id="b5c58-122">(Vea [controlar eventos en C++](handling-events-in-c.md)). Tenga cuidado de comparar el puntero **IWMPCdromRip** (proporcionado por el evento) con el puntero que representa la operación de copia desde CD, para asegurarse de que la operación ha generado el evento.</span><span class="sxs-lookup"><span data-stu-id="b5c58-122">(See [Handling Events in C++](handling-events-in-c.md).) Be careful to compare the **IWMPCdromRip** pointer (provided by the event) to the pointer that represents your ripping operation, to ensure that the event was raised by your operation.</span></span>

<span data-ttu-id="b5c58-123">En el ejemplo de código siguiente se muestra cómo usar estas funciones para recuperar el estado de una operación de copia desde CD.</span><span class="sxs-lookup"><span data-stu-id="b5c58-123">The following example code shows how to use these functions to retrieve the status of a ripping operation.</span></span>

<span data-ttu-id="b5c58-124">En el ejemplo de código se definen los siguientes controles de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b5c58-124">The following dialog controls are defined for the code example.</span></span>



| <span data-ttu-id="b5c58-125">Id. de control</span><span class="sxs-lookup"><span data-stu-id="b5c58-125">Control ID</span></span>                   | <span data-ttu-id="b5c58-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5c58-126">Description</span></span>                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c58-127">\_seguimiento actual de IDC \_</span><span class="sxs-lookup"><span data-stu-id="b5c58-127">IDC\_CURRENT\_TRACK</span></span>          | <span data-ttu-id="b5c58-128">Texto estático que representa el índice de la pista que se está copiando en ese momento.</span><span class="sxs-lookup"><span data-stu-id="b5c58-128">Static text that represents the index of the track currently being ripped.</span></span>                                         |
| <span data-ttu-id="b5c58-129">\_texto de \_ progreso de seguimiento de IDC \_</span><span class="sxs-lookup"><span data-stu-id="b5c58-129">IDC\_TRACK\_PROGRESS\_TEXT</span></span>   | <span data-ttu-id="b5c58-130">Texto estático que representa el progreso de la pista que se está copiando actualmente como porcentaje.</span><span class="sxs-lookup"><span data-stu-id="b5c58-130">Static text that represents the progress of the track currently being ripped as a percentage.</span></span>                      |
| <span data-ttu-id="b5c58-131">\_seguimiento de progreso de IDC \_</span><span class="sxs-lookup"><span data-stu-id="b5c58-131">IDC\_PROGRESS\_TRACK</span></span>         | <span data-ttu-id="b5c58-132">Barra de progreso con el intervalo de 0 a 100 que representa el progreso de la pista que se está copiando actualmente como porcentaje.</span><span class="sxs-lookup"><span data-stu-id="b5c58-132">Progress bar with range 0 to 100 that represents the progress of the track currently being ripped as a percentage.</span></span> |
| <span data-ttu-id="b5c58-133">\_texto de \_ progreso \_ General de IDC</span><span class="sxs-lookup"><span data-stu-id="b5c58-133">IDC\_OVERALL\_PROGRESS\_TEXT</span></span> | <span data-ttu-id="b5c58-134">Texto estático que representa el progreso del proceso de copia de copia total como un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="b5c58-134">Static text that represents the progress of the total ripping process as a percentage.</span></span>                             |
| <span data-ttu-id="b5c58-135">\_progreso \_ General de IDC</span><span class="sxs-lookup"><span data-stu-id="b5c58-135">IDC\_PROGRESS\_OVERALL</span></span>       | <span data-ttu-id="b5c58-136">Barra de progreso con el intervalo de 0 a 100 que representa el progreso del proceso de copia de copia total como un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="b5c58-136">Progress bar with range 0 to 100 that represents the progress of the total ripping process as a percentage.</span></span>        |
| <span data-ttu-id="b5c58-137">\_Estado RIP de IDC \_</span><span class="sxs-lookup"><span data-stu-id="b5c58-137">IDC\_RIP\_STATE</span></span>              | <span data-ttu-id="b5c58-138">Texto estático que muestra la operación que se está realizando actualmente ("copia desde CD", "detenida" o "desconocida")</span><span class="sxs-lookup"><span data-stu-id="b5c58-138">Static text that displays the operation currently being performed ("Ripping", "Stopped", or "Unknown")</span></span>             |



 


```C++
HRESULT CMainDlg::UpdateStatus (void)
{
    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get the current track index.
    HRESULT hr = bstrItemName.Append("CurrentRipTrackIndex");
    if (SUCCEEDED(hr))
    {
        hr = m_spPlaylist->getItemInfo(bstrItemName, &bstrVal);
    }

    // Update the dialog text with the track number.
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_CURRENT_TRACK, bstrVal.m_str);
    }

    // Get an IWMPMedia interface from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    if (SUCCEEDED(hr))
    {
        long lIndex = _wtol(bstrVal.m_str);
        hr = m_spPlaylist->get_item(lIndex, &spMedia);
    }

    // Update the current track progress bar and progress text.
    if (SUCCEEDED(hr))
    {
        bstrItemName.Empty();
        hr = bstrItemName.Append("RipProgress");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(bstrItemName, &bstrVal);
    }

    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemTextW(IDC_TRACK_PROGRESS_TEXT, bstrVal.m_str);

        // Obtain a numerical value from the progress string.
        long lTrackPosition = _wtol(bstrVal.m_str);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_TRACK),
            PBM_SETPOS, lTrackPosition, 0);
    }

    // Update the total progress bar and progress text.
    long lTotalPosition = 0;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripProgress(&lTotalPosition);
    }
    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemInt(IDC_OVERALL_PROGRESS_TEXT, lTotalPosition);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_OVERALL),
            PBM_SETPOS, lTotalPosition, 0);
    }

    // Update the ripping state.
    CComBSTR bstrState;
    WMPRipState wmprs = wmprsUnknown;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripState(&wmprs);
    }
    if (SUCCEEDED(hr))
    {
        switch (wmprs)
        {
            case wmprsUnknown:
            default:
                hr = bstrState.Append("Unknown");
                break;
            case wmprsRipping:
                hr = bstrState.Append("Ripping");
                break;
            case wmprsStopped:
                hr = bstrState.Append("Stopped");
                break;
        }
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_RIP_STATE, bstrState.m_str);
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="b5c58-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b5c58-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5c58-140">**Copia desde CD**</span><span class="sxs-lookup"><span data-stu-id="b5c58-140">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="b5c58-141">**Recuperación de la interfaz de copia desde CD**</span><span class="sxs-lookup"><span data-stu-id="b5c58-141">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="b5c58-142">**Inicio del proceso RIP**</span><span class="sxs-lookup"><span data-stu-id="b5c58-142">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="b5c58-143">**Seleccionar elementos para copiar desde CD**</span><span class="sxs-lookup"><span data-stu-id="b5c58-143">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> </dl>

 

 





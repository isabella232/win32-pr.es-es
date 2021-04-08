---
title: Recuperación del estado de la grabación
description: Recuperación del estado de la grabación
ms.assetid: 63b6525d-00be-4c68-8473-3bc1a58fde15
keywords:
- Windows Media Player, grabación de CD
- Modelo de objetos de Windows Media Player, grabación de CD
- modelo de objetos, grabación de CD
- Control ActiveX de Windows Media Player, grabación de CD
- Control ActiveX, grabación de CD
- Control ActiveX móvil de Windows Media Player, grabación de CD
- Windows Media Player Mobile, grabación de CD
- Grabación de CD, recuperación del estado de la grabación
- grabar CDs, recuperar el estado de la grabación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9b9ab1d865b728c3a23b9b77f45ab022226605
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994963"
---
# <a name="retrieving-the-burn-status"></a><span data-ttu-id="02efa-112">Recuperación del estado de la grabación</span><span class="sxs-lookup"><span data-stu-id="02efa-112">Retrieving the Burn Status</span></span>

<span data-ttu-id="02efa-113">En el ejemplo de código siguiente, se definen los siguientes controles de cuadro de diálogo:</span><span class="sxs-lookup"><span data-stu-id="02efa-113">In the code example that follows, the following dialog controls are defined:</span></span>



| <span data-ttu-id="02efa-114">Id. de control</span><span class="sxs-lookup"><span data-stu-id="02efa-114">Control ID</span></span>           | <span data-ttu-id="02efa-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="02efa-115">Description</span></span>                                                                    |
|----------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="02efa-116">\_Estado de grabación de IDC \_</span><span class="sxs-lookup"><span data-stu-id="02efa-116">IDC\_BURN\_STATE</span></span>     | <span data-ttu-id="02efa-117">Texto estático que representa el estado de la operación de grabación de CD.</span><span class="sxs-lookup"><span data-stu-id="02efa-117">Static text that represents the state of the CD burning operation.</span></span>             |
| <span data-ttu-id="02efa-118">progreso de IDC \_</span><span class="sxs-lookup"><span data-stu-id="02efa-118">IDC\_PROGRESS</span></span>        | <span data-ttu-id="02efa-119">Barra de progreso con un intervalo de 0 a 100 que representa el progreso total de la grabación.</span><span class="sxs-lookup"><span data-stu-id="02efa-119">Progress bar with a range of 0 to 100 that represents the total burn progress.</span></span> |
| <span data-ttu-id="02efa-120">\_texto de progreso de IDC \_</span><span class="sxs-lookup"><span data-stu-id="02efa-120">IDC\_PROGRESS\_TEXT</span></span>  | <span data-ttu-id="02efa-121">Texto estático que representa el progreso de la grabación total como un número comprendido entre 0 y 100.</span><span class="sxs-lookup"><span data-stu-id="02efa-121">Static text that represents the total burn progress as a number from 0 to 100.</span></span> |
| <span data-ttu-id="02efa-122">\_hora disponible de IDC \_</span><span class="sxs-lookup"><span data-stu-id="02efa-122">IDC\_AVAILABLE\_TIME</span></span> | <span data-ttu-id="02efa-123">Texto estático para mostrar la hora disponible en el CD, en segundos.</span><span class="sxs-lookup"><span data-stu-id="02efa-123">Static text to display the time available on the CD, in seconds.</span></span>               |
| <span data-ttu-id="02efa-124">\_espacio libre de IDC \_</span><span class="sxs-lookup"><span data-stu-id="02efa-124">IDC\_FREE\_SPACE</span></span>     | <span data-ttu-id="02efa-125">Texto estático para mostrar el espacio disponible en el CD, en bytes.</span><span class="sxs-lookup"><span data-stu-id="02efa-125">Static text to display the free space on the CD, in bytes.</span></span>                     |
| <span data-ttu-id="02efa-126">\_espacio total de IDC \_</span><span class="sxs-lookup"><span data-stu-id="02efa-126">IDC\_TOTAL\_SPACE</span></span>    | <span data-ttu-id="02efa-127">Texto estático que muestra la capacidad total del CD, en bytes.</span><span class="sxs-lookup"><span data-stu-id="02efa-127">Static text to display the total capacity of the CD, in bytes.</span></span>                 |



 

<span data-ttu-id="02efa-128">Puede supervisar el progreso de la operación de grabación llamando periódicamente a [IWMPCdromBurn:: get \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) mientras se graba el CD.</span><span class="sxs-lookup"><span data-stu-id="02efa-128">You can monitor the progress of the burning operation by periodically calling [IWMPCdromBurn::get\_burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) while the CD is being burned.</span></span> <span data-ttu-id="02efa-129">Este método recupera un valor de progreso para toda la operación de grabación.</span><span class="sxs-lookup"><span data-stu-id="02efa-129">This method retrieves a progress value for the entire burning operation.</span></span> <span data-ttu-id="02efa-130">El valor recuperado es un número que representa el porcentaje de grabación completada, de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="02efa-130">The value retrieved is a number that represents the percentage of burning completed, from 0 to 100.</span></span>


```C++
// Update the progress bar IDC_PROGRESS
// and the corresponding text string IDC_PROGRESS_TEXT.
long lProgress = 0;
hr = m_spCdromBurn->get_burnProgress(&lProgress);
if (SUCCEEDED(hr))
{
    SendMessage(GetDlgItem(IDC_PROGRESS),
        PBM_SETPOS, lProgress, 0);
    SetDlgItemInt(IDC_PROGRESS_TEXT, lProgress);
}

```



<span data-ttu-id="02efa-131">Puede obtener el estado actual de la operación de grabación llamando a [IWMPCdromBurn:: get \_ burnState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate).</span><span class="sxs-lookup"><span data-stu-id="02efa-131">You can get the current state of the burning operation by calling [IWMPCdromBurn::get\_burnState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate).</span></span> <span data-ttu-id="02efa-132">Este método recupera una enumeración que especifica la operación actual que se está llevando a cabo.</span><span class="sxs-lookup"><span data-stu-id="02efa-132">This method retrieves an enumeration specifying the current operation being performed.</span></span>


```C++
// Retrieve the burn state.
WMPBurnState wmpbs = wmpbsUnknown;
HRESULT hr = m_spCdromBurn->get_burnState(&wmpbs);

if (SUCCEEDED(hr))
{
    // Set the burn state string.
    CComBSTR bstrState;
    switch (wmpbs)
    {
        case wmpbsUnknown:
        default:
            hr = bstrState.Append("Unknown state.");
            break;
        case wmpbsBusy:
            hr = bstrState.Append("Windows Media Player is Busy.");
            break;
        case wmpbsReady:
            hr = bstrState.Append("Ready to begin burning.");
            break;
        case wmpbsWaitingForDisc:
            hr = bstrState.Append("Waiting for disc.");
            break;
        case wmpbsRefreshStatusPending:
            hr = bstrState.Append("The burn playlist has changed.");
            m_spCdromBurn->refreshStatus();
            break;
        case wmpbsPreparingToBurn:
            hr = bstrState.Append("Preparing to burn the CD.");
            break;
        case wmpbsBurning:
            hr = bstrState.Append("The CD is being burned.");
            break;
        case wmpbsStopped:
            hr = bstrState.Append("The burning operation is stopped.");
            break;
        case wmpbsErasing:
            hr = bstrState.Append("Erasing the CD.");
            break;
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_BURN_STATE, bstrState.m_str);
    }
}

```



<span data-ttu-id="02efa-133">Para recuperar el número de segundos de audio que puede contener el CD, llame a [IWMPCdromBurn:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) con "AvailableTime" como primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="02efa-133">To retrieve the number of seconds of audio the CD can hold, call [IWMPCdromBurn::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) with "AvailableTime" as the first parameter.</span></span> <span data-ttu-id="02efa-134">El valor recuperado por esta función se representa mediante una cadena.</span><span class="sxs-lookup"><span data-stu-id="02efa-134">The value retrieved by this function is represented by a string.</span></span>


```C++
// Set "AvailableTime" string
CComBSTR bstrTime;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("AvailableTime");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTime);
}
if (SUCCEEDED(hr))
{
    hr = bstrTime.Append(" seconds");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_AVAILABLE_TIME, bstrTime.m_str);
}

```



<span data-ttu-id="02efa-135">Para recuperar la cantidad de espacio libre en un disco, llame a **IWMPCdromBurn:: getItemInfo** con "FreeSpace" como primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="02efa-135">To retrieve the amount of free space on a disc, call **IWMPCdromBurn::getItemInfo** with "FreeSpace" as the first parameter.</span></span> <span data-ttu-id="02efa-136">El valor recuperado por esta función es una cadena que representa el número de bytes libres disponibles en el disco.</span><span class="sxs-lookup"><span data-stu-id="02efa-136">The value retrieved by this function is a string that represents the number of free bytes available on the disc.</span></span>


```C++
// Set "FreeSpace" string
CComBSTR bstrFreeSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("FreeSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrFreeSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrFreeSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_FREE_SPACE, bstrFreeSpace.m_str);
}

```



<span data-ttu-id="02efa-137">Para recuperar la capacidad total de un disco, llame a **IWMPCdromBurn:: getItemInfo** con "TotalSpace" como primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="02efa-137">To retrieve the total capacity of a disc, call **IWMPCdromBurn::getItemInfo** with "TotalSpace" as the first parameter.</span></span> <span data-ttu-id="02efa-138">El valor recuperado por esta función es una cadena que corresponde al número total de bytes del disco.</span><span class="sxs-lookup"><span data-stu-id="02efa-138">The value retrieved by this function is a string that corresponds to the total number of bytes on the disc.</span></span>


```C++
// Set "TotalSpace" string.
CComBSTR bstrTotalSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("TotalSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTotalSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrTotalSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_TOTAL_SPACE, bstrTotalSpace.m_str);
}

```



## <a name="related-topics"></a><span data-ttu-id="02efa-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02efa-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02efa-140">**Grabación de un CD**</span><span class="sxs-lookup"><span data-stu-id="02efa-140">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="02efa-141">**Recuperación de la interfaz de grabación de CD**</span><span class="sxs-lookup"><span data-stu-id="02efa-141">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="02efa-142">**Iniciar el proceso de grabación**</span><span class="sxs-lookup"><span data-stu-id="02efa-142">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="02efa-143">**Borrado de un CD regrabable**</span><span class="sxs-lookup"><span data-stu-id="02efa-143">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="02efa-144">**Recuperación de la unidad y el estado del disco**</span><span class="sxs-lookup"><span data-stu-id="02efa-144">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> </dl>

 

 





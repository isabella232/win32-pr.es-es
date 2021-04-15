---
title: Determinar el estado de sincronización de la lista de reproducción
description: Determinar el estado de sincronización de la lista de reproducción
ms.assetid: 634b659b-c3ae-4957-b17e-18fd92e915be
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
- dispositivos portátiles, determinar el estado de la lista de reproducción
- listas de reproducción de sincronización, estado de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9758cfbb73c698a40d6d4f48e645e57750d8a332
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695528"
---
# <a name="determining-playlist-synchronization-state"></a><span data-ttu-id="9d313-115">Determinar el estado de sincronización de la lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="9d313-115">Determining Playlist Synchronization State</span></span>

<span data-ttu-id="9d313-116">Windows Media Player 10 o posterior utiliza el atributo **SyncState** para contener información acerca de si un archivo multimedia digital determinado se ha copiado en un dispositivo portátil y, en caso de error, si se produjo un error en la copia porque el dispositivo no tiene suficiente memoria.</span><span class="sxs-lookup"><span data-stu-id="9d313-116">Windows Media Player 10 or later uses the **SyncState** attribute to contain information about whether a particular digital media file has been copied to a portable device and, in the case of a failure, whether copying failed because the device did not have enough memory.</span></span>

<span data-ttu-id="9d313-117">En el código de ejemplo siguiente se crea una función que recupera esta información de un archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="9d313-117">The following example code creates a function that retrieves this information from a digital media file.</span></span> <span data-ttu-id="9d313-118">La función toma los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="9d313-118">The function takes the following parameters:</span></span>

-   <span data-ttu-id="9d313-119">*pMedia*.</span><span class="sxs-lookup"><span data-stu-id="9d313-119">*pMedia*.</span></span> <span data-ttu-id="9d313-120">Puntero a una interfaz **IWMPMedia** que representa el archivo multimedia digital que se va a inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="9d313-120">Pointer to an **IWMPMedia** interface that represents the digital media file to inspect.</span></span>
-   <span data-ttu-id="9d313-121">*lPsIndex*.</span><span class="sxs-lookup"><span data-stu-id="9d313-121">*lPsIndex*.</span></span> <span data-ttu-id="9d313-122">Índice de asociación del dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="9d313-122">Partnership index of the current device.</span></span>
-   <span data-ttu-id="9d313-123">*pulOnDevice*.</span><span class="sxs-lookup"><span data-stu-id="9d313-123">*pulOnDevice*.</span></span> <span data-ttu-id="9d313-124">Puntero a una variable de **tipo Long** que recibe el valor que indica si el archivo multimedia digital se ha copiado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9d313-124">Pointer to a **long** variable that receives the value indicating whether the digital media file has been copied to the device.</span></span>
-   <span data-ttu-id="9d313-125">*pulDidNotFit*.</span><span class="sxs-lookup"><span data-stu-id="9d313-125">*pulDidNotFit*.</span></span> <span data-ttu-id="9d313-126">Puntero a una variable **Long** que recibe el valor que indica si se produjo un error en la operación de copia porque el dispositivo no tenía suficiente memoria.</span><span class="sxs-lookup"><span data-stu-id="9d313-126">Pointer to a **long** variable that receives the value indicating whether the copy operation failed because the device did not have enough memory.</span></span>

<span data-ttu-id="9d313-127">La información contenida en el atributo **SyncState** se codifica de manera bit a bit.</span><span class="sxs-lookup"><span data-stu-id="9d313-127">The information contained in the **SyncState** attribute is encoded in a bitwise fashion.</span></span> <span data-ttu-id="9d313-128">Puede ver cómo se usa esta función en el código de ejemplo en la [enumeración de los elementos multimedia](enumerating-the-media-items.md).</span><span class="sxs-lookup"><span data-stu-id="9d313-128">You can see how this function is used in the example code in [Enumerating the Media Items](enumerating-the-media-items.md).</span></span>


```C++
STDMETHODIMP CSyncSettings::GetPartnershipSyncState(IWMPMedia* pMedia, long lPsIndex, ULONG *pulOnDevice, ULONG *pulDidNotFit)
{
    ATLASSERT(pMedia); 
    ATLASSERT(lPsIndex > 0 && 
              lPsIndex < 17);
    ATLASSERT(pulOnDevice);
    ATLASSERT(pulDidNotFit);
  
    CComVariant varSyncStateVal;   
    CComPtr<IWMPMedia> spMedia(pMedia); 
    CComPtr<IWMPMedia3> spMedia3;     
    HRESULT hr = spMedia.QueryInterface(&spMedia3); 
    ULONG ulSyncState = 0; // Stores the ulVal member of varSyncStateVal. 
    ULONG lLSB = 0; // Represents least significant bit: Did the media fail to copy because it would not fit?
    ULONG lMSB = 0; // Represents most significant bit: Is the media on the device?

    // Calculate the bit shift required to isolate the partnership bit 
    // pair from the SyncState attribute.
    const int iRshift = (lPsIndex - 1) * 2;

    if(SUCCEEDED(hr) && spMedia3)
    {       
        hr = spMedia3->getItemInfoByType(CComBSTR("SyncState"), CComBSTR(""), 0, &varSyncStateVal);
    }

    if(SUCCEEDED(hr) && varSyncStateVal.vt == VT_UI4)
    {   
        // Get the value.
        ulSyncState = varSyncStateVal.ulVal;

        // Shift the bit pair to the rightmost position.
        ulSyncState >>= iRshift; 

        // Mask the rightmost bit pair.
        ulSyncState &= 3;

        // Get the LSB         
        lLSB = ulSyncState & ~2; // Sets the 2E1 bit to zero. 

        // Get the MSB
        ulSyncState >>= 1;
        lMSB = ulSyncState;       
    }

    // Return the bits.
    *pulOnDevice = lMSB;
    *pulDidNotFit = lLSB;

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="9d313-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9d313-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d313-130">**Interfaz IWMPMedia**</span><span class="sxs-lookup"><span data-stu-id="9d313-130">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="9d313-131">**IWMPMedia3::getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="9d313-131">**IWMPMedia3::getItemInfoByType**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype)
</dt> <dt>

[<span data-ttu-id="9d313-132">**Administrar listas de reproducción de sincronización**</span><span class="sxs-lookup"><span data-stu-id="9d313-132">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="9d313-133">**Atributo SyncState**</span><span class="sxs-lookup"><span data-stu-id="9d313-133">**SyncState Attribute**</span></span>](syncstate-attribute.md)
</dt> </dl>

 

 





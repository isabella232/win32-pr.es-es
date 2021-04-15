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
# <a name="determining-playlist-synchronization-state"></a>Determinar el estado de sincronización de la lista de reproducción

Windows Media Player 10 o posterior utiliza el atributo **SyncState** para contener información acerca de si un archivo multimedia digital determinado se ha copiado en un dispositivo portátil y, en caso de error, si se produjo un error en la copia porque el dispositivo no tiene suficiente memoria.

En el código de ejemplo siguiente se crea una función que recupera esta información de un archivo multimedia digital. La función toma los parámetros siguientes:

-   *pMedia*. Puntero a una interfaz **IWMPMedia** que representa el archivo multimedia digital que se va a inspeccionar.
-   *lPsIndex*. Índice de asociación del dispositivo actual.
-   *pulOnDevice*. Puntero a una variable de **tipo Long** que recibe el valor que indica si el archivo multimedia digital se ha copiado en el dispositivo.
-   *pulDidNotFit*. Puntero a una variable **Long** que recibe el valor que indica si se produjo un error en la operación de copia porque el dispositivo no tenía suficiente memoria.

La información contenida en el atributo **SyncState** se codifica de manera bit a bit. Puede ver cómo se usa esta función en el código de ejemplo en la [enumeración de los elementos multimedia](enumerating-the-media-items.md).


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPMedia3::getItemInfoByType**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype)
</dt> <dt>

[**Administrar listas de reproducción de sincronización**](managing-synchronization-playlists.md)
</dt> <dt>

[**Atributo SyncState**](syncstate-attribute.md)
</dt> </dl>

 

 





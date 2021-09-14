---
title: Determinar el estado de sincronización de la lista de reproducción
description: Determinar el estado de sincronización de la lista de reproducción
ms.assetid: 634b659b-c3ae-4957-b17e-18fd92e915be
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
- dispositivos portátiles, determinar el estado de la lista de reproducción de sincronización
- listas de reproducción de sincronización, estado de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9758cfbb73c698a40d6d4f48e645e57750d8a332
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068472"
---
# <a name="determining-playlist-synchronization-state"></a>Determinar el estado de sincronización de la lista de reproducción

Reproductor de Windows Media 10 o posterior usa el atributo **SyncState** para contener información sobre si un archivo multimedia digital determinado se ha copiado en un dispositivo portátil y, en caso de error, si no se pudo copiar porque el dispositivo no tenía suficiente memoria.

El código de ejemplo siguiente crea una función que recupera esta información de un archivo multimedia digital. La función toma los parámetros siguientes:

-   *pMedia*. Puntero a una **interfaz IWMPMedia** que representa el archivo multimedia digital que se inspeccionará.
-   *lPsIndex*. Índice de asociación del dispositivo actual.
-   *pulOnDevice*. Puntero **a** una variable larga que recibe el valor que indica si el archivo multimedia digital se ha copiado en el dispositivo.
-   *pulDidNotFit*. Puntero a una variable **larga** que recibe el valor que indica si la operación de copia no se pudo hacer porque el dispositivo no tenía suficiente memoria.

La información contenida en el **atributo SyncState** se codifica bit a bit. Puede ver cómo se usa esta función en el código de ejemplo de [Enumeración de los elementos multimedia](enumerating-the-media-items.md).


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

[**IWMPMedia (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPMedia3::getItemInfoByType**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype)
</dt> <dt>

[**Administración de listas de reproducción de sincronización**](managing-synchronization-playlists.md)
</dt> <dt>

[**Atributo SyncState**](syncstate-attribute.md)
</dt> </dl>

 

 





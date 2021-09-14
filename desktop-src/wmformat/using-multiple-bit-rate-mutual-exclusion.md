---
title: Uso de la exclusión mutua de velocidad de bits múltiple
description: Uso de la exclusión mutua de velocidad de bits múltiple
ms.assetid: 69898b4d-fe10-422e-9ed2-87b65aa7bdb3
keywords:
- velocidad de bits múltiple (MBR), exclusión mutua
- MBR (velocidad de bits múltiple), exclusión mutua
- exclusión mutua, velocidad de bits múltiple (MBR)
- profiles,multiple bit rate (MBR)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be77c7615845d10d07982676dfdb4dc8c617cebe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251439"
---
# <a name="using-multiple-bit-rate-mutual-exclusion"></a>Uso de la exclusión mutua de velocidad de bits múltiple

La exclusión mutua de velocidad de bits múltiple (MBR) es útil cuando se desea codificar contenido para diversos escenarios de reproducción. Una salida de vídeo de MBR consta de una sola entrada codificada varias veces, cada una con una configuración de velocidad de bits diferente. Cuando se lee un archivo con codificación MBR, el lector determinará qué secuencia usar en función del ancho de banda disponible.

El SDK Windows Media Format admite la codificación MBR para secuencias de vídeo y audio. Además, puede crear un tipo especial de codificación MBR denominada codificación MBR de tamaño múltiple de vídeo. El vídeo MBR de varios tamaños de vídeo funciona de forma idéntica al vídeo MBR normal, salvo que puede especificar diferentes tamaños de imagen para las secuencias de vídeo en la exclusión mutua.

En el ejemplo siguiente se muestra cómo configurar un perfil para vídeo de MBR con varios tamaños de vídeo. Crea un nuevo perfil con tres secuencias de vídeo de diferentes velocidades de bits y tamaños, e incluye en un objeto de exclusión mutua.


```C++
IWMProfileManager*  pProfileMgr = NULL;
IWMProfile*         pProfile    = NULL;
IWMMutualExclusion* pMutex      = NULL;
IWMStreamConfig*    pStream     = NULL;
IWMMediaProps*      pMediaProps = NULL;

WM_MEDIA_TYPE*      pMediaType  = NULL;
DWORD               cbMediaType = 0;

HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager object.
hr = WMCreateProfileManager(&pProfileMgr);

// Create an empty profile.
hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, &pProfile);

// Give the new profile a name and description.
hr = pProfile->SetName(L"MBR_Video_3_Stream_test");
hr = pProfile->SetDescription(L"Only for use with example code.");

// Create the first stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// Get the media properties interface for the new stream.
hr = pStream->QueryInterface(IID_IWMMediaProps, (void**)&pMediaProps);

// Get the media-type structure.
// First, get the size of the media-type structure.
hr = pMediaProps->GetMediaType(NULL, &cbMediaType);

// Allocate memory for the structure based on the retrieved size.
pMediaType = (WM_MEDIA_TYPE*) new BYTE[cbMediaType];

// Retrieve the media-type structure.
hr = pMediaProps->GetMediaType(pMediaType, &cbMediaType);

// Change the video size to 640 x 480.
pMediaType->pbFormat->bmiHeader.biWidth  = 640;
pMediaType->pbFormat->bmiHeader.biHeight = 480;

// Replace the WM_MEDIA_TYPE in the profile with the one just changed.
hr = pMediaProps->SetMediaType(pMediaType);

// Release the media properties interface and delete the structure.
pMediaProps->Release();
pMediaProps = NULL;
delete[] pMediaType;
pMediaType = NULL;

// Set the bit rate to 200.
hr = pStream->SetBitrate(200000);

// Set the stream number.
hr = pStream->SetStreamNumber(1);

// Include the new stream in the profile.
hr = pProfile->AddStream(pStream);

// Release the stream configuration interface.
pStream->Release();
pStream = NULL;

// For the remaining two streams, leave the video at its default size of
// 320 x 240 <entity type="ndash"/>- just change the bit rates.

// Repeat for a 100K stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);
hr = pStream->SetBitrate(100000);
hr = pStream->SetStreamNumber(2);
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Repeat for a 56K stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);
hr = pStream->SetBitrate(56000);
hr = pStream->SetStreamNumber(3);
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Now that we have three streams, create a mutual exclusion object.
hr = pProfile->CreateNewMutualExclusion(&pMutex);

// Add the three streams to the mutual exclusion.
hr = pMutex->AddStream(1);
hr = pMutex->AddStream(2);
hr = pMutex->AddStream(3);

// Configure the mutual exclusion for MBR video.
hr = pMutex->SetType(CLSID_WMMUTEX_Bitrate);

// Add the mutual exclusion to the profile.
hr = pProfile->AddMutualExclusion(pMutex);

// Release the mutual exclusion object.
pMutex->Release();
pMutex = NULL;

// TODO: Save the profile to a string, and save the string to a file.
// For more information, see To Save a Custom Profile.

// Release remaining interfaces.
pProfile->Release();
pProfile = NULL;

pProfileMgr->Release();
pProfileMgr = NULL;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMMediaProps (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**Interfaz IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**IWMProfile (interfaz)**](iwmprofile.md)
</dt> <dt>

[**Interfaz IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[**Uso de la exclusión mutua**](using-mutual-exclusion.md)
</dt> <dt>

[**TIPO \_ DE MEDIO \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)
</dt> </dl>

 

 





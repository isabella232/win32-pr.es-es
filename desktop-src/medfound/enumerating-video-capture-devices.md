---
description: En este tema se describe cómo enumerar los dispositivos de captura de vídeo en el sistema de usuarios y cómo crear una instancia de un dispositivo.
ms.assetid: b1267478-329b-4e46-a2ed-1ec11d2e2e6d
title: Enumeración de dispositivos de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476c4b41e6f8913414200c7a811ba9625f2c4bc9cfea66875ec5f15b788bdc05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061625"
---
# <a name="enumerating-video-capture-devices"></a>Enumeración de dispositivos de captura de vídeo

En este tema se describe cómo enumerar los dispositivos de captura de vídeo en el sistema del usuario y cómo crear una instancia de un dispositivo.

Para enumerar los dispositivos de captura de vídeo en el sistema, haga lo siguiente:

1.  Llame [**a MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un almacén de atributos. Esta función recibe un [**punteroATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
2.  Llame [**aATTRIBUTEAttributes::SetGUID para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) establecer el atributo [MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE \_ \_ TYPE.](mf-devsource-attribute-source-type.md) Establezca el valor del atributo en **MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE TYPE \_ \_ \_ VIDCAP \_ GUID**.
3.  Llame [**a MFEnumDeviceSources.**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) Esta función recibe una matriz de punteros [**DE DESACTIVATE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) y el tamaño de la matriz. Cada puntero representa un dispositivo de captura de vídeo distinto.

Para crear una instancia de un dispositivo de captura:

-   Llame [**a IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para obtener un puntero a la [**interfaz IMFMediaSource.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

El siguiente código muestra estos pasos:


```C++
HRESULT CreateVideoDeviceSource(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    IMFMediaSource *pSource = NULL;
    IMFAttributes *pAttributes = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to specify the enumeration parameters.
    HRESULT hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Source type: video capture devices
    hr = pAttributes->SetGUID(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate devices.
    UINT32 count;
    hr = MFEnumDeviceSources(pAttributes, &ppDevices, &count);
    if (FAILED(hr))
    {
        goto done;
    }

    if (count == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Create the media source object.
    hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(&pSource));
    if (FAILED(hr))
    {
        goto done;
    }

    *ppSource = pSource;
    (*ppSource)->AddRef();

done:
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
    SafeRelease(&pSource);
    return hr;
}
```



Después de crear el origen multimedia, suelte los punteros de interfaz y libere la memoria de la matriz:


```C++
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 




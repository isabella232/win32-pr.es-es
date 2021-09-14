---
title: Obtención de funcionalidades de formato a través de IWMDMDevice
description: Obtención de funcionalidades de formato en dispositivos que solo admiten IWMDMDevice
ms.assetid: bff079a1-d192-4e53-9b1d-9ad3b5dcca51
keywords:
- Windows Características Administrador de dispositivos multimedia, funcionalidades del dispositivo
- Administrador de dispositivos,funcionalidades del dispositivo
- guía de programación, funcionalidades del dispositivo
- aplicaciones de escritorio, funcionalidades de dispositivo
- creación de Windows aplicaciones Administrador de dispositivos multimedia, funcionalidades del dispositivo
- escribir archivos en dispositivos, funcionalidades del dispositivo
- Método IWMDMDevice
- Windows Método Administrador de dispositivos,IWMDMDevice
- Administrador de dispositivos,IWMDMDevice (método)
- guía de programación, método IWMDMDevice
- aplicaciones de escritorio, método IWMDMDevice
- crear Windows aplicaciones Administrador de dispositivos multimedia,método IWMDMDevice
- escribir archivos en dispositivos, método IWMDMDevice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a923919611b40197b1deed30e781042e008ef41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967864"
---
# <a name="getting-format-capabilities-through-iwmdmdevice"></a>Obtención de funcionalidades de formato a través de IWMDMDevice

El método recomendado para consultar las funcionalidades de reproducción de un dispositivo [**es IWMDMDevice3::GetFormatCapability.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) Sin embargo, si un dispositivo no admite este método, la aplicación en su lugar puede llamar a [**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) para recuperar una matriz de formatos de audio admitidos como estructuras [**\_ DEFORMATEX**](-waveformatex.md) y formatos MIME como cadenas del dispositivo.

Los pasos siguientes muestran cómo una aplicación puede usar este método para consultar formatos admitidos en un dispositivo:

1.  Llame **a GetFormatSupport** para recuperar matrices de formatos de audio y mime.
2.  Recorrer en bucle los formatos de audio recuperados y examinar cada [**\_ estructura DETENTEATEX**](-waveformatex.md) para intentar encontrar un formato de audio aceptable
3.  Recorrer en bucle las cadenas de formato MIME recuperadas (si lo desea) para buscar un tipo de archivo aceptable. El SDK no define constantes para formatos MIME; debe usar valores estándar del sector (que se pueden encontrar en el iana.org web). Un dispositivo debe enumerar los tipos MIME específicos que admite.

El siguiente código de C++ muestra cómo recuperar las funcionalidades de formato de un dispositivo mediante **GetFormatSupport.**


```C++
// Function to print out device caps for a device 
// that supports only IWMDMDevice.
void CWMDMController::GetCaps(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get all capabilities for audio and mime support.
    _WAVEFORMATEX* pAudioFormats;
    LPWSTR* pMimeFormats;
    UINT numAudioFormats = 0;
    UINT numMimeFormats = 0;
    hr = pDevice->GetFormatSupport(
        &pAudioFormats,
        &numAudioFormats,
        &pMimeFormats,
        &numMimeFormats);
    if (FAILED(hr)) return;

    // Print out audio format data.
    if (numAudioFormats > 0)
    {
        // TODO: Display a banner for the supported audio-format listing.
    }
    else
    {
        // TODO: Display a message indicating that no audio formats are supported.
    }
    for (int i = 0; i < numAudioFormats; i++)
    {
       // TODO: For each valid audio format, display the max channel, 
       // max samples/second, avg. bytes/sec, block alignment, and 
       // max bits/sample values.
    }

    // Print out MIME formats.
    if (numMimeFormats > 0)
        // TODO: Display a banner to precede the MIME format listing.
    else
        // TODO: Display a banner indicating that no MIME formats are supported.
    for (i = 0; i < numMimeFormats; i++)
    {
        // TODO: Display the specified MIME format.
    }
    return;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Detección de funcionalidades de formato de dispositivo**](discovering-device-format-capabilities.md)
</dt> <dt>

[**Obtención de funcionalidades de formato en dispositivos que admiten IWMDMDevice3**](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
</dt> </dl>

 

 





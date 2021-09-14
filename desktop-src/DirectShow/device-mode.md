---
description: Modo de dispositivo
ms.assetid: d56021be-616b-41cd-8cf0-9e0d314f62cd
title: Modo de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4657fbb49e2619d75911c18185109805116b9647
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061224"
---
# <a name="device-mode"></a>Modo de dispositivo

IEEE 1394 y cámaras usb pueden cambiar entre el modo de cámara y el modo de grabadora de cinta de vídeo (VTR). Cuando una cámara IEEE 1394 cambia de modo, el dispositivo se restablece y la aplicación debe enumerar de nuevo. No hay ninguna manera de que una aplicación cambie el modo mediante programación. Las cámaras de vídeo USB, por otro lado, pueden cambiar entre los modos de cámara y VTR sin restablecer y la aplicación puede cambiar el modo.

**Controlador MSDV**

Para obtener el modo actual en un dispositivo IEEE 1394, llame al método [**IAMExtDevice::GetCapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) con el valor ED \_ DEVCAP \_ DEVICE \_ TYPE. Si el método devuelve el valor ED DEVTYPE VCR, el dispositivo está en modo VTR y tiene funciones como pausar, detener, avanzar rápidamente y \_ \_ rebobinar. De lo contrario, si el método devuelve ED \_ DEVTYPE \_ CAMERA, el dispositivo está en modo de cámara. En el ejemplo de código siguiente se muestra cómo consultar el tipo de dispositivo:


```C++
if (MyDevCap.bHasDevice) 
{
    LONG lDeviceType = 0;
    MyDevCap.pDevice->GetCapability(ED_DEVCAP_DEVICE_TYPE, &lDeviceType, 0);

    if (lDeviceType == ED_DEVTYPE_VCR) 
    {
        // Device is a VTR. Enable all VTR functions.
    }
    else 
    {
        // Device is a camera. 
        // Enable record and record-pause; disable other functions.
    }
}
```



Si la cámara de vídeo se queda sin conexión, debe volver a consultarla cuando esté disponible a continuación. El administrador de gráficos de filtro publica un [**evento \_ EC DEVICE \_ LOST**](ec-device-lost.md) cuando se quita el dispositivo.

**Controlador UVC**

Dado que los dispositivos de vídeo USB pueden cambiar de modo sin restablecer, el código que se muestra en los ejemplos anteriores no es confiable para los dispositivos USB. En su lugar, use [**la interfaz ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) para obtener el modo actual. También puede usar esta interfaz para cambiar los modos mediante programación si el dispositivo lo admite.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de una videocamba de DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




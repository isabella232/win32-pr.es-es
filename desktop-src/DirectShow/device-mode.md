---
description: Modo de dispositivo
ms.assetid: d56021be-616b-41cd-8cf0-9e0d314f62cd
title: Modo de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4657fbb49e2619d75911c18185109805116b9647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495779"
---
# <a name="device-mode"></a>Modo de dispositivo

Las videocámaras IEEE 1394 y USB pueden cambiar entre el modo de cámara y el modo de grabadora de cintas de vídeo (VTR). Cuando una videocámara IEEE 1394 cambia de modo, el dispositivo se restablece y la aplicación debe volver a enumerarlo. No hay ninguna manera de que una aplicación cambie el modo mediante programación. Por otro lado, las videocámaras USB pueden cambiar entre los modos de cámara y VTR sin tener que restablecer y la aplicación puede cambiar el modo.

**Controlador MSDV**

Para obtener el modo actual en un dispositivo IEEE 1394, llame al método [**IAMExtDevice:: GetCapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) con el tipo de dispositivo de valor Ed \_ DEVCAP \_ \_ . Si el método devuelve el valor ED \_ DEVTYPE \_ VCR, el dispositivo está en modo VTR y tiene funciones como pausa, detener, avance rápido y rebobinado. De lo contrario, si el método devuelve ED \_ DEVTYPE \_ Camera, el dispositivo está en modo de cámara. En el ejemplo de código siguiente se muestra cómo consultar el tipo de dispositivo:


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



Si el camcorder se queda sin conexión, debe volver a consultarlo cuando esté disponible. El administrador de gráficos de filtros envía un evento de [**\_ dispositivo EC \_ perdido**](ec-device-lost.md) cuando se quita el dispositivo.

**Controlador UVC**

Dado que los dispositivos de vídeo USB pueden cambiar de modo sin restablecer, el código que se muestra en los ejemplos anteriores no es confiable para dispositivos USB. En su lugar, use la interfaz [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) para obtener el modo actual. También puede usar esta interfaz para cambiar los modos mediante programación si el dispositivo lo admite.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de una videocámara DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




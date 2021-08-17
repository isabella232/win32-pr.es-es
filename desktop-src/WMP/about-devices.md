---
title: Acerca de los dispositivos
description: Acerca de los dispositivos
ms.assetid: 9e68c5eb-5fcb-4d7d-8dbb-7e951f253df8
keywords:
- Reproductor de Windows Media,sincronizar dispositivos
- Reproductor de Windows Media de objetos, sincronizar dispositivos
- modelo de objetos, sincronizar dispositivos
- Reproductor de Windows Media ActiveX control, sincronización de dispositivos
- ActiveX control, sincronización de dispositivos
- Reproductor de Windows Media Control de ActiveX móviles, sincronización de dispositivos
- Reproductor de Windows Media Móvil, sincronización de dispositivos
- sincronizar dispositivos, acerca de
- sincronización de dispositivos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66383082bae772b48f913f6bd4615724de8f7b7735e387ba93407a9848f17074
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956925"
---
# <a name="about-devices"></a>Acerca de los dispositivos

Los dispositivos portátiles son dispositivos de hardware que los usuarios llevan para disfrutar del contenido multimedia digital cuando están fuera de su equipo. Normalmente, los dispositivos portátiles funcionan con batería. Algunos dispositivos solo pueden reproducir música. Otros dispositivos pueden reproducir vídeo y música.

Algunos dispositivos admiten la sincronización automática de contenido multimedia digital con Reproductor de Windows Media. Otros dispositivos solo admiten la transferencia manual. Puede determinar si un dispositivo determinado admite la sincronización automática llamando al estado [IWMPSyncDevice::get \_ ](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) y, a continuación, inspeccionando el [valor WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperado. Si el valor recuperado es **wmpdsManualDevice,** el dispositivo no admite la sincronización automática.

Puede enumerar los dispositivos conectados al equipo del usuario. Para ello, use primero [IWMPSyncServices::get \_ deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) para recuperar el recuento de dispositivos. A continuación, en un bucle, llame a [IWMPSyncServices::getDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice)y pase el valor de índice adecuado cada vez. Puede usar [IWMPSyncDevice::get \_ connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) para evaluar si un dispositivo determinado está conectado actualmente.

Para saber cuándo se conectan o se desconectan los dispositivos, puede recibir los eventos **DeviceConnect** **y DeviceDisconnect.** Estos eventos se reciben a través de **la interfaz IWMPEvents2.**

La **interfaz IWMPSyncDevice** proporciona métodos adicionales para permitirle obtener o establecer información sobre un dispositivo. Por ejemplo:

-   Los **\_ métodos get FriendlyName** y **\_ friendlyName** permiten recuperar y especificar el nombre del dispositivo definido por el usuario.
-   El **método \_ get deviceName** le permite recuperar el nombre del dispositivo que los usuarios ven en el shell Windows XP.
-   El **método getItemInfo** permite recuperar metadatos de dispositivos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de la sincronización de dispositivos**](about-device-synchronization.md)
</dt> <dt>

[**IWMPEvents2 (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**IWMPSyncDevice (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**Trabajar con dispositivos portátiles**](working-with-portable-devices.md)
</dt> </dl>

 

 





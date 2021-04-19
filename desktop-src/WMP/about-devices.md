---
title: Acerca de los dispositivos
description: Acerca de los dispositivos
ms.assetid: 9e68c5eb-5fcb-4d7d-8dbb-7e951f253df8
keywords:
- Windows Media Player, sincronizar dispositivos
- Modelo de objetos de Windows Media Player, sincronizar dispositivos
- modelo de objetos, sincronizar dispositivos
- Control ActiveX de Windows Media Player, sincronizar dispositivos
- Control ActiveX, sincronizar dispositivos
- Control ActiveX móvil de Windows Media Player, sincronizar dispositivos
- Windows Media Player Mobile, sincronizar dispositivos
- sincronizar dispositivos, acerca de
- sincronización de dispositivos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89a074e4edb5bdbc7d90391398d5e0e4133505a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695526"
---
# <a name="about-devices"></a>Acerca de los dispositivos

Los dispositivos portátiles son dispositivos de hardware que los usuarios llevan para disfrutar del contenido multimedia digital cuando están fuera de su equipo. Normalmente, los dispositivos portátiles funcionan con baterías. Algunos dispositivos solo pueden reproducir música. Otros dispositivos pueden reproducir vídeo y música.

Algunos dispositivos admiten la sincronización automática de contenido multimedia digital con Windows Media Player. Otros dispositivos solo admiten la transferencia manual. Para determinar si un dispositivo determinado admite la sincronización automática, llame a [IWMPSyncDevice:: get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) y, a continuación, inspeccione el valor de [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperado. Si el valor recuperado es **wmpdsManualDevice**, el dispositivo no admite la sincronización automática.

Puede enumerar los dispositivos conectados al equipo del usuario. Para ello, use primero [IWMPSyncServices:: get \_ deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) para recuperar el recuento de dispositivos. A continuación, en un bucle, llame a [IWMPSyncServices:: getDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), pasando el valor de índice adecuado cada vez. Puede usar [IWMPSyncDevice:: get \_ Connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) para evaluar si un dispositivo determinado está conectado actualmente.

Para saber cuándo se conectan o desconectan los dispositivos, puede recibir los eventos **DeviceConnect** y **DeviceDisconnect** . Estos eventos se reciben a través de la interfaz **IWMPEvents2** .

La interfaz **IWMPSyncDevice** proporciona métodos adicionales que permiten obtener o establecer información sobre un dispositivo. Por ejemplo:

-   Los métodos **Get \_ FriendlyName** y **Put \_ FriendlyName** permiten recuperar y especificar el nombre del dispositivo definido por el usuario.
-   El método **Get \_ deviceName** permite recuperar el nombre del dispositivo que los usuarios ven en el shell de Windows XP.
-   El método **getItemInfo** permite recuperar metadatos de los dispositivos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de la sincronización de dispositivos**](about-device-synchronization.md)
</dt> <dt>

[**Interfaz IWMPEvents2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Interfaz IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**Trabajar con dispositivos portátiles**](working-with-portable-devices.md)
</dt> </dl>

 

 





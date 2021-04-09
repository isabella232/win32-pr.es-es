---
title: Proveedores de dispositivos
description: Los proveedores de dispositivos son objetos registrados que el equipo inicia en cada inicio del sistema.
ms.assetid: 80c08993-0a8b-4ee9-93cd-bcc3c00e843b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67fac270342830045fc3bac9f0573f283d87dc6a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149329"
---
# <a name="device-providers"></a>Proveedores de dispositivos

Los proveedores de dispositivos son objetos registrados que el equipo inicia en cada inicio del sistema. Los proveedores de dispositivos registran y anulan el registro de dispositivos en ejecución con el host del dispositivo en respuesta a algún evento. Estos dispositivos son dispositivos que se han iniciado automáticamente durante el tiempo de inicio del sistema. Por motivos de seguridad, un proveedor de dispositivos debe ejecutarse generalmente como [LocalService](/windows/desktop/Services/localservice-account), en lugar de [LocalSystem](/windows/desktop/Services/localsystem-account).

Los proveedores de dispositivos se pueden usar para dispositivos transitorios. Los proveedores de dispositivos también se pueden usar para enlazar dispositivos a medios sondeados. Por ejemplo, un dispositivo periférico, como un reproductor de música digital, se conecta a un equipo a través de un puerto serie. Para exponer el reproductor de música como un dispositivo basado en UPnP, se necesitan un objeto de control de dispositivo y un conjunto de objetos de servicio. Estos objetos implementan las acciones de reproducción de música basadas en UPnP como comandos en serie. Sin embargo, el reproductor de música debe estar conectado al puerto serie y estar disponible para el control antes de que se registren estos objetos.

Dado que el puerto serie no ofrece un mecanismo de notificación explícito cuando los dispositivos están conectados, se requiere un código de sondeo. Este código se puede implementar en un objeto de proveedor de dispositivos, en un servicio o en una aplicación independiente. Cuando se inicia el equipo, el host del dispositivo crea una instancia del objeto de proveedor de dispositivos y, a continuación, invoca su método de [**Inicio**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) . Cuando el proveedor de dispositivos detecta la presencia de un dispositivo de reproducción de música, crea una instancia del objeto de control de dispositivo adecuado y lo registra mediante una llamada a [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice). Este método publica el dispositivo y lo anuncia en la red basada en UPnP.

También se puede lograr la misma funcionalidad implementando un servicio que sondea el puerto serie. Sin embargo, los proveedores de dispositivos simplifican las cosas al requerir solo la funcionalidad básica (el sondeo) que se va a implementar, ya que los proveedores de dispositivos se basan en el host del dispositivo para iniciarlos y detenerlos. El uso de proveedores de dispositivos es más sencillo que implementar un servicio.

En el momento del registro, y en cada siguiente inicio del sistema, el equipo crea una instancia del objeto de proveedor de dispositivos y, a continuación, invoca su método [**IUPnPDeviceProvider:: Start**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) , pasándole la cadena de inicialización especificada durante el registro.

Una vez que se llama al método [**Start**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) , el proveedor del dispositivo realiza cualquier procesamiento necesario y, cuando sea necesario, el proveedor del dispositivo registra los dispositivos mediante una llamada a [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), como se describe en la sección [registro de un dispositivo hospedado con el host del dispositivo](registering-a-hosted-device-with-the-device-host.md).

Cuando el equipo se apaga, el host del dispositivo invoca el método [**IUPnPDeviceProvider:: Stop**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-stop) para indicar que el proveedor de dispositivos termina sus operaciones.

 

 
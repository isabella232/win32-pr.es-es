---
title: Proveedores de dispositivos
description: Los proveedores de dispositivos son objetos registrados que el equipo inicia en cada inicio del sistema.
ms.assetid: 80c08993-0a8b-4ee9-93cd-bcc3c00e843b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfb81f5fceacff490be47609973b897a5b9bd199122b24db39d12ada8ec7355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867685"
---
# <a name="device-providers"></a>Proveedores de dispositivos

Los proveedores de dispositivos son objetos registrados que el equipo inicia en cada inicio del sistema. Los proveedores de dispositivos registran y anulan el registro de los dispositivos en ejecución con el host del dispositivo en respuesta a algún evento. Estos dispositivos son dispositivos que se han iniciado automáticamente en el momento del inicio del sistema. Por motivos de seguridad, un proveedor de dispositivos normalmente debe ejecutarse como [LocalService](/windows/desktop/Services/localservice-account), en lugar de [LocalSystem](/windows/desktop/Services/localsystem-account).

Los proveedores de dispositivos se pueden usar para dispositivos transitorios. Los proveedores de dispositivos también se pueden usar para establecer un puente entre los dispositivos y los medios sondeados. Por ejemplo, un dispositivo periférico, como un reproductor de música digital, está conectado a un equipo a través de un puerto serie. Para exponer el reproductor de música como un dispositivo basado en UPnP, se requiere un objeto de control de dispositivo y un conjunto de objetos de servicio. Estos objetos implementan las acciones del reproductor de música basado en UPnP como comandos serie. Sin embargo, el reproductor de música debe estar conectado al puerto serie y estar disponible para su control antes de registrar estos objetos.

Dado que el puerto serie no ofrece un mecanismo de notificación explícito cuando los dispositivos están conectados, se requiere código de sondeo. Este código se puede implementar en un objeto de proveedor de dispositivos, un servicio o en una aplicación independiente. Cuando se inicia el equipo, el host de dispositivo crea una instancia del objeto de proveedor de dispositivos y, a continuación, invoca su [**método Start.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) Cuando el proveedor de dispositivos detecta la presencia de un dispositivo de reproductor de música, crea una instancia del objeto de control de dispositivo adecuado y lo registra mediante una llamada a [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice). Este método publica el dispositivo y lo anuncia en la red basada en UPnP.

También se puede lograr la misma funcionalidad implementando un servicio que sondee el puerto serie. Sin embargo, los proveedores de dispositivos simplifican las cosas al requerir que solo se implemente la funcionalidad principal (el sondeo), ya que los proveedores de dispositivos dependen del host del dispositivo para iniciarlos y detenerlos. El uso de proveedores de dispositivos es más sencillo que implementar un servicio.

En el momento del registro y en cada inicio posterior del sistema, el equipo crea una instancia del objeto de proveedor de dispositivos y, a continuación, invoca su método [**IUPnPDeviceProvider::Start,**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) pasando la cadena de inicialización especificada durante el registro.

Una vez que se llama al método [**Start,**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) el proveedor de dispositivos realiza el procesamiento necesario y, cuando es necesario, el proveedor de dispositivos registra los dispositivos mediante una llamada a [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), como se describe en la sección Registro de un dispositivo hospedado con el [host de dispositivo.](registering-a-hosted-device-with-the-device-host.md)

Cuando se apaga el equipo, el host de dispositivo invoca el método [**IUPnPDeviceProvider::Stop**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-stop) para indicar que el proveedor de dispositivos finaliza sus operaciones.

 

 
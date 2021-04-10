---
title: Registro de un dispositivo hospedado con el host del dispositivo
description: Registrar un dispositivo hospedado significa proporcionar al host del dispositivo la descripción del dispositivo y su objeto de control de dispositivo.
ms.assetid: 1d85b412-9b1b-415d-8664-8d96a6644793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a607af4f6ada359a9ee32e98e416d8271fd502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268697"
---
# <a name="registering-a-hosted-device-with-the-device-host"></a>Registro de un dispositivo hospedado con el host del dispositivo

Registrar un dispositivo hospedado significa proporcionar al host del dispositivo la descripción del dispositivo y su objeto de control de dispositivo. A continuación, el host del dispositivo crea una descripción completa del dispositivo UPnP, lo publica y anuncia el dispositivo en la red mediante el protocolo de detección UPnP. Una vez que se publica un dispositivo, está disponible para los puntos de control.

Los dispositivos se registran de dos maneras:

-   Una aplicación crea una instancia del objeto de control de dispositivo y le pasa un puntero al host del dispositivo.
-   La aplicación pasa el identificador de programa (ProgID) de un objeto de control de dispositivo registrado al host del dispositivo. El host del dispositivo crea una instancia de ella cuando el host del dispositivo recibe la primera solicitud para el dispositivo.

Independientemente del método que se use, el host del dispositivo publica y anuncia el dispositivo en cuanto se registra. La diferencia entre los dos enfoques tiene que hacer con cuando se carga el código del dispositivo. Cuando la aplicación pasa un puntero al objeto de control de dispositivo, el código del dispositivo se carga y se ejecuta en el momento del registro. Cuando la aplicación pasa un ProgID, el código del dispositivo solo se carga cuando se invoca una acción, se consulta una propiedad o llega una solicitud de suscripción de eventos. El segundo enfoque es ligeramente más eficaz. Sin embargo, no es adecuado para dispositivos que deben estar en ejecución antes de que llegue cualquier solicitud de suscripción de control o evento, ya que el uso de este enfoque solo se crea cuando se necesitan. Este segundo método también puede crear problemas de rendimiento cuando recibe la primera solicitud para un tipo de dispositivo.

Si desea asegurarse de que el host del dispositivo anuncia automáticamente un dispositivo en la red cuando se inicia el equipo, invoque [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice). **RegisterDevice** garantiza que el código del dispositivo solo se carga cuando se recibe una solicitud de suscripción de control o evento.

Si los dispositivos son transitorios o con puentes, invoque [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)y el dispositivo no se volverá a anunciar automáticamente cuando se reinicie el equipo.

## <a name="discovery-announcement-lifetime"></a>Duración del anuncio de detección

Cada dispositivo registrado con el host del dispositivo está asociado a una duración, que se especifica en el dispositivo tras el registro. La duración del dispositivo es el período de tiempo durante el que son válidos los anuncios de detección del dispositivo. La duración se pasa al punto de control como un encabezado en el anuncio de detección inicial. El host del dispositivo actualiza automáticamente el anuncio antes de la fecha de expiración. Los valores de la duración del anuncio de detección deben ser de 15 minutos o más (el valor predeterminado es 30 minutos).

## <a name="device-identifiers-created-at-registration"></a>Identificadores de dispositivo creados en el registro

Al crear una plantilla de descripción de dispositivo, el desarrollador de dispositivos debe proporcionar la ruta de acceso del recurso a la descripción del servicio y los iconos asociados. La ruta de acceso del recurso viene determinada por la aplicación del dispositivo.

Puesto que el mismo dispositivo se puede registrar varias veces en el mismo equipo, el UDN especificado en la plantilla de Descripción del dispositivo no es suficiente para identificar un dispositivo de forma única. Por lo tanto, cuando se registra un dispositivo, el host del dispositivo crea un identificador de dispositivo. Este identificador de dispositivo, en asociación con UDN en la plantilla de Descripción del dispositivo, se puede usar para identificar un dispositivo de forma única.

Este identificador también se usa cuando el dispositivo no está registrado temporalmente y luego se vuelve a registrar. Cuando se anula el registro de un dispositivo temporalmente, el host del dispositivo no elimina el UDN. Entre las razones para no eliminar la UDN se incluyen:

-   El dispositivo se está actualizando.
-   Está cambiando las propiedades del dispositivo.
-   Un servicio no está disponible temporalmente.
-   Está agregando un nuevo servicio a un dispositivo.
-   Está actualizando el archivo DLL.
-   El dispositivo está en modo de suspensión.

Consulte las secciones siguientes para obtener más información sobre el registro:

-   [Cómo registrar un dispositivo con el host del dispositivo](how-to-register-a-device-with-the-device-host.md)
-   [Anulación del registro de un dispositivo](unregistering-a-device.md)
-   [**IUPnPRegistrar::UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice)
-   [**IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)

 

 





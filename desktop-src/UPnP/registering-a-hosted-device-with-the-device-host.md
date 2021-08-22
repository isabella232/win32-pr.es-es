---
title: Registro de un dispositivo hospedado con el host del dispositivo
description: Registrar un dispositivo hospedado significa proporcionar al host del dispositivo la descripción del dispositivo y su objeto de control de dispositivo.
ms.assetid: 1d85b412-9b1b-415d-8664-8d96a6644793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486d01364b684e2aa6792b8a6c0b91ccc87a26670057c67192fe587ac049c388
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999565"
---
# <a name="registering-a-hosted-device-with-the-device-host"></a>Registro de un dispositivo hospedado con el host del dispositivo

Registrar un dispositivo hospedado significa proporcionar al host del dispositivo la descripción del dispositivo y su objeto de control de dispositivo. A continuación, el host de dispositivo crea una descripción completa del dispositivo UPnP, la publica y anuncia el dispositivo en la red mediante el protocolo de detección de UPnP. Una vez que se publica un dispositivo, está disponible para los puntos de control.

Los dispositivos se registran de dos maneras:

-   Una aplicación crea una instancia del objeto de control de dispositivo y le pasa un puntero al host del dispositivo.
-   La aplicación pasa el ProgID de un objeto de control de dispositivo registrado al host del dispositivo. El host de dispositivo crea una instancia cuando el host del dispositivo recibe la primera solicitud del dispositivo.

Independientemente del método que se utilice, el host del dispositivo publica y anuncia el dispositivo en cuanto se registra. La diferencia entre los dos enfoques tiene que ver con cuando se carga el código del dispositivo. Cuando la aplicación pasa un puntero al objeto de control de dispositivo, el código del dispositivo se carga y se ejecuta en el momento del registro. Cuando la aplicación pasa un ProgID, el código del dispositivo solo se carga cuando se invoca una acción, se consulta una propiedad o llega una solicitud de suscripción de eventos. El segundo enfoque es ligeramente más eficaz. Sin embargo, no es adecuado para los dispositivos que deben ejecutarse antes de que lleguen las solicitudes de suscripción de eventos o control, ya que con este enfoque, los objetos de control de dispositivos solo se crean cuando son necesarios. Este segundo método también puede crear problemas de rendimiento cuando recibe la primera solicitud de un tipo de dispositivo.

Si desea asegurarse de que el host del dispositivo anuncia un dispositivo en la red automáticamente cuando se inicia el equipo, invoque [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice). **RegisterDevice** garantiza que el código del dispositivo solo se carga cuando se recibe una solicitud de suscripción de control o evento.

Si los dispositivos son transitorios o puentes, invoque [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)y el dispositivo no se anuncia automáticamente cuando se reinicia el equipo.

## <a name="discovery-announcement-lifetime"></a>Duración del anuncio de detección

Cada dispositivo registrado con el host de dispositivo está asociado a una duración, que especifica el dispositivo tras el registro. La duración del dispositivo es el período de tiempo durante el que los anuncios de detección del dispositivo son válidos. La duración se pasa al punto de control como un encabezado en el anuncio de detección inicial. El host del dispositivo actualiza automáticamente el anuncio antes de la hora de expiración. Los valores de duración del anuncio de detección deben ser de 15 minutos o más (el valor predeterminado es 30 minutos).

## <a name="device-identifiers-created-at-registration"></a>Identificadores de dispositivo creados en el registro

Al crear una plantilla de descripción de dispositivo, el desarrollador del dispositivo debe proporcionar la ruta de acceso del recurso a la descripción del servicio y los iconos asociados. La ruta de acceso del recurso viene determinada por la aplicación del dispositivo.

Puesto que el mismo dispositivo se puede registrar varias veces en el mismo equipo, el UDN especificado en la plantilla de descripción del dispositivo no es suficiente para identificar de forma única un dispositivo. Por lo tanto, cuando se registra un dispositivo, el host del dispositivo crea un identificador de dispositivo. Este identificador de dispositivo, en asociación con el UDN de la plantilla de descripción del dispositivo, se puede usar para identificar de forma única un dispositivo.

Este identificador también se usa cuando el dispositivo se anula temporalmente del registro y, a continuación, se vuelve a registrar. Cuando un dispositivo se anula temporalmente del registro, el host de dispositivo no elimina el UDN. Entre los motivos para no eliminar el UDN se incluyen:

-   El dispositivo se está actualizando.
-   Va a cambiar las propiedades del dispositivo.
-   Un servicio no está disponible temporalmente.
-   Va a agregar un nuevo servicio a un dispositivo.
-   Está actualizando el archivo DLL.
-   El dispositivo está en modo de espera.

Consulte las secciones siguientes para obtener más información sobre el registro:

-   [Cómo registrar un dispositivo con el host de dispositivo](how-to-register-a-device-with-the-device-host.md)
-   [Anulación del registro de un dispositivo](unregistering-a-device.md)
-   [**IUPnPRegistrar::UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice)
-   [**IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)

 

 





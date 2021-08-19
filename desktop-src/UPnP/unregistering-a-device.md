---
title: Anulación del registro de un dispositivo
description: Use el método IUPnPRegistrar UnregisterDevice para anular el registro de un dispositivo.
ms.assetid: 4f7624e3-4d60-406d-8521-1dfc9aee4408
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ff8eeb99ec0ba697c301e8cc15100bd06c0323b95f4099329c46729ceba9c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999495"
---
# <a name="unregistering-a-device"></a>Anulación del registro de un dispositivo

Use el [**método IUPnPRegistrar::UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice) para anular el registro de un dispositivo. El dispositivo se puede anular del registro (quitarse del host del dispositivo) de forma temporal o permanente, según el valor *de fPermanent*. Los desarrolladores deben quitar los dispositivos temporalmente si se volverán a registrar los dispositivos y los dispositivos deben usar la misma UDN. De lo contrario, los dispositivos se quitan permanentemente.

El GUID que se usa para anular el registro no es el UDN. Debe usar el identificador devuelto por [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) o [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).

> [!Note]  
> Puede liberar el [**objeto IUPnPRegistrar.**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) Solo se debe almacenar en caché el identificador.

 

Si *fPermanent* es **FALSE,** el dispositivo se quita temporalmente. Use [**la interfaz IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar) para volver a registrar el dispositivo. Los métodos [**IUPnPReregistrar::ReregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterdevice) e [**IUPnPReregistrar::ReregisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterrunningdevice) usan los mismos UDN o UDN, en el caso de dispositivos anidados, generados previamente por el host de dispositivo para el dispositivo no registrado.

Si *fPermanent* es **TRUE,** el dispositivo se quita permanentemente del host del dispositivo. Al volver a registrar este dispositivo en el mismo equipo, se crea una UDN diferente a la creada anteriormente.

> [!Note]  
> Cuando un dispositivo se registra varias veces en el mismo equipo, el host del dispositivo genera diferentes UDN para cada instancia del dispositivo.

 

 

 





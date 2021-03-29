---
title: Anulación del registro de un dispositivo
description: Use el método IUPnPRegistrar UnregisterDevice para anular el registro de un dispositivo.
ms.assetid: 4f7624e3-4d60-406d-8521-1dfc9aee4408
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c480433e3d8dbf4ff823728281018801ec35c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486995"
---
# <a name="unregistering-a-device"></a>Anulación del registro de un dispositivo

Use el método [**IUPnPRegistrar:: UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice) para anular el registro de un dispositivo. Se puede anular el registro del dispositivo (quitado del host del dispositivo) de forma temporal o permanente, en función del valor de *fPermanent*. Los desarrolladores deben quitar temporalmente los dispositivos si los dispositivos se van a volver a registrar y los dispositivos deben usar el mismo UDN. De lo contrario, los dispositivos se quitan de forma permanente.

El GUID que se usa para anular el registro no es UDN. Debe usar el identificador devuelto por [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) o [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).

> [!Note]  
> Puede liberar el objeto [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) . Solo el identificador debe almacenarse en caché.

 

Si *fPermanent* es **false**, el dispositivo se quita temporalmente. Use la interfaz [**IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar) para volver a registrar el dispositivo. Los métodos [**IUPnPReregistrar:: ReregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterdevice) y [**IUPnPReregistrar:: ReregisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterrunningdevice) usan el mismo UDN o UDNs, en el caso de los dispositivos anidados, generados anteriormente por el host del dispositivo para el dispositivo no registrado.

Si *fPermanent* es **true**, el dispositivo se quita de forma permanente del host del dispositivo. Al registrar este dispositivo de nuevo en el mismo equipo, se crea un UDN diferente del que se creó anteriormente.

> [!Note]  
> Cuando un dispositivo se registra varias veces en el mismo equipo, el host del dispositivo genera UDNs diferentes para cada instancia del dispositivo.

 

 

 





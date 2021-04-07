---
title: Control de dispositivos
description: Los dispositivos basados en UPnP se controlan mediante los servicios que exponen.
ms.assetid: 4edca439-f767-41e6-97bb-ead751930714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a72a4ffdf91bca358124dbb0a0d95ff9a61e30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903726"
---
# <a name="controlling-devices"></a>Control de dispositivos

Los dispositivos basados en UPnP se controlan mediante los servicios que exponen. Un servicio UPnP es la entidad más pequeña que se controla en la arquitectura UPnP. Los dispositivos exponen un servicio por cada función principal que realizan. Los dispositivos complejos normalmente se componen de varios servicios simples y otros dispositivos.

Un servicio se compone de un conjunto de variables de estado y un conjunto de acciones que una aplicación puede invocar que operan en esas variables de estado. En la API de punto de control con tecnología UPnP, los servicios se representan mediante objetos de **servicio** que exponen la interfaz [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) .

Un tipo de servicio define las variables de estado y las acciones admitidas por un servicio determinado. Por ejemplo, el tipo de servicio para un servicio de reloj define las acciones **getTime** y **setTime** , junto con una variable de estado de **tiempo** .

Un identificador de servicio distingue varios tipos de servicio comunes dentro de un único dispositivo. Por ejemplo, puede haber dos servicios de reloj en un reloj de alarma, uno para el reloj normal y el otro para la alarma. Debe haber una manera de diferenciar entre los dos servicios, que tienen tipos de servicio idénticos. El identificador de servicio proporciona una manera única de identificar una instancia de un tipo de servicio. Después, este identificador de servicio se usa para tener acceso al servicio correcto desde la colección [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) , porque el tipo de servicio no es un identificador único. La interfaz [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) también permite que las aplicaciones registren una función de devolución de llamada con el objeto de servicio. Cuando el valor de la variable de estado de un servicio cambia, el objeto de servicio invoca la devolución de llamada registrada para notificar el cambio a la aplicación. El marco UPnP también invoca esta devolución de llamada para notificar a las aplicaciones cuando una instancia de servicio ha dejado de estar disponible. El servicio puede dejar de estar disponible por diversos motivos, incluidos los errores de red transitorios.

Para obtener más información, vea los temas siguientes:

-   [Obtener objetos de servicio](obtaining-service-objects.md)
-   [Registrar una devolución de llamada](registering-a-callback.md)
-   [Consultar variables de estado](querying-state-variables.md)
-   [Invocar acciones](invoking-actions.md)

 

 





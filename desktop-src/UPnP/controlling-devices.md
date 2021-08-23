---
title: Controlar dispositivos
description: Los dispositivos basados en UPnP se controlan mediante los servicios que exponen.
ms.assetid: 4edca439-f767-41e6-97bb-ead751930714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410818552f1f6563b28fcb963fcfca5c9b3067973e325adfd66ede5bffaedb75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999635"
---
# <a name="controlling-devices"></a>Controlar dispositivos

Los dispositivos basados en UPnP se controlan mediante los servicios que exponen. Un servicio UPnP es la entidad controlable más pequeña de la arquitectura UPnP. Los dispositivos exponen un servicio para cada función principal que realizan. Los dispositivos complejos normalmente se componen de varios servicios simples y otros dispositivos.

Un servicio consta de un conjunto de variables de estado y un conjunto de acciones que una aplicación puede invocar y que funcionan en esas variables de estado. En la API de punto de control con tecnología UPnP, los servicios se representan mediante objetos **de** servicio que exponen la [**interfaz IUPnPService.**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)

Un tipo de servicio define las variables de estado y las acciones admitidas por un servicio determinado. Por ejemplo, el tipo de servicio para un servicio de reloj define las acciones **GetTime** y **SetTime,** junto con una variable **de estado Time.**

Un identificador de servicio diferencia varios tipos de servicio comunes dentro de un único dispositivo. Por ejemplo, puede haber dos servicios de reloj en un reloj de alarma, uno para el reloj normal y el otro para la alarma. Debe haber una manera de diferenciar entre los dos servicios, que tienen tipos de servicio idénticos. El identificador de servicio proporciona una manera única de identificar una instancia de un tipo de servicio. A continuación, este identificador de servicio se usa para acceder al servicio correcto desde la colección [**IUPnPServices,**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) ya que el tipo de servicio no es un identificador único. La [**interfaz IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) también permite a las aplicaciones registrar una función de devolución de llamada con el objeto de servicio. Cuando cambia el valor de la variable de estado de un servicio, el objeto de servicio invoca la devolución de llamada registrada para notificar el cambio a la aplicación. El marco UPnP también invoca esta devolución de llamada para notificar a las aplicaciones cuando una instancia de servicio ha quedado no disponible. El servicio puede quedar no disponible por diversos motivos, incluidos los errores transitorios de red.

Para obtener más información, vea los temas siguientes:

-   [Obtener objetos de servicio](obtaining-service-objects.md)
-   [Registro de una devolución de llamada](registering-a-callback.md)
-   [Consulta de variables de estado](querying-state-variables.md)
-   [Invocación de acciones](invoking-actions.md)

 

 





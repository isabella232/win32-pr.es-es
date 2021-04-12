---
title: Referencia de API de punto de control
description: Las siguientes interfaces forman parte de la API de punto de control con tecnología UPnP. La API de punto de control admite Microsoft Visual Basic Scripting Edition (VBScript), Microsoft Visual Basic y C++.
ms.assetid: 6f73bf8c-0423-430f-a654-58d076712aae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691a0d764f612d957ac11b3b052859f081bc7285
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356931"
---
# <a name="control-point-api-reference"></a>Referencia de API de punto de control

Las siguientes interfaces forman parte de la API de punto de control con tecnología UPnP. La API de punto de control admite Microsoft Visual Basic Scripting Edition (VBScript), Microsoft Visual Basic y C++.



| Interfaz                                                                                      | Descripción                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPAddressFamilyControl**](/windows/desktop/api/Upnp/nn-upnp-iupnpaddressfamilycontrol)                                 | Permite a una aplicación tener acceso a la marca de la familia de direcciones del objeto de buscador de dispositivos.                                                                                                                                          |
| [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)                                   | Permite a una aplicación cargar una descripción del dispositivo. Esta interfaz es segura para el scripting.                                                                                                                                     |
| [**IUPnPDescriptionDocumentCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocumentcallback)                   | Permite a una aplicación recibir los resultados de una operación de carga asincrónica.                                                                                                                                               |
| [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice)                                                             | Permite que una aplicación recupere información acerca de un dispositivo específico.                                                                                                                                                        |
| [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess)                                 | Permite a una aplicación obtener la dirección URL de un documento de Descripción del dispositivo.                                                                                                                                                     |
| [**IUPnPDeviceDocumentAccessEx**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccessex)                             | Proporciona un método para obtener el documento de Descripción del dispositivo XML completo para un dispositivo específico.                                                                                                                                  |
| [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)                                                 | Permite a una aplicación buscar un dispositivo.                                                                                                                                                                                       |
| [**IUPnPDeviceFinderAddCallbackWithInterface**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface) | Permite a una aplicación recibir los resultados de búsqueda asincrónicos del entorno UPnP junto con el GUID del adaptador de red a través del cual procede el anuncio del dispositivo.                                                  |
| [**IUPnPDeviceFinderCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefindercallback)                                 | Permite a una aplicación recibir los resultados de búsqueda asincrónicos del entorno UPnP.                                                                                                                                         |
| [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)                                                           | Enumera una colección de dispositivos.                                                                                                                                                                                            |
| [**IUPnPHttpHeaderControl**](/windows/desktop/api/Upnp/nn-upnp-iupnphttpheadercontrol)                                       | Permite a una aplicación establecer los encabezados HTTP "agente de usuario" de las instancias de clase que implementan las interfaces [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) o [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) . |
| [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)                                                           | Permite que una aplicación recupere información de estado e invoque acciones para un servicio.                                                                                                                                         |
| [**IUPnPServiceAsync**](/windows/desktop/api/Upnp/nn-upnp-iupnpserviceasync)                                                 | Las variables de estado de consulta de forma asincrónica e invocan acciones en una instancia de un servicio.                                                                                                                                           |
| [**IUPnPServiceCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpservicecallback)                                           | Permite a una aplicación recibir una notificación del entorno UPnP cuando se producen eventos.                                                                                                                                      |
| [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices)                                                         | Enumera una colección de servicios.                                                                                                                                                                                           |



 

 

 





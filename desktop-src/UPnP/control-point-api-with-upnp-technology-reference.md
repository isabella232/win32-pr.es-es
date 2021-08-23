---
title: Referencia de la API de punto de control
description: Las interfaces siguientes forman parte de la API de punto de control con tecnología UPnP. La API de punto de control admite Microsoft Visual Basic Scripting Edition (VBScript), Microsoft Visual Basic y C++.
ms.assetid: 6f73bf8c-0423-430f-a654-58d076712aae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b3dab16874ebeb7b43ef1e8cf28def13d3ef1d7169a5aae4836b39da66636b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058123"
---
# <a name="control-point-api-reference"></a>Referencia de la API de punto de control

Las interfaces siguientes forman parte de la API de punto de control con tecnología UPnP. La API de punto de control admite Microsoft Visual Basic Scripting Edition (VBScript), Microsoft Visual Basic y C++.



| Interfaz                                                                                      | Descripción                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPAddressFamilyControl**](/windows/desktop/api/Upnp/nn-upnp-iupnpaddressfamilycontrol)                                 | Permite que una aplicación acceda a la marca de familia de direcciones del objeto Device Finder.                                                                                                                                          |
| [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)                                   | Permite que una aplicación cargue una descripción del dispositivo. Esta interfaz es segura para el scripting.                                                                                                                                     |
| [**IUPnPDescriptionDocumentCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocumentcallback)                   | Permite que una aplicación reciba los resultados de una operación de carga asincrónica.                                                                                                                                               |
| [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice)                                                             | Permite que una aplicación recupere información sobre un dispositivo específico.                                                                                                                                                        |
| [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess)                                 | Permite que una aplicación obtenga la dirección URL de un documento de descripción del dispositivo.                                                                                                                                                     |
| [**IUPnPDeviceDocumentAccessEx**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccessex)                             | Proporciona un método para obtener todo el documento de descripción del dispositivo XML para un dispositivo específico.                                                                                                                                  |
| [**IUPnPDeviceDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)                                                 | Permite que una aplicación busque un dispositivo.                                                                                                                                                                                       |
| [**IUPnPDeviceAddCallbackWithInterface**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface) | Permite que una aplicación reciba resultados de búsqueda asincrónica del marco UPnP junto con el GUID del adaptador de red a través del cual llegó el anuncio del dispositivo.                                                  |
| [**IUPnPDeviceCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefindercallback)                                 | Permite que una aplicación reciba resultados de búsqueda asincrónica del marco UPnP.                                                                                                                                         |
| [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)                                                           | Enumera una colección de dispositivos.                                                                                                                                                                                            |
| [**IUPnPHttpHeaderControl**](/windows/desktop/api/Upnp/nn-upnp-iupnphttpheadercontrol)                                       | Permite que una aplicación establezca encabezados HTTP de "Agente de usuario" de instancias de clase que implementan las interfaces [**IUPnPDeviceDeviceDevice O**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) [**IUPnPDescriptionDocument.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) |
| [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)                                                           | Permite que una aplicación recupere información de estado e invoque acciones para un servicio.                                                                                                                                         |
| [**IUPnPServiceAsync**](/windows/desktop/api/Upnp/nn-upnp-iupnpserviceasync)                                                 | Consulta asincrónica de variables de estado e invocación de acciones en una instancia de un servicio.                                                                                                                                           |
| [**IUPnPServiceCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpservicecallback)                                           | Permite que una aplicación reciba notificaciones del marco UPnP cuando se producen eventos.                                                                                                                                      |
| [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices)                                                         | Enumera una colección de servicios.                                                                                                                                                                                           |



 

 

 





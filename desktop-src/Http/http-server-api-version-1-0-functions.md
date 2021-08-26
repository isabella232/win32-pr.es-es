---
title: Funciones de la API de servidor HTTP versión 1.0
description: La API del servidor HTTP proporciona las siguientes funciones para escribir aplicaciones.
ms.assetid: 1da9907d-a09d-41e1-aca1-9a8e2b91296f
keywords:
- Funciones de la API de servidor HTTP versión 1.0
- Functions HTTP , HTTP Server API versión 1.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8520753e56e995b5751b55ff71cf49f8e82d414e702b2df255c2901e69c397fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047205"
---
# <a name="http-server-api-version-10-functions"></a>Funciones de la API de servidor HTTP versión 1.0

La API del servidor HTTP proporciona las siguientes funciones para escribir aplicaciones.

## <a name="general"></a>General



| Función                                             | Descripción                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) | Crea una cola de solicitudes HTTP y le devuelve un identificador.                                                                         |
| [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)             | Inicializa la API del servidor HTTP para que la use el proceso de llamada.                                                                   |
| [**HttpPrepareUrl**](/windows/desktop/api/Http/nf-http-httpprepareurl)             | Analiza, analiza y normaliza una dirección URL unicode o punycode no normalizada para que sea segura y válida para usarla en otras funciones HTTP. |
| [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate)               | Dirige a la API del servidor HTTP para que limpie los recursos asociados a un proceso determinado.                                       |



 

## <a name="cache-management"></a>Administración de caché



| Función                                                       | Descripción                                                                                            |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**HttpAddFragmentToCache**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache)       | Almacena en caché un fragmento de datos para que se pueda usar para crear una respuesta dinámica sin leer desde el disco. |
| [**HttpFlushResponseCache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache)       | Quita los fragmentos almacenados en caché especificados de la caché HTTP.                                                |
| [**HttpReadFragmentFromCache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) | Recupera un fragmento de respuesta almacenado en caché especificado.                                                        |



 

## <a name="configuration"></a>Configuración



| Función                                                                 | Descripción                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) | Elimina la información especificada del almacén de configuración HTTP.  |
| [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)   | Consulta la información especificada en el almacén de configuración HTTP.   |
| [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration)       | Establece los valores especificados en el almacén de configuración de LA API del servidor HTTP. |



 

## <a name="input-and-output"></a>Entrada y salida



| Función                                                             | Descripción                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------|
| [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)             | Recupera una solicitud HTTP de una cola de solicitudes especificada.      |
| [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) | Recupera los datos del cuerpo de la entidad de una solicitud HTTP determinada.       |
| [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)                 | Envía una respuesta HTTP para una solicitud HTTP determinada.          |
| [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)     | Envía datos de cuerpo de entidad de una respuesta HTTP.                    |
| [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)               | Notifica a la aplicación cuando se ha desconectado un cliente HTTP. |



 

## <a name="ssl"></a>SSL



| Función                                                             | Descripción                                             |
|----------------------------------------------------------------------|---------------------------------------------------------|
| [**HttpReceiveClientCertificate**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) | Recupera el certificado de cliente para una conexión SSL. |



 

## <a name="url-registration"></a>Registro de direcciones URL



| Función                               | Descripción                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)       | Registra una dirección URL para que las solicitudes HTTP se enrute a una cola de solicitudes especificada.           |
| [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) | Anula el registro de una dirección URL especificada para que las solicitudes ya no se enruten a una cola especificada. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estructuras de API de servidor HTTP versión 1.0](http-server-api-version-1-0-structures.md)
</dt> </dl>

 

 





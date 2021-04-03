---
title: Tareas del servidor HTTP
description: Normalmente, las tareas del servidor HTTP se realizan en un orden específico; es decir, se debe completar una tarea y la salida obtenida antes de que comience la siguiente tarea.
ms.assetid: 08f8e7e9-23b9-403f-b00c-8912919d65b1
keywords:
- Tareas del servidor HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22455dbda21aca32b26f586eed6e51cef7509af2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780119"
---
# <a name="http-server-tasks"></a>Tareas del servidor HTTP

Normalmente, las tareas del servidor HTTP se realizan en un orden específico; es decir, se debe completar una tarea y la salida obtenida antes de que comience la siguiente tarea.

Se crea una página de tareas para presentar código de ejemplo sobre tareas específicas que realiza una aplicación de servidor HTTP. Una página de tareas se vincula al archivo de extensión de C del ejemplo de servidor HTTP. Al instalar el PSDK en la unidad C: \\ de un equipo local, la aplicación de ejemplo de servidor completa se instala en C: \\ archivos de programa \\ Microsoft SDK \\ Samples \\ netds \\ http \\ Server.

En la lista siguiente se identifican las tareas del servidor HTTP:

-   [Inicializar el servicio HTTP](#initialize-the-http-service)
-   [Registrar las direcciones URL para escuchar en](#register-the-urls-to-listen-on)
-   [Llamar a la rutina para recibir una solicitud](#call-the-routine-to-receive-a-request)
-   [Recibir la solicitud](#receive-the-request)
-   [Controlar la solicitud HTTP](#handle-the-http-request)
-   [Enviar la respuesta HTTP](#send-the-http-response)
-   [Enviar la respuesta HTTP POST](#send-the-http-post-response)
-   [Limpieza de la API del servidor HTTP](#clean-up-the-http-server-api)

## <a name="initialize-the-http-service"></a>Inicializar el servicio HTTP

El servicio HTTP se inicializa con la función [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) y el identificador de la cola de solicitudes se crea mediante [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle). El servidor debe inicializarse antes de que se pueda llamar a cualquier otra función de servidor. La cola de solicitudes debe crearse antes de que el servicio pueda registrar las direcciones URL para escuchar las solicitudes HTTP entrantes.

Para obtener más información y un ejemplo de código, consulte [inicializar el servicio http](http-server-sample-application.md).

## <a name="register-the-urls-to-listen-on"></a>Registrar las direcciones URL para escuchar en

Para que la API del servidor HTTP escuche las solicitudes entrantes, las direcciones URL específicas se registran con la API mediante una llamada a la función [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) . Las solicitudes entrantes que coincidan con estas direcciones URL se enrutan a la cola de solicitudes especificada en esta llamada.

Para obtener más información y un ejemplo de código, vea [registrar las direcciones URL para escuchar en](http-server-sample-application.md).

## <a name="call-the-routine-to-receive-a-request"></a>Llamar a la rutina para recibir una solicitud

La función DoReceiveRequest asigna el búfer de solicitud, inicializa el identificador de solicitud e inicia el bucle para recibir solicitudes.

Para obtener más información y un ejemplo de código, consulte [llamar a la rutina para recibir una solicitud](http-server-sample-application.md).

## <a name="receive-the-request"></a>Recibir la solicitud

La API del servidor HTTP proporciona una estructura de solicitud para almacenar la solicitud de entrada analizada. La aplicación asigna esta estructura y se inicializa cuando se recibe una solicitud entrante. La aplicación llama a la función [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) para recibir la solicitud. Si el búfer de solicitud es demasiado pequeño para recibir la solicitud, la aplicación puede aumentar el tamaño del búfer y volver a llamar a **HttpReceiveHttpRequest** para recibir la solicitud completa.

Para obtener más información y un ejemplo de código, consulte [recibir una solicitud](http-server-sample-application.md).

## <a name="handle-the-http-request"></a>Controlar la solicitud HTTP

En la aplicación de ejemplo se muestra cómo controlar los verbos de solicitud GET y POST de HTTP. La aplicación envía un error 503 (**no \_ implementado**) si los verbos están presentes en la solicitud que la aplicación no controla.

Tenga en cuenta que la dirección URL que se usará en el control de solicitudes es la dirección URL procesada incluida en el miembro **CookedUrl** de la estructura de la [**\_ solicitud HTTP \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) . No se trata de la dirección URL no procesada en el miembro **pRawUrl** , que es únicamente para fines estadísticos y de seguimiento.

Para obtener más información y un ejemplo de código, vea [controlar la solicitud HTTP](http-server-sample-application.md).

## <a name="send-the-http-response"></a>Enviar la respuesta HTTP

La estructura de respuesta se asigna y se inicializa con el código de estado y una frase de motivo en la \_ macro Initialize http \_ Response. Un encabezado HTTP conocido se agrega a la estructura de respuesta en la \_ \_ macro agregar encabezado conocido y el cuerpo de la entidad se agrega a la respuesta de un bloque de datos de la memoria. Se llama a la función [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) para enviar la respuesta. En este ejemplo, la aplicación envía una respuesta sencilla 200 aceptar a la solicitud GET.

Para obtener más información y un ejemplo de código, vea [enviar una respuesta http](http-server-sample-application.md).

## <a name="send-the-http-post-response"></a>Enviar la respuesta HTTP POST

La solicitud POST requiere más procesamiento que la solicitud GET. El cuerpo de la entidad de solicitud se recibe llamando a la función [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) . La aplicación envía la respuesta y el cuerpo de la entidad de respuesta en llamadas independientes a la API del servidor HTTP. Los encabezados de respuesta se envían con [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse). El cuerpo de la entidad se envía en un bloque de datos desde un identificador de archivo con la función [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) .

Para obtener más información y un ejemplo de código, vea [enviar una respuesta http post](http-server-sample-application.md).

## <a name="clean-up-the-http-server-api"></a>Limpieza de la API del servidor HTTP

Las operaciones de limpieza para la API del servidor HTTP incluyen:

-   Quitando todas las direcciones URL registradas.
-   Cerrando el identificador de la cola de solicitudes.
-   Finalización de los recursos creados por la API del servidor HTTP.

La aplicación llama a la función [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) para anular el registro de las direcciones URL registradas por la función [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) inicial. La aplicación también llama a [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) para cada llamada a [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) con la configuración de marca coincidente. Esta llamada finaliza todos los recursos creados por la llamada a **HttpInitialize**.

Para obtener más información y un ejemplo de código, vea [Cleanup The http Server API](http-server-sample-application.md).

 

 





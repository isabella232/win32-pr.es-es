---
title: Tareas del servidor HTTP
description: Normalmente, las tareas del servidor HTTP se realizan en un orden específico; Es decir, se debe completar una tarea y obtener la salida antes de que comience la siguiente tarea.
ms.assetid: 08f8e7e9-23b9-403f-b00c-8912919d65b1
keywords:
- Tareas del servidor HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d89f72074ba870981421e228b0ff271505b3fce1e30cd49e79d58463570c0b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830065"
---
# <a name="http-server-tasks"></a>Tareas del servidor HTTP

Normalmente, las tareas del servidor HTTP se realizan en un orden específico; Es decir, se debe completar una tarea y obtener la salida antes de que comience la siguiente tarea.

Se crea una página de tareas para presentar código de ejemplo sobre tareas específicas que realiza una aplicación de servidor HTTP. Una página de tareas se vincula al archivo de extensión C del ejemplo de servidor HTTP. Al instalar el PSDK en la unidad C: de un equipo local, la aplicación de ejemplo de servidor completa se instala en C: Archivos de programa \\ \\ Microsoft SDK Samples \\ \\ \\ netds \\ http \\ server.

En la lista siguiente se identifican las tareas del servidor HTTP:

-   [Inicialización del servicio HTTP](#initialize-the-http-service)
-   [Registro de las direcciones URL en las que se escuchará](#register-the-urls-to-listen-on)
-   [Llamada a la rutina para recibir una solicitud](#call-the-routine-to-receive-a-request)
-   [Recibir la solicitud](#receive-the-request)
-   [Control de la solicitud HTTP](#handle-the-http-request)
-   [Envío de la respuesta HTTP](#send-the-http-response)
-   [Envío de la respuesta HTTP POST](#send-the-http-post-response)
-   [Limpieza de la API del servidor HTTP](#clean-up-the-http-server-api)

## <a name="initialize-the-http-service"></a>Inicialización del servicio HTTP

El servicio HTTP se inicializa mediante la función [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) y el identificador de la cola de solicitudes se crea mediante [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle). El servidor debe inicializarse antes de que se pueda llamar a cualquier otra función del servidor. La cola de solicitudes debe crearse antes de que el servicio pueda registrar direcciones URL para escuchar las solicitudes HTTP entrantes.

Para obtener más información y un ejemplo de código, vea [Inicializar el servicio HTTP](http-server-sample-application.md).

## <a name="register-the-urls-to-listen-on"></a>Registro de las direcciones URL en las que se escuchará

Para que la API del servidor HTTP escuche las solicitudes entrantes, las direcciones URL específicas se registran con la API mediante una llamada a la [**función HttpAddUrl.**](/windows/desktop/api/Http/nf-http-httpaddurl) Las solicitudes entrantes que coinciden con estas direcciones URL se enruta a la cola de solicitudes especificada en esta llamada.

Para obtener más información y un ejemplo de código, vea [Registrar las direcciones URL para escuchar en](http-server-sample-application.md).

## <a name="call-the-routine-to-receive-a-request"></a>Llamada a la rutina para recibir una solicitud

La función DoReceiveRequest asigna el búfer de solicitud, inicializa el identificador de solicitud e inicia el bucle para recibir solicitudes.

Para obtener más información y un ejemplo de código, vea [Llamar a la rutina para recibir una solicitud.](http-server-sample-application.md)

## <a name="receive-the-request"></a>Recibir la solicitud

La API del servidor HTTP proporciona una estructura de solicitudes para almacenar la solicitud entrante analizada. La aplicación asigna esta estructura y se inicializa cuando se recibe una solicitud entrante. La aplicación llama a [**la función HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) para recibir la solicitud. Si el búfer de solicitudes es demasiado pequeño para recibir la solicitud, la aplicación puede aumentar el tamaño del búfer y volver a llamar a **HttpReceiveHttpRequest** para recibir toda la solicitud.

Para obtener más información y un ejemplo de código, vea [Recibir una solicitud.](http-server-sample-application.md)

## <a name="handle-the-http-request"></a>Control de la solicitud HTTP

La aplicación de ejemplo muestra cómo controlar los verbos de solicitud HTTP GET y POST. La aplicación envía un error 503 **(NOT \_ IMPLEMENTED)** si hay verbos presentes en la solicitud que la aplicación no controla.

Tenga en cuenta que la dirección URL que se usará para controlar las solicitudes es la dirección URL procesada contenida en el miembro **CookedUrl** de la [**estructura HTTP REQUEST \_ \_ V1.**](/windows/desktop/api/Http/ns-http-http_request_v1) No utilice la dirección URL sin procesar en el **miembro pRawUrl,** que es únicamente para fines estadísticos y de seguimiento.

Para obtener más información y un ejemplo de código, [vea Controlar la solicitud HTTP.](http-server-sample-application.md)

## <a name="send-the-http-response"></a>Envío de la respuesta HTTP

La estructura de respuesta se asigna e inicializa con el código de estado y una frase de motivo en la macro INITIALIZE \_ HTTP \_ RESPONSE. Se agrega un encabezado HTTP conocido a la estructura de respuesta en la macro ADD KNOWN HEADER y el cuerpo de la entidad se agrega a la respuesta desde un bloque de datos \_ \_ de la memoria. Se [**llama a la función HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) para enviar la respuesta. En este ejemplo, la aplicación envía una respuesta 200 OK simple a la solicitud GET.

Para obtener más información y un ejemplo de código, vea [Enviar una respuesta HTTP.](http-server-sample-application.md)

## <a name="send-the-http-post-response"></a>Envío de la respuesta HTTP POST

La solicitud POST requiere más procesamiento que la solicitud GET. El cuerpo de la entidad de solicitud se recibe mediante una llamada a la [**función HttpReceiveRequestEntityBody.**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) La aplicación envía la respuesta y el cuerpo de la entidad de respuesta en llamadas independientes a la API del servidor HTTP. Los encabezados de respuesta se envían con [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse). El cuerpo de la entidad se envía en un bloque de datos desde un identificador de archivo con la [**función HttpSendResponseEntityBody.**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)

Para obtener más información y un ejemplo de código, vea [Enviar una respuesta HTTP POST](http-server-sample-application.md).

## <a name="clean-up-the-http-server-api"></a>Limpieza de la API del servidor HTTP

Las operaciones de limpieza de la API del servidor HTTP incluyen:

-   Quitar todas las direcciones URL registradas.
-   Cierre el identificador a la cola de solicitudes.
-   Terminación de los recursos creados por la API del servidor HTTP.

La aplicación llama a la [**función HttpRemoveUrl para**](/windows/desktop/api/Http/nf-http-httpremoveurl) anular el registro de las direcciones URL registradas por la [**función HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) inicial. La aplicación también llama a [**HttpTerminate para**](/windows/desktop/api/Http/nf-http-httpterminate) cada llamada a [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) con la configuración de marca correspondiente. Esta llamada finaliza todos los recursos creados por la llamada a **HttpInitialize**.

Para obtener más información y un ejemplo de código, vea [Cleanup the HTTP Server API](http-server-sample-application.md).

 

 





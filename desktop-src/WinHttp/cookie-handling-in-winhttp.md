---
description: Control de cookies en WinHTTP
ms.assetid: ef0f0847-05f6-4477-8e48-e0bea66314ab
title: Control de cookies en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3b596225dc3c741ab9ed0139a63e343e7afb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707491"
---
# <a name="cookie-handling-in-winhttp"></a>Control de cookies en WinHTTP

Los datos de la sesión HTTP se pasan entre el cliente y el servidor en el encabezado de la cookie de la solicitud o la respuesta. El servidor envía cookies al cliente en el encabezado Set-Cookie de la respuesta y la API WinHTTP reenvía la cookie del servidor al servidor en el encabezado de la cookie de la solicitud. Las especificaciones de control de cookies, descritas en RFC 2109 (mecanismo de administración de Estado HTTP), se implementan de forma predeterminada en WinHTTP. Las especificaciones recientes de administración de cookies, descritas en RFC 2964, no son compatibles con WinHTTP.

WinHTTP obtiene la cookie del encabezado servidores Set-Cookie y la almacena en una caché por sesión. Esta cookie se vuelve a enviar en las solicitudes posteriores de la misma sesión de WinHTTP en la que el destino coincide con el origen de la cookie. La API de WinHTTP vuelve a generar el encabezado de la cookie de solicitud para cada segmento de la solicitud.

En la lista siguiente se describen varias opciones que las aplicaciones cliente de WinHTTP pueden utilizar para controlar las cookies:

-   Control automático de cookies: WinHTTP controla automáticamente las cookies y la aplicación cliente no realiza ningún control de cookies personalizado.
-   Deshabilitar el control de cookies automático: el control automático de cookies en la API WinHTTP está deshabilitado y no se envían cookies.
-   Especificar manualmente todas las cookies: el control automático de cookies está deshabilitado y la aplicación cliente agrega o quita todos los encabezados de cookie para cada solicitud de la sesión.
-   Control manual y automático de cookies: Combine el control de cookies automática y manual.

## <a name="disabling-automatic-cookie-handling"></a>Deshabilitar el control automático de cookies

Para deshabilitar el control de cookies, la aplicación cliente WinHTTP llama a la función [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con el parámetro *DWOPTION* establecido en WinHTTP \_ OPTION \_ Disable \_ Feature, y el parámetro *lpBuffer* establecido en WinHTTP \_ deshabilitar \_ cookies. El parámetro *hInternet* puede ser un identificador de sesión o un identificador de solicitud. Cuando se deshabilita el control de cookies en un identificador de solicitud que ha enviado una solicitud anterior, el cliente debe quitar manualmente los encabezados de cookie de solicitud existentes con la función [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) antes de enviar la solicitud siguiente. Para obtener más información, consulte [quitar encabezados de cookies](#removing-cookie-headers).

**Nota:**  La aplicación cliente debe establecer todas las cookies de la sesión después de que se haya deshabilitado el modo automático.

## <a name="manually-specifying-all-cookies"></a>Especificación manual de todas las cookies

Cuando se deshabilita el control automático de cookies, la aplicación cliente WinHTTP tiene la opción de especificar manualmente todas las cookies. Para establecer manualmente la cookie, la aplicación llama a [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) especificando el encabezado de la cookie en el parámetro *pwszHeaders* . La aplicación cliente debe borrar todos los encabezados de cookie antes de volver a enviar la solicitud.

La aplicación cliente también debe cambiar el encabezado de la cookie cuando se ha redirigido la solicitud. Para cambiar la cookie en las solicitudes redirigidas, el cliente especifica una función de devolución de llamada con [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) que responde al caso de devolución de llamada de redirección. El controlador de devolución de llamada debe borrar la cookie enviada anteriormente en la solicitud mediante una llamada a [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders). Para obtener más información acerca de cómo quitar encabezados de cookies, consulte [quitar encabezados de cookies](#removing-cookie-headers).

## <a name="manual-and-automatic-cookie-handling"></a>Control manual y automático de cookies

Las aplicaciones cliente de WinHTTP pueden combinar el mecanismo de control de cookies automático de WinHTTP con el control manual de cookies. La aplicación agrega cookies personalizadas al encabezado de cookie generado automáticamente antes de enviar la solicitud con la función [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) . La cookie personalizada debe ser el primer encabezado de cookie en la solicitud de la API de WinHTTP para almacenar correctamente en caché la cookie. La aplicación cliente también debe quitar las cookies enviadas en las solicitudes anteriores antes de volver a enviar una solicitud en el mismo identificador de solicitud. Para obtener más información, consulte quitar encabezados de cookies.

Las cookies agregadas a una solicitud antes de la llamada a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) se incluyen en todas las solicitudes WinHTTP enviadas en nombre de las siguientes llamadas a **WinHttpSendRequest** y [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) . Es posible que la aplicación cliente tenga que borrar el encabezado de la cookie cuando se haya Redirigido la solicitud. Para borrar la cookie en las solicitudes redirigidas, el cliente especifica una función de devolución de llamada con [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) que responde al caso de devolución de llamada de redirección. El controlador de devolución de llamada debe borrar la cookie que se envió previamente en la solicitud mediante una llamada a [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders). Es posible que la función de devolución de llamada no establezca cookies personalizadas nuevas en la devolución de llamada de redirección. El cliente debe esperar a que se complete **WinHttpReceiveResponse** antes de agregar nuevas cookies para la siguiente llamada a **WinHttpSendRequest** .

## <a name="removing-cookie-headers"></a>Quitar encabezados de cookies

Es posible que la aplicación cliente WinHTTP tenga que borrar la cookie de solicitud existente antes de volver a enviar una solicitud para evitar que las cookies enviadas en solicitudes anteriores se envíen de nuevo en la solicitud actual. para obtener más información, vea la nota siguiente. Tenga en cuenta también que no es necesario borrar las cookies antes de que se envíe la primera solicitud en el identificador de solicitud. El cliente puede borrar las cookies existentes mediante una llamada a [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) con un encabezado de cookie vacío en el parámetro *pwszHeaders* y el indicador de \_ \_ reemplazo de la marca de WinHTTP ADDREQ \_ establecido en el parámetro *dwModifier* . En el ejemplo de código siguiente se muestra cómo borrar el encabezado de la cookie en la solicitud.

``` syntax
WinHttpAddRequestHeaders( hRequest, 
                          L"Cookie:", 
                          -1, 
                          WINHTTP_ADDREQ_FLAG_REPLACE);
```

La API WinHTTP tiene distintos comportamientos de control de cookies para las versiones del sistema operativo anteriores a Windows XP con Service Pack 2 (SP2) y Windows Server 2003 con Service Pack 1 (SP1).

* * Windows XP con SP2 y versiones posteriores y Windows Server 2003 con SP1 y versiones posteriores: * *

La API WinHTTP borra todas las cookies enviadas en las solicitudes anteriores para el identificador de solicitud. El cliente puede Agregar manualmente nuevos encabezados de cookie antes de cada llamada a WinHttpSendRequest. Si la funcionalidad de control de cookies automática de la API WinHTTP no se ha deshabilitado, la API de WinHTTP anexará el nuevo encabezado de cookie (o agregará un encabezado de cookie nuevo si la aplicación cliente no agregó uno manualmente) con la cookie del servidor.

* * Windows XP con SP2 y Windows Server 2003 con SP1: * *

La API de WinHTTP no borra el encabezado de la cookie de solicitud una vez finalizada la [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) . Las cookies enviadas en solicitudes anteriores se reenviarán en las llamadas posteriores a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). La aplicación cliente WinHTTP debe borrar los encabezados de cookies existentes antes de volver a enviar una solicitud en el identificador de solicitud.

 

 




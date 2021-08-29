---
description: Control de cookies en WinHTTP
ms.assetid: ef0f0847-05f6-4477-8e48-e0bea66314ab
title: Control de cookies en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004f228ba69f3d1cc7476c01ea084dac64379a7ff62d91c7c4920f7320cbd111
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133248"
---
# <a name="cookie-handling-in-winhttp"></a>Control de cookies en WinHTTP

Los datos de sesión HTTP se pasan entre el cliente y el servidor en el encabezado de cookie de la solicitud o la respuesta. El servidor envía cookies al cliente en el encabezado Set-cookie de la respuesta y la API WinHTTP vuelve a enviar la cookie del servidor al servidor en el encabezado de cookie de la solicitud. Las especificaciones de control de cookies, descritas en rfc 2109 (Mecanismo de administración de estado HTTP), se implementan de forma predeterminada en WinHTTP. WinHTTP no admite las especificaciones recientes de control de cookies, descritas en rfc 2964.

WinHTTP obtiene la cookie de los servidores Set-Cookie encabezado y la almacena en una caché por sesión. Esta cookie se reenvia en solicitudes posteriores en la misma sesión WinHTTP donde el destino coincide con el origen de la cookie. La API WinHTTP vuelve a generar el encabezado de cookie de solicitud para cada etapa de la solicitud.

En la lista siguiente se describen varias opciones que las aplicaciones cliente WinHTTP pueden usar para controlar las cookies:

-   Control automático de cookies: WinHTTP controla automáticamente las cookies y la aplicación cliente no realiza ningún control de cookies personalizado.
-   Deshabilitar el control automático de cookies: el control automático de cookies en la API WinHTTP está deshabilitado y no se envía ninguna cookie.
-   Especificar manualmente todas las cookies: el control automático de cookies está deshabilitado y la aplicación cliente agrega o quita todos los encabezados de cookie para cada solicitud de la sesión.
-   Control manual y automático de cookies: combine el control automático y manual de cookies.

## <a name="disabling-automatic-cookie-handling"></a>Deshabilitación del control automático de cookies

Para deshabilitar el control de cookies, la aplicación cliente WinHTTP llama a la función [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con el parámetro *dwOption* establecido en WINHTTP OPTION DISABLE FEATURE y el parámetro lpBuffer establecido en \_ \_ \_ WINHTTP DISABLE  \_ \_ COOKIES. El *parámetro hInternet* puede ser un identificador de sesión o un identificador de solicitud. Cuando el control de cookies está deshabilitado en un identificador de solicitud que ha enviado una solicitud anterior, el cliente debe quitar manualmente los encabezados de cookie de solicitud existentes con la función [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) antes de enviar la siguiente solicitud. Para más información, consulte [Eliminación de encabezados de cookies.](#removing-cookie-headers)

**Nota**  La aplicación cliente debe establecer todas las cookies en la sesión después de deshabilitar el modo automático.

## <a name="manually-specifying-all-cookies"></a>Especificar manualmente todas las cookies

Cuando se deshabilita el control automático de cookies, la aplicación cliente WinHTTP tiene la opción de especificar manualmente todas las cookies. Para establecer manualmente la cookie, la aplicación llama a [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) especificando el encabezado de cookie en el *parámetro pwszHeaders.* La aplicación cliente debe borrar todos los encabezados de cookie antes de volver a enviar la solicitud.

La aplicación cliente también debe cambiar el encabezado de cookie cuando se ha redirigido la solicitud. Para cambiar la cookie en las solicitudes redirigidas, el cliente especifica una función de devolución de llamada [**con WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) que responde al caso de devolución de llamada de redirección. El controlador de devolución de llamada debe borrar la cookie enviada previamente en la solicitud mediante una llamada [**a WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders). Para obtener más información sobre cómo quitar encabezados de cookie, consulte [Eliminación de encabezados de cookies.](#removing-cookie-headers)

## <a name="manual-and-automatic-cookie-handling"></a>Control manual y automático de cookies

Las aplicaciones cliente WinHTTP pueden combinar el mecanismo de control automático de cookies WinHTTP con el control manual de cookies. La aplicación agrega cookies personalizadas al encabezado de cookie generado automáticamente antes de enviar la solicitud con la [**función WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) La cookie personalizada debe ser el primer encabezado de cookie en la solicitud para que la API WinHTTP almacena en caché correctamente la cookie. La aplicación cliente también debe quitar las cookies enviadas en solicitudes anteriores antes de volver a enviar una solicitud en el mismo identificador de solicitud. Para más información, consulte Eliminación de encabezados de cookies.

Las cookies agregadas a una solicitud antes de la llamada a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) se incluyen en todas las solicitudes WinHTTP enviadas en nombre de las siguientes llamadas **WinHttpSendRequest** y [**WinHttpReceiveResponse.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) Es posible que la aplicación cliente tenga que borrar el encabezado de cookie cuando se ha redirigido la solicitud. Para borrar la cookie en las solicitudes redirigidas, el cliente especifica una función de devolución de llamada [**con WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) que responde al caso de devolución de llamada de redirección. El controlador de devolución de llamada debe borrar la cookie que se envió anteriormente en la solicitud mediante una llamada [**a WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders). Es posible que la función de devolución de llamada no establezca nuevas cookies personalizadas en la devolución de llamada de redireccionamiento. El cliente debe esperar a **que WinHttpReceiveResponse** se complete antes de agregar nuevas cookies para la siguiente **llamada WinHttpSendRequest.**

## <a name="removing-cookie-headers"></a>Eliminación de encabezados de cookies

Es posible que la aplicación cliente WinHTTP tenga que borrar la cookie de solicitud existente antes de volver a enviar una solicitud para evitar que las cookies enviadas en solicitudes anteriores se envíen de nuevo en la solicitud actual. Para obtener más información, vea la nota siguiente. Tenga en cuenta también que las cookies no tienen que borrarse antes de que se envíe la primera solicitud en el identificador de solicitud. El cliente puede borrar las cookies existentes llamando a [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) con un encabezado de cookie vacío en el parámetro *pwszHeaders* y la marca WINHTTP ADDREQ FLAG REPLACE establecida en el \_ parámetro \_ \_ *dwModifier.* En el ejemplo de código siguiente se muestra cómo borrar el encabezado de cookie en la solicitud.

``` syntax
WinHttpAddRequestHeaders( hRequest, 
                          L"Cookie:", 
                          -1, 
                          WINHTTP_ADDREQ_FLAG_REPLACE);
```

La API WinHTTP tiene distintos comportamientos de control de cookies para versiones del sistema operativo anteriores a Windows XP con Service Pack 2 (SP2) y Windows Server 2003 con Service Pack 1 (SP1).

**Windows XP con SP2 y versiones posteriores y Windows Server 2003 con SP1 y versiones posteriores: **

La API WinHTTP borra todas las cookies enviadas en solicitudes anteriores para el identificador de solicitud. El cliente puede agregar manualmente nuevos encabezados de cookie antes de cada llamada a WinHttpSendRequest. Si la funcionalidad de control automático de cookies de la API WinHTTP no se ha deshabilitado, la API WinHTTP anexará el nuevo encabezado de cookie (o agregará un nuevo encabezado de cookie si la aplicación cliente no agregó uno manualmente) con la cookie del servidor.

**Windows XP con SP2 y Windows Server 2003 con SP1: **

La API WinHTTP no borra el encabezado de cookie de solicitud una vez [**completado WinHttpReceiveResponse.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) Las cookies enviadas en solicitudes anteriores se reenviarán en llamadas posteriores [**a WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). La aplicación cliente WinHTTP debe borrar los encabezados de cookies existentes antes de volver a enviar una solicitud en el identificador de solicitud.

 

 




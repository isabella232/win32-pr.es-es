---
description: Microsoft Windows HTTP Services (WinHTTP) está destinado a aplicaciones de servidor de nivel intermedio y back-end que requieren acceso a una pila de cliente HTTP.
ms.assetid: 5b0cf321-8f69-4526-a628-e6ca0f9d4a58
title: Porte de aplicaciones WinINet a WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b111cd79e7ce7edfb09d43993ee2735ce09275f51c58bcfad319fb073dccc5b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052013"
---
# <a name="porting-wininet-applications-to-winhttp"></a>Porte de aplicaciones WinINet a WinHTTP

Microsoft Windows HTTP Services (WinHTTP) está destinado a aplicaciones de servidor de nivel intermedio y back-end que requieren acceso a una pila de cliente HTTP. [Microsoft Windows Internet (WinINet)](winhttp-start-page.md) proporciona una pila de cliente HTTP para las aplicaciones cliente, así como acceso a los protocolos protocolo de transferencia de archivos (FTP), SOCKSv4 y Gopher. Esta información general puede ayudar a determinar si la porción de las aplicaciones WinINet a WinHTTP sería beneficiosa. También se describen los requisitos de conversión específicos.

-   [Aspectos que se deben tener en cuenta antes de portear la aplicación WinINet](#things-to-consider-before-porting-your-wininet-application)
-   [Equivalentes de WinHTTP a funciones de WinINet](#winhttp-equivalents-to-wininet-functions)
-   [Diferente control de solicitudes asincrónicas](#different-handling-of-asynchronous-requests)
-   [Diferencias en las notificaciones de devolución de llamada WinHTTP](#differences-in-winhttp-callback-notifications)
-   [Diferencias de autenticación](#authentication-differences)
-   [Diferencias en las transacciones HTTP seguras](#differences-in-secure-http-transactions)

## <a name="things-to-consider-before-porting-your-wininet-application"></a>Aspectos que se deben tener en cuenta antes de portear la aplicación WinINet

Considere la posibilidad de portear la aplicación WinINet a WinHTTP si la aplicación se beneficiaría de:

-   Una pila de cliente HTTP segura para el servidor.
-   Uso de pila minimizado.
-   Escalabilidad de una aplicación de servidor.
-   Menos dependencias en las API relacionadas con la plataforma.
-   Compatibilidad con la suplantación de subprocesos.
-   Una pila HTTP fácil de usar.
-   Acceso al objeto [**WinHttpRequest**](winhttprequest.md) que admite scripts.

No considere la posibilidad de portear la aplicación WinINet a WinHTTP si debe admitir una o varias de las siguientes opciones:

-   El protocolo FTP o Gopher de la pila HTTP.
-   Compatibilidad con el protocolo SOCKSv4 para comunicarse con servidores proxy de SOCKS.
-   Servicios de acceso telefónico automático.

Si decide portabilidad de la aplicación a WinHTTP, las secciones siguientes le guiarán a través del proceso de conversión.

Para obtener una aplicación de ejemplo para WinINet y WinHTTP, compare el ejemplo AsyncDemo para WinINet con el ejemplo AsyncDemo para WinHTTP.

## <a name="winhttp-equivalents-to-wininet-functions"></a>Equivalentes de WinHTTP a funciones de WinINet

En la tabla siguiente se enumeran las funciones de WinINet relacionadas con la pila de cliente HTTP junto con los equivalentes de WinHTTP.

Si la aplicación requiere funciones winINet que no aparecen en la lista, no porte la aplicación a WinHTTP.



| Función WinINet                                                       | Equivalente de WinHTTP                                                                                                                                                                                     | Cambios importantes                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HttpAddRequestHeaders**](/windows/desktop/api/wininet/nf-wininet-httpaddrequestheadersa)             | [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                                                                                                                                           | Ninguno.                                                                                                                                                                                                                                                                                                                                |
| [**HttpEndRequest**](/windows/desktop/api/wininet/nf-wininet-httpendrequesta)                           | [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)                                                                                                                                               | El valor de contexto se establece [**con WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) Las opciones de solicitud se establecen [**con WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) [**Se debe llamar a WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) después de enviar una solicitud.                      |
| [**HttpOpenRequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta)                         | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                                                                                       | El valor de contexto se establece [**con WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)                                                                                                                                                                                                      |
| [**HttpQueryInfo**](/windows/desktop/api/wininet/nf-wininet-httpqueryinfoa)                             | [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)                                                                                                                                                     | Ninguno.                                                                                                                                                                                                                                                                                                                                |
| [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta)                         | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | El valor de contexto se puede establecer [**con WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                                                                                                                  |
| [**HttpSendRequestEx**](/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa)                     | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | No se pueden proporcionar búferes.                                                                                                                                                                                                                                                                                                          |
| [**InternetNtenicalizeUrl**](/windows/desktop/api/wininet/nf-wininet-internetcanonicalizeurla)         | No equivalente                                                                                                                                                                                          | Las direcciones URL ahora se ponen en forma canónica [**en WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                                                                                                                                                                              |
| [**InternetCheckConnection**](/windows/desktop/api/wininet/nf-wininet-internetcheckconnectiona)         | No equivalente                                                                                                                                                                                          | No se implementa en WinHTTP.                                                                                                                                                                                                                                                                                                          |
| [**InternetCloseHandle**](/windows/desktop/api/wininet/nf-wininet-internetclosehandle)                 | [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)                                                                                                                                                       | El cierre de un identificador primario en WinHTTP no cierra de forma recursiva los identificadores secundarios.                                                                                                                                                                                                                                                         |
| [**InternetCombineUrl**](/windows/desktop/api/wininet/nf-wininet-internetcombineurla)                   | No equivalente                                                                                                                                                                                          | Las direcciones URL se pueden ensamblar con la [**función WinHttpCreateUrl.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)                                                                                                                                                                                                                                                |
| [**InternetConfirmZoneCrossing**](/windows/desktop/api/wininet/nf-wininet-internetconfirmzonecrossing) | No equivalente                                                                                                                                                                                          | No se implementa en WinHTTP.                                                                                                                                                                                                                                                                                                          |
| [**InternetConnect**](/windows/desktop/api/wininet/nf-wininet-internetconnecta)                         | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                                                                                               | El valor de contexto se establece [**con WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) Las opciones de solicitud se establecen [**con WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) Las credenciales de usuario se establecen [**con WinHttpSetCredentials.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)                                 |
| [**InternetCrackUrl**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla)                       | [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)                                                                                                                                                             | Comportamiento opuesto de la marca ESCAPE de ICU: con InternetCrackUrl , esta marca hace que las secuencias de escape (%xx) se conviertan en caracteres, pero con \_ [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl), hace que los caracteres de escape de una solicitud HTTP se conviertan en secuencias de escape. [](/windows/desktop/api/wininet/nf-wininet-internetcrackurla) |
| [**InternetCreateUrl**](/windows/desktop/api/wininet/nf-wininet-internetcreateurla)                     | [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)                                                                                                                                                           | Ninguno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetErrorDlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg)                       | No equivalente                                                                                                                                                                                          | Dado que WinHTTP está destinado a aplicaciones del lado servidor, no implementa ninguna interfaz de usuario.                                                                                                                                                                                                                                   |
| [**InternetGetCookie**](/windows/desktop/api/wininet/nf-wininet-internetgetcookiea)                     | No equivalente                                                                                                                                                                                          | WinHTTP no conserva los datos entre sesiones y no puede acceder a las cookies de WinINet.                                                                                                                                                                                                                                                    |
| [**InternetAbrir**](/windows/desktop/api/wininet/nf-wininet-internetopena)                               | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                                                                                     | Ninguno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetOpenUrl**](/windows/desktop/api/wininet/nf-wininet-internetopenurla)                         | [**WinHttpConnect,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) [**WinHttpOpenRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) [**WinHttpSendRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) | Esta funcionalidad está disponible en las funciones WinHTTP enumeradas.                                                                                                                                                                                                                                                                     |
| [**InternetQueryDataAvailable**](/windows/desktop/api/wininet/nf-wininet-internetquerydataavailable)   | [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)                                                                                                                                         | No hay parámetros reservados.                                                                                                                                                                                                                                                                                                              |
| [**InternetQueryOption**](/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona)                 | [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)                                                                                                                                                       | WinHTTP ofrece un conjunto diferente de opciones de WinINet. Para obtener más información y las opciones que ofrece WinHTTP, vea [**Marcas de opción**](option-flags.md).                                                                                                                                                                               |
| [**InternetReadFile**](/windows/desktop/api/wininet/nf-wininet-internetreadfile)                       | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | Ninguno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetReadFileEx**](/windows/desktop/api/wininet/nf-wininet-internetreadfileexa)                   | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | En lugar de una estructura, el búfer es una región de memoria dirigida con un puntero.                                                                                                                                                                                                                                                  |
| [**InternetSetOption**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona)                     | [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)                                                                                                                                                           | Ninguno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetSetStatusCallback**](/windows/desktop/api/wininet/nf-wininet-internetsetstatuscallback)     | [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)                                                                                                                                           | Para obtener más información, vea "Diferente control de solicitudes asincrónicas" en este tema.                                                                                                                                                                                                                                               |
| [**InternetTimeFromSystemTime**](/windows/desktop/api/wininet/nf-wininet-internettimefromsystemtime)   | [**WinHttpTimeFromSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)                                                                                                                                         | Ninguno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetTimeToSystemTime**](/windows/desktop/api/wininet/nf-wininet-internettimetosystemtime)       | [**WinHttpTimeToSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)                                                                                                                                             | Ninguno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetWriteFile**](/windows/desktop/api/wininet/nf-wininet-internetwritefile)                     | [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)                                                                                                                                                           | Ninguno.                                                                                                                                                                                                                                                                                                                                |



 

## <a name="different-handling-of-asynchronous-requests"></a>Diferente control de solicitudes asincrónicas

Tenga en cuenta que en WinINet y WinHTTP, algunas funciones pueden completar solicitudes asincrónicas de forma sincrónica o asincrónica. La aplicación debe controlar cualquier situación. Hay diferencias significativas en la forma en que WinINet y WinHTTP controlan estas funciones potencialmente asincrónicas.

Wininet

-   Finalización sincrónica: si una llamada a función winINet potencialmente asincrónica se completa de forma sincrónica, los parámetros OUT de la función devuelven los resultados de la operación. Cuando se produzca un error, recupere el código de error llamando a [**GetLastError después**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) de la llamada a la función WinINet.

-   Finalización asincrónica: si una llamada a función potencialmente asincrónica se completa de forma asincrónica, los resultados de la operación y los errores son accesibles en la función de devolución de llamada. La función de devolución de llamada se ejecuta en un subproceso de trabajo, no en el subproceso que realizó la llamada de función inicial.

En otras palabras, la aplicación debe duplicar la lógica para controlar los resultados de estas operaciones en dos lugares: inmediatamente después de la llamada a la función y en la función de devolución de llamada.

WinHTTP simplifica este modelo al permitirle implementar la lógica operativa solo en la función de devolución de llamada, que recibe una notificación de finalización independientemente de si la operación se completó de forma sincrónica o asincrónica. Cuando se habilita la operación asincrónica, los parámetros OUT de las funciones WinHTTP no devuelven datos significativos y deben establecerse en **NULL.**

La única diferencia significativa entre la finalización asincrónica y sincrónica en WinHTTP, desde la perspectiva de la aplicación, es en la que se ejecuta la función de devolución de llamada.

WinHTTP

-   Finalización sincrónica: cuando una operación se completa de forma sincrónica, los resultados se devuelven en una función de devolución de llamada que se ejecuta en el mismo subproceso que la llamada de función original.

-   Finalización asincrónica: cuando una operación se completa de forma asincrónica, los resultados se devuelven en una función de devolución de llamada que se ejecuta en un subproceso de trabajo.

Aunque la mayoría de los errores también se pueden controlar completamente dentro de la función de devolución de llamada, las aplicaciones WinHTTP deben estar preparadas para que una función devuelva **FALSE** debido a un ERROR INVALID PARAMETER u otro error similar recuperado mediante una llamada a \_ \_ [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

A diferencia de WinINet, que puede ejecutar varias operaciones asincrónicas simultáneamente, WinHTTP aplica una directiva de una operación asincrónica pendiente por identificador de solicitud. Si una operación está pendiente y se llama a otra función WinHTTP, se produce un error en la segunda función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR \_ INVALID \_ OPERATION.

WinHTTP simplifica este modelo al permitirle implementar la lógica operativa solo en la función de devolución de llamada, que recibe una notificación de finalización independientemente de si la operación se completó de forma sincrónica o asincrónica. Cuando se habilita la operación asincrónica, los parámetros OUT de las funciones WinHTTP no devuelven datos significativos y deben establecerse en **NULL.**

## <a name="differences-in-winhttp-callback-notifications"></a>Diferencias en las notificaciones de devolución de llamada WinHTTP

La función de devolución de llamada de estado recibe actualizaciones sobre el estado de las operaciones a través de marcas de notificación. En WinHTTP, las notificaciones se seleccionan mediante el *parámetro dwNotificationFlags* de la [**función WinHttpSetStatusCallback.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) Use la **marca WINHTTP \_ CALLBACK \_ FLAG ALL \_ \_ NOTIFICATIONS** para recibir una notificación de todas las actualizaciones de estado.

Las notificaciones que indican que una operación determinada está completa se denominan notificaciones de finalización o simplemente finalizaciones. En WinINet, cada vez que la función de devolución de llamada recibe una finalización, el parámetro *lpvStatusInformation* contiene una estructura [**INTERNET \_ ASYNC \_ RESULT.**](/windows/desktop/api/wininet/ns-wininet-internet_async_result) En WinHTTP, esta estructura no está disponible para todas las finalizaciones. Es importante revisar la página de referencia de [**WINHTTP \_ STATUS \_ CALLBACK,**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback)que contiene información sobre las notificaciones y qué tipo de datos se pueden esperar para cada una.

En WinHTTP, una única finalización, **WINHTTP \_ CALLBACK \_ STATUS REQUEST \_ \_ ERROR**, indica que se produjo un error en una operación. Todas las demás finalizaciones indican una operación correcta.

Tanto WinINet como WinHTTP usan un valor de contexto definido por el usuario para pasar información del subproceso principal a la función de devolución de llamada de estado, que se puede ejecutar en un subproceso de trabajo. En WinINet, el valor de contexto utilizado por la función de devolución de llamada de estado se establece mediante una llamada a una de varias funciones. En WinHTTP, el valor de contexto solo se establece [**con WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) Por este problema, es posible en WinHTTP que se produzca una notificación antes de establecer un valor de contexto. Si la función de devolución de llamada recibe una notificación antes de establecer el valor de contexto, la aplicación debe estar preparada para recibir **NULL** en el parámetro *dwContext* de la función de devolución de llamada.

## <a name="authentication-differences"></a>Diferencias de autenticación

En WinINet, las credenciales de usuario se establecen mediante una llamada a la función [**InternetSetOption,**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona) mediante código similar al proporcionado en el ejemplo de código siguiente.

``` syntax
// Use the WinINet InternetSetOption function to set the 
// user credentials to the user name contained in strUsername 
// and the password to the contents of strPassword.
       
InternetSetOption( hRequest, INTERNET_OPTION_PROXY_USERNAME, 
                   strUsername, strlen(strUsername) + 1 );

InternetSetOption( hRequest, INTERNET_OPTION_PROXY_PASSWORD, 
                   strPassword, strlen(strPassword) + 1 );
```

Por motivos de compatibilidad, las credenciales de usuario se pueden establecer de forma similar en WinHTTP mediante la función [**WinHttpSetOption,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) pero esto no se recomienda porque puede suponer una vulnerabilidad de seguridad.

En su lugar, cuando una aplicación recibe un código de estado 401 en WinHTTP, el método recomendado para establecer credenciales es identificar primero un esquema de autenticación mediante [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) y, en segundo lugar, establecer las credenciales mediante [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials). En el ejemplo de código siguiente se muestra cómo hacerlo.

``` syntax
DWORD dwSupportedSchemes;
DWORD dwPrefered;
DWORD dwTarget;

// Obtain the supported and first schemes.
WinHttpQueryAuthSchemes( hRequest, &dwSupportedSchemes, &dwPrefered, &dwTarget );

// Set the credentials before resending the request.
WinHttpSetCredentials( hRequest, dwTarget, dwPrefered, strUsername, strPassword, NULL );
```

Dado que no hay ningún equivalente a [**InternetErrorDlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg) en WinHTTP, las aplicaciones que obtienen credenciales a través de una interfaz de usuario deben proporcionar su propia interfaz.

A diferencia de WinINet, WinHTTP no almacena en caché las contraseñas. Se deben proporcionar credenciales de usuario válidas para cada solicitud.

WinHTTP no admite el esquema de autenticación de contraseña distribuida (DPA) compatible con WinINet. Sin embargo, WinHTTP admite Microsoft Passport 1.4. Para más información sobre el uso de la autenticación de Passport en WinHTTP, consulte [Autenticación de Passport en WinHTTP.](passport-authentication-in-winhttp.md)

WinHTTP no se basa en Internet Explorer configuración para determinar la directiva de inicio de sesión automático. En su lugar, la directiva de inicio de sesión automático se establece [**con WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Para obtener más información sobre la autenticación en WinHTTP, incluida la directiva de inicio de sesión automático, vea [Autenticación en WinHTTP.](authentication-in-winhttp.md)

## <a name="differences-in-secure-http-transactions"></a>Diferencias en las transacciones HTTP seguras

En WinINet, inicie una sesión segura mediante [**HttpOpenRequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta) o [**InternetConnect,**](/windows/desktop/api/wininet/nf-wininet-internetconnecta)pero en WinHTTP, debe llamar a [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) mediante la **marca WINHTTP \_ FLAG \_ SECURE.**

En una transacción HTTP segura, se pueden usar certificados de servidor para autenticar un servidor en el cliente. En WinINet, si un certificado de servidor contiene errores, [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta) produce un error y proporciona detalles sobre los errores del certificado.

En WinHttp, los errores de certificado de servidor se controlan según la versión como se muestra a continuación:

-   A partir de WinHttp 5.1, si se produce un error en un certificado de servidor o contiene errores, la llamada a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) notifica un ERROR SEGURO DE ESTADO DE DEVOLUCIÓN DE LLAMADA **WINHTTP \_ \_ \_ \_** en la función de devolución de llamada. Si se omite el error generado por **WinHttpSendRequest,** las llamadas posteriores a [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) producirán un \_ error ERROR WINHTTP \_ OPERATION \_ CANCELLED.
-   En WinHTTP 5.0, los errores en los certificados de servidor no provocan, de forma predeterminada, un error en una solicitud. En su lugar, los errores se notifican en la función de devolución de llamada con la notificación **WINHTTP \_ CALLBACK \_ STATUS SECURE \_ \_ FAILURE.**

En algunas plataformas anteriores, WinINet admite los protocolos Private Communication Technology (PCT) o Fortezza, aunque no en Windows XP.

WinHTTP no admite los protocolos PCT y Fortezza en ninguna plataforma y, en su lugar, se basa en Capa de sockets seguros (SSL) 2.0, SSL 3.0 o Seguridad de la capa de transporte (TLS) 1.0.

 

 

---
description: Los servicios HTTP de Microsoft Windows (WinHTTP) están destinados a las aplicaciones de servidor de nivel intermedio y back-end que requieren acceso a una pila de cliente HTTP.
ms.assetid: 5b0cf321-8f69-4526-a628-e6ca0f9d4a58
title: Trasladar aplicaciones WinINet a WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f64c4ecc825934d32b1d363f010bd04e1484428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003014"
---
# <a name="porting-wininet-applications-to-winhttp"></a>Trasladar aplicaciones WinINet a WinHTTP

Los servicios HTTP de Microsoft Windows (WinHTTP) están destinados a las aplicaciones de servidor de nivel intermedio y back-end que requieren acceso a una pila de cliente HTTP. [Microsoft Windows Internet (WinInet)](winhttp-start-page.md) proporciona una pila de cliente http para las aplicaciones cliente, así como el acceso a los protocolos protocolo de transferencia de archivos (FTP), SOCKSv4 y Gopher. Esta información general puede ayudar a determinar si es beneficioso trasladar las aplicaciones WinINet a WinHTTP. También se describen los requisitos de conversión específicos.

-   [Aspectos que deben tenerse en cuenta antes de migrar la aplicación WinINet](#things-to-consider-before-porting-your-wininet-application)
-   [Equivalentes de WinHTTP a funciones WinINet](#winhttp-equivalents-to-wininet-functions)
-   [Control diferente de las solicitudes asincrónicas](#different-handling-of-asynchronous-requests)
-   [Diferencias en las notificaciones de devolución de llamada de WinHTTP](#differences-in-winhttp-callback-notifications)
-   [Diferencias de autenticación](#authentication-differences)
-   [Diferencias en las transacciones HTTP seguras](#differences-in-secure-http-transactions)

## <a name="things-to-consider-before-porting-your-wininet-application"></a>Aspectos que deben tenerse en cuenta antes de migrar la aplicación WinINet

Considere la posibilidad de migrar la aplicación WinINet a WinHTTP si la aplicación se beneficiaría de:

-   Una pila de cliente HTTP segura para el servidor.
-   Uso minimizado de la pila.
-   Escalabilidad de una aplicación de servidor.
-   Menos dependencias en las API relacionadas con la plataforma.
-   Compatibilidad con la suplantación de subprocesos.
-   Pila HTTP fácil de atender.
-   Acceso al objeto [**WinHttpRequest**](winhttprequest.md) que admite scripts.

No considere la posibilidad de migrar la aplicación WinINet a WinHTTP si debe ser compatible con uno o varios de los siguientes elementos:

-   El protocolo FTP o Gopher de la pila HTTP.
-   Compatibilidad con el protocolo SOCKSv4 para comunicarse con servidores proxy SOCKS.
-   Servicios de acceso telefónico automáticos.

Si decide migrar la aplicación a WinHTTP, las siguientes secciones le guiarán a través del proceso de conversión.

Para obtener una aplicación de ejemplo para WinINet y WinHTTP, compare el ejemplo AsyncDemo de WinINet con el ejemplo AsyncDemo para WinHTTP.

## <a name="winhttp-equivalents-to-wininet-functions"></a>Equivalentes de WinHTTP a funciones WinINet

En la tabla siguiente se enumeran las funciones de WinINet relacionadas con la pila de cliente HTTP junto con los equivalentes de WinHTTP.

Si la aplicación requiere funciones WinINet que no aparecen en la lista, no lleve la aplicación a WinHTTP.



| Función WinINet                                                       | Equivalente de WinHTTP                                                                                                                                                                                     | Cambios importantes                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HttpAddRequestHeaders**](/windows/desktop/api/wininet/nf-wininet-httpaddrequestheadersa)             | [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                                                                                                                                           | Ninguno.                                                                                                                                                                                                                                                                                                                                |
| [**HttpEndRequest**](/windows/desktop/api/wininet/nf-wininet-httpendrequesta)                           | [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)                                                                                                                                               | El valor de contexto se establece con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Las opciones de solicitud se establecen con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). Se debe llamar a [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) después de enviar una solicitud.                      |
| [**HttpOpenRequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta)                         | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                                                                                       | El valor de contexto se establece con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).                                                                                                                                                                                                      |
| [**HttpQueryInfo**](/windows/desktop/api/wininet/nf-wininet-httpqueryinfoa)                             | [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)                                                                                                                                                     | Ninguno.                                                                                                                                                                                                                                                                                                                                |
| [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta)                         | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | El valor de contexto se puede establecer con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).                                                                                                                                                                                                                                                  |
| [**HttpSendRequestEx**](/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa)                     | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | No se pueden proporcionar búferes.                                                                                                                                                                                                                                                                                                          |
| [**InternetCanonicalizeUrl**](/windows/desktop/api/wininet/nf-wininet-internetcanonicalizeurla)         | No equivalente                                                                                                                                                                                          | Las direcciones URL ahora se colocan en formato canónico en [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).                                                                                                                                                                                                                                              |
| [**InternetCheckConnection**](/windows/desktop/api/wininet/nf-wininet-internetcheckconnectiona)         | No equivalente                                                                                                                                                                                          | No se implementa en WinHTTP.                                                                                                                                                                                                                                                                                                          |
| [**InternetCloseHandle**](/windows/desktop/api/wininet/nf-wininet-internetclosehandle)                 | [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)                                                                                                                                                       | Al cerrar un identificador primario en WinHTTP no se cierran de forma recursiva los identificadores secundarios.                                                                                                                                                                                                                                                         |
| [**InternetCombineUrl**](/windows/desktop/api/wininet/nf-wininet-internetcombineurla)                   | No equivalente                                                                                                                                                                                          | Las direcciones URL se pueden ensamblar con la función [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) .                                                                                                                                                                                                                                                |
| [**InternetConfirmZoneCrossing**](/windows/desktop/api/wininet/nf-wininet-internetconfirmzonecrossing) | No equivalente                                                                                                                                                                                          | No se implementa en WinHTTP.                                                                                                                                                                                                                                                                                                          |
| [**InternetConnect**](/windows/desktop/api/wininet/nf-wininet-internetconnecta)                         | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                                                                                               | El valor de contexto se establece con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Las opciones de solicitud se establecen con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). Las credenciales de usuario se establecen con [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).                                 |
| [**InternetCrackUrl**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla)                       | [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)                                                                                                                                                             | Comportamiento opuesto de la marca de escape de ICU \_ : con [**InternetCrackUrl**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla), esta marca hace que las secuencias de escape (% XX) se conviertan en caracteres, pero con [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl), hace que los caracteres que se deben escapar de una solicitud HTTP se conviertan en secuencias de escape. |
| [**InternetCreateUrl**](/windows/desktop/api/wininet/nf-wininet-internetcreateurla)                     | [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)                                                                                                                                                           | Ninguno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetErrorDlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg)                       | No equivalente                                                                                                                                                                                          | Dado que WinHTTP está destinado a aplicaciones del lado servidor, no implementa ninguna interfaz de usuario.                                                                                                                                                                                                                                   |
| [**InternetGetCookie**](/windows/desktop/api/wininet/nf-wininet-internetgetcookiea)                     | No equivalente                                                                                                                                                                                          | WinHTTP no conserva los datos entre sesiones y no puede tener acceso a las cookies de WinINet.                                                                                                                                                                                                                                                    |
| [**InternetOpen**](/windows/desktop/api/wininet/nf-wininet-internetopena)                               | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                                                                                     | Ninguno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetOpenUrl**](/windows/desktop/api/wininet/nf-wininet-internetopenurla)                         | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect), [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) | Esta funcionalidad está disponible en las funciones WinHTTP enumeradas.                                                                                                                                                                                                                                                                     |
| [**InternetQueryDataAvailable**](/windows/desktop/api/wininet/nf-wininet-internetquerydataavailable)   | [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)                                                                                                                                         | No hay parámetros reservados.                                                                                                                                                                                                                                                                                                              |
| [**InternetQueryOption**](/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona)                 | [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)                                                                                                                                                       | WinHTTP ofrece un conjunto diferente de opciones de WinINet. Para obtener más información y las opciones que ofrece WinHTTP, vea [**marcas de opciones**](option-flags.md).                                                                                                                                                                               |
| [**InternetReadFile**](/windows/desktop/api/wininet/nf-wininet-internetreadfile)                       | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | Ninguno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetReadFileEx**](/windows/desktop/api/wininet/nf-wininet-internetreadfileexa)                   | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | En lugar de una estructura, el búfer es una región de memoria direccionada con un puntero.                                                                                                                                                                                                                                                  |
| [**InternetSetOption**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona)                     | [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)                                                                                                                                                           | Ninguno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetSetStatusCallback**](/windows/desktop/api/wininet/nf-wininet-internetsetstatuscallback)     | [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)                                                                                                                                           | Para obtener más información, vea el tema sobre el control diferente de las solicitudes asincrónicas en este tema.                                                                                                                                                                                                                                               |
| [**InternetTimeFromSystemTime**](/windows/desktop/api/wininet/nf-wininet-internettimefromsystemtime)   | [**WinHttpTimeFromSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)                                                                                                                                         | Ninguno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetTimeToSystemTime**](/windows/desktop/api/wininet/nf-wininet-internettimetosystemtime)       | [**WinHttpTimeToSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)                                                                                                                                             | Ninguno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetWriteFile**](/windows/desktop/api/wininet/nf-wininet-internetwritefile)                     | [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)                                                                                                                                                           | Ninguno.                                                                                                                                                                                                                                                                                                                                |



 

## <a name="different-handling-of-asynchronous-requests"></a>Control diferente de las solicitudes asincrónicas

Tenga en cuenta que en WinINet y WinHTTP, algunas funciones pueden completar solicitudes asincrónicas de forma sincrónica o asincrónica. La aplicación debe controlar cualquiera de las situaciones. Hay diferencias significativas en cómo WinINet y WinHTTP controlan estas funciones potencialmente asincrónicas.

WinINet

-   Finalización sincrónica: Si una llamada a una función de WinINet potencialmente asincrónica se completa sincrónicamente, los parámetros de salida de la función devuelven los resultados de la operación. Cuando se produce un error, recupere el código de error llamando a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) después de la llamada a la función Wininet.

-   Finalización asincrónica: Si una llamada a una función potencialmente asincrónica se completa de forma asincrónica, los resultados de la operación y los errores se pueden obtener en la función de devolución de llamada. La función de devolución de llamada se ejecuta en un subproceso de trabajo, no en el subproceso que realizó la llamada de función inicial.

En otras palabras, la aplicación debe duplicar la lógica para controlar los resultados de estas operaciones en dos lugares: inmediatamente después de la llamada de función y en la función de devolución de llamada.

WinHTTP simplifica este modelo, ya que permite implementar la lógica operativa solo en la función de devolución de llamada, que recibe una notificación de finalización independientemente de si la operación se completó de forma sincrónica o asincrónica. Cuando se habilita la operación asincrónica, los parámetros OUT de las funciones WinHTTP no devuelven datos significativos y deben establecerse en **null**.

La única diferencia significativa entre la finalización asincrónica y sincrónica en WinHTTP, desde la perspectiva de la aplicación, es donde se ejecuta la función de devolución de llamada.

WinHTTP

-   Finalización sincrónica: cuando una operación se completa de forma sincrónica, los resultados se devuelven en una función de devolución de llamada que se ejecuta en el mismo subproceso que la llamada de función original.

-   Finalización asincrónica: cuando una operación se completa de forma asincrónica, los resultados se devuelven en una función de devolución de llamada que se ejecuta en un subproceso de trabajo.

Aunque la mayoría de los errores también se pueden controlar por completo dentro de la función de devolución de llamada, las aplicaciones WinHTTP deben estar preparadas para que una función devuelva **false** debido a un error de \_ parámetro no válido \_ u otro error similar recuperado mediante una llamada a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

A diferencia de WinINet, que puede ejecutar varias operaciones asincrónicas simultáneamente, WinHTTP aplica una directiva de una operación asincrónica pendiente por identificador de solicitud. Si una operación está pendiente y se llama a otra función de WinHTTP, se produce un error en la segunda función y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error de \_ operación no válida \_ .

WinHTTP simplifica este modelo, ya que permite implementar la lógica operativa solo en la función de devolución de llamada, que recibe una notificación de finalización independientemente de si la operación se completó de forma sincrónica o asincrónica. Cuando se habilita la operación asincrónica, los parámetros OUT de las funciones WinHTTP no devuelven datos significativos y deben establecerse en **null**.

## <a name="differences-in-winhttp-callback-notifications"></a>Diferencias en las notificaciones de devolución de llamada de WinHTTP

La función de devolución de llamada de estado recibe actualizaciones sobre el estado de las operaciones a través de marcas de notificación. En WinHTTP, las notificaciones se seleccionan mediante el parámetro *dwNotificationFlags* de la función [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) . Use la marca de **\_ devolución de llamada WinHTTP \_ marca todas las \_ \_ notificaciones** para recibir notificaciones de todas las actualizaciones de estado.

Las notificaciones que indican que se ha completado una operación determinada se denominan notificaciones de finalización o simplemente finalizaciones. En WinINet, cada vez que la función de devolución de llamada recibe una finalización, el parámetro *lpvStatusInformation* contiene una estructura de [**\_ \_ resultados asincrónica de Internet**](/windows/desktop/api/wininet/ns-wininet-internet_async_result) . En WinHTTP, esta estructura no está disponible para todas las finalizaciones. Es importante revisar la página de referencia de la [**\_ devolución de \_ llamada de estado de WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback), que contiene información sobre las notificaciones y el tipo de datos que se puede esperar para cada uno.

En WinHTTP, un **error de solicitud de \_ Estado de devolución de llamada \_ \_ \_ de WinHTTP**, una sola finalización, indica que se produjo un error en una operación. Todas las demás finalizaciones indican una operación correcta.

Tanto WinINet como WinHTTP usan un valor de contexto definido por el usuario para pasar información del subproceso principal a la función de devolución de llamada de estado, que se puede ejecutar en un subproceso de trabajo. En WinINet, el valor de contexto utilizado por la función de devolución de llamada de estado se establece mediante una llamada a una de varias funciones. En WinHTTP, el valor de contexto se establece solo con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Debido a esto, es posible que se produzca una notificación antes de que se establezca un valor de contexto en WinHTTP. Si la función de devolución de llamada recibe una notificación antes de que se establezca el valor de contexto, la aplicación debe estar preparada para recibir **null** en el parámetro *dwContext* de la función de devolución de llamada.

## <a name="authentication-differences"></a>Diferencias de autenticación

En WinINet, las credenciales de usuario se establecen mediante una llamada a la función [**InternetSetOption**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona) , con código similar al que se proporciona en el ejemplo de código siguiente.

``` syntax
// Use the WinINet InternetSetOption function to set the 
// user credentials to the user name contained in strUsername 
// and the password to the contents of strPassword.
       
InternetSetOption( hRequest, INTERNET_OPTION_PROXY_USERNAME, 
                   strUsername, strlen(strUsername) + 1 );

InternetSetOption( hRequest, INTERNET_OPTION_PROXY_PASSWORD, 
                   strPassword, strlen(strPassword) + 1 );
```

Por compatibilidad, las credenciales de usuario se pueden establecer de forma similar en WinHTTP mediante la función [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , pero esto no se recomienda porque puede suponer una vulnerabilidad de seguridad.

En su lugar, cuando una aplicación recibe un código de estado 401 en WinHTTP, el método recomendado para establecer credenciales es primero identificar un esquema de autenticación mediante [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) y, en segundo lugar, establecer las credenciales con [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials). En el ejemplo de código siguiente se muestra cómo hacerlo.

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

WinHTTP no admite el esquema de autenticación de contraseña distribuida (DPA) compatible con WinINet. Sin embargo, WinHTTP no admite Microsoft Passport 1,4. Para obtener más información acerca del uso de la autenticación de Passport en WinHTTP, consulte [autenticación de Passport en WinHTTP](passport-authentication-in-winhttp.md).

WinHTTP no depende de la configuración de Internet Explorer para determinar la Directiva de inicio de sesión automático. En su lugar, la Directiva de inicio de sesión automático se establece con [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Para obtener más información acerca de la autenticación en WinHTTP, incluida la Directiva de inicio de sesión automático, consulte [autenticación en WinHTTP](authentication-in-winhttp.md).

## <a name="differences-in-secure-http-transactions"></a>Diferencias en las transacciones HTTP seguras

En WinINet, inicie una sesión segura con [**HttpOpenRequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta) o [**InternetConnect**](/windows/desktop/api/wininet/nf-wininet-internetconnecta), pero en WinHTTP, debe llamar a [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) mediante la marca **de \_ \_ seguridad de marca WinHTTP** .

En una transacción HTTP segura, los certificados de servidor se pueden usar para autenticar un servidor en el cliente. En WinINet, si un certificado de servidor contiene errores, [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta) produce un error y proporciona detalles sobre los errores de certificado.

En WinHttp, los errores de certificado de servidor se administran según la versión de la siguiente manera:

-   A partir de WinHttp 5,1, si se produce un error en un certificado de servidor o contiene errores, la llamada a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) notifica un error de protección de **Estado de devolución de \_ llamada \_ \_ \_ de WinHTTP** en la función de devolución de llamada. Si se omite el error generado por **WinHttpSendRequest** , las llamadas posteriores a [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) producirán un error en la \_ \_ operación WinHTTP \_ cancelada.
-   En WinHTTP 5,0, los errores en los certificados de servidor no hacen que se produzca un error en una solicitud. En su lugar, los errores se notifican en la función de devolución de llamada con la notificación de **\_ \_ \_ \_ error seguro de estado de devolución de llamada de WinHTTP** .

En algunas plataformas anteriores, WinINet admitía los protocolos de tecnología de comunicaciones privada (PCT) y/o Fortezza, aunque no en Windows XP.

WinHTTP no admite los protocolos PCT y Fortezza en ninguna plataforma y, en su lugar, se basa en Capa de sockets seguros (SSL) 2,0, SSL 3,0 o la seguridad de la capa de transporte (TLS) 1,0.

 

 

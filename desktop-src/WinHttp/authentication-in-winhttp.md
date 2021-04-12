---
description: Algunos servidores HTTP y proxies requieren autenticación antes de permitir el acceso a los recursos de Internet. Las funciones de los servicios HTTP de Microsoft Windows (WinHTTP) admiten la autenticación de servidor y proxy para las sesiones HTTP.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Autenticación en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dd40e6da1f455e04e24fa740cf4d83da7e0472e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276978"
---
# <a name="authentication-in-winhttp"></a>Autenticación en WinHTTP

Algunos servidores HTTP y proxies requieren autenticación antes de permitir el acceso a los recursos de Internet. Las funciones de los servicios HTTP de Microsoft Windows (WinHTTP) admiten la autenticación de servidor y proxy para las sesiones HTTP.

## <a name="about-http-authentication"></a>Acerca de la autenticación HTTP

Si se requiere autenticación, la aplicación HTTP recibe un código de estado 401 (el servidor requiere autenticación) o 407 (el proxy requiere autenticación). Junto con el código de estado, el proxy o servidor envía uno o más encabezados de autenticación: WWW-Authenticate (para la autenticación de servidor) o Proxy-Authenticate (para la autenticación de proxy).

Cada encabezado Authenticate contiene un esquema de autenticación compatible y, para los esquemas básico y de Resumen, un dominio Kerberos. Si se admiten varios esquemas de autenticación, el servidor devuelve varios encabezados de autenticación. El valor de dominio Kerberos distingue entre mayúsculas y minúsculas y define un conjunto de servidores o servidores proxy para los que se aceptan las mismas credenciales. Por ejemplo, el encabezado "WWW-Authenticate: Basic realm =" example "" podría devolverse cuando se requiere la autenticación del servidor. Este encabezado especifica que se deben proporcionar las credenciales del usuario para el dominio "example".

Una aplicación HTTP puede incluir un campo de encabezado de autorización con una solicitud que envía al servidor. El encabezado Authorization contiene el esquema de autenticación y la respuesta adecuada que requiere dicho esquema. Por ejemplo, el encabezado "Authorization: Basic <username: password>" se agregaría a la solicitud y se enviará al servidor si el cliente recibió el encabezado de respuesta "WWW-Authenticate: Basic realm =" example "".

> [!Note]  
> Aunque se muestran aquí como texto sin formato, el nombre de usuario y la contraseña están [*codificados en Base64*](glossary.md).

 

Hay dos tipos generales de esquemas de autenticación:

-   Esquema de autenticación básica, en el que el nombre de usuario y la contraseña se envían en texto no cifrado al servidor.

    El esquema de autenticación básica se basa en el modelo que un cliente debe identificarse con un nombre de usuario y una contraseña para cada dominio Kerberos. El servidor solo da servicio a la solicitud si la solicitud se envía con un encabezado de autorización que incluye un nombre de usuario y una contraseña válidos.

-   Esquemas de desafío-respuesta, como Kerberos, en los que el servidor desafía el cliente con los [*datos de autenticación*](glossary.md). El cliente transforma los datos con las credenciales de usuario y envía los datos transformados de nuevo al servidor para la autenticación.

    Los esquemas de desafío-respuesta permiten una autenticación más segura. En un esquema de desafío-respuesta, el nombre de usuario y la contraseña nunca se transmiten a través de la red. Una vez que el cliente selecciona un esquema de desafío-respuesta, el servidor devuelve un código de estado adecuado con un desafío que contiene los [*datos de autenticación*](glossary.md) de ese esquema. Después, el cliente vuelve a enviar la solicitud con la respuesta adecuada para obtener el servicio solicitado. Los esquemas de desafío-respuesta pueden tardar varios intercambios en completarse.

La tabla siguiente contiene los esquemas de autenticación que son compatibles con WinHTTP, el tipo de autenticación y una descripción del esquema.



| Scheme            | Tipo               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Básico (texto sin formato) | Básico              | Utiliza una cadena [*codificada en Base64*](glossary.md) que contiene el nombre de usuario y la contraseña.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Digest            | Desafío-respuesta | Desafíos del uso de un valor de nonce (cadena de datos especificada por el servidor). Una respuesta válida contiene una suma de comprobación del nombre de usuario, la contraseña, el valor de nonce dado, el [*verbo http*](glossary.md)y el identificador uniforme de recursos (URI) solicitado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| NTLM              | Desafío-respuesta | Requiere que los [*datos de autenticación*](glossary.md) se transformen con las credenciales de usuario para demostrar la identidad. Para que la autenticación NTLM funcione correctamente, se deben realizar varios intercambios en la misma conexión. Por lo tanto, no se puede usar la autenticación NTLM si un proxy intermedio no admite conexiones persistentes. También se produce un error en la autenticación NTLM si se usa [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la marca de mantenimiento de conexión de [**WinHTTP \_ deshabilitar \_ \_**](option-flags.md) , que deshabilita la semántica Keep-Alive.                                                                                                                                                                                                                                       |
| Passport          | Desafío-respuesta | Utiliza [Microsoft Passport 1,4](passport-authentication-in-winhttp.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Negotiate         | Desafío-respuesta | Si el servidor y el cliente usan Windows 2000 o una versión posterior, se usa la autenticación Kerberos. En caso contrario, se usa la autenticación NTLM. Kerberos está disponible en Windows 2000 y en sistemas operativos posteriores y se considera que es más seguro que la autenticación NTLM. Para que la autenticación Negotiate funcione correctamente, se deben realizar varios intercambios en la misma conexión. Por lo tanto, no se puede usar negociar autenticación si un proxy intermedio no admite conexiones persistentes. También se produce un error en la autenticación Negotiate si se usa [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la marca de mantenimiento de conexión de [**WinHTTP \_ deshabilitar \_ \_**](option-flags.md) que deshabilita la semántica Keep-Alive. El esquema de autenticación Negotiate se denomina a veces autenticación integrada de Windows. |



 

## <a name="authentication-in-winhttp-applications"></a>Autenticación en aplicaciones WinHTTP

La interfaz de programación de aplicaciones (API) de WinHTTP proporciona dos funciones que se usan para tener acceso a recursos de Internet en situaciones en las que se requiere autenticación: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) y [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).

Cuando se recibe una respuesta con un código de estado 401 o 407, [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) se puede usar para analizar los encabezados de autenticación con el fin de determinar los esquemas de autenticación admitidos y el destino de autenticación. El destino de autenticación es el servidor o proxy que solicita la autenticación. **WinHttpQueryAuthSchemes** también determina el primer esquema de autenticación, de los esquemas disponibles, en función de las preferencias de esquema de autenticación sugeridas por el servidor. Este método para elegir un esquema de autenticación es el que sugiere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) permite que una aplicación especifique el esquema de autenticación que se usa junto con un nombre de usuario y contraseña válidos para su uso en el servidor proxy o el servidor de destino. Después de establecer las credenciales y volver a enviar la solicitud, se generan los encabezados necesarios y se agregan automáticamente a la solicitud. Dado que algunos esquemas de autenticación requieren varias transacciones, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) podría devolver el ERROR, error de \_ solicitud de \_ reenvío de WinHTTP \_ . Cuando se encuentra este error, la aplicación debe continuar reenviando la solicitud hasta que se reciba una respuesta que no contenga un código de estado 401 o 407. Un código de estado 200 indica que el recurso está disponible y que la solicitud se ha realizado correctamente. Consulte [**códigos de estado http**](http-status-codes.md) para ver otros códigos de estado que se pueden devolver.

Si se conocen un esquema de autenticación aceptable y las credenciales antes de que se envíe una solicitud al servidor, una aplicación puede llamar a [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) antes de llamar a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). En este caso, WinHTTP intenta la autenticación previa con el servidor proporcionando credenciales o [*datos de autenticación*](glossary.md) en la solicitud inicial al servidor. La autenticación previa puede reducir el número de intercambios en el proceso de autenticación y, por tanto, mejorar el rendimiento de la aplicación.

La autenticación previa se puede usar con los esquemas de autenticación siguientes:

-   Básica: siempre es posible.
-   Negocie la resolución en Kerberos. es muy probable que sea posible; la única excepción es cuando los sesgos temporales se desconectan entre el cliente y el controlador de dominio.
-   (Negociar la resolución en NTLM): nunca es posible.
-   NTLM: solo es posible en Windows Server 2008 R2.
-   Digest: nunca es posible.
-   Passport: nunca es posible; después de la respuesta de desafío inicial, WinHTTP usa las cookies para realizar la autenticación previa en Passport.

Una aplicación WinHTTP típica completa los pasos siguientes para controlar la autenticación.

-   Solicite un recurso con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) y [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).
-   Compruebe los encabezados de respuesta con [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).
-   Si se devuelve un código de estado 401 o 407 que indica que se requiere autenticación, llame a [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) para buscar un esquema aceptable.
-   Establezca el esquema de autenticación, el nombre de usuario y la contraseña con [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).
-   Vuelva a enviar la solicitud con el mismo identificador de solicitud mediante una llamada a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).

Las credenciales establecidas por [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) solo se usan para una solicitud. WinHTTP no almacena en caché las credenciales para usarlas en otras solicitudes, lo que significa que se deben escribir las aplicaciones que pueden responder a varias solicitudes. Si se vuelve a usar una conexión autenticada, es posible que no se realicen desafíos en otras solicitudes, pero el código debe ser capaz de responder a una solicitud en cualquier momento.

### <a name="example-retrieving-a-document"></a>Ejemplo: recuperar un documento

En el código de ejemplo siguiente se intenta recuperar un documento especificado de un servidor HTTP. El código de estado se recupera de la respuesta para determinar si se requiere autenticación. Si se encuentra un código de estado 200, el documento está disponible. Si se encuentra un código de estado 401 o 407, se requiere autenticación antes de poder recuperar el documento. Para cualquier otro código de estado, se muestra un mensaje de error. Consulte [**códigos de estado http**](http-status-codes.md) para obtener una lista de posibles códigos de estado.


```C++
#include <windows.h>
#include <winhttp.h>
#include <stdio.h>

#pragma comment(lib, "winhttp.lib")

DWORD ChooseAuthScheme( DWORD dwSupportedSchemes )
{
  //  It is the server's responsibility only to accept 
  //  authentication schemes that provide a sufficient
  //  level of security to protect the servers resources.
  //
  //  The client is also obligated only to use an authentication
  //  scheme that adequately protects its username and password.
  //
  //  Thus, this sample code does not use Basic authentication  
  //  becaus Basic authentication exposes the client's username
  //  and password to anyone monitoring the connection.
  
  if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NEGOTIATE )
    return WINHTTP_AUTH_SCHEME_NEGOTIATE;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NTLM )
    return WINHTTP_AUTH_SCHEME_NTLM;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_PASSPORT )
    return WINHTTP_AUTH_SCHEME_PASSPORT;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_DIGEST )
    return WINHTTP_AUTH_SCHEME_DIGEST;
  else
    return 0;
}

struct SWinHttpSampleGet
{
  LPCWSTR szServer;
  LPCWSTR szPath;
  BOOL fUseSSL;
  LPCWSTR szServerUsername;
  LPCWSTR szServerPassword;
  LPCWSTR szProxyUsername;
  LPCWSTR szProxyPassword;
};

void WinHttpAuthSample( IN SWinHttpSampleGet *pGetRequest )
{
  DWORD dwStatusCode = 0;
  DWORD dwSupportedSchemes;
  DWORD dwFirstScheme;
  DWORD dwSelectedScheme;
  DWORD dwTarget;
  DWORD dwLastStatus = 0;
  DWORD dwSize = sizeof(DWORD);
  BOOL  bResults = FALSE;
  BOOL  bDone = FALSE;

  DWORD dwProxyAuthScheme = 0;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  INTERNET_PORT nPort = ( pGetRequest->fUseSSL ) ? 
                        INTERNET_DEFAULT_HTTPS_PORT  :
                        INTERNET_DEFAULT_HTTP_PORT;

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, 
                               pGetRequest->szServer, 
                               nPort, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, 
                                   L"GET", 
                                   pGetRequest->szPath,
                                   NULL, 
                                   WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES,
                                   ( pGetRequest->fUseSSL ) ? 
                                       WINHTTP_FLAG_SECURE : 0 );

  // Continue to send a request until status code 
  // is not 401 or 407.
  if( hRequest == NULL )
    bDone = TRUE;

  while( !bDone )
  {
    //  If a proxy authentication challenge was responded to, reset
    //  those credentials before each SendRequest, because the proxy  
    //  may require re-authentication after responding to a 401 or  
    //  to a redirect. If you don't, you can get into a 
    //  407-401-407-401- loop.
    if( dwProxyAuthScheme != 0 )
      bResults = WinHttpSetCredentials( hRequest, 
                                        WINHTTP_AUTH_TARGET_PROXY, 
                                        dwProxyAuthScheme, 
                                        pGetRequest->szProxyUsername,
                                        pGetRequest->szProxyPassword,
                                        NULL );
    // Send a request.
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS,
                                   0,
                                   WINHTTP_NO_REQUEST_DATA,
                                   0, 
                                   0, 
                                   0 );

    // End the request.
    if( bResults )
      bResults = WinHttpReceiveResponse( hRequest, NULL );

    // Resend the request in case of 
    // ERROR_WINHTTP_RESEND_REQUEST error.
    if( !bResults && GetLastError( ) == ERROR_WINHTTP_RESEND_REQUEST)
        continue;

    // Check the status code.
    if( bResults ) 
      bResults = WinHttpQueryHeaders( hRequest, 
                                      WINHTTP_QUERY_STATUS_CODE |
                                      WINHTTP_QUERY_FLAG_NUMBER,
                                      NULL, 
                                      &dwStatusCode, 
                                      &dwSize, 
                                      NULL );

    if( bResults )
    {
      switch( dwStatusCode )
      {
        case 200: 
          // The resource was successfully retrieved.
          // You can use WinHttpReadData to read the 
          // contents of the server's response.
          printf( "The resource was successfully retrieved.\n" );
          bDone = TRUE;
          break;

        case 401:
          // The server requires authentication.
          printf(" The server requires authentication. Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
          {
            dwSelectedScheme = ChooseAuthScheme( dwSupportedSchemes);

            if( dwSelectedScheme == 0 )
              bDone = TRUE;
            else
              bResults = WinHttpSetCredentials( hRequest, 
                                        dwTarget, 
                                        dwSelectedScheme,
                                        pGetRequest->szServerUsername,
                                        pGetRequest->szServerPassword,
                                        NULL );
          }

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check
          // for a repeated sequence of status codes.
          if( dwLastStatus == 401 )
            bDone = TRUE;

          break;

        case 407:
          // The proxy requires authentication.
          printf( "The proxy requires authentication.  Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
            dwProxyAuthScheme = ChooseAuthScheme(dwSupportedSchemes);

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check 
          // for a repeated sequence of status codes.
          if( dwLastStatus == 407 )
            bDone = TRUE;
          break;

        default:
          // The status code does not indicate success.
          printf("Error. Status code %d returned.\n", dwStatusCode);
          bDone = TRUE;
      }
    }

    // Keep track of the last status code.
    dwLastStatus = dwStatusCode;

    // If there are any errors, break out of the loop.
    if( !bResults ) 
        bDone = TRUE;
  }

  // Report any errors.
  if( !bResults )
  {
    DWORD dwLastError = GetLastError( );
    printf( "Error %d has occurred.\n", dwLastError );
  }

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
}

```



## <a name="automatic-logon-policy"></a>Directiva de inicio de sesión automático

La Directiva de inicio de sesión automático (inicio de sesión automático) determina cuándo es aceptable que WinHTTP incluya las credenciales predeterminadas en una solicitud. Las credenciales predeterminadas son el token de subproceso actual o el token de sesión, dependiendo de si se usa WinHTTP en modo sincrónico o asincrónico. El token de subproceso se usa en modo sincrónico y el token de sesión se utiliza en modo asincrónico. Estas credenciales predeterminadas suelen ser el nombre de usuario y la contraseña usados para iniciar sesión en Microsoft Windows.

La Directiva de inicio de sesión automático se implementó para impedir que estas credenciales se utilicen de forma ocasional para autenticarse en un servidor que no es de confianza. De forma predeterminada, el nivel de seguridad se establece en \_ nivel de seguridad de inicio de sesión automático de WinHTTP \_ \_ \_ , lo que permite usar las credenciales predeterminadas solo para las solicitudes de la intranet. La Directiva de inicio de sesión automático solo se aplica a los esquemas de autenticación NTLM y Negotiate. Las credenciales nunca se transmiten automáticamente con otros esquemas.

La Directiva de inicio de sesión automático se puede establecer mediante la función [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la opción WinHTTP de la marca de [**\_ \_ \_ Directiva de inicio**](option-flags.md) de sesión automático. Esta marca solo se aplica al identificador de la solicitud. Cuando la Directiva se establece en el \_ nivel de seguridad de inicio de sesión automático de WinHTTP \_ , se \_ \_ pueden enviar credenciales predeterminadas a todos los servidores. Cuando la Directiva se establece en el \_ nivel de seguridad de inicio de sesión automático de WinHTTP \_ \_ \_ alto, las credenciales predeterminadas no se pueden usar para la autenticación. Se recomienda encarecidamente que use el inicio de sesión automático en el nivel medio.

## <a name="stored-user-names-and-passwords"></a>Nombres de usuarios y contraseñas almacenados

Windows XP presentó el concepto de nombres de usuario y contraseñas almacenados. Si las credenciales de Passport de un usuario se guardan mediante el **Asistente para registro de Passport** o el **cuadro de diálogo credencial** estándar, se guardan en los nombres de usuario y contraseñas almacenados. Al usar WinHTTP en Windows XP o versiones posteriores, WinHTTP usa automáticamente las credenciales en los nombres de usuario y contraseñas almacenados si no se establecen explícitamente las credenciales. Esto es similar a la compatibilidad con las credenciales de inicio de sesión predeterminadas para NTLM/Kerberos. Sin embargo, el uso de las credenciales predeterminadas de Passport no está sujeto a la configuración de la Directiva de inicio de sesión automático.

 

 




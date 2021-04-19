---
description: Algunos servidores HTTP y servidores proxy requieren autenticación antes de permitir el acceso a los recursos en Internet. Las funciones de servicios HTTP de Microsoft Windows (WinHTTP) admiten la autenticación de servidor y proxy para sesiones HTTP.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Autenticación en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75c6703e9d28902c5705f0b8ab8433193c4d085
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380831"
---
# <a name="authentication-in-winhttp"></a>Autenticación en WinHTTP

Algunos servidores HTTP y servidores proxy requieren autenticación antes de permitir el acceso a los recursos en Internet. Las funciones de servicios HTTP de Microsoft Windows (WinHTTP) admiten la autenticación de servidor y proxy para sesiones HTTP.

## <a name="about-http-authentication"></a>Acerca de la autenticación HTTP

Si se requiere autenticación, la aplicación HTTP recibe un código de estado 401 (el servidor requiere autenticación) o 407 (el proxy requiere autenticación). Junto con el código de estado, el servidor o proxy envía uno o varios encabezados de autenticación: WWW-Authenticate (para la autenticación del servidor) o Proxy-Authenticate (para la autenticación de proxy).

Cada encabezado de autenticación contiene un esquema de autenticación compatible y, para los esquemas Básico e Implícita, un dominio kerberos. Si se admiten varios esquemas de autenticación, el servidor devuelve varios encabezados de autenticación. El valor de dominio kerberos distingue mayúsculas de minúsculas y define un conjunto de servidores o servidores proxy para los que se aceptan las mismas credenciales. Por ejemplo, el encabezado "WWW-Authenticate: Basic Realm="example" podría devolverse cuando se requiere la autenticación del servidor. Este encabezado especifica que se deben proporcionar credenciales de usuario para el dominio "ejemplo".

Una aplicación HTTP puede incluir un campo de encabezado de autorización con una solicitud que envía al servidor. El encabezado de autorización contiene el esquema de autenticación y la respuesta adecuada requerida por ese esquema. Por ejemplo, el encabezado "Authorization: Basic" se agregaría a la solicitud y se enviaría al servidor si el cliente recibió el encabezado de respuesta \<username:password> "WWW-Authenticate: Basic Realm="example"".

> [!Note]  
> Aunque se muestran aquí como texto sin formato, el nombre de usuario y la contraseña están [*codificados en base64.*](glossary.md)

 

Hay dos tipos generales de esquemas de autenticación:

-   Esquema de autenticación básico, en el que el nombre de usuario y la contraseña se envían sin formato al servidor.

    El esquema de autenticación básica se basa en el modelo que un cliente debe identificarse con un nombre de usuario y una contraseña para cada dominio. El servidor solo proporciona servicios a la solicitud si la solicitud se envía con un encabezado de autorización que incluye un nombre de usuario y una contraseña válidos.

-   Esquemas de desafío-respuesta, como Kerberos, en los que el servidor reta al cliente con datos [*de autenticación*](glossary.md). El cliente transforma los datos con las credenciales de usuario y envía los datos transformados de vuelta al servidor para la autenticación.

    Los esquemas de desafío-respuesta permiten una autenticación más segura. En un esquema de desafío-respuesta, el nombre de usuario y la contraseña nunca se transmiten a través de la red. Una vez que el cliente selecciona un esquema de desafío-respuesta, el servidor devuelve un código de estado adecuado con un desafío que contiene los datos de [*autenticación*](glossary.md) para ese esquema. A continuación, el cliente vuelve a enviar la solicitud con la respuesta adecuada para obtener el servicio solicitado. Los esquemas de desafío-respuesta pueden tardar varios intercambios en completarse.

La tabla siguiente contiene los esquemas de autenticación admitidos por WinHTTP, el tipo de autenticación y una descripción del esquema.



| Scheme            | Tipo               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Básico (texto no cifrado) | Básico              | Usa una [*cadena codificada en base64*](glossary.md) que contiene el nombre de usuario y la contraseña.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Digest            | Desafío-respuesta | Desafíos al usar un valor nonce (una cadena de datos especificada por el servidor). Una respuesta válida contiene una suma de comprobación del nombre de usuario, la contraseña, el valor nonce especificado, el verbo [*HTTP*](glossary.md)y el identificador uniforme de recursos (URI) solicitado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| NTLM              | Desafío-respuesta | Requiere que los [*datos de autenticación*](glossary.md) se transformen con las credenciales de usuario para demostrar la identidad. Para que la autenticación NTLM funcione correctamente, deben realizarse varios intercambios en la misma conexión. Por lo tanto, no se puede usar la autenticación NTLM si un proxy que interviene no admite conexiones keep-alive. También se produce un error en la autenticación NTLM si se usa [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la marca [**WINHTTP \_ DISABLE KEEP \_ \_ ALIVE**](option-flags.md) que deshabilita la semántica de keep-alive.                                                                                                                                                                                                                                       |
| Passport          | Desafío-respuesta | Usa [Microsoft Passport 1.4](passport-authentication-in-winhttp.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Negotiate         | Desafío-respuesta | Si el servidor y el cliente usan Windows 2000 o posterior, se usa la autenticación Kerberos. De lo contrario, se usa la autenticación NTLM. Kerberos está disponible en sistemas operativos Windows 2000 y versiones posteriores y se considera más seguro que la autenticación NTLM. Para que la autenticación Negotiate funcione correctamente, deben realizarse varios intercambios en la misma conexión. Por lo tanto, no se puede usar la autenticación Negotiate si un proxy que interviene no admite conexiones de conexión continua. La autenticación negotiate también produce un error si se usa [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la marca [**WINHTTP \_ DISABLE KEEP \_ \_ ALIVE**](option-flags.md) que deshabilita la semántica de conexión continua. El esquema de autenticación Negotiate a veces se denomina Integrated autenticación de Windows. |



 

## <a name="authentication-in-winhttp-applications"></a>Autenticación en aplicaciones WinHTTP

La interfaz de programación de aplicaciones (API) WinHTTP proporciona dos funciones que se usan para acceder a los recursos de Internet en situaciones en las que se requiere autenticación: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) y [**WinHttpQueryAuthSchemes.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)

Cuando se recibe una respuesta con un código de estado 401 o 407, Se puede usar [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) para analizar los encabezados de autenticación para determinar los esquemas de autenticación admitidos y el destino de autenticación. El destino de autenticación es el servidor o proxy que solicita la autenticación. **WinHttpQueryAuthSchemes** también determina el primer esquema de autenticación, a partir de los esquemas disponibles, en función de las preferencias de esquema de autenticación sugeridas por el servidor. Este método para elegir un esquema de autenticación es el comportamiento sugerido por [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

[**WinHttpSetCredentials permite**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) a una aplicación especificar el esquema de autenticación que se usa junto con un nombre de usuario y una contraseña válidos para su uso en el servidor o proxy de destino. Después de establecer las credenciales y volver a enviar la solicitud, los encabezados necesarios se generan y se agregan a la solicitud automáticamente. Dado que algunos esquemas de autenticación requieren varias [**transacciones, WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) podría devolver el error, ERROR \_ WINHTTP \_ RESEND \_ REQUEST. Cuando se produce este error, la aplicación debe seguir reenendiendo la solicitud hasta que se reciba una respuesta que no contenga un código de estado 401 o 407. Un código de estado 200 indica que el recurso está disponible y la solicitud es correcta. Consulte [**Códigos de estado HTTP para**](http-status-codes.md) obtener códigos de estado adicionales que se pueden devolver.

Si se conocen un esquema de autenticación aceptable y las credenciales antes de enviar una solicitud al servidor, una aplicación puede llamar a [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) antes de llamar a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). En este caso, WinHTTP intenta la autenticación [](glossary.md) previa con el servidor proporcionando credenciales o datos de autenticación en la solicitud inicial al servidor. La autenticación previa puede reducir el número de intercambios en el proceso de autenticación y, por tanto, mejorar el rendimiento de la aplicación.

La autenticación previa se puede usar con los siguientes esquemas de autenticación:

-   Básico: siempre es posible.
-   Negociación de la resolución en Kerberos: es muy probable que sea posible. la única excepción es cuando los sesgos de tiempo están desactivados entre el cliente y el controlador de dominio.
-   (Negociar la resolución en NTLM): nunca es posible.
-   NTLM: solo es posible en Windows Server 2008 R2.
-   Implícita: nunca es posible.
-   Passport: nunca es posible; después del desafío-respuesta inicial, WinHTTP usa cookies para autenticarse previamente en Passport.

Una aplicación WinHTTP típica completa los pasos siguientes para controlar la autenticación.

-   Solicite un recurso con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) y [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
-   Compruebe los encabezados de respuesta [**con WinHttpQueryHeaders.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
-   Si se devuelve un código de estado 401 o 407 que indica que se requiere autenticación, llame a [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) para encontrar un esquema aceptable.
-   Establezca el esquema de autenticación, el nombre de usuario y la contraseña [**con WinHttpSetCredentials.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
-   Vuelva a enviar la solicitud con el mismo identificador de solicitud mediante una llamada [**a WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).

Las credenciales establecidas [**por WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) solo se usan para una solicitud. WinHTTP no almacena en caché las credenciales que se usarán en otras solicitudes, lo que significa que se deben escribir aplicaciones que puedan responder a varias solicitudes. Si se vuelve a usar una conexión autenticada, es posible que no se reta a otras solicitudes, pero el código debe poder responder a una solicitud en cualquier momento.

### <a name="example-retrieving-a-document"></a>Ejemplo: Recuperar un documento

El código de ejemplo siguiente intenta recuperar un documento especificado de un servidor HTTP. El código de estado se recupera de la respuesta para determinar si se requiere autenticación. Si se encuentra un código de estado 200, el documento está disponible. Si se encuentra un código de estado 401 o 407, se requiere autenticación para poder recuperar el documento. Para cualquier otro código de estado, se muestra un mensaje de error. Consulte [**Códigos de estado HTTP**](http-status-codes.md) para obtener una lista de posibles códigos de estado.


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

La directiva de inicio de sesión automático (inicio de sesión automático) determina cuándo es aceptable que WinHTTP incluya las credenciales predeterminadas en una solicitud. Las credenciales predeterminadas son el token de subproceso actual o el token de sesión en función de si WinHTTP se usa en modo sincrónico o asincrónico. El token de subproceso se usa en modo sincrónico y el token de sesión se usa en modo asincrónico. Estas credenciales predeterminadas suelen ser el nombre de usuario y la contraseña que se usan para iniciar sesión en Microsoft Windows.

La directiva de inicio de sesión automático se implementó para evitar que estas credenciales se usaran ocasionalmente para autenticarse en un servidor que no es de confianza. De forma predeterminada, el nivel de seguridad se establece en WINHTTP \_ AUTOLOGON SECURITY LEVEL MEDIUM, lo que permite usar las credenciales predeterminadas solo para las solicitudes \_ \_ de \_ intranet. La directiva de inicio de sesión automático solo se aplica a los esquemas de autenticación NTLM y Negotiate. Las credenciales nunca se transmiten automáticamente con otros esquemas.

La directiva de inicio de sesión automático se puede establecer mediante la [**función WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la [**marca WINHTTP OPTION \_ \_ AUTOLOGON \_ POLICY.**](option-flags.md) Esta marca solo se aplica al identificador de solicitud. Cuando la directiva se establece en WINHTTP AUTOLOGON SECURITY LEVEL LOW, las credenciales predeterminadas se pueden \_ enviar a todos los \_ \_ \_ servidores. Cuando la directiva se establece en WINHTTP AUTOLOGON SECURITY LEVEL HIGH, las credenciales predeterminadas \_ no se pueden usar para la \_ \_ \_ autenticación. Se recomienda encarecidamente usar el inicio de sesión automático en el nivel MEDIO.

## <a name="stored-user-names-and-passwords"></a>Nombres de usuarios y contraseñas almacenados

Windows XP introdujo el concepto de nombres de usuario y contraseñas almacenados. Si las credenciales de Passport de un usuario se guardan mediante el Asistente para registro de **Passport** o el cuadro de diálogo de credenciales estándar **,** se guarda en los nombres de usuario y contraseñas almacenados. Cuando se usa WinHTTP en Windows XP o versiones posteriores, WinHTTP usa automáticamente las credenciales de los nombres de usuario almacenados y contraseñas si las credenciales no se establecen explícitamente. Esto es similar a la compatibilidad con las credenciales de inicio de sesión predeterminadas para NTLM/Kerberos. Sin embargo, el uso de credenciales predeterminadas de Passport no está sujeto a la configuración de la directiva de inicio de sesión automático.

 

 




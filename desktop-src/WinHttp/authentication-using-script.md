---
description: En esta sección se muestra cómo escribir un script que use el objeto WinHttpRequest para tener acceso a los datos de un servidor que requiera autenticación HTTP.
ms.assetid: 9e46777c-4d79-4f9b-9b31-1280ed1e3289
title: Autenticación mediante script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1d33b8042cd1fd15d46e15dfb3624e0d3b4a885b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716129"
---
# <a name="authentication-using-script"></a>Autenticación mediante script

En esta sección se muestra cómo escribir un script que use el objeto [**WinHttpRequest**](winhttprequest.md) para tener acceso a los datos de un servidor que requiera autenticación http.

-   [Requisitos previos y requisitos](#prerequisites-and-requirements)
-   [Obtener acceso a un sitio web con autenticación](#accessing-a-web-site-with-authentication)
-   [Comprobación de los códigos de estado](#checking-the-status-codes)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites-and-requirements"></a>Requisitos previos y requisitos

Además de tener conocimientos prácticos de Microsoft JScript, este ejemplo requiere lo siguiente:

-   La versión actual del kit de desarrollo de software (SDK) de Microsoft Windows.
-   La herramienta de configuración de proxy para establecer la configuración de proxy para los servicios HTTP de Microsoft Windows (WinHTTP), si la conexión a Internet se realiza a través de un servidor proxy. Vea [Proxycfg.exe, una herramienta de configuración de proxy](proxycfg-exe--a-proxy-configuration-tool.md) para obtener más información.
-   Familiaridad con la [terminología](network-terminology.md) y los conceptos de la red.

## <a name="accessing-a-web-site-with-authentication"></a>Obtener acceso a un sitio web con autenticación

**Para crear un script que muestre la autenticación de, haga lo siguiente:**

1.  Abra un editor de texto como el Bloc de notas de Microsoft.
2.  Copie el código siguiente en el editor de texto después de reemplazar " \[ authenticationSite \] " con el texto adecuado para especificar la dirección URL de un sitio que requiere autenticación http.

    ```VB
    // Load the WinHttpRequest object.
    var WinHttpReq = 
              new ActiveXObject("WinHttp.WinHttpRequest.5.1");

    function getText1( )
    {
      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false;

      // Send a request to the server and wait for a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "No Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText);
      WScript.Echo( WinHttpReq.GetAllResponseHeaders);
      WScript.Echo( );
    };

    function getText2( )
    {
      // HttpRequest SetCredentials flags
      HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;

      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false );

      // Set credentials for server.
      WinHttpReq.SetCredentials( "User Name", 
                                 "Password",
                                 HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

      // It might also be necessary to supply credentials 
      // to the proxy if you connect to the Internet 
      // through a proxy that requires authentication.

      // Send a request to the server and wait for 
      // a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
      WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
      WScript.Echo( );
    };

    getText1( );
    getText2( );
    ```

    

3.  Guarde el archivo como "Auth.js".
4.  En un símbolo del sistema, escriba "cscript Auth.js" y presione Entrar.

Ahora tiene un programa que solicita un recurso de dos maneras diferentes. El primer método solicita el recurso sin proporcionar credenciales. Se devuelve un código de estado 401 para indicar que el servidor requiere autenticación. También se muestran los encabezados de respuesta y deben ser similares a los siguientes:

``` syntax
Connection: Keep-Alive
Content-Length: 0
Date: Fri, 27 Apr 2001 01:47:18 GMT
Content-Type: text/html
Server: Microsoft-IIS/5.0
WWW-Authenticate: NTLM
WWW-Authenticate: Negotiate
Cache-control: private
```

Aunque la respuesta indica que se denegó el acceso al recurso, sigue devoluciones de varios encabezados que proporcionan información sobre el recurso. El encabezado denominado "WWW-Authenticate" indica que el servidor requiere autenticación para este recurso. Si había un encabezado denominado "proxy-Authenticate", indicaría que el servidor proxy requiere autenticación. Cada encabezado de autenticación contiene un esquema de autenticación disponible y, a veces, un dominio Kerberos. El valor de dominio Kerberos distingue entre mayúsculas y minúsculas y define un conjunto de servidores o servidores proxy para los que se deben aceptar las mismas credenciales.

Hay dos encabezados denominados "WWW-Authenticate", que indican que se admiten varios esquemas de autenticación. Si llama al método [**GetResponseHeader**](iwinhttprequest-getresponseheader.md) para buscar los encabezados "www-Authenticate", el método solo devuelve el contenido del primer encabezado de ese nombre. En este caso, devuelve un valor de "NTLM". Para asegurarse de que se procesan todas las repeticiones de un encabezado, use en su lugar el método [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) .

La segunda llamada al método solicita el mismo recurso, pero primero proporciona credenciales de autenticación mediante una llamada al método [**SetCredentials**](iwinhttprequest-setcredentials.md) . La siguiente sección de código muestra cómo se usa este método.


```VB
WinHttpReq.SetCredentials( "User Name", "Password",
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
```



Este método establece el nombre de usuario en "UserName", la contraseña en "Password" e indica que las credenciales de autorización se aplican al servidor de recursos. Las credenciales de autenticación también se pueden enviar a un proxy.

Cuando se suministran las credenciales, el servidor devuelve un código de estado 200 que indica que se puede recuperar el documento.

## <a name="checking-the-status-codes"></a>Comprobación de los códigos de estado

El ejemplo anterior es una instrucción, pero requiere que el usuario proporcione explícitamente las credenciales. Una aplicación que proporciona credenciales cuando es necesario y no proporciona credenciales cuando no es necesario es más útil. Para implementar una característica que lo hace, debe modificar el ejemplo para examinar el código de estado devuelto con la respuesta.

Para obtener una lista completa de los posibles códigos de estado, junto con las descripciones, consulte [**códigos de estado http**](http-status-codes.md). En este ejemplo, sin embargo, debería encontrar solo uno de los tres códigos. Un código de estado 200 indica que un recurso está disponible y se está enviando con la respuesta. Un código de estado 401 indica que el servidor requiere autenticación. Un código de estado 407 indica que el proxy requiere autenticación.

Modifique el ejemplo que creó en la última sección reemplazando la función "getText2" con el código siguiente (reemplace " \[ authenticationSite \] " por su propio texto para especificar la dirección URL de un sitio que requiere autenticación http):


```VB
function getText2() {
  WScript.Echo( "Credentials: " );

  // HttpRequest SetCredentials flags.
  HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
  HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

  // Specify the target resource.
  var targURL = "https://[authenticationSite]";
  WinHttpReq.open( "GET", targURL, false );

  var Done = false;
  var Attempts = 0;
  do
  {
    // Keep track of the number of request attempts.
    Attempts++;

    // Send a request to the server and wait for a response.
    WinHttpReq.send( );

    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status)
    {
      // A 200 status indicates that the resource was retrieved.
      case 200:
        Done = true;
        break;

      // A 401 status indicates that the server 
      // requires authentication.
      case 401:
        WScript.Echo( "Requires Server UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the server.
        WinHttpReq.SetCredentials( "User Name", 
                             "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        break;

      // A 407 status indicates that the proxy 
      // requires authentication.
      case 407:
        WScript.Echo( "Requires Proxy UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the proxy.
        WinHttpReq.SetCredentials( "User Name", 
                              "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_PROXY );
        break;
    }
  } while( ( !Done ) && ( Attempts < 3 ) );

  // Display the results of the request.
  WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
  WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
  WScript.Echo( );
};
```



De nuevo, guarde y ejecute el archivo. El segundo método todavía recupera el documento, pero solo proporciona credenciales cuando sea necesario. La función "getText2" ejecuta los métodos [**Open**](iwinhttprequest-open.md) y [**send**](iwinhttprequest-send.md) como si no fuera necesaria la autenticación. El estado se recupera con la propiedad [**status**](iwinhttprequest-status.md) y una instrucción switch responde al código de estado resultante. Si el estado es 401 (el servidor requiere autenticación) o 407 (el proxy requiere autenticación), se vuelve a ejecutar el método [**abierto**](iwinhttprequest-open.md) . Esto va seguido del método [**SetCredentials**](iwinhttprequest-setcredentials.md) , que establece el nombre de usuario y la contraseña. A continuación, el código recorre en bucle el método [**send**](iwinhttprequest-send.md) . Si, después de tres intentos, el recurso no se puede recuperar correctamente, la función detiene la ejecución.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación en WinHTTP](authentication-in-winhttp.md)
</dt> <dt>

[WinHttpRequest](winhttprequest.md)
</dt> <dt>

[**SetCredentials**](iwinhttprequest-setcredentials.md)
</dt> <dt>

[Solicitud de comentarios HTTP/1.1 (RFC 2616)](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 




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
# <a name="authentication-using-script"></a><span data-ttu-id="77ff7-103">Autenticación mediante script</span><span class="sxs-lookup"><span data-stu-id="77ff7-103">Authentication Using Script</span></span>

<span data-ttu-id="77ff7-104">En esta sección se muestra cómo escribir un script que use el objeto [**WinHttpRequest**](winhttprequest.md) para tener acceso a los datos de un servidor que requiera autenticación http.</span><span class="sxs-lookup"><span data-stu-id="77ff7-104">This section demonstrates how to write script that uses the [**WinHttpRequest**](winhttprequest.md) object to access data from a server that requires HTTP authentication.</span></span>

-   [<span data-ttu-id="77ff7-105">Requisitos previos y requisitos</span><span class="sxs-lookup"><span data-stu-id="77ff7-105">Prerequisites and Requirements</span></span>](#prerequisites-and-requirements)
-   [<span data-ttu-id="77ff7-106">Obtener acceso a un sitio web con autenticación</span><span class="sxs-lookup"><span data-stu-id="77ff7-106">Accessing a Web Site With Authentication</span></span>](#accessing-a-web-site-with-authentication)
-   [<span data-ttu-id="77ff7-107">Comprobación de los códigos de estado</span><span class="sxs-lookup"><span data-stu-id="77ff7-107">Checking the Status Codes</span></span>](#checking-the-status-codes)
-   [<span data-ttu-id="77ff7-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77ff7-108">Related topics</span></span>](#related-topics)

## <a name="prerequisites-and-requirements"></a><span data-ttu-id="77ff7-109">Requisitos previos y requisitos</span><span class="sxs-lookup"><span data-stu-id="77ff7-109">Prerequisites and Requirements</span></span>

<span data-ttu-id="77ff7-110">Además de tener conocimientos prácticos de Microsoft JScript, este ejemplo requiere lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="77ff7-110">In addition to a working knowledge of Microsoft JScript, this example requires the following:</span></span>

-   <span data-ttu-id="77ff7-111">La versión actual del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="77ff7-111">The current version of the Microsoft Windows Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="77ff7-112">La herramienta de configuración de proxy para establecer la configuración de proxy para los servicios HTTP de Microsoft Windows (WinHTTP), si la conexión a Internet se realiza a través de un servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="77ff7-112">The proxy configuration tool to establish the proxy settings for Microsoft Windows HTTP Services (WinHTTP), if your connection to the Internet is through a proxy server.</span></span> <span data-ttu-id="77ff7-113">Vea [Proxycfg.exe, una herramienta de configuración de proxy](proxycfg-exe--a-proxy-configuration-tool.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="77ff7-113">See [Proxycfg.exe, a Proxy Configuration Tool](proxycfg-exe--a-proxy-configuration-tool.md) for more information.</span></span>
-   <span data-ttu-id="77ff7-114">Familiaridad con la [terminología](network-terminology.md) y los conceptos de la red.</span><span class="sxs-lookup"><span data-stu-id="77ff7-114">A familiarity with [network terminology](network-terminology.md) and concepts.</span></span>

## <a name="accessing-a-web-site-with-authentication"></a><span data-ttu-id="77ff7-115">Obtener acceso a un sitio web con autenticación</span><span class="sxs-lookup"><span data-stu-id="77ff7-115">Accessing a Web Site With Authentication</span></span>

<span data-ttu-id="77ff7-116">**Para crear un script que muestre la autenticación de, haga lo siguiente:**</span><span class="sxs-lookup"><span data-stu-id="77ff7-116">**To create a script that demonstrates authentication, do the following:**</span></span>

1.  <span data-ttu-id="77ff7-117">Abra un editor de texto como el Bloc de notas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="77ff7-117">Open a text editor such as Microsoft Notepad.</span></span>
2.  <span data-ttu-id="77ff7-118">Copie el código siguiente en el editor de texto después de reemplazar " \[ authenticationSite \] " con el texto adecuado para especificar la dirección URL de un sitio que requiere autenticación http.</span><span class="sxs-lookup"><span data-stu-id="77ff7-118">Copy the following code into the text editor after replacing "\[authenticationSite\]" with the appropriate text to specify the URL of a site that requires HTTP authentication.</span></span>

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

    

3.  <span data-ttu-id="77ff7-119">Guarde el archivo como "Auth.js".</span><span class="sxs-lookup"><span data-stu-id="77ff7-119">Save the file as "Auth.js".</span></span>
4.  <span data-ttu-id="77ff7-120">En un símbolo del sistema, escriba "cscript Auth.js" y presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="77ff7-120">From a command prompt, type "cscript Auth.js" and press ENTER.</span></span>

<span data-ttu-id="77ff7-121">Ahora tiene un programa que solicita un recurso de dos maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="77ff7-121">You now have a program that requests a resource two different ways.</span></span> <span data-ttu-id="77ff7-122">El primer método solicita el recurso sin proporcionar credenciales.</span><span class="sxs-lookup"><span data-stu-id="77ff7-122">The first method requests the resource without supplying credentials.</span></span> <span data-ttu-id="77ff7-123">Se devuelve un código de estado 401 para indicar que el servidor requiere autenticación.</span><span class="sxs-lookup"><span data-stu-id="77ff7-123">A 401 status code is returned to indicate that the server requires authentication.</span></span> <span data-ttu-id="77ff7-124">También se muestran los encabezados de respuesta y deben ser similares a los siguientes:</span><span class="sxs-lookup"><span data-stu-id="77ff7-124">The response headers are also displayed and should look similar to the following:</span></span>

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

<span data-ttu-id="77ff7-125">Aunque la respuesta indica que se denegó el acceso al recurso, sigue devoluciones de varios encabezados que proporcionan información sobre el recurso.</span><span class="sxs-lookup"><span data-stu-id="77ff7-125">Although the response indicates that access to the resource was denied, it still returns several headers that provide some information about the resource.</span></span> <span data-ttu-id="77ff7-126">El encabezado denominado "WWW-Authenticate" indica que el servidor requiere autenticación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="77ff7-126">The header named "WWW-Authenticate" indicates that the server requires authentication for this resource.</span></span> <span data-ttu-id="77ff7-127">Si había un encabezado denominado "proxy-Authenticate", indicaría que el servidor proxy requiere autenticación.</span><span class="sxs-lookup"><span data-stu-id="77ff7-127">If there was a header named "Proxy-Authenticate", it would indicate that the proxy server requires authentication.</span></span> <span data-ttu-id="77ff7-128">Cada encabezado de autenticación contiene un esquema de autenticación disponible y, a veces, un dominio Kerberos.</span><span class="sxs-lookup"><span data-stu-id="77ff7-128">Each authenticate header contains an available authentication scheme and sometimes a realm.</span></span> <span data-ttu-id="77ff7-129">El valor de dominio Kerberos distingue entre mayúsculas y minúsculas y define un conjunto de servidores o servidores proxy para los que se deben aceptar las mismas credenciales.</span><span class="sxs-lookup"><span data-stu-id="77ff7-129">The realm value is case-sensitive and defines a set of servers or proxies for which the same credentials should be accepted.</span></span>

<span data-ttu-id="77ff7-130">Hay dos encabezados denominados "WWW-Authenticate", que indican que se admiten varios esquemas de autenticación.</span><span class="sxs-lookup"><span data-stu-id="77ff7-130">There are two headers named "WWW-Authenticate", which indicate that multiple authentication schemes are supported.</span></span> <span data-ttu-id="77ff7-131">Si llama al método [**GetResponseHeader**](iwinhttprequest-getresponseheader.md) para buscar los encabezados "www-Authenticate", el método solo devuelve el contenido del primer encabezado de ese nombre.</span><span class="sxs-lookup"><span data-stu-id="77ff7-131">If you call the [**GetResponseHeader**](iwinhttprequest-getresponseheader.md) method to find "WWW-Authenticate" headers, the method only returns the contents of the first header of that name.</span></span> <span data-ttu-id="77ff7-132">En este caso, devuelve un valor de "NTLM".</span><span class="sxs-lookup"><span data-stu-id="77ff7-132">In this case, it returns a value of "NTLM".</span></span> <span data-ttu-id="77ff7-133">Para asegurarse de que se procesan todas las repeticiones de un encabezado, use en su lugar el método [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) .</span><span class="sxs-lookup"><span data-stu-id="77ff7-133">To ensure that all occurrences of a header are processed, use the [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) method instead.</span></span>

<span data-ttu-id="77ff7-134">La segunda llamada al método solicita el mismo recurso, pero primero proporciona credenciales de autenticación mediante una llamada al método [**SetCredentials**](iwinhttprequest-setcredentials.md) .</span><span class="sxs-lookup"><span data-stu-id="77ff7-134">The second method call requests the same resource, but first supplies authentication credentials by calling the [**SetCredentials**](iwinhttprequest-setcredentials.md) method.</span></span> <span data-ttu-id="77ff7-135">La siguiente sección de código muestra cómo se usa este método.</span><span class="sxs-lookup"><span data-stu-id="77ff7-135">The following section of code shows how this method is used.</span></span>


```VB
WinHttpReq.SetCredentials( "User Name", "Password",
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
```



<span data-ttu-id="77ff7-136">Este método establece el nombre de usuario en "UserName", la contraseña en "Password" e indica que las credenciales de autorización se aplican al servidor de recursos.</span><span class="sxs-lookup"><span data-stu-id="77ff7-136">This method sets the user name to "UserName", the password to "Password", and indicates that the authorization credentials apply to the resource server.</span></span> <span data-ttu-id="77ff7-137">Las credenciales de autenticación también se pueden enviar a un proxy.</span><span class="sxs-lookup"><span data-stu-id="77ff7-137">Authentication credentials can also be sent to a proxy.</span></span>

<span data-ttu-id="77ff7-138">Cuando se suministran las credenciales, el servidor devuelve un código de estado 200 que indica que se puede recuperar el documento.</span><span class="sxs-lookup"><span data-stu-id="77ff7-138">When credentials are supplied, the server returns a 200 status code that indicates that the document can be retrieved.</span></span>

## <a name="checking-the-status-codes"></a><span data-ttu-id="77ff7-139">Comprobación de los códigos de estado</span><span class="sxs-lookup"><span data-stu-id="77ff7-139">Checking the Status Codes</span></span>

<span data-ttu-id="77ff7-140">El ejemplo anterior es una instrucción, pero requiere que el usuario proporcione explícitamente las credenciales.</span><span class="sxs-lookup"><span data-stu-id="77ff7-140">The previous example is instructional, but it requires that the user explicitly supply credentials.</span></span> <span data-ttu-id="77ff7-141">Una aplicación que proporciona credenciales cuando es necesario y no proporciona credenciales cuando no es necesario es más útil.</span><span class="sxs-lookup"><span data-stu-id="77ff7-141">An application that supplies credentials when it is necessary and does not supply credentials when it is not necessary is more useful.</span></span> <span data-ttu-id="77ff7-142">Para implementar una característica que lo hace, debe modificar el ejemplo para examinar el código de estado devuelto con la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77ff7-142">To implement a feature that does this, you must modify your example to examine the status code returned with the response.</span></span>

<span data-ttu-id="77ff7-143">Para obtener una lista completa de los posibles códigos de estado, junto con las descripciones, consulte [**códigos de estado http**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="77ff7-143">For a complete list of possible status codes, along with descriptions, see [**HTTP Status Codes**](http-status-codes.md).</span></span> <span data-ttu-id="77ff7-144">En este ejemplo, sin embargo, debería encontrar solo uno de los tres códigos.</span><span class="sxs-lookup"><span data-stu-id="77ff7-144">For this example, however, you should encounter only one of three codes.</span></span> <span data-ttu-id="77ff7-145">Un código de estado 200 indica que un recurso está disponible y se está enviando con la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77ff7-145">A status code of 200 indicates that a resource is available and is being sent with the response.</span></span> <span data-ttu-id="77ff7-146">Un código de estado 401 indica que el servidor requiere autenticación.</span><span class="sxs-lookup"><span data-stu-id="77ff7-146">A status code of 401 indicates that the server requires authentication.</span></span> <span data-ttu-id="77ff7-147">Un código de estado 407 indica que el proxy requiere autenticación.</span><span class="sxs-lookup"><span data-stu-id="77ff7-147">A status code of 407 indicates that the proxy requires authentication.</span></span>

<span data-ttu-id="77ff7-148">Modifique el ejemplo que creó en la última sección reemplazando la función "getText2" con el código siguiente (reemplace " \[ authenticationSite \] " por su propio texto para especificar la dirección URL de un sitio que requiere autenticación http):</span><span class="sxs-lookup"><span data-stu-id="77ff7-148">Modify the example you created in the last section by replacing the "getText2" function with the following code (replace "\[authenticationSite\]" with your own text to specifies the URL of a site that requires HTTP authentication):</span></span>


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



<span data-ttu-id="77ff7-149">De nuevo, guarde y ejecute el archivo.</span><span class="sxs-lookup"><span data-stu-id="77ff7-149">Again, save and run the file.</span></span> <span data-ttu-id="77ff7-150">El segundo método todavía recupera el documento, pero solo proporciona credenciales cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="77ff7-150">The second method still retrieves the document, but it only provides credentials when required.</span></span> <span data-ttu-id="77ff7-151">La función "getText2" ejecuta los métodos [**Open**](iwinhttprequest-open.md) y [**send**](iwinhttprequest-send.md) como si no fuera necesaria la autenticación.</span><span class="sxs-lookup"><span data-stu-id="77ff7-151">The "getText2" function executes the [**Open**](iwinhttprequest-open.md) and [**Send**](iwinhttprequest-send.md) methods as if authentication was not required.</span></span> <span data-ttu-id="77ff7-152">El estado se recupera con la propiedad [**status**](iwinhttprequest-status.md) y una instrucción switch responde al código de estado resultante.</span><span class="sxs-lookup"><span data-stu-id="77ff7-152">The status is retrieved with the [**Status**](iwinhttprequest-status.md) property and a switch statement responds to the resulting status code.</span></span> <span data-ttu-id="77ff7-153">Si el estado es 401 (el servidor requiere autenticación) o 407 (el proxy requiere autenticación), se vuelve a ejecutar el método [**abierto**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="77ff7-153">If the status is 401 (server requires authentication) or 407 (proxy requires authentication), the [**Open**](iwinhttprequest-open.md) method is executed again.</span></span> <span data-ttu-id="77ff7-154">Esto va seguido del método [**SetCredentials**](iwinhttprequest-setcredentials.md) , que establece el nombre de usuario y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="77ff7-154">This is followed by the [**SetCredentials**](iwinhttprequest-setcredentials.md) method, which sets the user name and password.</span></span> <span data-ttu-id="77ff7-155">A continuación, el código recorre en bucle el método [**send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="77ff7-155">The code then loops back to the [**Send**](iwinhttprequest-send.md) method.</span></span> <span data-ttu-id="77ff7-156">Si, después de tres intentos, el recurso no se puede recuperar correctamente, la función detiene la ejecución.</span><span class="sxs-lookup"><span data-stu-id="77ff7-156">If, after three attempts, the resource cannot be successfully retrieved, then the function stops execution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77ff7-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77ff7-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77ff7-158">Autenticación en WinHTTP</span><span class="sxs-lookup"><span data-stu-id="77ff7-158">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="77ff7-159">WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="77ff7-159">WinHttpRequest</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="77ff7-160">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="77ff7-160">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)
</dt> <dt>

[<span data-ttu-id="77ff7-161">Solicitud de comentarios HTTP/1.1 (RFC 2616)</span><span class="sxs-lookup"><span data-stu-id="77ff7-161">HTTP/1.1 Request for Comments (RFC 2616)</span></span>](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 




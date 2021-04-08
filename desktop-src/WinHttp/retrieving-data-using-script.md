---
description: En este tema se incluye un ejemplo de cómo escribir un script que obtenga datos a través de los servicios HTTP de Microsoft Windows (WinHTTP) de forma sincrónica o asincrónica.
ms.assetid: 84b847f8-4d9e-4fea-9e87-df4c65b54a02
title: Recuperación de datos mediante script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734516cf75f92cc43ab4cb15f22bd97aa803ec33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000883"
---
# <a name="retrieving-data-using-script"></a><span data-ttu-id="558b2-103">Recuperación de datos mediante script</span><span class="sxs-lookup"><span data-stu-id="558b2-103">Retrieving Data Using Script</span></span>

<span data-ttu-id="558b2-104">En este tema se incluye un ejemplo de cómo escribir un script que obtenga datos a través de los servicios HTTP de Microsoft Windows (WinHTTP) de forma sincrónica o asincrónica.</span><span class="sxs-lookup"><span data-stu-id="558b2-104">This topic includes an example of how to write a script that obtains data through Microsoft Windows HTTP Services (WinHTTP) either synchronously or asynchronously.</span></span> <span data-ttu-id="558b2-105">Los conceptos que se muestran en este ejemplo proporcionan la base para escribir aplicaciones de cliente o de servidor de nivel intermedio que requieran acceso a los datos mediante el protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="558b2-105">The concepts demonstrated in this example provide the basis for writing client or middle-tier server applications that require access to data using the HTTP protocol.</span></span>

-   [<span data-ttu-id="558b2-106">Requisitos previos y requisitos</span><span class="sxs-lookup"><span data-stu-id="558b2-106">Prerequisites and Requirements</span></span>](#prerequisites-and-requirements)
-   [<span data-ttu-id="558b2-107">Recuperar datos sincrónicamente</span><span class="sxs-lookup"><span data-stu-id="558b2-107">Retrieving Data Synchronously</span></span>](#retrieving-data-synchronously)
-   [<span data-ttu-id="558b2-108">Recuperar datos de forma asincrónica</span><span class="sxs-lookup"><span data-stu-id="558b2-108">Retrieving Data Asynchronously</span></span>](#retrieving-data-asynchronously)
-   [<span data-ttu-id="558b2-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="558b2-109">Related topics</span></span>](#related-topics)

## <a name="prerequisites-and-requirements"></a><span data-ttu-id="558b2-110">Requisitos previos y requisitos</span><span class="sxs-lookup"><span data-stu-id="558b2-110">Prerequisites and Requirements</span></span>

<span data-ttu-id="558b2-111">Además de tener conocimientos prácticos de Microsoft JScript, este ejemplo requiere lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="558b2-111">In addition to a working knowledge of Microsoft JScript, this example requires the following:</span></span>

-   <span data-ttu-id="558b2-112">La versión actual del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="558b2-112">The current version of the Microsoft Windows Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="558b2-113">La herramienta de configuración de proxy para establecer la configuración de proxy para los servicios HTTP de Microsoft Windows (WinHTTP), si la conexión a Internet se realiza a través de un servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="558b2-113">The proxy configuration tool to establish the proxy settings for Microsoft Windows HTTP Services (WinHTTP), if your connection to the Internet is through a proxy server.</span></span> <span data-ttu-id="558b2-114">Para obtener más información, vea [ProxyCfg.exe, una herramienta de configuración de proxy](proxycfg-exe--a-proxy-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="558b2-114">For more information, see [ProxyCfg.exe, a Proxy Configuration Tool](proxycfg-exe--a-proxy-configuration-tool.md).</span></span>
-   <span data-ttu-id="558b2-115">Familiaridad con la [terminología](network-terminology.md) y los conceptos de la red.</span><span class="sxs-lookup"><span data-stu-id="558b2-115">A familiarity with [network terminology](network-terminology.md) and concepts.</span></span>

## <a name="retrieving-data-synchronously"></a><span data-ttu-id="558b2-116">Recuperar datos sincrónicamente</span><span class="sxs-lookup"><span data-stu-id="558b2-116">Retrieving Data Synchronously</span></span>

<span data-ttu-id="558b2-117">**Para crear un script que obtenga el texto de una página web sincrónicamente, haga lo siguiente:**</span><span class="sxs-lookup"><span data-stu-id="558b2-117">**To create a script that obtains the text from a Web page synchronously, do the following:**</span></span>

1.  <span data-ttu-id="558b2-118">Abra un editor de texto.</span><span class="sxs-lookup"><span data-stu-id="558b2-118">Open a text editor.</span></span>
2.  <span data-ttu-id="558b2-119">Copie el código siguiente en el editor de texto.</span><span class="sxs-lookup"><span data-stu-id="558b2-119">Copy the following code into the text editor.</span></span>

    ```JScript
    function getText(strURL)
    {
        var strResult;
        
        try
        {
            // Create the WinHTTPRequest ActiveX Object.
            var WinHttpReq = new ActiveXObject(
                                      "WinHttp.WinHttpRequest.5.1");
            
            //  Create an HTTP request.
            var temp = WinHttpReq.Open("GET", strURL, false);

            //  Send the HTTP request.
            WinHttpReq.Send();
            
            //  Retrieve the response text.
            strResult = WinHttpReq.ResponseText;
        }
        catch (objError)
        {
            strResult = objError + "\n"
            strResult += "WinHTTP returned error: " + 
                (objError.number & 0xFFFF).toString() + "\n\n";
            strResult += objError.description;
        }
        
        //  Return the response text.
        return strResult;
    }

    WScript.Echo(getText("https://www.microsoft.com/default.htm"));
    ```

    

3.  <span data-ttu-id="558b2-120">Guarde el archivo como "Retrieve.js".</span><span class="sxs-lookup"><span data-stu-id="558b2-120">Save the file as "Retrieve.js".</span></span>
4.  <span data-ttu-id="558b2-121">En un símbolo del sistema, escriba "cscript Retrieve.js" y presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="558b2-121">From a command prompt, type "cscript Retrieve.js" and press ENTER.</span></span>

<span data-ttu-id="558b2-122">Ahora tiene un script que utiliza un objeto [**WinHttpRequest**](winhttprequest.md) para obtener el código fuente HTML de la página web en https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="558b2-122">You now have a script that uses a [**WinHttpRequest**](winhttprequest.md) object to obtain the HTML source code for the Web page at https://www.microsoft.com.</span></span> <span data-ttu-id="558b2-123">Es posible que tenga que esperar varios segundos para que aparezca el código.</span><span class="sxs-lookup"><span data-stu-id="558b2-123">You might have to wait several seconds for the code to appear.</span></span>

<span data-ttu-id="558b2-124">La aplicación contiene solo una función, "getText".</span><span class="sxs-lookup"><span data-stu-id="558b2-124">The application contains only one function, "getText".</span></span> <span data-ttu-id="558b2-125">La primera línea del script crea el objeto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="558b2-125">The first line of the script creates the [**WinHttpRequest**](winhttprequest.md) object.</span></span>


```JScript
    // Create the WinHTTPRequest ActiveX Object.
    var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```



<span data-ttu-id="558b2-126">Cuando el motor de JScript encuentra esta línea, crea una instancia de este objeto.</span><span class="sxs-lookup"><span data-stu-id="558b2-126">When the JScript engine encounters this line, it creates an instance of this object.</span></span> <span data-ttu-id="558b2-127">Si aparece el mensaje de error "el componente ActiveX no puede crear el objeto" en esta línea, lo más probable es que el WinHttp.dll no se haya registrado correctamente o que no esté presente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="558b2-127">If you get the error message, "ActiveX component can't create object", on this line, most likely the WinHttp.dll was not properly registered or is not present on the system.</span></span>

<span data-ttu-id="558b2-128">La siguiente línea del script llama al método [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="558b2-128">The next line of the script calls the [**Open**](iwinhttprequest-open.md) method.</span></span>


```JScript
    //  Create an HTTP request.
    WinHttpReq.Open("GET", "https://www.microsoft.com", false);
```



<span data-ttu-id="558b2-129">Tres parámetros especifican qué [*verbo http*](glossary.md) se debe usar, el nombre del recurso y si se va a usar WinHTTP de forma sincrónica o asincrónica.</span><span class="sxs-lookup"><span data-stu-id="558b2-129">Three parameters specify which [*HTTP verb*](glossary.md) to use, the name of the resource, and whether to use WinHTTP synchronously or asynchronously.</span></span> <span data-ttu-id="558b2-130">En este ejemplo, el método usa el *verbo http*"Get" para obtener datos de https://www.microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="558b2-130">In this example, the method is using the *HTTP verb*"GET" to obtain data from https://www.microsoft.com.</span></span> <span data-ttu-id="558b2-131">Al especificar **false** para el último parámetro, se determina que la transacción se produce sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="558b2-131">Specifying **FALSE** for the last parameter determines that the transaction occurs synchronously.</span></span> <span data-ttu-id="558b2-132">El método [**Open**](iwinhttprequest-open.md) no establece una conexión con el recurso, ya que el nombre podría implicar.</span><span class="sxs-lookup"><span data-stu-id="558b2-132">The [**Open**](iwinhttprequest-open.md) method does not establish a connection to the resource as the name might imply.</span></span> <span data-ttu-id="558b2-133">En su lugar, inicializa las estructuras de datos internas que mantienen información sobre la sesión, la conexión y la solicitud.</span><span class="sxs-lookup"><span data-stu-id="558b2-133">Rather, it initializes the internal data structures that maintain information about the session, connection, and request.</span></span>

<span data-ttu-id="558b2-134">El método [**send**](iwinhttprequest-send.md) ensambla los encabezados de solicitud y envía la solicitud.</span><span class="sxs-lookup"><span data-stu-id="558b2-134">The [**Send**](iwinhttprequest-send.md) method assembles the request headers and sends the request.</span></span> <span data-ttu-id="558b2-135">Cuando se llama en modo sincrónico, el método [**send**](iwinhttprequest-send.md) también espera una respuesta antes de permitir que la aplicación continúe.</span><span class="sxs-lookup"><span data-stu-id="558b2-135">When called in synchronous mode, the [**Send**](iwinhttprequest-send.md) method also waits for a response before allowing the application to continue.</span></span>


```JScript
    // Send the HTTP request.
    WinHttpReq.Send();
```



<span data-ttu-id="558b2-136">Después de enviar la solicitud, el script devuelve el valor de la propiedad [**responseText**](iwinhttprequest-responsetext.md) del objeto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="558b2-136">After sending the request, the script returns the value of the [**ResponseText**](iwinhttprequest-responsetext.md) property of the [**WinHttpRequest**](winhttprequest.md) object.</span></span> <span data-ttu-id="558b2-137">Esta propiedad contiene el cuerpo de la entidad de la respuesta, en este caso, el origen de un documento.</span><span class="sxs-lookup"><span data-stu-id="558b2-137">This property contains the entity body of the response, in this case, the source of a document.</span></span>


```JScript
    // Get the response text.
    return WinHttpReq.ResponseText;
```



<span data-ttu-id="558b2-138">La ejecución del script se pausa mientras se recupera todo el texto del recurso.</span><span class="sxs-lookup"><span data-stu-id="558b2-138">Execution of the script pauses while the entire text of the resource is retrieved.</span></span> <span data-ttu-id="558b2-139">El texto del recurso se devuelve desde la función y se muestra.</span><span class="sxs-lookup"><span data-stu-id="558b2-139">The resource text is returned from the function and displayed.</span></span>

<span data-ttu-id="558b2-140">El objeto [**WinHttpRequest**](winhttprequest.md) garantiza que se liberan los recursos internos asignados a la transacción http.</span><span class="sxs-lookup"><span data-stu-id="558b2-140">The [**WinHttpRequest**](winhttprequest.md) object ensures that any internal resources that are allocated for the HTTP transaction are released.</span></span>

## <a name="retrieving-data-asynchronously"></a><span data-ttu-id="558b2-141">Recuperar datos de forma asincrónica</span><span class="sxs-lookup"><span data-stu-id="558b2-141">Retrieving Data Asynchronously</span></span>

<span data-ttu-id="558b2-142">La recuperación asincrónica de datos mediante WinHTTP es muy similar a la recuperación sincrónica de datos.</span><span class="sxs-lookup"><span data-stu-id="558b2-142">Retrieving data asynchronously using WinHTTP is very similar to retrieving data synchronously.</span></span> <span data-ttu-id="558b2-143">Modifique el script de la sección anterior realizando dos pequeños cambios.</span><span class="sxs-lookup"><span data-stu-id="558b2-143">Modify the script from the previous section by making two small changes.</span></span>

1.  <span data-ttu-id="558b2-144">Establezca el tercer parámetro del método [**Open**](iwinhttprequest-open.md) en "true" en lugar de "false" para especificar que los métodos WinHTTP deben realizarse de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="558b2-144">Set the third parameter of the [**Open**](iwinhttprequest-open.md) method to "true" instead of "false" to specify that WinHTTP methods should be performed asynchronously.</span></span>
    ```JScript
       //  Create a HTTP request.
        var temp = WinHttpReq.Open("GET", strURL, true);
    ```

    

2.  <span data-ttu-id="558b2-145">Invoque el método [**WaitForResponse**](iwinhttprequest-waitforresponse.md) antes de tener acceso a la propiedad [**responseText**](iwinhttprequest-responsetext.md) para asegurarse de que se ha recibido la respuesta completa.</span><span class="sxs-lookup"><span data-stu-id="558b2-145">Invoke the [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method before accessing the [**ResponseText**](iwinhttprequest-responsetext.md) property to ensure that the entire response has been received.</span></span>
    ```JScript
        //  Send the HTTP request.
        WinHttpReq.Send();
            
        // Wait for the entire response.
        WinHttpReq.WaitForResponse();
            
        //  Retrieve the response text.
        strResult = WinHttpReq.ResponseText;
    ```

    

<span data-ttu-id="558b2-146">La principal ventaja de usar WinHTTP de forma asincrónica en script es que el método [**send**](iwinhttprequest-send.md) se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="558b2-146">The main advantage to using WinHTTP asynchronously in script is that the [**Send**](iwinhttprequest-send.md) method returns immediately.</span></span> <span data-ttu-id="558b2-147">Un subproceso de trabajo prepara y envía la solicitud.</span><span class="sxs-lookup"><span data-stu-id="558b2-147">The request is prepared and sent by a worker thread.</span></span> <span data-ttu-id="558b2-148">Esto permite que la aplicación haga otras cosas mientras está esperando la respuesta.</span><span class="sxs-lookup"><span data-stu-id="558b2-148">This enables your application to do other things while it is waiting for the response.</span></span> <span data-ttu-id="558b2-149">Antes de intentar tener acceso a la respuesta, asegúrese de que se ha recibido la respuesta completa llamando al método [**WaitForResponse**](iwinhttprequest-waitforresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="558b2-149">Before attempting to access the response, ensure that the entire response has been received by calling the [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method.</span></span> <span data-ttu-id="558b2-150">De lo contrario, se puede producir un error.</span><span class="sxs-lookup"><span data-stu-id="558b2-150">Otherwise an error can occur.</span></span>

<span data-ttu-id="558b2-151">El método [**WaitForResponse**](iwinhttprequest-waitforresponse.md) también se puede usar para especificar un valor de tiempo de espera para la transacción.</span><span class="sxs-lookup"><span data-stu-id="558b2-151">The [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method can also be used to specify a time-out value for the transaction.</span></span> <span data-ttu-id="558b2-152">Un parámetro opcional le permite especificar el valor de tiempo de espera en segundos.</span><span class="sxs-lookup"><span data-stu-id="558b2-152">An optional parameter enables you to specify the time-out value in seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="558b2-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="558b2-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="558b2-154">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="558b2-154">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="558b2-155">Solicitud de comentarios HTTP/1.1 (RFC 2616)</span><span class="sxs-lookup"><span data-stu-id="558b2-155">HTTP/1.1 Request for Comments (RFC 2616)</span></span>](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 




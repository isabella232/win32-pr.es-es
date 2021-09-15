---
description: En este tema se incluye un ejemplo de cómo escribir un script que obtiene datos a través de Servicios HTTP de Microsoft Windows (WinHTTP) de forma sincrónica o asincrónica.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476130"
---
# <a name="retrieving-data-using-script"></a>Recuperación de datos mediante script

En este tema se incluye un ejemplo de cómo escribir un script que obtiene datos a través de Servicios HTTP de Microsoft Windows (WinHTTP) de forma sincrónica o asincrónica. Los conceptos que se muestran en este ejemplo proporcionan la base para escribir aplicaciones de cliente o de servidor de nivel intermedio que requieren acceso a los datos mediante el protocolo HTTP.

-   [Requisitos previos y requisitos](#prerequisites-and-requirements)
-   [Recuperar datos de forma sincrónica](#retrieving-data-synchronously)
-   [Recuperar datos de forma asincrónica](#retrieving-data-asynchronously)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites-and-requirements"></a>Requisitos previos y requisitos

Además de un conocimiento práctico de Microsoft JScript, este ejemplo requiere lo siguiente:

-   La versión actual de Microsoft Windows Software Development Kit (SDK).
-   La herramienta de configuración de proxy para establecer la configuración de proxy para Los servicios HTTP de Microsoft Windows (WinHTTP), si la conexión a Internet se establece a través de un servidor proxy. Para obtener más información, [ veaProxyCfg.exe, una herramienta de configuración de proxy](proxycfg-exe--a-proxy-configuration-tool.md).
-   Familiaridad con la [terminología y los conceptos](network-terminology.md) de red.

## <a name="retrieving-data-synchronously"></a>Recuperar datos de forma sincrónica

**Para crear un script que obtenga el texto de una página web de forma sincrónica, haga lo siguiente:**

1.  Abra un editor de texto.
2.  Copie el código siguiente en el editor de texto.

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

    

3.  Guarde el archivo como "Retrieve.js".
4.  En un símbolo del sistema, escriba "cscript Retrieve.js" y presione ENTRAR.

Ahora tiene un script que usa un [**objeto WinHttpRequest**](winhttprequest.md) para obtener el código fuente HTML de la página web en https://www.microsoft.com . Es posible que tenga que esperar varios segundos para que aparezca el código.

La aplicación solo contiene una función, "getText". La primera línea del script crea el [**objeto WinHttpRequest.**](winhttprequest.md)


```JScript
    // Create the WinHTTPRequest ActiveX Object.
    var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```



Cuando el JScript encuentra esta línea, crea una instancia de este objeto . Si recibe el mensaje de error "ActiveX component can't create object", en esta línea, lo más probable es que el WinHttp.dll no se haya registrado correctamente o no esté presente en el sistema.

La siguiente línea del script llama al [**método**](iwinhttprequest-open.md) Open.


```JScript
    //  Create an HTTP request.
    WinHttpReq.Open("GET", "https://www.microsoft.com", false);
```



Tres parámetros especifican qué [*verbo HTTP usar,*](glossary.md) el nombre del recurso y si se debe usar WinHTTP de forma sincrónica o asincrónica. En este ejemplo, el método usa el *verbo HTTP*"GET" para obtener datos de https://www.microsoft.com . Si se **especifica FALSE** para el último parámetro, se determina que la transacción se produce sincrónicamente. El [**método Open**](iwinhttprequest-open.md) no establece una conexión con el recurso, ya que el nombre podría implicar. En su lugar, inicializa las estructuras de datos internas que mantienen información sobre la sesión, la conexión y la solicitud.

El [**método Send**](iwinhttprequest-send.md) ensambla los encabezados de solicitud y envía la solicitud. Cuando se llama en modo sincrónico, [**el método Send**](iwinhttprequest-send.md) también espera una respuesta antes de permitir que la aplicación continúe.


```JScript
    // Send the HTTP request.
    WinHttpReq.Send();
```



Después de enviar la solicitud, el script devuelve el valor de la [**propiedad ResponseText**](iwinhttprequest-responsetext.md) del [**objeto WinHttpRequest.**](winhttprequest.md) Esta propiedad contiene el cuerpo de la entidad de la respuesta, en este caso, el origen de un documento.


```JScript
    // Get the response text.
    return WinHttpReq.ResponseText;
```



La ejecución del script se detiene mientras se recupera todo el texto del recurso. El texto del recurso se devuelve desde la función y se muestra.

El [**objeto WinHttpRequest**](winhttprequest.md) garantiza que se liberan todos los recursos internos asignados para la transacción HTTP.

## <a name="retrieving-data-asynchronously"></a>Recuperar datos de forma asincrónica

Recuperar datos de forma asincrónica mediante WinHTTP es muy similar a recuperar datos de forma sincrónica. Modifique el script de la sección anterior realizando dos pequeños cambios.

1.  Establezca el tercer parámetro del método [**Open**](iwinhttprequest-open.md) en "true" en lugar de "false" para especificar que los métodos WinHTTP se deben realizar de forma asincrónica.
    ```JScript
       //  Create a HTTP request.
        var temp = WinHttpReq.Open("GET", strURL, true);
    ```

    

2.  [**Invoque el método WaitForResponse**](iwinhttprequest-waitforresponse.md) antes de acceder a [**la propiedad ResponseText**](iwinhttprequest-responsetext.md) para asegurarse de que se ha recibido toda la respuesta.
    ```JScript
        //  Send the HTTP request.
        WinHttpReq.Send();
            
        // Wait for the entire response.
        WinHttpReq.WaitForResponse();
            
        //  Retrieve the response text.
        strResult = WinHttpReq.ResponseText;
    ```

    

La principal ventaja de usar WinHTTP de forma asincrónica en el script es que el [**método Send**](iwinhttprequest-send.md) se devuelve inmediatamente. Un subproceso de trabajo prepara y envía la solicitud. Esto permite que la aplicación haga otras cosas mientras espera la respuesta. Antes de intentar acceder a la respuesta, asegúrese de que se ha recibido toda la respuesta llamando al [**método WaitForResponse.**](iwinhttprequest-waitforresponse.md) De lo contrario, puede producirse un error.

El [**método WaitForResponse**](iwinhttprequest-waitforresponse.md) también se puede usar para especificar un valor de tiempo de espera para la transacción. Un parámetro opcional permite especificar el valor de tiempo de espera en segundos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[SOLICITUD HTTP/1.1 para comentarios (RFC 2616)](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 




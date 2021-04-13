---
description: Si el host y el cliente genéricos se ejecutan correctamente, pero el host y el cliente reales siguen produciendo errores, es posible que la solicitud de metadatos no se inicie. El registro de WinHTTP se puede usar para comprobar que los mensajes salientes se generan y se envían correctamente.
ms.assetid: ab4568bd-fc05-4e2a-ac8c-f035e6583a36
title: Uso del registro de WinHTTP para comprobar el tráfico Get
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448e4a127baf90a64291cbd14477c424270b332d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276966"
---
# <a name="using-winhttp-logging-to-verify-get-traffic"></a>Uso del registro de WinHTTP para comprobar el tráfico Get

Si el host y el cliente genéricos se ejecutan correctamente, pero el host y el cliente reales siguen produciendo errores, es posible que la solicitud de metadatos no se inicie. El registro de [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) se puede usar para comprobar que los mensajes salientes se generan y se envían correctamente.

Las aplicaciones cliente basadas en WSDAPI usan [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) para conectarse a los dispositivos. Los hosts de dispositivo basados en WSDAPI no usan WinHTTP. Además, algunos proxies de terceros no utilizan WinHTTP. Al solucionar problemas de un host o proxy que no usa WinHTTP, omita este procedimiento de diagnóstico y siga los procedimientos de [inspección de seguimientos de red para el intercambio de metadatos http para](inspecting-network-traces-for-http-metadata-exchange.md)continuar con la solución de problemas.

El registro de [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) no muestra todo el tráfico de nivel TCP. Vaya a [inspeccionar los seguimientos de red para el intercambio de metadatos http](inspecting-network-traces-for-http-metadata-exchange.md) si el tráfico que está por encima del tráfico HTTP es de interés.

**Para usar el registro de WinHTTP para comprobar el tráfico Get**

1.  [Capture los registros de WinHTTP.](capturing-winhttp-logs.md)
2.  Inicie Bloc de notas u otro procesador de texto. El editor de texto se debe ejecutar como administrador.
3.  Abra el archivo de registro de WinHTTP.
4.  Compruebe que se han enviado las solicitudes HTTP y los mensajes de metadatos necesarios.

Si se encuentra un mensaje [Get](get--metadata-exchange--http-request-and-message.md) para el host en los registros de WinHTTP, las solicitudes de metadatos se envían a winhttp correctamente. Siga los procedimientos que se indican en [inspeccionar seguimientos de red para el intercambio de metadatos http para](inspecting-network-traces-for-http-metadata-exchange.md)continuar con la solución de problemas.

Si no se encuentra un mensaje [Get](get--metadata-exchange--http-request-and-message.md) para el host en los registros de WinHTTP, no se iniciará la solicitud de metadatos. Esto puede ocurrir cuando el host publica XAddrs no válidos. Compruebe que el XAddrs en el host cumple las [reglas de validación de XAddr](xaddr-validation-rules.md).

## <a name="verifying-that-the-required-http-requests-and-metadata-messages-were-sent"></a>Comprobando que se enviaron los mensajes de metadatos y las solicitudes HTTP necesarios

Se deben realizar los siguientes eventos para el intercambio de metadatos correcto:

-   El cliente WSDAPI genera una solicitud HTTP de salida. Esta solicitud se envía al host WSDAPI.
-   El cliente envía un mensaje [Get](get--metadata-exchange--http-request-and-message.md) al host.

Estos eventos se capturan en los registros de WinHTTP.

El siguiente fragmento de archivo de registro de WinHTTP muestra una solicitud HTTP de salida generada por un cliente de WSDAPI.

``` syntax
16:51:47.893 ::*0000004* :: WinHttpSendRequest(0x36aae0, "", 0, 0x0, 0, 658, 0)
16:51:47.893 ::*0000004* :: WinHttpSendRequest() returning TRUE
16:51:47.897 ::*0000004* :: sending data:
16:51:47.897 ::*0000004* :: 226 (0xe2) bytes
16:51:47.897 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.897 ::*0000004* :: POST /dbe17c74-3b21-4f52-addc-b84b444f73a0 HTTP/1.1
16:51:47.897 ::*0000004* :: Content-Type: application/soap+xml
16:51:47.897 ::*0000004* :: User-Agent: WSDAPI
16:51:47.897 ::*0000004* :: Host: 192.168.0.1:5357
16:51:47.897 ::*0000004* :: Content-Length: 658
16:51:47.897 ::*0000004* :: Connection: Keep-Alive
16:51:47.897 ::*0000004* :: Cache-Control: no-cache
16:51:47.897 ::*0000004* :: Pragma: no-cache
16:51:47.897 ::*0000004* :: 
16:51:47.897 ::*0000004* :: 
16:51:47.897 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
```

El siguiente fragmento de archivo de registro de WinHTTP muestra un mensaje [Get](get--metadata-exchange--http-request-and-message.md) . Este mensaje debe seguir inmediatamente a la solicitud HTTP.

``` syntax
16:51:47.898 ::*0000004* :: WinHttpWriteData(0x36aae0, 0x11aa7c4, 658, 0x0)
16:51:47.899 ::*0000004* :: sending data:
16:51:47.899 ::*0000004* :: 658 (0x292) bytes
16:51:47.899 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.899 ::*0000004* :: <?xml version="1.0" encoding="utf-8" ?>
16:51:47.899 ::*0000004* :: <soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"><soap:Header><wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To><wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action><wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID><wsa:ReplyTo><wsa:Address>https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:Address></wsa:ReplyTo><wsa:From><wsa:Address>urn:uuid:b32467b5-e7ee-4ae3-8a8e-f5aa417c23b6</wsa:Address></wsa:From></soap:Header><soap:Body></soap:Body></soap:Envelope>
16:51:47.899 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
16:51:47.899 ::*0000004* :: WinHttpWriteData() returning TRUE
```

El elemento **Action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>` ) identifica el mensaje como un mensaje [Get](get--metadata-exchange--http-request-and-message.md) . Compruebe que el valor del elemento **to** (por ejemplo, `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>` ) coincide con el identificador de dispositivo anunciado por el host en los mensajes UDP WS-Discovery originales. El identificador de dispositivo anunciado por el host se puede comprobar mediante el host de depuración WSD. Para obtener más información, vea [usar un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).

Además, la respuesta del host a la solicitud de metadatos se puede encontrar en los registros de WinHTTP del cliente. El host genera un mensaje [GetResponse](getresponse--metadata-exchange--message.md) en respuesta al mensaje [Get](get--metadata-exchange--http-request-and-message.md) del cliente.

El siguiente fragmento de archivo de registro de WinHTTP muestra un mensaje de [GetResponse](getresponse--metadata-exchange--message.md) entrante recibido por un cliente WSDAPI.

``` syntax
16:51:47.899 ::*0000004* :: WinHttpReceiveResponse(0x36aae0, 0x0)
16:51:47.899 ::*0000004* :: WinHttpReceiveResponse() returning TRUE
16:51:47.899 ::*Session* :: DllMain(0x73fc0000, DLL_THREAD_ATTACH, 0x0)
16:51:47.902 ::*0000004* :: received data:
16:51:47.902 ::*0000004* :: 1024 (0x400) bytes
16:51:47.902 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.902 ::*0000004* :: HTTP/1.1 200 
16:51:47.902 ::*0000004* :: Content-Type: application/soap+xml
16:51:47.902 ::*0000004* :: Server: Microsoft-HTTPAPI/2.0
16:51:47.902 ::*0000004* :: Date: Fri, 15 Jun 2007 23:51:47 GMT
16:51:47.905 ::*0000004* :: Content-Length: 2228
16:51:47.905 ::*0000004* :: 
16:51:47.905 ::*0000004* :: <?xml version="1.0" encoding="utf-8" ?>
16:51:47.905 ::*0000004* :: <soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof" xmlns:un0="http://schemas.microsoft.com/windows/pnpx/2005/10" xmlns:pub="http://schemas.microsoft.com/windows/pub/2005/07"><soap:Header><wsa:To>https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:To><wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action><wsa:MessageID>urn:uuid:2884cbcc-2848-4c35-9327-5ab5451a8729</wsa:MessageID><wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo></soap:Header><soap:Body><wsx:Metadata><wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice"><wsdp:ThisDevice><wsd
16:51:47.905 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
```

El elemento **Action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>` ) identifica el mensaje como un mensaje [GetResponse](getresponse--metadata-exchange--message.md) . Compruebe que el valor del elemento **latesto** del mensaje GetResponse coincide con el valor del elemento **MessageID** del mensaje [Get](get--metadata-exchange--http-request-and-message.md) . En este ejemplo, el valor del elemento **latesto** ( `<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>` ) coincide con el valor del elemento **MessageID** del mensaje get ( `<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>` ).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[Captura de registros de WinHTTP](capturing-winhttp-logs.md)
</dt> <dt>

[Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introducción con la solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 

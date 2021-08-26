---
description: Si el host y el cliente genéricos se realiza correctamente, pero el host y el cliente reales siguen con errores, es posible que no se inicie la solicitud de metadatos. El registro winHTTP se puede usar para comprobar que los mensajes salientes se generan y envían correctamente.
ms.assetid: ab4568bd-fc05-4e2a-ac8c-f035e6583a36
title: Uso del registro WinHTTP para comprobar la obtener tráfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 031359dac8c8fa890568d6833cbfdf8c3d41d43bd52403a7def61a7392e8e23a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995225"
---
# <a name="using-winhttp-logging-to-verify-get-traffic"></a>Uso del registro WinHTTP para comprobar la obtener tráfico

Si el host y el cliente genéricos se realiza correctamente, pero el host y el cliente reales siguen con errores, es posible que no se inicie la solicitud de metadatos. [El registro winHTTP](/windows/desktop/WinHttp/winhttp-start-page) se puede usar para comprobar que los mensajes salientes se generan y envían correctamente.

Las aplicaciones cliente basadas en WSDAPI usan [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) para conectarse a dispositivos. Los hosts de dispositivos basados en WSDAPI no usan WinHTTP. Además, algunos servidores proxy de terceros no usan WinHTTP. Al solucionar problemas de un host o proxy que no usa WinHTTP, omita este procedimiento de diagnóstico y continúe con la solución de problemas siguiendo los procedimientos descritos en Inspección de seguimientos de red para [metadatos HTTP](inspecting-network-traces-for-http-metadata-exchange.md)Exchange .

[El registro winHTTP](/windows/desktop/WinHttp/winhttp-start-page) no muestra todo el tráfico de nivel TCP. Vaya a [Inspección de seguimientos de red](inspecting-network-traces-for-http-metadata-exchange.md) para los metadatos HTTP Exchange si el tráfico además del tráfico HTTP es de interés.

**Para usar el registro WinHTTP para comprobar obtener tráfico**

1.  [Capture los registros winHTTP.](capturing-winhttp-logs.md)
2.  Inicie Bloc de notas u otro procesador de texto. El editor de texto debe ejecutarse como administrador.
3.  Abra el archivo de registro WinHTTP.
4.  Compruebe que se enviaron las solicitudes HTTP y los mensajes de metadatos necesarios.

Si se [encuentra un](get--metadata-exchange--http-request-and-message.md) mensaje Get para el host en los registros winHTTP, las solicitudes de metadatos se envían correctamente a WinHTTP. Para continuar la solución de problemas, siga los procedimientos descritos [en Inspección de seguimientos de red para metadatos HTTP Exchange](inspecting-network-traces-for-http-metadata-exchange.md).

Si no [se encuentra](get--metadata-exchange--http-request-and-message.md) un mensaje Get para el host en los registros WinHTTP, no se inicia la solicitud de metadatos. Esto puede ocurrir cuando el host publica XAddrs no válidos. Compruebe que los XAddrs del host cumplen las [reglas de validación de XAddr](xaddr-validation-rules.md).

## <a name="verifying-that-the-required-http-requests-and-metadata-messages-were-sent"></a>Comprobación de que se enviaron las solicitudes HTTP y los mensajes de metadatos necesarios

Deben producirse los siguientes eventos para el intercambio de metadatos correcto:

-   El cliente WSDAPI genera una solicitud HTTP saliente. Esta solicitud se envía al host de WSDAPI.
-   El cliente envía un [mensaje Get](get--metadata-exchange--http-request-and-message.md) al host.

Estos eventos se capturan en los registros de WinHTTP.

El siguiente fragmento de código de archivo de registro WinHTTP muestra una solicitud HTTP saliente generada por un cliente WSDAPI.

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

El siguiente fragmento de código del archivo de registro WinHTTP muestra [un mensaje Get.](get--metadata-exchange--http-request-and-message.md) Este mensaje debe seguir inmediatamente la solicitud HTTP.

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

El **elemento Action** ( ) identifica el mensaje como un mensaje `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>` [Get.](get--metadata-exchange--http-request-and-message.md) Compruebe que el valor del elemento **To** (por ejemplo, ) coincide con el identificador de dispositivo anunciado por el host en los mensajes `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>` WS-Discovery UDP original. El identificador de dispositivo anunciado por el host se puede comprobar mediante el host de depuración de WSD. Para obtener más información, [vea Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).

Además, la respuesta del host a la solicitud de metadatos se puede encontrar en los registros WinHTTP del cliente. El host genera un mensaje [GetResponse](getresponse--metadata-exchange--message.md) en respuesta al mensaje [Get del](get--metadata-exchange--http-request-and-message.md) cliente.

El siguiente fragmento de código de archivo de registro WinHTTP muestra un mensaje [GetResponse](getresponse--metadata-exchange--message.md) entrante recibido por un cliente WSDAPI.

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

El **elemento Action** ( ) identifica el mensaje como un mensaje `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>` [GetResponse.](getresponse--metadata-exchange--message.md) Compruebe que el valor del elemento **RelatesTo** del mensaje GetResponse coincide con el valor del **elemento MessageID** del [mensaje Get.](get--metadata-exchange--http-request-and-message.md) En este ejemplo, el valor del elemento **RelatesTo** ( ) coincide con el valor del `<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>` **elemento MessageID** del mensaje Get ( `<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>` ).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[Captura de registros WinHTTP](capturing-winhttp-logs.md)
</dt> <dt>

[Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Tareas iniciales solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 

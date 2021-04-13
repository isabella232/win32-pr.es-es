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
# <a name="using-winhttp-logging-to-verify-get-traffic"></a><span data-ttu-id="a3ac9-104">Uso del registro de WinHTTP para comprobar el tráfico Get</span><span class="sxs-lookup"><span data-stu-id="a3ac9-104">Using WinHTTP Logging to Verify Get Traffic</span></span>

<span data-ttu-id="a3ac9-105">Si el host y el cliente genéricos se ejecutan correctamente, pero el host y el cliente reales siguen produciendo errores, es posible que la solicitud de metadatos no se inicie.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-105">If the generic host and client succeed but the actual host and client still fail, it is possible that the metadata request is not being initiated.</span></span> <span data-ttu-id="a3ac9-106">El registro de [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) se puede usar para comprobar que los mensajes salientes se generan y se envían correctamente.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-106">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logging can be used to verify that outbound messages are being generated and sent correctly.</span></span>

<span data-ttu-id="a3ac9-107">Las aplicaciones cliente basadas en WSDAPI usan [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) para conectarse a los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-107">WSDAPI-based client applications use [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) to connect to devices.</span></span> <span data-ttu-id="a3ac9-108">Los hosts de dispositivo basados en WSDAPI no usan WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-108">WSDAPI-based device hosts do not use WinHTTP.</span></span> <span data-ttu-id="a3ac9-109">Además, algunos proxies de terceros no utilizan WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-109">Also, some third-party proxies do not use WinHTTP.</span></span> <span data-ttu-id="a3ac9-110">Al solucionar problemas de un host o proxy que no usa WinHTTP, omita este procedimiento de diagnóstico y siga los procedimientos de [inspección de seguimientos de red para el intercambio de metadatos http para](inspecting-network-traces-for-http-metadata-exchange.md)continuar con la solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-110">When troubleshooting a host or proxy that does not use WinHTTP, skip this diagnostic procedure and continue troubleshooting by following the procedures in [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="a3ac9-111">El registro de [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) no muestra todo el tráfico de nivel TCP.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-111">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logging does not show all TCP-level traffic.</span></span> <span data-ttu-id="a3ac9-112">Vaya a [inspeccionar los seguimientos de red para el intercambio de metadatos http](inspecting-network-traces-for-http-metadata-exchange.md) si el tráfico que está por encima del tráfico HTTP es de interés.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-112">Skip to [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md) if traffic besides the HTTP traffic is of interest.</span></span>

<span data-ttu-id="a3ac9-113">**Para usar el registro de WinHTTP para comprobar el tráfico Get**</span><span class="sxs-lookup"><span data-stu-id="a3ac9-113">**To use WinHTTP logging to verify Get traffic**</span></span>

1.  [<span data-ttu-id="a3ac9-114">Capture los registros de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-114">Capture the WinHTTP logs.</span></span>](capturing-winhttp-logs.md)
2.  <span data-ttu-id="a3ac9-115">Inicie Bloc de notas u otro procesador de texto.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-115">Start Notepad or another text editor.</span></span> <span data-ttu-id="a3ac9-116">El editor de texto se debe ejecutar como administrador.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-116">The text editor must be run as Administrator.</span></span>
3.  <span data-ttu-id="a3ac9-117">Abra el archivo de registro de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-117">Open the WinHTTP log file.</span></span>
4.  <span data-ttu-id="a3ac9-118">Compruebe que se han enviado las solicitudes HTTP y los mensajes de metadatos necesarios.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-118">Verify that the required HTTP requests and metadata messages were sent.</span></span>

<span data-ttu-id="a3ac9-119">Si se encuentra un mensaje [Get](get--metadata-exchange--http-request-and-message.md) para el host en los registros de WinHTTP, las solicitudes de metadatos se envían a winhttp correctamente.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-119">If a [Get](get--metadata-exchange--http-request-and-message.md) message for the host is found in the WinHTTP logs, then the metadata requests are being sent to WinHTTP successfully.</span></span> <span data-ttu-id="a3ac9-120">Siga los procedimientos que se indican en [inspeccionar seguimientos de red para el intercambio de metadatos http para](inspecting-network-traces-for-http-metadata-exchange.md)continuar con la solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-120">Continue troubleshooting by following the procedures in [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="a3ac9-121">Si no se encuentra un mensaje [Get](get--metadata-exchange--http-request-and-message.md) para el host en los registros de WinHTTP, no se iniciará la solicitud de metadatos.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-121">If a [Get](get--metadata-exchange--http-request-and-message.md) message cannot be found for the host in the WinHTTP logs, then the metadata request is not being initiated.</span></span> <span data-ttu-id="a3ac9-122">Esto puede ocurrir cuando el host publica XAddrs no válidos.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-122">This can happen when the host publishes invalid XAddrs.</span></span> <span data-ttu-id="a3ac9-123">Compruebe que el XAddrs en el host cumple las [reglas de validación de XAddr](xaddr-validation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="a3ac9-123">Verify that the XAddrs on the host conform to the [XAddr validation rules](xaddr-validation-rules.md).</span></span>

## <a name="verifying-that-the-required-http-requests-and-metadata-messages-were-sent"></a><span data-ttu-id="a3ac9-124">Comprobando que se enviaron los mensajes de metadatos y las solicitudes HTTP necesarios</span><span class="sxs-lookup"><span data-stu-id="a3ac9-124">Verifying that the required HTTP requests and metadata messages were sent</span></span>

<span data-ttu-id="a3ac9-125">Se deben realizar los siguientes eventos para el intercambio de metadatos correcto:</span><span class="sxs-lookup"><span data-stu-id="a3ac9-125">The following events must occur for successful metadata exchange:</span></span>

-   <span data-ttu-id="a3ac9-126">El cliente WSDAPI genera una solicitud HTTP de salida.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-126">The WSDAPI client generates an outbound HTTP request.</span></span> <span data-ttu-id="a3ac9-127">Esta solicitud se envía al host WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-127">This request is sent to the WSDAPI host.</span></span>
-   <span data-ttu-id="a3ac9-128">El cliente envía un mensaje [Get](get--metadata-exchange--http-request-and-message.md) al host.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-128">The client sends a [Get](get--metadata-exchange--http-request-and-message.md) message to the host.</span></span>

<span data-ttu-id="a3ac9-129">Estos eventos se capturan en los registros de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-129">These events are captured in the WinHTTP logs.</span></span>

<span data-ttu-id="a3ac9-130">El siguiente fragmento de archivo de registro de WinHTTP muestra una solicitud HTTP de salida generada por un cliente de WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-130">The following WinHTTP log file snippet shows an outbound HTTP request generated by a WSDAPI client.</span></span>

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

<span data-ttu-id="a3ac9-131">El siguiente fragmento de archivo de registro de WinHTTP muestra un mensaje [Get](get--metadata-exchange--http-request-and-message.md) .</span><span class="sxs-lookup"><span data-stu-id="a3ac9-131">The following WinHTTP log file snippet shows a [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="a3ac9-132">Este mensaje debe seguir inmediatamente a la solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-132">This message should immediately follow the HTTP request.</span></span>

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

<span data-ttu-id="a3ac9-133">El elemento **Action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>` ) identifica el mensaje como un mensaje [Get](get--metadata-exchange--http-request-and-message.md) .</span><span class="sxs-lookup"><span data-stu-id="a3ac9-133">The **Action** element (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>`) identifies the message as a [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="a3ac9-134">Compruebe que el valor del elemento **to** (por ejemplo, `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>` ) coincide con el identificador de dispositivo anunciado por el host en los mensajes UDP WS-Discovery originales.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-134">Verify that the value of the **To** element (for example, `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>`) matches the device ID advertised by the host in the original UDP WS-Discovery messages.</span></span> <span data-ttu-id="a3ac9-135">El identificador de dispositivo anunciado por el host se puede comprobar mediante el host de depuración WSD.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-135">The device ID advertised by the host can be checked by using the WSD Debug Host.</span></span> <span data-ttu-id="a3ac9-136">Para obtener más información, vea [usar un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="a3ac9-136">For more information, see [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="a3ac9-137">Además, la respuesta del host a la solicitud de metadatos se puede encontrar en los registros de WinHTTP del cliente.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-137">In addition, the host's response to the metadata request can be found in the client's WinHTTP logs.</span></span> <span data-ttu-id="a3ac9-138">El host genera un mensaje [GetResponse](getresponse--metadata-exchange--message.md) en respuesta al mensaje [Get](get--metadata-exchange--http-request-and-message.md) del cliente.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-138">The host generates a [GetResponse](getresponse--metadata-exchange--message.md) message in response to the client's [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span>

<span data-ttu-id="a3ac9-139">El siguiente fragmento de archivo de registro de WinHTTP muestra un mensaje de [GetResponse](getresponse--metadata-exchange--message.md) entrante recibido por un cliente WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="a3ac9-139">The following WinHTTP log file snippet shows an inbound [GetResponse](getresponse--metadata-exchange--message.md) message received by a WSDAPI client.</span></span>

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

<span data-ttu-id="a3ac9-140">El elemento **Action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>` ) identifica el mensaje como un mensaje [GetResponse](getresponse--metadata-exchange--message.md) .</span><span class="sxs-lookup"><span data-stu-id="a3ac9-140">The **Action** element (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>`) identifies the message as a [GetResponse](getresponse--metadata-exchange--message.md) message.</span></span> <span data-ttu-id="a3ac9-141">Compruebe que el valor del elemento **latesto** del mensaje GetResponse coincide con el valor del elemento **MessageID** del mensaje [Get](get--metadata-exchange--http-request-and-message.md) .</span><span class="sxs-lookup"><span data-stu-id="a3ac9-141">Verify that the value of the **RelatesTo** element of the GetResponse message matches the value of the **MessageID** element of the [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="a3ac9-142">En este ejemplo, el valor del elemento **latesto** ( `<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>` ) coincide con el valor del elemento **MessageID** del mensaje get ( `<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>` ).</span><span class="sxs-lookup"><span data-stu-id="a3ac9-142">In this example, the value of the **RelatesTo** element (`<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>`) matches the value of the **MessageID** element of the Get message (`<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>`).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3ac9-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3ac9-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3ac9-144">WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a3ac9-144">WinHTTP</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[<span data-ttu-id="a3ac9-145">Captura de registros de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a3ac9-145">Capturing WinHTTP Logs</span></span>](capturing-winhttp-logs.md)
</dt> <dt>

[<span data-ttu-id="a3ac9-146">Procedimientos de diagnóstico de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="a3ac9-146">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="a3ac9-147">Introducción con la solución de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="a3ac9-147">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 

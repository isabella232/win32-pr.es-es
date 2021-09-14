---
description: Obtenga información sobre la inspección de seguimientos de red para el intercambio de metadatos HTTP. Use un analizador de paquetes de red que muestre paquetes sin procesar.
ms.assetid: b3b6c4d1-5fa3-41fb-ae1d-067638e385b0
title: Inspección de seguimientos de red para los metadatos HTTP Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e653b0852f84382873973cd63fbd3223a245dd4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966968"
---
# <a name="inspecting-network-traces-for-http-metadata-exchange"></a>Inspección de seguimientos de red para los metadatos HTTP Exchange

Cualquier analizador de paquetes de red que pueda mostrar paquetes sin procesar se puede usar para inspeccionar las solicitudes de intercambio de metadatos HTTP. Monitor de red de Microsoft 3 (Netmon) se recomienda. Para obtener más información sobre Netmon, consulte [Descarga de netmon y filtros DPWS de ejemplo.](downloading-netmon-and-sample-dpws-filters.md)

Este procedimiento de diagnóstico puede no ser tan útil para los clientes y hosts que usan un canal seguro para las comunicaciones porque el contenido del mensaje está cifrado.

**Para inspeccionar los seguimientos de red para el intercambio de metadatos HTTP**

1.  Configure el host y el cliente para que se ejecuten a través de la red (es decir, asegúrese de que el host y el cliente funcionarán en equipos diferentes).
2.  Instale el analizador de paquetes (Netmon) en el cliente o el host.
3.  Configure el analizador de paquetes para capturar el tráfico en el adaptador de red que conecta el host y el cliente.
4.  Reproduzca el error iniciando el host y el cliente o presionando F5 en el Explorador de red.
5.  Filtre los resultados para aislar WS-Discovery tráfico de intercambio de metadatos. Para ver los filtros de Netmon de ejemplo, consulte [Descarga de netmon y filtros DPWS de ejemplo.](downloading-netmon-and-sample-dpws-filters.md)
    > [!Note]  
    > Este paso es opcional.

     

6.  Compruebe que los mensajes enviados entre el cliente y el host cumplen los requisitos básicos de tráfico.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Comprobación de que los mensajes cumplen los requisitos de tráfico

Los clientes y hosts de WSDAPI deben enviar mensajes que cumplan los criterios siguientes. Para obtener información general sobre los patrones de mensaje, vea [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md).

-   Los mensajes deben cumplir los requisitos de tráfico proporcionados en el tema [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md)( Inspeccionar seguimientos de red para la detección de WS de UDP), a menos que esté absolutamente seguro de que WS-Discovery no se está usando para el intercambio de metadatos.
-   Se debe establecer una conexión TCP entre el cliente y la primera dirección de transporte proporcionada en el elemento **XAddrs** de un [mensaje ProbeMatches](probematches-message.md) o [ResolveMatches.](resolvematches-message.md) En la lista siguiente se muestra un intercambio de paquetes típico que se usa para establecer una conexión TCP.
    -   El cliente envía un paquete TCP SYN al host en un puerto especificado.
    -   El host envía un paquete TCP SYN/ACK al cliente.
    -   El cliente envía un paquete TCP ACK al host en un puerto especificado.

    Una vez que el cliente ha enviado un paquete TCP ACK, se establece la conexión TCP. Tenga en cuenta que este intercambio de mensajes no se producirá si se ha establecido previamente una conexión TCP.
-   El cliente debe enviar una solicitud [HTTP Get](get--metadata-exchange--http-request-and-message.md) y un mensaje válidos.
-   El host debe estar escuchando en la ruta de acceso URL especificada en la [solicitud Get](get--metadata-exchange--http-request-and-message.md) HTTP.
-   El **elemento To** de un mensaje [Get](get--metadata-exchange--http-request-and-message.md) metadata debe estar presente y no estar vacío. El valor del elemento **To** debe coincidir con una de las direcciones de punto de conexión del host. La dirección del punto de conexión de un host se anuncia normalmente en un [mensaje ProbeMatches](probematches-message.md) o [ResolveMatches.](resolvematches-message.md)
-   El host debe enviar un encabezado de respuesta HTTP válido. Si la solicitud inicial se ha realizado correctamente, el encabezado de respuesta debe contener el código de estado HTTP/1.1 200.
-   El host debe enviar un mensaje [GetResponse](getresponse--metadata-exchange--message.md) válido.
-   El **elemento RelatesTo** de un [mensaje GetResponse](getresponse--metadata-exchange--message.md) debe estar presente y no debe estar vacío. Su valor debe coincidir con el valor del **elemento MessageId** del mensaje [Get](get--metadata-exchange--http-request-and-message.md) correspondiente.

Si las solicitudes HTTP o los mensajes de intercambio de metadatos enviados por el programa no cumplen estos requisitos de tráfico, la causa del problema se ha identificado correctamente y no es necesario realizar más pasos de solución de problemas. Vuelva a escribir el programa para que genere mensajes y solicitudes compatibles y vuelva a probar el programa.

Si el origen del problema todavía no se puede identificar, póngase en contacto con el soporte técnico de Microsoft para obtener ayuda. Antes de ponerse en contacto con el soporte técnico, recopile los archivos de registro adecuados para ayudar a identificar la causa principal del problema. Para obtener más información, vea [Habilitación del seguimiento de WSDAPI.](enabling-wsdapi-tracing.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Tareas iniciales solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Descarga de netmon y filtros DPWS de ejemplo](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 




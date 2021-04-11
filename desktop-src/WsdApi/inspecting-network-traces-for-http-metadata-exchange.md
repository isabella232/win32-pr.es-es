---
description: Cualquier analizador de paquetes de red que pueda mostrar paquetes sin procesar se puede usar para inspeccionar las solicitudes de intercambio de metadatos HTTP. Se recomienda Monitor de red de Microsoft 3 (Netmon). Para obtener más información acerca de Netmon, consulte descarga de los filtros Netmon y DPWS de ejemplo.
ms.assetid: b3b6c4d1-5fa3-41fb-ae1d-067638e385b0
title: Inspeccionando seguimientos de red para el intercambio de metadatos HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9993c542789b7f11eb35344dd6b0b03bfbafc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276235"
---
# <a name="inspecting-network-traces-for-http-metadata-exchange"></a>Inspeccionando seguimientos de red para el intercambio de metadatos HTTP

Cualquier analizador de paquetes de red que pueda mostrar paquetes sin procesar se puede usar para inspeccionar las solicitudes de intercambio de metadatos HTTP. Se recomienda Monitor de red de Microsoft 3 (Netmon). Para obtener más información acerca de Netmon, consulte [descarga de los filtros Netmon y DPWS de ejemplo](downloading-netmon-and-sample-dpws-filters.md).

Este procedimiento de diagnóstico puede no ser tan útil para los clientes y hosts que usan un canal seguro para las comunicaciones porque el contenido del mensaje está cifrado.

**Para inspeccionar los seguimientos de red para el intercambio de metadatos HTTP**

1.  Configure el host y el cliente para que se ejecuten en la red (es decir, asegúrese de que el host y el cliente funcionarán en equipos diferentes).
2.  Instale el analizador de paquetes (Netmon) en el cliente o en el host.
3.  Configure el analizador de paquetes para capturar el tráfico en el adaptador de red que conecta el host y el cliente.
4.  Reproduzca el error iniciando el host y el cliente, o presionando F5 en el explorador de red.
5.  Filtre los resultados para aislar WS-Discovery y el tráfico de intercambio de metadatos. Para ver los filtros de ejemplo de Netmon, consulte [descarga de los filtros Netmon y DPWS de ejemplo](downloading-netmon-and-sample-dpws-filters.md).
    > [!Note]  
    > Este paso es opcional.

     

6.  Compruebe que los mensajes enviados entre el cliente y el host cumplan los requisitos de tráfico básicos.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Comprobando que los mensajes cumplen los requisitos de tráfico

Los clientes y hosts WSDAPI deben enviar mensajes que cumplan los criterios siguientes. Para obtener información general acerca de los patrones de mensajes, consulte [patrones de mensajes de intercambio de metadatos y detección](discovery-and-metadata-exchange-message-patterns.md).

-   Los mensajes deben cumplir los requisitos de tráfico que se proporcionan en el tema [inspeccionando los seguimientos de red para WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md), a menos que esté absolutamente seguro de que WS-Discovery no se utiliza para el intercambio de metadatos.
-   Se debe establecer una conexión TCP entre el cliente y la primera dirección de transporte proporcionada en el elemento **XAddrs** de un mensaje [ProbeMatches](probematches-message.md) o [ResolveMatches](resolvematches-message.md) . La siguiente lista muestra un intercambio de paquetes típico que se usa para establecer una conexión TCP.
    -   El cliente envía un paquete TCP SYN al host en un puerto especificado.
    -   El host envía un paquete TCP SYN/ACK al cliente.
    -   El cliente envía un paquete de confirmación TCP al host en un puerto especificado.

    Una vez que el cliente ha enviado un paquete de confirmación TCP, se establece la conexión TCP. Tenga en cuenta que este intercambio de mensajes no se producirá si se ha establecido previamente una conexión TCP.
-   El cliente debe enviar un mensaje y una solicitud HTTP [Get](get--metadata-exchange--http-request-and-message.md) válidos.
-   El host debe estar escuchando en la ruta de acceso de la dirección URL especificada en la solicitud [Get](get--metadata-exchange--http-request-and-message.md) http.
-   El elemento **to** de un mensaje [Get](get--metadata-exchange--http-request-and-message.md) Metadata debe estar presente y no estar vacío. El valor del elemento **to** debe coincidir con una de las direcciones de punto de conexión del host. La dirección del punto de conexión de un host se anuncia normalmente en un mensaje [ProbeMatches](probematches-message.md) o [ResolveMatches](resolvematches-message.md) .
-   El host debe enviar un encabezado de respuesta HTTP válido. Si la solicitud inicial se realizó correctamente, el encabezado de respuesta debe contener el código de Estado HTTP/1.1 200.
-   El host debe enviar un mensaje de [GetResponse](getresponse--metadata-exchange--message.md) válido.
-   El **elemento** de la reutilización de un mensaje [GetResponse](getresponse--metadata-exchange--message.md) debe estar presente y no debe estar vacío. Su valor debe coincidir con el valor del elemento **MessageId** del mensaje [Get](get--metadata-exchange--http-request-and-message.md) correspondiente.

Si las solicitudes HTTP o los mensajes de intercambio de metadatos enviados por el programa no cumplen estos requisitos de tráfico, la causa del problema se ha identificado correctamente y no es necesario realizar más pasos de solución de problemas. Vuelva a escribir el programa para que genere mensajes y solicitudes compatibles y vuelva a probar el programa.

Si aún no se puede identificar el origen del problema, póngase en contacto con el soporte técnico de Microsoft para obtener ayuda. Antes de ponerse en contacto con el servicio de soporte técnico, recopile los archivos de registro adecuados para ayudar a identificar la causa principal del problema. Para obtener más información, vea [Habilitar el seguimiento de WSDAPI](enabling-wsdapi-tracing.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introducción con la solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Descarga de los filtros Netmon y DPWS de ejemplo](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 




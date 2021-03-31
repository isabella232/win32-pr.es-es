---
description: Cualquier analizador de paquetes de red que pueda mostrar paquetes sin procesar se puede usar para inspeccionar los paquetes de WS-Discovery UDP. Se recomienda Monitor de red de Microsoft 3 (Netmon). Para obtener más información acerca de Netmon, consulte descarga de los filtros Netmon y DPWS de ejemplo.
ms.assetid: f12f9847-b87f-4d5f-bee3-4d219f9ad898
title: Inspeccionando seguimientos de red para WS-Discovery UDP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85f4acd79588ef48c7f8e1ace2a44c9a3458475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277118"
---
# <a name="inspecting-network-traces-for-udp-ws-discovery"></a>Inspeccionando seguimientos de red para WS-Discovery UDP

Cualquier analizador de paquetes de red que pueda mostrar paquetes sin procesar se puede usar para inspeccionar los paquetes de WS-Discovery UDP. Se recomienda Monitor de red de Microsoft 3 (Netmon). Para obtener más información acerca de Netmon, consulte [descarga de los filtros Netmon y DPWS de ejemplo](downloading-netmon-and-sample-dpws-filters.md).

**Para inspeccionar los seguimientos de red para WS-Discovery de UDP**

1.  Configure el host y el cliente para que se ejecuten en la red (es decir, asegúrese de que el host y el cliente funcionarán en equipos diferentes).
2.  Instale el analizador de paquetes (Netmon) en el cliente o en el host.
3.  Configure el analizador de paquetes para capturar el tráfico en el adaptador de red que conecta el host y el cliente.
4.  Reproduzca el error iniciando el host y el cliente, o presionando F5 en el explorador de red.
5.  Filtre los resultados para aislar WS-Discovery tráfico. Para ver los filtros de ejemplo de Netmon, consulte [descarga de los filtros Netmon y DPWS de ejemplo](downloading-netmon-and-sample-dpws-filters.md).
    > [!Note]  
    > Este paso es opcional.

     

6.  Compruebe que los mensajes enviados entre el cliente y el host cumplan los requisitos de tráfico básicos.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Comprobando que los mensajes cumplen los requisitos de tráfico

Los clientes y hosts WSDAPI deben enviar mensajes que cumplan los criterios siguientes. Para obtener información general acerca de los patrones de mensajes, consulte [patrones de mensajes de intercambio de metadatos y detección](discovery-and-metadata-exchange-message-patterns.md).

-   Los mensajes de [sondeo](probe-message.md) se deben enviar mediante multidifusión de UDP al puerto 3702.
-   El elemento **Types** de un mensaje de [sondeo](probe-message.md) debe estar presente y no debe estar vacío. Debe contener los tipos a los que responderá un host.
-   Un mensaje [ProbeMatches](probematches-message.md) se debe enviar a través de unidifusión al puerto UDP desde el que se envió el [sondeo](probe-message.md) .
-   El **elemento de** la reutilización de un mensaje [ProbeMatches](probematches-message.md) debe estar presente y no debe estar vacío. Su valor debe coincidir con el valor del elemento **MessageId** del mensaje de [sondeo](probe-message.md) correspondiente.
-   Si se incluyó un elemento **XAddrs** en el mensaje [ProbeMatches](probematches-message.md) , se deben validar las direcciones de transporte proporcionadas. Para obtener más información, consulte [reglas de validación de XAddr](xaddr-validation-rules.md).
-   Se debe enviar un mensaje [ProbeMatches](probematches-message.md) en los 4 segundos del mensaje de [sondeo](probe-message.md) correspondiente. El Firewall de Windows puede quitar un mensaje ProbeMatches enviado más de 4 segundos después de un mensaje de sondeo.
-   Si no se incluyó ningún elemento **XAddrs** en el mensaje [ProbeMatches](probematches-message.md) y el cliente o el host enviará un mensaje http (como una [solicitud de intercambio de metadatos o](get--metadata-exchange--http-request-and-message.md) un mensaje de servicio), el cliente o host debe enviar un mensaje de [resolución](resolve-message.md) por multidifusión de UDP al puerto 3702.
-   Si se envía un mensaje de [resolución](resolve-message.md) , se debe enviar un mensaje de [ResolveMatches](resolvematches-message.md) de unidifusión al puerto UDP desde el que se envió el mensaje de resolución.
-   Se debe enviar un mensaje [ResolveMatches](resolvematches-message.md) en los 4 segundos del mensaje de [resolución](resolve-message.md) correspondiente. El Firewall de Windows puede quitar un ResolveMatchesmessage enviado más de 4 segundos después de un mensaje de resolución.

Si los mensajes enviados por el programa no se ajustan a estos requisitos de mensaje, la causa del problema se ha identificado correctamente y no es necesario realizar más pasos para la solución de problemas. Vuelva a escribir el programa para que genere mensajes conformes y vuelva a probar el programa.

Si aún no se puede identificar el origen del problema, póngase en contacto con el soporte técnico de Microsoft para obtener ayuda. Antes de ponerse en contacto con el servicio de soporte técnico, recopile los archivos de registro adecuados para ayudar a identificar la causa principal del problema. Para obtener más información, vea [Habilitar el seguimiento de WSDAPI](enabling-wsdapi-tracing.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introducción con la solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Descarga de los filtros Netmon y DPWS de ejemplo](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 




---
description: Cualquier analizador de paquetes de red que pueda mostrar paquetes sin procesar se puede usar para inspeccionar los paquetes UDP WS-Discovery paquetes. Monitor de red de Microsoft 3 (Netmon) se recomienda. Para obtener más información sobre Netmon, consulte Descarga de netmon y filtros DPWS de ejemplo.
ms.assetid: f12f9847-b87f-4d5f-bee3-4d219f9ad898
title: Inspección de seguimientos de red para la conexión UDP WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce21e2943a37640eb091aa03c02eba0886164166b2959e31e897ee788424cd41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117920759"
---
# <a name="inspecting-network-traces-for-udp-ws-discovery"></a>Inspección de seguimientos de red para la conexión UDP WS-Discovery

Cualquier analizador de paquetes de red que pueda mostrar paquetes sin procesar se puede usar para inspeccionar los paquetes UDP WS-Discovery paquetes. Monitor de red de Microsoft 3 (Netmon) se recomienda. Para obtener más información sobre Netmon, consulte [Descarga de netmon y filtros DPWS de ejemplo.](downloading-netmon-and-sample-dpws-filters.md)

**Para inspeccionar los seguimientos de red para la detección de WS de UDP**

1.  Configure el host y el cliente para que se ejecuten a través de la red (es decir, asegúrese de que el host y el cliente funcionarán en equipos diferentes).
2.  Instale el analizador de paquetes (Netmon) en el cliente o el host.
3.  Configure el analizador de paquetes para capturar el tráfico en el adaptador de red que conecta el host y el cliente.
4.  Reproduzca el error iniciando el host y el cliente o presionando F5 en el Explorador de red.
5.  Filtre los resultados para aislar WS-Discovery tráfico. Para ver los filtros netmon de ejemplo, consulte [Descarga de netmon y filtros DPWS de ejemplo.](downloading-netmon-and-sample-dpws-filters.md)
    > [!Note]  
    > Este paso es opcional.

     

6.  Compruebe que los mensajes enviados entre el cliente y el host cumplen los requisitos básicos de tráfico.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Comprobación de que los mensajes cumplen los requisitos de tráfico

Los clientes y hosts de WSDAPI deben enviar mensajes que cumplan los criterios siguientes. Para obtener información general sobre los patrones de mensaje, vea [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md).

-   [Los mensajes](probe-message.md) de sondeo deben enviarse mediante multidifusión UDP al puerto 3702.
-   El **elemento Types** de un mensaje [probe](probe-message.md) debe estar presente y no debe estar vacío. Debe contener los tipos a los que responderá un host.
-   Se debe enviar un mensaje [ProbeMatches](probematches-message.md) unidifusión al puerto UDP desde el [que](probe-message.md) se envió el sondeo.
-   El **elemento RelatesTo** de un [mensaje ProbeMatches](probematches-message.md) debe estar presente y no debe estar vacío. Su valor debe coincidir con el valor del **elemento MessageId** del mensaje [probe](probe-message.md) correspondiente.
-   Si se **incluyó un elemento XAddrs** en el mensaje [ProbeMatches,](probematches-message.md) se deben validar las direcciones de transporte proporcionadas. Para obtener más información, vea [Reglas de validación de XAddr](xaddr-validation-rules.md).
-   Un [mensaje ProbeMatches](probematches-message.md) debe enviarse en un plazo de 4 segundos desde el mensaje [de sondeo](probe-message.md) correspondiente. El Windows firewall puede quitar un mensaje ProbeMatches enviado más de 4 segundos después de un mensaje de sondeo.
-   Si no se incluyó ningún elemento **XAddrs** en el mensaje [ProbeMatches](probematches-message.md) y el cliente o host enviará un mensaje HTTP (por ejemplo, una solicitud get [metadata](get--metadata-exchange--http-request-and-message.md) exchange o un mensaje de servicio), el cliente o host debe enviar un mensaje [resolve](resolve-message.md) mediante multidifusión UDP al puerto 3702.
-   Si se [envía un](resolve-message.md) mensaje Resolver, se debe enviar un mensaje [ResolveMatches](resolvematches-message.md) unidifusión al puerto UDP desde el que se envió el mensaje Resolver.
-   Un [mensaje ResolveMatches](resolvematches-message.md) debe enviarse en un plazo de 4 segundos desde el mensaje [Resolve](resolve-message.md) correspondiente. El Windows firewall puede quitar un mensaje ResolveMatchesmessage enviado más de 4 segundos después de un mensaje resolver.

Si los mensajes enviados por el programa no cumplen estos requisitos de mensaje, la causa del problema se ha identificado correctamente y no es necesario realizar más pasos de solución de problemas. Vuelva a escribir el programa para que genere mensajes compatibles y vuelva a probar el programa.

Si el origen del problema todavía no se puede identificar, póngase en contacto con el soporte técnico de Microsoft para obtener ayuda. Antes de ponerse en contacto con el soporte técnico, recopile los archivos de registro adecuados para ayudar a identificar la causa principal del problema. Para obtener más información, vea Habilitación del seguimiento [de WSDAPI.](enabling-wsdapi-tracing.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Tareas iniciales solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Descarga de netmon y filtros DPWS de ejemplo](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 




---
description: Obtenga información sobre la inspección de seguimientos de red mediante la detección directa. Un analizador de paquetes de red que muestra paquetes sin procesar puede inspeccionar las solicitudes de intercambio de metadatos HTTP.
ms.assetid: 9b124117-06e7-4637-9863-0f9650861526
title: Inspección de seguimientos de red para aplicaciones mediante la detección dirigida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f8e96778b2d75f511c625073ef1d0bbc30dd4c815a327f42432abd0d221756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991735"
---
# <a name="inspecting-network-traces-for-applications-using-directed-discovery"></a>Inspección de seguimientos de red para aplicaciones mediante la detección dirigida

Cualquier analizador de paquetes de red que pueda mostrar paquetes sin procesar se puede usar para inspeccionar las solicitudes de intercambio de metadatos HTTP. Monitor de red de Microsoft 3 (Netmon) se recomienda. Para obtener más información sobre Netmon, vea [Descarga de netmon y filtros de DPWS de ejemplo.](downloading-netmon-and-sample-dpws-filters.md)

**Para inspeccionar los seguimientos de red para la detección dirigida**

1.  Configure el host y el cliente para que se ejecuten a través de la red (es decir, asegúrese de que el host y el cliente funcionarán en equipos diferentes).
2.  Instale el analizador de paquetes (Netmon) en el cliente o en el host.
3.  Configure el analizador de paquetes para capturar el tráfico en el adaptador de red que conecta el host y el cliente.
4.  Reproduzca el error iniciando el host y el cliente o presionando F5 en el Explorador de red.
5.  Filtre los resultados para aislar el tráfico WS-Discovery y el intercambio de metadatos. Para ver los filtros de Netmon de ejemplo, consulte [Descarga de netmon y filtros DE DPWS de ejemplo.](downloading-netmon-and-sample-dpws-filters.md)
    > [!Note]  
    > Este paso es opcional.

     

6.  Compruebe que los mensajes enviados entre el cliente y el host cumplen los requisitos básicos de tráfico.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Comprobación de que los mensajes cumplen los requisitos de tráfico

Los clientes y hosts de WSDAPI deben enviar mensajes que cumplan los criterios siguientes. Para obtener información general sobre los patrones de mensaje, vea [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md).

-   [Los](probe-message.md) mensajes de sondeo deben enviarse mediante HTTP o HTTPS, normalmente al puerto 5357 o 5358.
-   El **elemento Types** de un mensaje [probe](probe-message.md) debe estar presente y no debe estar vacío. Debe contener los tipos a los que responderá un host.
-   Se [debe enviar un mensaje ProbeMatches](probematches-message.md) al puerto HTTP o HTTPS desde el que se envió el sondeo. [](probe-message.md)
-   El **elemento RelatesTo** de un [mensaje ProbeMatches](probematches-message.md) debe estar presente y no debe estar vacío. Su valor debe coincidir con el valor del **elemento MessageId** del mensaje [Probe](probe-message.md) correspondiente.
-   Si se **incluyó un elemento XAddrs** en el [mensaje ProbeMatches,](probematches-message.md) se deben validar las direcciones de transporte proporcionadas. Para obtener más información, vea [Reglas de validación de XAddr](xaddr-validation-rules.md).
-   Un [mensaje ProbeMatches](probematches-message.md) debe enviarse en un plazo de 4 segundos desde el mensaje [de sondeo](probe-message.md) correspondiente. El Windows firewall puede quitar un mensaje ProbeMatches enviado más de 4 segundos después de un mensaje de sondeo.
-   Si no se incluyó ningún elemento **XAddrs** en el mensaje [ProbeMatches](probematches-message.md) y [](get--metadata-exchange--http-request-and-message.md) el cliente o host enviará un mensaje HTTP (por ejemplo, una solicitud de intercambio de metadatos Get o un mensaje de servicio), el cliente o host debe enviar un mensaje [Resolve](resolve-message.md) mediante HTTP o HTTPS. Este mensaje normalmente se envía al puerto 5357 o 5358.
-   Si se [envía un](resolve-message.md) mensaje Resolver, se debe enviar un mensaje [ResolveMatches](resolvematches-message.md) al puerto HTTP o HTTPS desde el que se envió el mensaje Resolver.
-   Se [debe enviar un mensaje ResolveMatches](resolvematches-message.md) en un plazo de 4 segundos desde el mensaje [Resolve](resolve-message.md) correspondiente. El Windows firewall puede quitar un mensaje ResolveMatches enviado más de 4 segundos después de un mensaje resolver.

Si los mensajes enviados por el programa no cumplen estos requisitos de mensaje, la causa del problema se ha identificado correctamente y no es necesario realizar más pasos de solución de problemas. Vuelva a escribir el programa para que genere mensajes compatibles y vuelva a probar el programa.

Si el origen del problema todavía no se puede identificar, póngase en contacto con el soporte técnico de Microsoft para obtener ayuda. Antes de ponerse en contacto con el soporte técnico, recopile los archivos de registro adecuados para ayudar a identificar la causa principal del problema. Para obtener más información, vea [Habilitación del seguimiento de WSDAPI.](enabling-wsdapi-tracing.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de aplicaciones mediante la detección dirigida](troubleshooting-applications-using-directed-discovery.md)
</dt> <dt>

[Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Tareas iniciales solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Descarga de netmon y filtros DPWS de ejemplo](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 




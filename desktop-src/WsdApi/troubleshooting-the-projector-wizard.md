---
description: Enumera los procedimientos de diagnóstico que se deben usar al solucionar problemas del asistente de proyector.
ms.assetid: 54efc88c-0b8e-4652-8655-817a288863d1
title: Solución de problemas del asistente de proyector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3776e86d3a156fa86873900aa9e804df9830ec64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696359"
---
# <a name="troubleshooting-the-projector-wizard"></a>Solución de problemas del asistente de proyector

Asistente para proyector:

-   Usa siempre WS-Discovery UDP para la detección de dispositivos
-   Siempre usa HTTP para el intercambio de metadatos
-   A veces usa el descubrimiento dirigido

Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con el Asistente para proyector.

**Para solucionar problemas del Asistente para proyector**

1.  Si se usa la detección dirigida, [solucione los problemas de detección dirigida](troubleshooting-applications-using-directed-discovery.md).
2.  [Inspeccione la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md).
3.  [Use un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).
4.  [Use el cliente de depuración WSD para comprobar el tráfico de multidifusión](using-wsddebug-client-to-verify-multicast-traffic.md).
5.  [Inspeccione los seguimientos de red para WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).
6.  [Usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
7.  [Use el registro de WinHTTP para comprobar el tráfico de obtención](using-winhttp-logging-to-verify-get-traffic.md).
8.  [Inspeccione los seguimientos de red para el intercambio de metadatos http](inspecting-network-traces-for-http-metadata-exchange.md).

Si el origen del problema no se puede identificar mediante los procedimientos de diagnóstico anteriores, siga las instrucciones de [habilitación del seguimiento de WSDAPI](enabling-wsdapi-tracing.md) y póngase en contacto con el soporte técnico de Microsoft.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con la solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 




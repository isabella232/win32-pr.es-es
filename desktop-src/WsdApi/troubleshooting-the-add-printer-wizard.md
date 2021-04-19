---
description: Enumera los procedimientos de diagnóstico que se deben usar al solucionar problemas del Asistente para agregar impresoras.
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: Solucionar problemas del Asistente para agregar impresoras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b0054758e3ec721598ad279a073a32862af368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696898"
---
# <a name="troubleshooting-the-add-printer-wizard"></a>Solucionar problemas del Asistente para agregar impresoras

Asistente para agregar impresoras:

-   Usa siempre WS-Discovery UDP para la detección de dispositivos
-   Siempre inicia una conexión HTTP o HTTPS para el intercambio de metadatos
-   A veces usa el descubrimiento dirigido
-   A veces, usa un canal seguro (HTTPS) para el intercambio de metadatos

Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con el Asistente para agregar impresoras.

**Para solucionar problemas del Asistente para agregar impresoras**

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
</dt> <dt>

[Solución de problemas de aplicaciones con la detección dirigida](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 




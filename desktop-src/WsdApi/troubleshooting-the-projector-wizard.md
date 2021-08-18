---
description: Enumera los procedimientos de diagnóstico que se usarán al solucionar problemas del Asistente para proyectores.
ms.assetid: 54efc88c-0b8e-4652-8655-817a288863d1
title: Solución de problemas del Asistente para proyectores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5767e9827174d2d8135ac6dfb96c335d49acb82f0a0162b06f22a89c4dbdebef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856075"
---
# <a name="troubleshooting-the-projector-wizard"></a>Solución de problemas del Asistente para proyectores

Asistente para proyector:

-   Siempre usa udp WS-Discovery para la detección de dispositivos
-   Siempre usa HTTP para el intercambio de metadatos
-   A veces usa la detección dirigida

Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con el Asistente para proyectores.

**Para solucionar problemas del Asistente para proyectores**

1.  Si se usa la detección dirigida, [solucione problemas de detección dirigida.](troubleshooting-applications-using-directed-discovery.md)
2.  [Inspeccione la configuración del adaptador y del firewall.](inspecting-adapter-and-firewall-settings.md)
3.  [Use un host y un cliente genéricos para UDP WS-Discovery.](using-a-generic-host-and-client-for-udp-ws-discovery.md)
4.  [Use el cliente de depuración de WSD para comprobar el tráfico de multidifusión.](using-wsddebug-client-to-verify-multicast-traffic.md)
5.  [Inspeccione los seguimientos de red de UDP WS-Discovery.](inspecting-network-traces-for-udp-ws-discovery.md)
6.  [Use un host y un cliente genéricos para el intercambio de metadatos HTTP.](using-a-generic-host-and-client-for-http-metadata-exchange.md)
7.  [Use el registro winHTTP para comprobar que obtiene el tráfico.](using-winhttp-logging-to-verify-get-traffic.md)
8.  [Inspeccione los seguimientos de red para el intercambio de metadatos HTTP.](inspecting-network-traces-for-http-metadata-exchange.md)

Si el origen del problema no se puede identificar mediante los procedimientos de diagnóstico anteriores, siga las instrucciones de Habilitación del seguimiento de [WSDAPI](enabling-wsdapi-tracing.md) y póngase en contacto con el soporte técnico de Microsoft.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 




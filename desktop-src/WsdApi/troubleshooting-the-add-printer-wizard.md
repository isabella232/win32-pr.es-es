---
description: Enumera los procedimientos de diagnóstico que se deben usar al solucionar problemas del Asistente para agregar impresoras.
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: Solución de problemas del Asistente para agregar impresoras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6c6971108b0f6fb46a373be47943a3ccbc7fcd97b830733c139653f991debd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860055"
---
# <a name="troubleshooting-the-add-printer-wizard"></a>Solución de problemas del Asistente para agregar impresoras

Asistente para agregar impresoras:

-   Siempre usa udp WS-Discovery la detección de dispositivos
-   Siempre inicia una conexión HTTP o HTTPS para el intercambio de metadatos
-   A veces usa la detección dirigida
-   A veces usa un canal seguro (HTTPS) para el intercambio de metadatos.

Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con el Asistente para agregar impresoras.

**Para solucionar problemas del Asistente para agregar impresoras**

1.  Si se usa la detección dirigida, [solucione problemas de detección dirigida.](troubleshooting-applications-using-directed-discovery.md)
2.  [Inspeccione la configuración del adaptador y del firewall.](inspecting-adapter-and-firewall-settings.md)
3.  [Use un host y un cliente genéricos para UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
4.  [Use el cliente de depuración de WSD para comprobar el tráfico de multidifusión.](using-wsddebug-client-to-verify-multicast-traffic.md)
5.  [Inspeccione los seguimientos de red de UDP WS-Discovery.](inspecting-network-traces-for-udp-ws-discovery.md)
6.  [Use un host y un cliente genéricos para el intercambio de metadatos HTTP.](using-a-generic-host-and-client-for-http-metadata-exchange.md)
7.  [Use el registro WinHTTP para comprobar que obtiene el tráfico.](using-winhttp-logging-to-verify-get-traffic.md)
8.  [Inspeccione los seguimientos de red para el intercambio de metadatos HTTP.](inspecting-network-traces-for-http-metadata-exchange.md)

Si el origen del problema no se puede identificar mediante los procedimientos de diagnóstico anteriores, siga las instrucciones de Habilitación del seguimiento de [WSDAPI](enabling-wsdapi-tracing.md) y póngase en contacto con el soporte técnico de Microsoft.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Solución de problemas de aplicaciones mediante la detección dirigida](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 




---
description: Enumera los procedimientos de diagnóstico que se deben usar al solucionar problemas de Explorador de red.
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: Solución de problemas de Explorador de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a7c8e270fa3f1e07ce9b44fb9ce619d9fe5225e2c4d3ae87896d5e7cf20a2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120585"
---
# <a name="troubleshooting-the-network-explorer"></a>Solución de problemas de Explorador de red

El Explorador de red:

-   Siempre usa udp WS-Discovery para la detección de dispositivos
-   Inicia siempre una conexión HTTP o HTTPS para el intercambio de metadatos.
-   A veces usa un canal seguro (HTTPS) para el intercambio de metadatos

Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con el Explorador de red.

**Para solucionar problemas de Explorador de red**

1.  [Inspeccione la configuración del adaptador y del firewall.](inspecting-adapter-and-firewall-settings.md)
2.  [Use un host y un cliente genéricos para UDP WS-Discovery.](using-a-generic-host-and-client-for-udp-ws-discovery.md)
3.  [Use el cliente de depuración de WSD para comprobar el tráfico de multidifusión.](using-wsddebug-client-to-verify-multicast-traffic.md)
4.  [Inspeccione los seguimientos de red de UDP WS-Discovery.](inspecting-network-traces-for-udp-ws-discovery.md)
5.  [Use un host y un cliente genéricos para el intercambio de metadatos HTTP.](using-a-generic-host-and-client-for-http-metadata-exchange.md)
6.  [Use el registro winHTTP para comprobar que obtiene el tráfico.](using-winhttp-logging-to-verify-get-traffic.md)
7.  [Inspeccione los seguimientos de red para el intercambio de metadatos HTTP.](inspecting-network-traces-for-http-metadata-exchange.md)

El Explorador de red usa [la detección de funciones](/previous-versions/windows/desktop/fundisc/fd-portal) para enumerar los dispositivos de red. Para obtener más información sobre la solución de problemas, vea [Solución de problemas de clientes de detección de funciones.](troubleshooting-function-discovery-clients.md)

Si el origen del problema no se puede identificar mediante los procedimientos de diagnóstico anteriores, siga las instrucciones de Habilitación del seguimiento de [WSDAPI](enabling-wsdapi-tracing.md) y póngase en contacto con el soporte técnico de Microsoft.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Solución de problemas de clientes de detección de funciones](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 

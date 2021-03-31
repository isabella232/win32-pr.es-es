---
description: Enumera los procedimientos de diagnóstico que se deben usar al solucionar problemas del explorador de red.
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: Solución de problemas del explorador de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09afe7acbcb20d706c8645d84c68014b0e33d799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001133"
---
# <a name="troubleshooting-the-network-explorer"></a>Solución de problemas del explorador de red

El explorador de red:

-   Usa siempre WS-Discovery UDP para la detección de dispositivos
-   Siempre inicia una conexión HTTP o HTTPS para el intercambio de metadatos
-   A veces, usa un canal seguro (HTTPS) para el intercambio de metadatos

Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con el explorador de red.

**Para solucionar problemas del explorador de red**

1.  [Inspeccione la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md).
2.  [Use un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Use el cliente de depuración WSD para comprobar el tráfico de multidifusión](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Inspeccione los seguimientos de red para WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Use el registro de WinHTTP para comprobar el tráfico de obtención](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Inspeccione los seguimientos de red para el intercambio de metadatos http](inspecting-network-traces-for-http-metadata-exchange.md).

El explorador de red usa la [detección de funciones](/previous-versions/windows/desktop/fundisc/fd-portal) para enumerar los dispositivos de red. Para obtener más información sobre la solución de problemas, consulte [solución de problemas de clientes de detección de funciones](troubleshooting-function-discovery-clients.md).

Si el origen del problema no se puede identificar mediante los procedimientos de diagnóstico anteriores, siga las instrucciones de [habilitación del seguimiento de WSDAPI](enabling-wsdapi-tracing.md) y póngase en contacto con el soporte técnico de Microsoft.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con la solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Solución de problemas de clientes de detección de funciones](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 

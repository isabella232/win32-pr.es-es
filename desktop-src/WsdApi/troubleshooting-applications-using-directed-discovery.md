---
description: Las aplicaciones que usan la detección dirigida envían mensajes de sondeo a través de HTTP o HTTPS para detectar dispositivos.
ms.assetid: 599f5962-da91-4688-b333-a784f06581ed
title: Solución de problemas de aplicaciones WSDAPI mediante la detección dirigida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e58403ec7d77b2bd3d018f43e3f591820ee16334be5620b5d5c64b8f42e40815
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117920425"
---
# <a name="troubleshooting-wsdapi-applications-using-directed-discovery"></a>Solución de problemas de aplicaciones WSDAPI mediante la detección dirigida

Las aplicaciones que usan la detección dirigida envían [mensajes de](probe-message.md) sondeo a través de HTTP o HTTPS para detectar dispositivos. Los mensajes [ProbeMatches](probematches-message.md) correspondientes enviados en respuesta también se envían a través de HTTP o HTTPS. La detección dirigida se puede iniciar mediante el Asistente para agregar impresora, un cliente de detección de funciones o una aplicación WSDAPI. Los mensajes Probe y ProbeMatches son estructuralmente idénticos a los enviados a través de UDP. Los mensajes tienen como prefijo los encabezados HTTP o HTTPS adecuados.

Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con una aplicación mediante la detección dirigida.

**Para solucionar problemas de una aplicación WSDAPI mediante la detección dirigida**

1.  [Inspeccione la configuración del adaptador y del firewall.](inspecting-adapter-and-firewall-settings.md)
2.  [Use un host y un cliente genéricos para el intercambio de metadatos HTTP.](using-a-generic-host-and-client-for-http-metadata-exchange.md)
3.  [Use el registro winHTTP para comprobar que obtiene el tráfico.](using-winhttp-logging-to-verify-get-traffic.md)
4.  [Inspeccione los seguimientos de red de una aplicación mediante la detección dirigida](inspecting-network-traces-for-applications-using-directed-discovery.md).

Si el origen del problema no se puede identificar mediante los procedimientos de diagnóstico anteriores, siga las instrucciones de Habilitación del seguimiento de [WSDAPI](enabling-wsdapi-tracing.md) y póngase en contacto con el soporte técnico de Microsoft.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Solución de problemas del Asistente para agregar impresoras](troubleshooting-the-add-printer-wizard.md)
</dt> <dt>

[Solución de problemas de aplicaciones WSDAPI](troubleshooting-wsdapi-applications.md)
</dt> </dl>

 

 




---
description: Las aplicaciones que usan la detección dirigida envían mensajes de sondeo a través de HTTP o HTTPS para detectar dispositivos.
ms.assetid: 599f5962-da91-4688-b333-a784f06581ed
title: Solución de problemas de aplicaciones WSDAPI mediante la detección dirigida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34ebec44c58545c65a4ff04941c5f98c9bc047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544790"
---
# <a name="troubleshooting-wsdapi-applications-using-directed-discovery"></a>Solución de problemas de aplicaciones WSDAPI mediante la detección dirigida

Las aplicaciones que usan la detección dirigida envían mensajes de [sondeo](probe-message.md) a través de http o https para detectar dispositivos. Los mensajes [ProbeMatches](probematches-message.md) correspondientes enviados en respuesta también se envían a través de http o https. La detección dirigida se puede iniciar mediante el Asistente para agregar impresoras, un cliente de detección de funciones o una aplicación WSDAPI. Los mensajes probe y ProbeMatches son estructuralmente idénticos a los enviados a través de UDP. Los mensajes tienen como prefijo los encabezados HTTP o HTTPS adecuados.

Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con una aplicación mediante la detección dirigida.

**Para solucionar problemas de una aplicación WSDAPI mediante la detección dirigida**

1.  [Inspeccione la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md).
2.  [Usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Use el registro de WinHTTP para comprobar el tráfico de obtención](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Inspeccione los seguimientos de red para una aplicación mediante la detección dirigida](inspecting-network-traces-for-applications-using-directed-discovery.md).

Si el origen del problema no se puede identificar mediante los procedimientos de diagnóstico anteriores, siga las instrucciones de [habilitación del seguimiento de WSDAPI](enabling-wsdapi-tracing.md) y póngase en contacto con el soporte técnico de Microsoft.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con la solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Solucionar problemas del Asistente para agregar impresoras](troubleshooting-the-add-printer-wizard.md)
</dt> <dt>

[Solución de problemas de aplicaciones WSDAPI](troubleshooting-wsdapi-applications.md)
</dt> </dl>

 

 




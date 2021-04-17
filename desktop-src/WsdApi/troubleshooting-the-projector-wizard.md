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
# <a name="troubleshooting-the-projector-wizard"></a><span data-ttu-id="e6043-103">Solución de problemas del asistente de proyector</span><span class="sxs-lookup"><span data-stu-id="e6043-103">Troubleshooting the Projector Wizard</span></span>

<span data-ttu-id="e6043-104">Asistente para proyector:</span><span class="sxs-lookup"><span data-stu-id="e6043-104">The Projector Wizard:</span></span>

-   <span data-ttu-id="e6043-105">Usa siempre WS-Discovery UDP para la detección de dispositivos</span><span class="sxs-lookup"><span data-stu-id="e6043-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="e6043-106">Siempre usa HTTP para el intercambio de metadatos</span><span class="sxs-lookup"><span data-stu-id="e6043-106">Always uses HTTP for metadata exchange</span></span>
-   <span data-ttu-id="e6043-107">A veces usa el descubrimiento dirigido</span><span class="sxs-lookup"><span data-stu-id="e6043-107">Sometimes uses directed discovery</span></span>

<span data-ttu-id="e6043-108">Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con el Asistente para proyector.</span><span class="sxs-lookup"><span data-stu-id="e6043-108">The following diagnostic procedures should be used (in order) to help identify problems with the Projector Wizard.</span></span>

<span data-ttu-id="e6043-109">**Para solucionar problemas del Asistente para proyector**</span><span class="sxs-lookup"><span data-stu-id="e6043-109">**To troubleshoot the Projector Wizard**</span></span>

1.  <span data-ttu-id="e6043-110">Si se usa la detección dirigida, [solucione los problemas de detección dirigida](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="e6043-110">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="e6043-111">[Inspeccione la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="e6043-111">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="e6043-112">[Use un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="e6043-112">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="e6043-113">[Use el cliente de depuración WSD para comprobar el tráfico de multidifusión](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="e6043-113">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="e6043-114">[Inspeccione los seguimientos de red para WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="e6043-114">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="e6043-115">[Usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="e6043-115">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="e6043-116">[Use el registro de WinHTTP para comprobar el tráfico de obtención](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="e6043-116">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="e6043-117">[Inspeccione los seguimientos de red para el intercambio de metadatos http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="e6043-117">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="e6043-118">Si el origen del problema no se puede identificar mediante los procedimientos de diagnóstico anteriores, siga las instrucciones de [habilitación del seguimiento de WSDAPI](enabling-wsdapi-tracing.md) y póngase en contacto con el soporte técnico de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e6043-118">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6043-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e6043-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6043-120">Introducción con la solución de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="e6043-120">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 




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
# <a name="troubleshooting-the-add-printer-wizard"></a><span data-ttu-id="beec6-103">Solucionar problemas del Asistente para agregar impresoras</span><span class="sxs-lookup"><span data-stu-id="beec6-103">Troubleshooting the Add Printer Wizard</span></span>

<span data-ttu-id="beec6-104">Asistente para agregar impresoras:</span><span class="sxs-lookup"><span data-stu-id="beec6-104">The Add Printer Wizard:</span></span>

-   <span data-ttu-id="beec6-105">Usa siempre WS-Discovery UDP para la detección de dispositivos</span><span class="sxs-lookup"><span data-stu-id="beec6-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="beec6-106">Siempre inicia una conexión HTTP o HTTPS para el intercambio de metadatos</span><span class="sxs-lookup"><span data-stu-id="beec6-106">Always initiates a HTTP or HTTPS connection for metadata exchange</span></span>
-   <span data-ttu-id="beec6-107">A veces usa el descubrimiento dirigido</span><span class="sxs-lookup"><span data-stu-id="beec6-107">Sometimes uses directed discovery</span></span>
-   <span data-ttu-id="beec6-108">A veces, usa un canal seguro (HTTPS) para el intercambio de metadatos</span><span class="sxs-lookup"><span data-stu-id="beec6-108">Sometimes uses a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="beec6-109">Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con el Asistente para agregar impresoras.</span><span class="sxs-lookup"><span data-stu-id="beec6-109">The following diagnostic procedures should be used (in order) to help identify problems with the Add Printer Wizard.</span></span>

<span data-ttu-id="beec6-110">**Para solucionar problemas del Asistente para agregar impresoras**</span><span class="sxs-lookup"><span data-stu-id="beec6-110">**To troubleshoot the Add Printer Wizard**</span></span>

1.  <span data-ttu-id="beec6-111">Si se usa la detección dirigida, [solucione los problemas de detección dirigida](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="beec6-111">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="beec6-112">[Inspeccione la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="beec6-112">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="beec6-113">[Use un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="beec6-113">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="beec6-114">[Use el cliente de depuración WSD para comprobar el tráfico de multidifusión](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="beec6-114">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="beec6-115">[Inspeccione los seguimientos de red para WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="beec6-115">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="beec6-116">[Usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="beec6-116">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="beec6-117">[Use el registro de WinHTTP para comprobar el tráfico de obtención](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="beec6-117">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="beec6-118">[Inspeccione los seguimientos de red para el intercambio de metadatos http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="beec6-118">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="beec6-119">Si el origen del problema no se puede identificar mediante los procedimientos de diagnóstico anteriores, siga las instrucciones de [habilitación del seguimiento de WSDAPI](enabling-wsdapi-tracing.md) y póngase en contacto con el soporte técnico de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="beec6-119">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="beec6-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="beec6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="beec6-121">Introducción con la solución de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="beec6-121">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="beec6-122">Solución de problemas de aplicaciones con la detección dirigida</span><span class="sxs-lookup"><span data-stu-id="beec6-122">Troubleshooting Applications Using Directed Discovery</span></span>](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 




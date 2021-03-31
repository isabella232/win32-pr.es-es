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
# <a name="troubleshooting-the-network-explorer"></a><span data-ttu-id="59fad-103">Solución de problemas del explorador de red</span><span class="sxs-lookup"><span data-stu-id="59fad-103">Troubleshooting the Network Explorer</span></span>

<span data-ttu-id="59fad-104">El explorador de red:</span><span class="sxs-lookup"><span data-stu-id="59fad-104">The Network Explorer:</span></span>

-   <span data-ttu-id="59fad-105">Usa siempre WS-Discovery UDP para la detección de dispositivos</span><span class="sxs-lookup"><span data-stu-id="59fad-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="59fad-106">Siempre inicia una conexión HTTP o HTTPS para el intercambio de metadatos</span><span class="sxs-lookup"><span data-stu-id="59fad-106">Always initiates a HTTP or HTTPS connection for metadata exchange</span></span>
-   <span data-ttu-id="59fad-107">A veces, usa un canal seguro (HTTPS) para el intercambio de metadatos</span><span class="sxs-lookup"><span data-stu-id="59fad-107">Sometimes uses a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="59fad-108">Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con el explorador de red.</span><span class="sxs-lookup"><span data-stu-id="59fad-108">The following diagnostic procedures should be used (in order) to help identify problems with the Network Explorer.</span></span>

<span data-ttu-id="59fad-109">**Para solucionar problemas del explorador de red**</span><span class="sxs-lookup"><span data-stu-id="59fad-109">**To troubleshoot the Network Explorer**</span></span>

1.  <span data-ttu-id="59fad-110">[Inspeccione la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="59fad-110">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
2.  <span data-ttu-id="59fad-111">[Use un host y un cliente genéricos para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="59fad-111">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
3.  <span data-ttu-id="59fad-112">[Use el cliente de depuración WSD para comprobar el tráfico de multidifusión](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="59fad-112">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
4.  <span data-ttu-id="59fad-113">[Inspeccione los seguimientos de red para WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="59fad-113">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
5.  <span data-ttu-id="59fad-114">[Usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="59fad-114">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
6.  <span data-ttu-id="59fad-115">[Use el registro de WinHTTP para comprobar el tráfico de obtención](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="59fad-115">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
7.  <span data-ttu-id="59fad-116">[Inspeccione los seguimientos de red para el intercambio de metadatos http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="59fad-116">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="59fad-117">El explorador de red usa la [detección de funciones](/previous-versions/windows/desktop/fundisc/fd-portal) para enumerar los dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="59fad-117">The Network Explorer uses [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) to enumerate network devices.</span></span> <span data-ttu-id="59fad-118">Para obtener más información sobre la solución de problemas, consulte [solución de problemas de clientes de detección de funciones](troubleshooting-function-discovery-clients.md).</span><span class="sxs-lookup"><span data-stu-id="59fad-118">For more troubleshooting information, see [Troubleshooting Function Discovery Clients](troubleshooting-function-discovery-clients.md).</span></span>

<span data-ttu-id="59fad-119">Si el origen del problema no se puede identificar mediante los procedimientos de diagnóstico anteriores, siga las instrucciones de [habilitación del seguimiento de WSDAPI](enabling-wsdapi-tracing.md) y póngase en contacto con el soporte técnico de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="59fad-119">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59fad-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59fad-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59fad-121">Introducción con la solución de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="59fad-121">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="59fad-122">Solución de problemas de clientes de detección de funciones</span><span class="sxs-lookup"><span data-stu-id="59fad-122">Troubleshooting Function Discovery Clients</span></span>](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 

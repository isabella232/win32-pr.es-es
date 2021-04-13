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
# <a name="troubleshooting-wsdapi-applications-using-directed-discovery"></a><span data-ttu-id="0793c-103">Solución de problemas de aplicaciones WSDAPI mediante la detección dirigida</span><span class="sxs-lookup"><span data-stu-id="0793c-103">Troubleshooting WSDAPI Applications Using Directed Discovery</span></span>

<span data-ttu-id="0793c-104">Las aplicaciones que usan la detección dirigida envían mensajes de [sondeo](probe-message.md) a través de http o https para detectar dispositivos.</span><span class="sxs-lookup"><span data-stu-id="0793c-104">Applications that use directed discovery send [Probe](probe-message.md) messages over HTTP or HTTPS to discover devices.</span></span> <span data-ttu-id="0793c-105">Los mensajes [ProbeMatches](probematches-message.md) correspondientes enviados en respuesta también se envían a través de http o https.</span><span class="sxs-lookup"><span data-stu-id="0793c-105">The corresponding [ProbeMatches](probematches-message.md) messages sent in response are also sent over HTTP or HTTPS.</span></span> <span data-ttu-id="0793c-106">La detección dirigida se puede iniciar mediante el Asistente para agregar impresoras, un cliente de detección de funciones o una aplicación WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="0793c-106">Directed discovery can be initiated by the Add Printer Wizard, a Function Discovery client, or a WSDAPI application.</span></span> <span data-ttu-id="0793c-107">Los mensajes probe y ProbeMatches son estructuralmente idénticos a los enviados a través de UDP.</span><span class="sxs-lookup"><span data-stu-id="0793c-107">The Probe and ProbeMatches messages are structurally identical to those sent over UDP.</span></span> <span data-ttu-id="0793c-108">Los mensajes tienen como prefijo los encabezados HTTP o HTTPS adecuados.</span><span class="sxs-lookup"><span data-stu-id="0793c-108">The messages are prefixed with the appropriate HTTP or HTTPS headers.</span></span>

<span data-ttu-id="0793c-109">Se deben usar los siguientes procedimientos de diagnóstico (en orden) para ayudar a identificar problemas con una aplicación mediante la detección dirigida.</span><span class="sxs-lookup"><span data-stu-id="0793c-109">The following diagnostic procedures should be used (in order) to help identify problems with an application using directed discovery.</span></span>

<span data-ttu-id="0793c-110">**Para solucionar problemas de una aplicación WSDAPI mediante la detección dirigida**</span><span class="sxs-lookup"><span data-stu-id="0793c-110">**To troubleshoot a WSDAPI application using directed discovery**</span></span>

1.  <span data-ttu-id="0793c-111">[Inspeccione la configuración del adaptador y del firewall](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="0793c-111">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
2.  <span data-ttu-id="0793c-112">[Usar un host y un cliente genéricos para el intercambio de metadatos http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="0793c-112">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
3.  <span data-ttu-id="0793c-113">[Use el registro de WinHTTP para comprobar el tráfico de obtención](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="0793c-113">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
4.  <span data-ttu-id="0793c-114">[Inspeccione los seguimientos de red para una aplicación mediante la detección dirigida](inspecting-network-traces-for-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="0793c-114">[Inspect network traces for an application using directed discovery](inspecting-network-traces-for-applications-using-directed-discovery.md).</span></span>

<span data-ttu-id="0793c-115">Si el origen del problema no se puede identificar mediante los procedimientos de diagnóstico anteriores, siga las instrucciones de [habilitación del seguimiento de WSDAPI](enabling-wsdapi-tracing.md) y póngase en contacto con el soporte técnico de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0793c-115">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0793c-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0793c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0793c-117">Introducción con la solución de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="0793c-117">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="0793c-118">Solucionar problemas del Asistente para agregar impresoras</span><span class="sxs-lookup"><span data-stu-id="0793c-118">Troubleshooting the Add Printer Wizard</span></span>](troubleshooting-the-add-printer-wizard.md)
</dt> <dt>

[<span data-ttu-id="0793c-119">Solución de problemas de aplicaciones WSDAPI</span><span class="sxs-lookup"><span data-stu-id="0793c-119">Troubleshooting WSDAPI Applications</span></span>](troubleshooting-wsdapi-applications.md)
</dt> </dl>

 

 




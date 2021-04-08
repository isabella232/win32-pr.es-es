---
title: Servicio SNMP
description: 'La implementación de Microsoft Windows del Protocolo simple de administración de redes (SNMP) se usa para configurar dispositivos remotos, supervisar el rendimiento de la red, auditar el uso de la red y detectar errores de red o acceso inadecuado. Importante: la API SNMP de Microsoft Windows solo es compatible con las versiones de protocolo hasta SNMPv2C. No es compatible con las versiones posteriores del protocolo.'
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP SNMP
- SNMP SNMP, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71df55c79244c0f74ef685271834adc01ca7e981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078249"
---
# <a name="snmp-service"></a><span data-ttu-id="603fc-106">Servicio SNMP</span><span class="sxs-lookup"><span data-stu-id="603fc-106">SNMP Service</span></span>

<span data-ttu-id="603fc-107">\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="603fc-107">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="603fc-108">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="603fc-108">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="603fc-109">En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]</span><span class="sxs-lookup"><span data-stu-id="603fc-109">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

## <a name="purpose"></a><span data-ttu-id="603fc-110">Propósito</span><span class="sxs-lookup"><span data-stu-id="603fc-110">Purpose</span></span>

<span data-ttu-id="603fc-111">La implementación de Microsoft Windows del Protocolo simple de administración de redes (SNMP) se usa para configurar dispositivos remotos, supervisar el rendimiento de la red, auditar el uso de la red y detectar errores de red o acceso inadecuado.</span><span class="sxs-lookup"><span data-stu-id="603fc-111">The Microsoft Windows implementation of the Simple Network Management Protocol (SNMP) is used to configure remote devices, monitor network performance, audit network usage, and detect network faults or inappropriate access.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="603fc-112">La API SNMP de Microsoft Windows solo admite versiones de protocolo de hasta SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="603fc-112">The Microsoft Windows SNMP API only supports protocol versions up to SNMPv2C.</span></span> <span data-ttu-id="603fc-113">No es compatible con las versiones posteriores del protocolo.</span><span class="sxs-lookup"><span data-stu-id="603fc-113">It does not support any later versions of the protocol.</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="603fc-114">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="603fc-114">Where applicable</span></span>

<span data-ttu-id="603fc-115">SNMP utiliza una arquitectura distribuida que consta de aplicaciones de administración y aplicaciones de agente.</span><span class="sxs-lookup"><span data-stu-id="603fc-115">SNMP uses a distributed architecture consisting of management applications and agent applications.</span></span> <span data-ttu-id="603fc-116">El servicio SNMP implementa un agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="603fc-116">The SNMP service implements an SNMP agent.</span></span> <span data-ttu-id="603fc-117">Para usar la información que proporciona el servicio SNMP, debe tener al menos un host que ejecute una aplicación de administración SNMP.</span><span class="sxs-lookup"><span data-stu-id="603fc-117">To use the information the SNMP service provides, you must have at least one host that is running an SNMP management application.</span></span> <span data-ttu-id="603fc-118">Puede usar software de administración SNMP de terceros o puede desarrollar su propia aplicación de software de administración SNMP.</span><span class="sxs-lookup"><span data-stu-id="603fc-118">You can use third-party SNMP management software, or you can develop your own SNMP management software application.</span></span> <span data-ttu-id="603fc-119">Las siguientes API están disponibles para este propósito:</span><span class="sxs-lookup"><span data-stu-id="603fc-119">The following APIs are available for this purpose:</span></span>

-   <span data-ttu-id="603fc-120">API de administración de SNMP, un conjunto de funciones que se pueden usar para desarrollar rápidamente sistemas de administración SNMP básicos</span><span class="sxs-lookup"><span data-stu-id="603fc-120">SNMP Management API, a set of functions that can be used to quickly develop basic SNMP management systems</span></span>
-   <span data-ttu-id="603fc-121">WinSNMP API, versión 2,0, un conjunto de funciones para codificar, descodificar, enviar y recibir mensajes SNMP</span><span class="sxs-lookup"><span data-stu-id="603fc-121">WinSNMP API, version 2.0, a set of functions for encoding, decoding, sending, and receiving SNMP messages</span></span>

<span data-ttu-id="603fc-122">Además, la API del agente de extensión SNMP define la interfaz entre el servicio SNMP y los archivos DLL del agente de extensión SNMP de terceros.</span><span class="sxs-lookup"><span data-stu-id="603fc-122">Additionally, the SNMP Extension Agent API defines the interface between the SNMP service and third-party SNMP extension agent DLLs.</span></span> <span data-ttu-id="603fc-123">Las funciones de la API de la utilidad SNMP se pueden usar para simplificar el procesamiento de mensajes SNMP.</span><span class="sxs-lookup"><span data-stu-id="603fc-123">The SNMP Utility API functions can be used to simplify the processing of SNMP messages.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="603fc-124">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="603fc-124">Developer audience</span></span>

<span data-ttu-id="603fc-125">Las API enumeradas en la sección anterior están diseñadas para que las usen los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="603fc-125">The APIs listed in the preceding section are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="603fc-126">Es necesario estar familiarizado con SNMP y SNMPv2C, así como tener conocimientos prácticos de los conceptos de administración de redes y redes.</span><span class="sxs-lookup"><span data-stu-id="603fc-126">Familiarity with SNMP and SNMPv2C, as well as a working knowledge of networking and network management concepts, are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="603fc-127">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="603fc-127">Run-time requirements</span></span>

<span data-ttu-id="603fc-128">Para obtener más información sobre el sistema operativo necesario para usar una función determinada, vea la sección requisitos de la página de referencia de esa función.</span><span class="sxs-lookup"><span data-stu-id="603fc-128">For more information about the operating system required to use a particular function, see the Requirements section of the reference page for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="603fc-129">En esta sección</span><span class="sxs-lookup"><span data-stu-id="603fc-129">In this section</span></span>



| <span data-ttu-id="603fc-130">Tema</span><span class="sxs-lookup"><span data-stu-id="603fc-130">Topic</span></span>                                                                                                | <span data-ttu-id="603fc-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="603fc-131">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="603fc-132">Novedades de SNMP</span><span class="sxs-lookup"><span data-stu-id="603fc-132">New in SNMP</span></span>](new-in-snmp.md)<br/>                                                            | <span data-ttu-id="603fc-133">Información sobre las actualizaciones de SNMP.</span><span class="sxs-lookup"><span data-stu-id="603fc-133">Information on updates to SNMP.</span></span><br/>                                                                                                      |
| <span data-ttu-id="603fc-134">[Protocolo simple de administración de redes (SNMP)](simple-network-management-protocol-snmp-.md):</span><span class="sxs-lookup"><span data-stu-id="603fc-134">[Simple Network Management Protocol (SNMP)](simple-network-management-protocol-snmp-.md)</span></span><br/> | <span data-ttu-id="603fc-135">Información y referencia de API para SNMP, incluida la API de administración de SNMP, la API del agente de extensión SNMP y las funciones de API de la utilidad SNMP.</span><span class="sxs-lookup"><span data-stu-id="603fc-135">Information and API reference for SNMP, including the SNMP Management API, SNMP Extension Agent API, and SNMP Utility API functions.</span></span><br/> |
| [<span data-ttu-id="603fc-136">API WinSNMP</span><span class="sxs-lookup"><span data-stu-id="603fc-136">WinSNMP API</span></span>](snmp-reference.md)<br/>                                                         | <span data-ttu-id="603fc-137">Información y referencia de la API para la interfaz de programación de aplicaciones (API WinSNMP) de Microsoft Windows SNMP.</span><span class="sxs-lookup"><span data-stu-id="603fc-137">Information and API reference for the Microsoft Windows SNMP Application Programming Interface (WinSNMP API).</span></span> <br/>                       |



 

## <a name="related-topics"></a><span data-ttu-id="603fc-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="603fc-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="603fc-139">Protocolo de configuración dinámica de host (DHCP)</span><span class="sxs-lookup"><span data-stu-id="603fc-139">Dynamic Host Configuration Protocol (DHCP)</span></span>](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[<span data-ttu-id="603fc-140">Administración de red</span><span class="sxs-lookup"><span data-stu-id="603fc-140">Network Management</span></span>](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[<span data-ttu-id="603fc-141">Servicio de acceso remoto y enrutamiento</span><span class="sxs-lookup"><span data-stu-id="603fc-141">Routing and Remote Access Service</span></span>](/windows/desktop/RRAS/portal)
</dt> </dl>

 


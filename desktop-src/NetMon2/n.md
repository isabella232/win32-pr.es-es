---
description: Glosario de términos de Monitor de red que comienzan por la letra N.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: a9b0e907-45c0-4301-9e83-398dd1c1c39a
title: N (Monitor de red)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54404640b13bff3b098b9d223e656e8f1905c055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911637"
---
# <a name="n-network-monitor"></a><span data-ttu-id="61918-103">N (Monitor de red)</span><span class="sxs-lookup"><span data-stu-id="61918-103">N (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="61918-104"><span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**NDIS**</span><span class="sxs-lookup"><span data-stu-id="61918-104"><span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**NDIS**</span></span>
</dt> <dd>

<span data-ttu-id="61918-105">Consulte Especificación de interfaz de controlador de red.</span><span class="sxs-lookup"><span data-stu-id="61918-105">See network driver interface specification.</span></span>

</dd> <dt>

<span data-ttu-id="61918-106"><span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**Especificación de interfaz de controlador de red (NDIS)**</span><span class="sxs-lookup"><span data-stu-id="61918-106"><span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**network driver interface specification (NDIS)**</span></span>
</dt> <dd>

<span data-ttu-id="61918-107">Especificación de la interfaz entre los controladores de dispositivo y una red.</span><span class="sxs-lookup"><span data-stu-id="61918-107">The specification for the interface between device drivers and a network.</span></span> <span data-ttu-id="61918-108">Todos los transportes llaman a la interfaz NDIS para tener acceso a tarjetas de interfaz de red y trabajar con ellas.</span><span class="sxs-lookup"><span data-stu-id="61918-108">All transports call the NDIS interface to access and work with network interface cards.</span></span>

</dd> <dt>

<span data-ttu-id="61918-109"><span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Agente Monitor de red**</span><span class="sxs-lookup"><span data-stu-id="61918-109"><span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Network Monitor agent**</span></span>
</dt> <dd>

<span data-ttu-id="61918-110">Componente de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="61918-110">A Network Monitor component.</span></span> <span data-ttu-id="61918-111">El agente permite a un equipo remoto capturar datos de la red.</span><span class="sxs-lookup"><span data-stu-id="61918-111">The agent enables a remote computer to capture data from the network.</span></span> <span data-ttu-id="61918-112">Cuando una instalación de Monitor de red se conecta de forma remota al agente de Monitor de red e inicia una captura, las estadísticas de la captura se transfieren a través de la red al equipo de administración.</span><span class="sxs-lookup"><span data-stu-id="61918-112">When a Network Monitor installation connects remotely to the Network Monitor agent and initiates a capture, statistics from the capture are transferred over the network to the managing computer.</span></span> <span data-ttu-id="61918-113">La transferencia continúa a intervalos especificados cuando se realiza la conexión.</span><span class="sxs-lookup"><span data-stu-id="61918-113">The transfer proceeds at intervals specified when the connection is made.</span></span>

</dd> <dt>

<span data-ttu-id="61918-114"><span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**proveedor de paquetes de red (NPP)**</span><span class="sxs-lookup"><span data-stu-id="61918-114"><span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**network packet provider (NPP)**</span></span>
</dt> <dd>

<span data-ttu-id="61918-115">El componente de Monitor de red que recopila el tráfico de red en fotogramas y, después, pasa los fotogramas a una aplicación de experto y NPP.</span><span class="sxs-lookup"><span data-stu-id="61918-115">The Network Monitor component that collects network traffic in frames, and then passes the frames to an expert, and NPP application.</span></span> <span data-ttu-id="61918-116">Un NPP utiliza el Monitor de red controlador del sistema (Nmnt.sys) para obtener los fotogramas recopilados de la red y proporciona varias interfaces COM que pasan los fotogramas a una aplicación de experto, monitor y proveedor de paquetes de red (NPP) donde se pueden mostrar y analizar.</span><span class="sxs-lookup"><span data-stu-id="61918-116">An NPP uses the Network Monitor system driver (Nmnt.sys) to get the frames collected from the network, and provides several COM interfaces that pass the frames to an expert, monitor, and network packet provider (NPP) application where they can be displayed and analyzed.</span></span>

</dd> <dt>

<span data-ttu-id="61918-117"><span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**NPP**</span><span class="sxs-lookup"><span data-stu-id="61918-117"><span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**NPP**</span></span>
</dt> <dd>

<span data-ttu-id="61918-118">Consulte proveedor de paquetes de red.</span><span class="sxs-lookup"><span data-stu-id="61918-118">See network packet provider.</span></span>

</dd> <dt>

<span data-ttu-id="61918-119"><span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**Aplicación NPP**</span><span class="sxs-lookup"><span data-stu-id="61918-119"><span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**NPP application**</span></span>
</dt> <dd>

<span data-ttu-id="61918-120">Aplicación que omite la interfaz de usuario de Monitor de red y la herramienta de control de supervisión, y se conecta directamente al proveedor de paquetes de red (NPP).</span><span class="sxs-lookup"><span data-stu-id="61918-120">An application that bypasses both the Network Monitor UI and Monitor Control Tool, and connects directly to the network packet provider (NPP).</span></span> <span data-ttu-id="61918-121">Una aplicación NPP puede conectarse al componente NPP con cualquiera de las cinco interfaces COM NPP.</span><span class="sxs-lookup"><span data-stu-id="61918-121">An NPP application can connect to the NPP component with any of the five NPP COM interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="61918-122"><span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**Buscador de NPP**</span><span class="sxs-lookup"><span data-stu-id="61918-122"><span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**NPP Finder**</span></span>
</dt> <dd>

<span data-ttu-id="61918-123">El componente de Monitor de red que se comunica con NPPs.</span><span class="sxs-lookup"><span data-stu-id="61918-123">The Network Monitor component that communicates with NPPs.</span></span>

</dd> </dl>

 

 




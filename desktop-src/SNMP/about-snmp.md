---
title: Acerca de SNMP
description: SNMP utiliza una arquitectura distribuida que consta de administradores y agentes.
ms.assetid: 55be55a8-1968-4373-a969-f7e03b75a824
keywords:
- SNMP, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1dab65173c96dce4bbd2f30edbca2a91f6153d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078196"
---
# <a name="about-snmp"></a><span data-ttu-id="d9437-104">Acerca de SNMP</span><span class="sxs-lookup"><span data-stu-id="d9437-104">About SNMP</span></span>

<span data-ttu-id="d9437-105">\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="d9437-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d9437-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="d9437-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="d9437-107">En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]</span><span class="sxs-lookup"><span data-stu-id="d9437-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="d9437-108">SNMP utiliza una arquitectura distribuida que consta de administradores y agentes.</span><span class="sxs-lookup"><span data-stu-id="d9437-108">SNMP uses a distributed architecture consisting of managers and agents.</span></span> <span data-ttu-id="d9437-109">Un agente es una aplicación SNMP que responde a las consultas de las aplicaciones del administrador SNMP.</span><span class="sxs-lookup"><span data-stu-id="d9437-109">An agent is an SNMP application that responds to queries from SNMP manager applications.</span></span> <span data-ttu-id="d9437-110">El agente SNMP es responsable de recuperar y actualizar la información de administración local en función de las solicitudes del administrador de SNMP.</span><span class="sxs-lookup"><span data-stu-id="d9437-110">The SNMP agent is responsible for retrieving and updating local management information based on the requests of the SNMP manager.</span></span> <span data-ttu-id="d9437-111">El agente también notifica a los administradores registrados cuando se producen eventos o capturas significativos.</span><span class="sxs-lookup"><span data-stu-id="d9437-111">The agent also notifies registered managers when significant events or traps occur.</span></span> <span data-ttu-id="d9437-112">Un administrador es una aplicación SNMP que genera consultas a las aplicaciones del agente SNMP y recibe capturas de aplicaciones del agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="d9437-112">A manager is an SNMP application that generates queries to SNMP agent applications and receives traps from SNMP agent applications.</span></span>

<span data-ttu-id="d9437-113">En los equipos que ejecutan Microsoft Windows XP/Windows 2000/Windows NT, el agente SNMP se implementa mediante el servicio SNMP (SNMP.EXE).</span><span class="sxs-lookup"><span data-stu-id="d9437-113">On computers running Microsoft Windows XP/Windows 2000/Windows NT, the SNMP agent is implemented by the SNMP service (SNMP.EXE).</span></span> <span data-ttu-id="d9437-114">Normalmente, el administrador SNMP es una aplicación de consola de administración SNMP de terceros.</span><span class="sxs-lookup"><span data-stu-id="d9437-114">The SNMP manager is typically a third-party SNMP management console application.</span></span> <span data-ttu-id="d9437-115">No es necesario que la aplicación de consola de administración se ejecute en el mismo host que el agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="d9437-115">The management console application does not need to run on the same host as the SNMP agent.</span></span> <span data-ttu-id="d9437-116">Para usar la información que proporciona el servicio SNMP de Microsoft, necesita al menos una aplicación de consola de administración SNMP.</span><span class="sxs-lookup"><span data-stu-id="d9437-116">To use the information the Microsoft SNMP service provides, you need at least one SNMP management console application.</span></span> <span data-ttu-id="d9437-117">El sistema incluye bibliotecas que admiten aplicaciones de consola de administración de SNMP, pero no incluye una aplicación de consola de administración de SNMP en este momento.</span><span class="sxs-lookup"><span data-stu-id="d9437-117">The system includes libraries that support SNMP management console applications, but it does not include an SNMP management console application at this time.</span></span>

 

 
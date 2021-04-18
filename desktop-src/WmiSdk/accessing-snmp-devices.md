---
description: Permite a las aplicaciones cliente obtener acceso a información de SNMP a través de WMI.
ms.assetid: d9e3fd1d-8320-4407-9a9e-e2eb5dd62fef
ms.tgt_platform: multiple
title: Acceso a dispositivos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a349053f054f3e8ad9dffb7c108d2bee6c6d8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697845"
---
# <a name="accessing-snmp-devices"></a><span data-ttu-id="14007-103">Acceso a dispositivos SNMP</span><span class="sxs-lookup"><span data-stu-id="14007-103">Accessing SNMP Devices</span></span>

<span data-ttu-id="14007-104">El proveedor del Protocolo simple de administración de redes (SNMP) permite a las aplicaciones cliente obtener acceso a información de SNMP a través de WMI.</span><span class="sxs-lookup"><span data-stu-id="14007-104">The Simple Network Management Protocol (SNMP) provider allows client applications to access SNMP information through WMI.</span></span> <span data-ttu-id="14007-105">El [proveedor SNMP](snmp-provider.md) actúa como puerta de enlace a los sistemas y dispositivos que utilizan SNMP para la administración.</span><span class="sxs-lookup"><span data-stu-id="14007-105">The [SNMP provider](snmp-provider.md) acts as a gateway to systems and devices that use SNMP for management.</span></span> <span data-ttu-id="14007-106">Solo el equipo de administración o supervisión debe ejecutar WMI porque puede leer desde cualquier dispositivo habilitado para SNMP.</span><span class="sxs-lookup"><span data-stu-id="14007-106">Only the management or monitoring computer must be running WMI because it can read from any SNMP-enabled device.</span></span>

> [!Note]  
> <span data-ttu-id="14007-107">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="14007-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="14007-108">Las variables de objeto de la base de información de administración de SNMP (MIB) se pueden leer y escribir en, y las capturas de SNMP se pueden asignar automáticamente a eventos de WMI, que se pueden definir para cualquier operación arbitraria de creación, eliminación o actualización a los datos más allá de las capturas definidas por MIB.</span><span class="sxs-lookup"><span data-stu-id="14007-108">SNMP Management Information Base (MIB) object variables can be read from and written to, and SNMP traps can be automatically mapped to WMI events, which can be defined for any arbitrary create, delete, or update operations to data beyond the MIB-defined traps.</span></span> <span data-ttu-id="14007-109">Esta característica de WMI funciona como una extensión de las funcionalidades SNMP estándar.</span><span class="sxs-lookup"><span data-stu-id="14007-109">This feature of WMI functions as an extension of standard SNMP capabilities.</span></span> <span data-ttu-id="14007-110">Para obtener más información, consulte [supervisión de eventos](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="14007-110">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

<span data-ttu-id="14007-111">Las herramientas que se describen en los temas siguientes están diseñadas para que las usen los programadores de Windows Scripting y C/C++.</span><span class="sxs-lookup"><span data-stu-id="14007-111">The tools described in the following topics are designed for use by Windows scripting and C/C++ programmers.</span></span> <span data-ttu-id="14007-112">Se recomienda estar familiarizado con WMI, SNMPv1 y SNMPv2C, y el conocimiento práctico de los conceptos de administración de redes y redes.</span><span class="sxs-lookup"><span data-stu-id="14007-112">Familiarity with WMI, SNMPv1 and SNMPv2C, and a working knowledge of networking and network management concepts are recommended.</span></span>

<span data-ttu-id="14007-113">Para obtener más información acerca del uso de WMI con SNMP, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="14007-113">For more information about using WMI with SNMP, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

 




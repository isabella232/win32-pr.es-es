---
title: Configuración de directiva de grupo SNMP
description: Si usa el complemento Microsoft Management Console (MMC) para directiva de grupo para administrar la configuración de directivas basada en el registro que se aplica a SNMP, pueden existir una o varias de las subclaves siguientes.
ms.assetid: de21d2f5-3337-47ba-afcf-347e289873d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 817797dbc0e67f6006e12751beca533cbbec3656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149510"
---
# <a name="configuring-snmp-group-policy"></a><span data-ttu-id="3a189-103">Configuración de directiva de grupo SNMP</span><span class="sxs-lookup"><span data-stu-id="3a189-103">Configuring SNMP Group Policy</span></span>

<span data-ttu-id="3a189-104">Si usa el complemento Microsoft Management Console (MMC) para directiva de grupo para administrar la configuración de directivas basada en el registro que se aplica a SNMP, pueden existir una o varias de las subclaves siguientes.</span><span class="sxs-lookup"><span data-stu-id="3a189-104">If you use the Microsoft Management Console (MMC) snap-in for Group Policy to administer registry-based policy settings that apply to SNMP, one or more of the following subkeys may exist.</span></span>

<span data-ttu-id="3a189-105">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\  \\ **parámetros** SNMP \\ **ValidCommunities**</span><span class="sxs-lookup"><span data-stu-id="3a189-105">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**ValidCommunities**</span></span>

<span data-ttu-id="3a189-106">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\  \\ **parámetros** SNMP \\ **PermittedManagers**</span><span class="sxs-lookup"><span data-stu-id="3a189-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**PermittedManagers**</span></span>

<span data-ttu-id="3a189-107">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\  \\ **parámetros** SNMP \\ **TrapConfiguration**</span><span class="sxs-lookup"><span data-stu-id="3a189-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**TrapConfiguration**</span></span>

<span data-ttu-id="3a189-108">Normalmente, solo los miembros del grupo local administradores pueden tener acceso a las subclaves del registro siguientes que almacenan los datos de configuración para el servicio SNMP:</span><span class="sxs-lookup"><span data-stu-id="3a189-108">Typically, only members of the Administrators local group can access the following registry subkeys that store configuration data for the SNMP service:</span></span>

<span data-ttu-id="3a189-109">**HKEY \_ \_** \\  \\  \\  \\  \\ **Parámetros** \\  SNMP de System CurrentControlSet Services del equipo local ValidCommunities</span><span class="sxs-lookup"><span data-stu-id="3a189-109">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**SNMP**\\**Parameters**\\**ValidCommunities**</span></span>

<span data-ttu-id="3a189-110">**HKEY \_ \_** \\  \\  \\  \\  \\ **Parámetros** \\  SNMP de System CurrentControlSet Services del equipo local PermittedManagers</span><span class="sxs-lookup"><span data-stu-id="3a189-110">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**SNMP**\\**Parameters**\\**PermittedManagers**</span></span>

<span data-ttu-id="3a189-111">Para obtener más información acerca de la configuración de directivas basada en el registro, consulte [acerca de directiva de grupo](/previous-versions/windows/desktop/Policy/about-group-policy).</span><span class="sxs-lookup"><span data-stu-id="3a189-111">For more information about registry-based policy settings, see [About Group Policy](/previous-versions/windows/desktop/Policy/about-group-policy).</span></span>

 

 
---
description: Un AppContainer se implementa agregando nueva información al token de proceso, cambiando SeAccessCheck () para que todos los objetos de la lista de control de acceso (ACL) heredados y no modificados bloqueen las solicitudes de acceso de los procesos de AppContainer de forma predeterminada, y vuelva a crear los objetos de ACL que deben estar disponibles para AppContainers.
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: Implementar un AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a6fc4c8d807d6a45f27f4f7a79d69ceb97edeb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912429"
---
# <a name="implementing-an-appcontainer"></a><span data-ttu-id="b95a3-103">Implementar un AppContainer</span><span class="sxs-lookup"><span data-stu-id="b95a3-103">Implementing an AppContainer</span></span>

<span data-ttu-id="b95a3-104">Un AppContainer se implementa agregando nueva información al token de proceso, cambiando [**SeAccessCheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) para que todos los objetos de la lista de control de acceso (ACL) heredados y no modificados bloqueen las solicitudes de acceso de los procesos de AppContainer de forma predeterminada, y vuelva a crear los objetos de ACL que deben estar disponibles para AppContainers.</span><span class="sxs-lookup"><span data-stu-id="b95a3-104">An AppContainer is implemented by adding new information to the process token, changing [**SeAccessCheck()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) so that all legacy, unmodified access control list (ACL) objects block access requests from AppContainer processes by default, and re-ACL objects that should be available to AppContainers.</span></span>

## <a name="the-process"></a><span data-ttu-id="b95a3-105">El proceso</span><span class="sxs-lookup"><span data-stu-id="b95a3-105">The process</span></span>

<span data-ttu-id="b95a3-106">Comience agregando nueva información para el token de proceso.</span><span class="sxs-lookup"><span data-stu-id="b95a3-106">Begin by adding new information for the process token.</span></span> <span data-ttu-id="b95a3-107">A continuación, cambie **SeAccessCheck ()** para que todas las ACL heredadas y sin modificar bloqueen de forma predeterminada las solicitudes de acceso de los procesos de AppContainer.</span><span class="sxs-lookup"><span data-stu-id="b95a3-107">Then change **SeAccessCheck()** so that all legacy, unmodified ACLs will block access requests from AppContainer processes by default.</span></span> <span data-ttu-id="b95a3-108">Por último, vuelva a crear los recursos de la ACL que deben estar disponibles para AppContainers</span><span class="sxs-lookup"><span data-stu-id="b95a3-108">Finally, re-ACL resources that should be available to AppContainers</span></span>

<span data-ttu-id="b95a3-109">El SID del AppContainer es un identificador único persistente para el appcontainer.</span><span class="sxs-lookup"><span data-stu-id="b95a3-109">The AppContainer SID is a persistent unique identifier for the appcontainer.</span></span> <span data-ttu-id="b95a3-110">Los SID de capacidad conceden acceso a grupos de recursos a grupos de AppContainers.</span><span class="sxs-lookup"><span data-stu-id="b95a3-110">Capability SIDs grant access to groups of resources to groups of AppContainers.</span></span> <span data-ttu-id="b95a3-111">Un AppContainerNumber es un **valor DWORD** transitorio que se usa para distinguir entre AppContainers.</span><span class="sxs-lookup"><span data-stu-id="b95a3-111">An AppContainerNumber is a transient **DWORD** used to distinguish between AppContainers.</span></span> <span data-ttu-id="b95a3-112">Sin embargo, no debe usarse como una identidad para el AppContainer.</span><span class="sxs-lookup"><span data-stu-id="b95a3-112">However, it should not be used as an identity for the AppContainer.</span></span>

<span data-ttu-id="b95a3-113">Para permitir que un único AppContainer tenga acceso a un recurso, agregue su AppContainerSID a la ACL para ese recurso.</span><span class="sxs-lookup"><span data-stu-id="b95a3-113">To allow a single AppContainer to access a resource, add its AppContainerSID to the ACL for that resource.</span></span>

<span data-ttu-id="b95a3-114">Para permitir que varias AppContainers específicas tengan acceso a un recurso, agregue todos sus AppContainerSIDs a la ACL para ese recurso.</span><span class="sxs-lookup"><span data-stu-id="b95a3-114">To allow several specific AppContainers to access a resource, add all of their AppContainerSIDs to the ACL for that resource.</span></span>

<span data-ttu-id="b95a3-115">Para administrar grupos de permisos, cree un SID de funcionalidad (un GUID) y coloque ese SID de capacidad en todos los recursos que se van a conceder.</span><span class="sxs-lookup"><span data-stu-id="b95a3-115">To manage groups of permissions, create a Capability SID (a GUID) and put that Capability SID on all of the resources to be granted.</span></span> <span data-ttu-id="b95a3-116">A continuación, agregue el SID de capacidad al token de proceso.</span><span class="sxs-lookup"><span data-stu-id="b95a3-116">Then add the Capability SID to your process token.</span></span>

<span data-ttu-id="b95a3-117">Para permitir que todos los AppContainers tengan acceso a un recurso, agregue el SID **todos los paquetes de aplicación** a la ACL para ese recurso.</span><span class="sxs-lookup"><span data-stu-id="b95a3-117">To allow all AppContainers to access a resource, add the **ALL APPLICATION PACKAGES** SID to the ACL for that resource.</span></span> <span data-ttu-id="b95a3-118">Esto actúa como un carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="b95a3-118">This acts like a wildcard.</span></span>

<span data-ttu-id="b95a3-119">Tanto AppContainerSID como CapabilitySID admiten las máscaras de acceso en entradas de Access Control (ACE).</span><span class="sxs-lookup"><span data-stu-id="b95a3-119">Both AppContainerSID and CapabilitySID support access masks in Access Control Entries (ACE).</span></span> <span data-ttu-id="b95a3-120">Establezca según corresponda.</span><span class="sxs-lookup"><span data-stu-id="b95a3-120">Set as appropriate.</span></span>

 

 

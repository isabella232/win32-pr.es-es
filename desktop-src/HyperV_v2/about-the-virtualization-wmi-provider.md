---
description: El proveedor WMI de Hyper-V permite a los desarrolladores y generadores de scripts crear rápidamente herramientas, utilidades y mejoras personalizadas para la plataforma de virtualización. Las interfaces WMI pueden administrar todos los aspectos de los servicios de Hyper-V.
ms.assetid: 773BB141-7B9C-4015-81A0-BD17B8233CCD
title: Acerca del proveedor WMI de Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70c30b329f7e8a3fd3ae65b49f8467a8f712707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667483"
---
# <a name="about-the-hyper-v-wmi-provider"></a><span data-ttu-id="f5b8a-104">Acerca del proveedor WMI de Hyper-V</span><span class="sxs-lookup"><span data-stu-id="f5b8a-104">About the Hyper-V WMI provider</span></span>

<span data-ttu-id="f5b8a-105">El proveedor WMI de Hyper-V permite a los desarrolladores y generadores de scripts crear rápidamente herramientas, utilidades y mejoras personalizadas para la plataforma de virtualización.</span><span class="sxs-lookup"><span data-stu-id="f5b8a-105">The WMI provider for Hyper-V enable developers, and scripters, to quickly build custom tools, utilities, and enhancements for the virtualization platform.</span></span> <span data-ttu-id="f5b8a-106">Las interfaces WMI pueden administrar todos los aspectos de los servicios de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="f5b8a-106">The WMI interfaces can manage all aspects of the Hyper-V services.</span></span>

## <a name="about-microsoft-windows-server-2008-r2-hyper-v"></a><span data-ttu-id="f5b8a-107">Acerca de Microsoft Windows Server 2008 R2 Hyper-V</span><span class="sxs-lookup"><span data-stu-id="f5b8a-107">About Microsoft Windows Server 2008 R2 Hyper-V</span></span>

<span data-ttu-id="f5b8a-108">Microsoft Windows Server 2008 R2 Hyper-V permite a los administradores del sistema consolidar servidores de hardware independientes en un único servidor que ejecuta Microsoft Windows Server 2008 R2 como sistema operativo host.</span><span class="sxs-lookup"><span data-stu-id="f5b8a-108">Microsoft Windows Server 2008 R2 Hyper-V allows system administrators to consolidate separate hardware servers on to a single server running Microsoft Windows Server 2008 R2 as the host operating system.</span></span>

<span data-ttu-id="f5b8a-109">Cada una de las máquinas virtuales hospedadas se ejecuta en su propio entorno virtual independiente y aislado.</span><span class="sxs-lookup"><span data-stu-id="f5b8a-109">Each of the hosted virtual machines runs in its own separate and isolated virtual environment.</span></span> <span data-ttu-id="f5b8a-110">Esto permite al administrador administrar, proporcionar y mantener fácilmente un gran número de máquinas virtuales, a la vez que reduce la necesidad de ejecutar varias soluciones de hardware para usar varios productos y sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="f5b8a-110">This allows the administrator to easily manage, provide for, and maintain large numbers of virtual machines while reducing the need to run multiple hardware solutions to use various products and operating systems.</span></span>

<span data-ttu-id="f5b8a-111">Otra ventaja del entorno de máquina virtual está en pruebas y soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="f5b8a-111">Another advantage of the virtual machine environment is in test and support.</span></span> <span data-ttu-id="f5b8a-112">Las nuevas configuraciones de servidor y sistema se pueden implementar y probar en paralelo con el sistema existente sin requerir costosos tiempos de inactividad durante la fase de implementación.</span><span class="sxs-lookup"><span data-stu-id="f5b8a-112">New server and system configurations can be deployed and tested in parallel with the existing system without requiring costly downtime during the rollout phase.</span></span> <span data-ttu-id="f5b8a-113">Cada máquina virtual se puede configurar para que use configuraciones diferentes mientras se ejecuta en una plataforma estándar para generar mejores resultados de pruebas.</span><span class="sxs-lookup"><span data-stu-id="f5b8a-113">Each virtual machine can be setup to use varying configurations while running on a standard platform to produce better test results.</span></span> <span data-ttu-id="f5b8a-114">Gracias a la compatibilidad con los sistemas operativos anteriores, uno puede admitir y probar el hardware, los sistemas y las aplicaciones heredados.</span><span class="sxs-lookup"><span data-stu-id="f5b8a-114">With support for earlier operating systems, one can support and test legacy hardware, systems and applications.</span></span> <span data-ttu-id="f5b8a-115">La compatibilidad con instantáneas le permite tomar una instantánea del estado de una máquina virtual para que pueda volver a un evento anterior si es necesario.</span><span class="sxs-lookup"><span data-stu-id="f5b8a-115">Snapshot support allows you to take a snapshot of a virtual machine's state so you can return to a prior event if needed.</span></span>

<span data-ttu-id="f5b8a-116">Hyper-V expone una interfaz enriquecida que permite al usuario supervisar y controlar el entorno de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f5b8a-116">Hyper-V exposes a rich interface which permits the user to monitor and control the virtual machine environment.</span></span> <span data-ttu-id="f5b8a-117">La mayor parte de Hyper-V se puede controlar mediante el proveedor WMI, lo que permite una personalización sencilla y eficaz de las máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="f5b8a-117">Most of Hyper-V can be controlled by using the WMI provider, which allows easy, yet powerful customization of the virtual machines.</span></span> <span data-ttu-id="f5b8a-118">Para obtener más información sobre lo que se puede controlar con el proveedor WMI, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="f5b8a-118">For more information about what can be controlled with the WMI provider, see the following topics:</span></span>

-   [<span data-ttu-id="f5b8a-119">Servicio de administración del sistema virtual</span><span class="sxs-lookup"><span data-stu-id="f5b8a-119">Virtual system management service</span></span>](virtual-system-management-service.md)
-   [<span data-ttu-id="f5b8a-120">Servicio de red</span><span class="sxs-lookup"><span data-stu-id="f5b8a-120">Networking service</span></span>](networking-service.md)
-   [<span data-ttu-id="f5b8a-121">Servicio de administración de recursos</span><span class="sxs-lookup"><span data-stu-id="f5b8a-121">Resource management service</span></span>](resource-management-service.md)
-   [<span data-ttu-id="f5b8a-122">Novedades del proveedor WMI de Hyper-V</span><span class="sxs-lookup"><span data-stu-id="f5b8a-122">What's new in Hyper-V WMI provider</span></span>](what-s-new-in-hyper-v.md)

 

 




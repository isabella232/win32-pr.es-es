---
description: Memoria dinámica
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Memoria dinámica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcc54a1b85f4fc39bf6383e05a2e6e535edd1d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088473"
---
# <a name="dynamic-memory"></a><span data-ttu-id="73fab-103">Memoria dinámica</span><span class="sxs-lookup"><span data-stu-id="73fab-103">Dynamic Memory</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="73fab-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="73fab-104">Affected Platforms</span></span>

<span data-ttu-id="73fab-105">**Clientes (que se ejecutan como máquinas virtuales):** Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="73fab-105">**Clients (running as virtual machines)** - Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="73fab-106">**Servidores:** Windows Server 2008 R2 Hyper-V SP1</span><span class="sxs-lookup"><span data-stu-id="73fab-106">**Servers** - Windows Server 2008 R2 Hyper-V SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="73fab-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="73fab-107">Feature Impact</span></span>

 <span data-ttu-id="73fab-108">**Gravedad:** baja</span><span class="sxs-lookup"><span data-stu-id="73fab-108">**Severity** - Low</span></span>  
<span data-ttu-id="73fab-109">**Frecuencia:** alta</span><span class="sxs-lookup"><span data-stu-id="73fab-109">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="73fab-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="73fab-110">Description</span></span>

<span data-ttu-id="73fab-111">En un nivel alto, Hyper-V Memoria dinámica es una mejora de la administración de memoria para el rol de Hyper-V incluido en Windows Server 2008 R2 SP1.</span><span class="sxs-lookup"><span data-stu-id="73fab-111">At a high level, Hyper-V Dynamic Memory is a memory management enhancement for the Hyper-V role included in Windows Server 2008 R2 SP1.</span></span> <span data-ttu-id="73fab-112">Está diseñado para su uso en producción y permite a los clientes lograr mayores relaciones de consolidación y densidad de máquina virtual (VM) al mismo tiempo que optimiza el uso de memoria en la máquina física.</span><span class="sxs-lookup"><span data-stu-id="73fab-112">It is designed for production use and enables customers to achieve higher consolidation/virtual machine (VM) density ratios while optimizing the memory utilization in the physical machine.</span></span> <span data-ttu-id="73fab-113">La asignación de memoria estática se reduce y se asigna memoria adicional según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="73fab-113">The static memory allocation is reduced and additional memory is allocated on an as needed basis.</span></span> <span data-ttu-id="73fab-114">Memoria dinámica afecta a los desarrolladores de software que desean asegurarse de que su software funciona correctamente en un entorno de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="73fab-114">Dynamic Memory impacts software developers who want to ensure that their software works correctly in a virtual machine environment.</span></span>

## <a name="usage-scenario"></a><span data-ttu-id="73fab-115">Escenario de uso</span><span class="sxs-lookup"><span data-stu-id="73fab-115">Usage Scenario</span></span>

<span data-ttu-id="73fab-116">Hay dos escenarios de uso clave en los que Memoria dinámica en juego, las aplicaciones del lado host y las aplicaciones del lado invitado.</span><span class="sxs-lookup"><span data-stu-id="73fab-116">There are two key usage scenarios where Dynamic Memory comes into play, host-side applications and guest-side applications.</span></span>

<span data-ttu-id="73fab-117">**Aplicaciones del lado host (herramientas de administración)**</span><span class="sxs-lookup"><span data-stu-id="73fab-117">**Host-side applications (management tools)**</span></span>

<span data-ttu-id="73fab-118">Las herramientas antiguas que administran un nuevo servidor de Windows Server 2008 R2 SP1 no podrán acceder a la nueva Memoria dinámica configuración.</span><span class="sxs-lookup"><span data-stu-id="73fab-118">Old tools managing a new Windows Server 2008 R2 SP1 server will not be able to access the new Dynamic Memory settings.</span></span> <span data-ttu-id="73fab-119">Se han desarrollado nuevas API WMI y contadores de rendimiento para administrar la nueva configuración de Memoria dinámica para máquinas virtuales de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="73fab-119">New WMI APIs and performance counters have been developed to manage the new Dynamic Memory settings for Hyper-V virtual machines.</span></span> <span data-ttu-id="73fab-120">Los desarrolladores de software que trabajan en herramientas de administración deben aprovechar estas API y contadores para su uso con Windows Server 2008 R2 SP1 con el rol de Hyper-V instalado.</span><span class="sxs-lookup"><span data-stu-id="73fab-120">Software developers working on management tools should take advantage of these APIs and counters for use with Windows Server 2008 R2 SP1 with the Hyper-V role installed.</span></span> <span data-ttu-id="73fab-121">Los detalles sobre estas nuevas API estarán disponibles a través de la documentación del proveedor WMI de [Hyper-V en MSDN.](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)</span><span class="sxs-lookup"><span data-stu-id="73fab-121">Details about these new APIs will be available via [Hyper-V WMI Provider documentation on MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).</span></span>

<span data-ttu-id="73fab-122">**Aplicaciones del lado invitado**</span><span class="sxs-lookup"><span data-stu-id="73fab-122">**Guest-side applications**</span></span>

<span data-ttu-id="73fab-123">Los desarrolladores que escriben software para su uso dentro de una máquina virtual configurada para usar Memoria dinámica deben tener en cuenta que la memoria del sistema de máquina virtual ya no es constante.</span><span class="sxs-lookup"><span data-stu-id="73fab-123">Developers writing software for use inside a virtual machine configured to use Dynamic Memory need to keep in mind that VM system memory is no longer constant.</span></span> <span data-ttu-id="73fab-124">Por lo tanto, su aplicación debe liberar memoria cuando ya no sea necesario para permitir que otras aplicaciones aprovechen el recurso.</span><span class="sxs-lookup"><span data-stu-id="73fab-124">Consequently, their application should free memory when it is no longer needed to allow other applications to take advantage of the resource.</span></span>

<span data-ttu-id="73fab-125">Las asignaciones de memoria y las desa asignaciones siguen funcionando de la forma habitual para las aplicaciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="73fab-125">Memory allocations and de-allocations continue to work as normal for user applications.</span></span> <span data-ttu-id="73fab-126">Memoria dinámica es completamente transparente para la mayoría de las aplicaciones de usuario final.</span><span class="sxs-lookup"><span data-stu-id="73fab-126">Dynamic Memory is completely transparent to most end user applications.</span></span> <span data-ttu-id="73fab-127">Sin embargo, si el software que se está desarrollando usa contadores de rendimiento de memoria en la máquina virtual, se deben realizar pruebas cuidadosas en un entorno habilitado para Memoria dinámica para asegurarse de que el software tenga en cuenta los cambios realizados en la asignación de memoria del sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="73fab-127">However if the software being developed makes use of memory performance counters in the virtual machine then careful testing should be performed in a Dynamic Memory enabled environment to ensure that the software takes the changes that are made to the Guest operating system memory allocation into account.</span></span> <span data-ttu-id="73fab-128">La memoria disponible ya no es "estática" desde la perspectiva de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="73fab-128">Available memory is no longer "static" from the virtual machine?s perspective.</span></span>

## <a name="solutions"></a><span data-ttu-id="73fab-129">Soluciones</span><span class="sxs-lookup"><span data-stu-id="73fab-129">Solutions</span></span>

<span data-ttu-id="73fab-130">Las máquinas virtuales deben tener instalados los servicios de integración (SP1) actualizados para aprovechar las ventajas de Memoria dinámica.</span><span class="sxs-lookup"><span data-stu-id="73fab-130">Virtual machines must have updated integration services (SP1) installed in order to take advantage of Dynamic Memory.</span></span> <span data-ttu-id="73fab-131">Asegúrese de que todas las máquinas usadas en la administración de máquinas virtuales de Hyper-V usan los bits más recientes de Windows Server 2008 R2 SP1.</span><span class="sxs-lookup"><span data-stu-id="73fab-131">Ensure that all machines used in the management of Hyper-V virtual machines are using the latest Windows Server 2008 R2 SP1 bits.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="73fab-132">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="73fab-132">Links to Other Resources</span></span>

-   [<span data-ttu-id="73fab-133">Memoria dinámica en el blog de Hyper-V</span><span class="sxs-lookup"><span data-stu-id="73fab-133">Dynamic Memory Coming To Hyper-V blog</span></span>](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [<span data-ttu-id="73fab-134">Uso del proveedor WMI de Hyper-V</span><span class="sxs-lookup"><span data-stu-id="73fab-134">Using the Hyper-V WMI Provider</span></span>](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a><span data-ttu-id="73fab-135">Declinación de responsabilidades</span><span class="sxs-lookup"><span data-stu-id="73fab-135">Disclaimer</span></span>

<span data-ttu-id="73fab-136">La información contenida en este documento está relacionada con la versión preliminar del producto de software que puede modificarse considerablemente antes de su primera versión comercial.</span><span class="sxs-lookup"><span data-stu-id="73fab-136">The information contained in this document relates to prerelease software product that may be substantially modified before its first commercial release.</span></span> <span data-ttu-id="73fab-137">En consecuencia, es posible que la información no describa o refleje con precisión el producto de software cuando se lanza por primera vez comercialmente.</span><span class="sxs-lookup"><span data-stu-id="73fab-137">Accordingly, the information may not accurately describe or reflect the software product when first commercially released.</span></span> <span data-ttu-id="73fab-138">Este documento es meramente informativo.</span><span class="sxs-lookup"><span data-stu-id="73fab-138">This document is for informational purposes only.</span></span> <span data-ttu-id="73fab-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span><span class="sxs-lookup"><span data-stu-id="73fab-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span></span>

 

 

---
description: .
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Memoria dinámica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1e868a89714a7f6f1d77f9416515897876c150
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697737"
---
# <a name="dynamic-memory"></a><span data-ttu-id="fd18a-103">Memoria dinámica</span><span class="sxs-lookup"><span data-stu-id="fd18a-103">Dynamic Memory</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="fd18a-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="fd18a-104">Affected Platforms</span></span>

<span data-ttu-id="fd18a-105">**Clientes (que se ejecutan como máquinas virtuales)** : Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd18a-105">**Clients (running as virtual machines)** - Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="fd18a-106">**Servidores** : Windows Server 2008 R2 Hyper-V SP1</span><span class="sxs-lookup"><span data-stu-id="fd18a-106">**Servers** - Windows Server 2008 R2 Hyper-V SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="fd18a-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="fd18a-107">Feature Impact</span></span>

 <span data-ttu-id="fd18a-108">**Gravedad** baja</span><span class="sxs-lookup"><span data-stu-id="fd18a-108">**Severity** - Low</span></span>  
<span data-ttu-id="fd18a-109">**Frecuencia** : alta</span><span class="sxs-lookup"><span data-stu-id="fd18a-109">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="fd18a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd18a-110">Description</span></span>

<span data-ttu-id="fd18a-111">En un nivel alto, Hyper-V Memoria dinámica es una mejora de la administración de memoria para el rol Hyper-V que se incluye en Windows Server 2008 R2 SP1.</span><span class="sxs-lookup"><span data-stu-id="fd18a-111">At a high level, Hyper-V Dynamic Memory is a memory management enhancement for the Hyper-V role included in Windows Server 2008 R2 SP1.</span></span> <span data-ttu-id="fd18a-112">Está diseñado para su uso en producción y permite a los clientes lograr mayores proporciones de la consolidación o la densidad de la máquina virtual (VM) a la vez que optimiza el uso de memoria en el equipo físico.</span><span class="sxs-lookup"><span data-stu-id="fd18a-112">It is designed for production use and enables customers to achieve higher consolidation/virtual machine (VM) density ratios while optimizing the memory utilization in the physical machine.</span></span> <span data-ttu-id="fd18a-113">Se reduce la asignación de memoria estática y se asigna memoria adicional según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="fd18a-113">The static memory allocation is reduced and additional memory is allocated on an as needed basis.</span></span> <span data-ttu-id="fd18a-114">Memoria dinámica afecta a los desarrolladores de software que desean asegurarse de que su software funciona correctamente en un entorno de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fd18a-114">Dynamic Memory impacts software developers who want to ensure that their software works correctly in a virtual machine environment.</span></span>

## <a name="usage-scenario"></a><span data-ttu-id="fd18a-115">Escenario de uso</span><span class="sxs-lookup"><span data-stu-id="fd18a-115">Usage Scenario</span></span>

<span data-ttu-id="fd18a-116">Hay dos escenarios de uso clave en los que Memoria dinámica entra en juego, en las aplicaciones del lado host y en las aplicaciones del lado invitado.</span><span class="sxs-lookup"><span data-stu-id="fd18a-116">There are two key usage scenarios where Dynamic Memory comes into play, host-side applications and guest-side applications.</span></span>

<span data-ttu-id="fd18a-117">**Aplicaciones del lado host (herramientas de administración)**</span><span class="sxs-lookup"><span data-stu-id="fd18a-117">**Host-side applications (management tools)**</span></span>

<span data-ttu-id="fd18a-118">Las herramientas antiguas que administran un nuevo servidor de Windows Server 2008 R2 SP1 no podrán tener acceso a la nueva configuración de Memoria dinámica.</span><span class="sxs-lookup"><span data-stu-id="fd18a-118">Old tools managing a new Windows Server 2008 R2 SP1 server will not be able to access the new Dynamic Memory settings.</span></span> <span data-ttu-id="fd18a-119">Se han desarrollado nuevas API y contadores de rendimiento de WMI para administrar la nueva configuración de Memoria dinámica para máquinas virtuales de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="fd18a-119">New WMI APIs and performance counters have been developed to manage the new Dynamic Memory settings for Hyper-V virtual machines.</span></span> <span data-ttu-id="fd18a-120">Los desarrolladores de software que trabajan en herramientas de administración deben aprovechar estas API y contadores para su uso con Windows Server 2008 R2 SP1 con el rol de Hyper-V instalado.</span><span class="sxs-lookup"><span data-stu-id="fd18a-120">Software developers working on management tools should take advantage of these APIs and counters for use with Windows Server 2008 R2 SP1 with the Hyper-V role installed.</span></span> <span data-ttu-id="fd18a-121">Los detalles sobre estas nuevas API estarán disponibles a través [de la documentación del proveedor de WMI de Hyper-V en MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).</span><span class="sxs-lookup"><span data-stu-id="fd18a-121">Details about these new APIs will be available via [Hyper-V WMI Provider documentation on MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).</span></span>

<span data-ttu-id="fd18a-122">**Aplicaciones del invitado**</span><span class="sxs-lookup"><span data-stu-id="fd18a-122">**Guest-side applications**</span></span>

<span data-ttu-id="fd18a-123">Los desarrolladores que escriben software para su uso en una máquina virtual configurada para utilizar Memoria dinámica deben tener en cuenta que la memoria del sistema de la máquina virtual ya no es constante.</span><span class="sxs-lookup"><span data-stu-id="fd18a-123">Developers writing software for use inside a virtual machine configured to use Dynamic Memory need to keep in mind that VM system memory is no longer constant.</span></span> <span data-ttu-id="fd18a-124">Por lo tanto, la aplicación debe liberar memoria cuando ya no se necesite para permitir que otras aplicaciones aprovechen el recurso.</span><span class="sxs-lookup"><span data-stu-id="fd18a-124">Consequently, their application should free memory when it is no longer needed to allow other applications to take advantage of the resource.</span></span>

<span data-ttu-id="fd18a-125">Las asignaciones de memoria y las anulaciones de asignación continúan funcionando como es habitual en las aplicaciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="fd18a-125">Memory allocations and de-allocations continue to work as normal for user applications.</span></span> <span data-ttu-id="fd18a-126">Memoria dinámica es completamente transparente para la mayoría de las aplicaciones de usuario final.</span><span class="sxs-lookup"><span data-stu-id="fd18a-126">Dynamic Memory is completely transparent to most end user applications.</span></span> <span data-ttu-id="fd18a-127">Sin embargo, si el software que se está desarrollando utiliza contadores de rendimiento de memoria en la máquina virtual, se deben realizar pruebas exhaustivas en un entorno de Memoria dinámica habilitado para asegurarse de que el software realice los cambios que se realizan en la asignación de memoria del sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="fd18a-127">However if the software being developed makes use of memory performance counters in the virtual machine then careful testing should be performed in a Dynamic Memory enabled environment to ensure that the software takes the changes that are made to the Guest operating system memory allocation into account.</span></span> <span data-ttu-id="fd18a-128">La memoria disponible ya no es "estática" de la perspectiva de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fd18a-128">Available memory is no longer "static" from the virtual machine?s perspective.</span></span>

## <a name="solutions"></a><span data-ttu-id="fd18a-129">Soluciones</span><span class="sxs-lookup"><span data-stu-id="fd18a-129">Solutions</span></span>

<span data-ttu-id="fd18a-130">Las máquinas virtuales deben tener instalado Integration Services (SP1) para poder aprovechar las ventajas de Memoria dinámica.</span><span class="sxs-lookup"><span data-stu-id="fd18a-130">Virtual machines must have updated integration services (SP1) installed in order to take advantage of Dynamic Memory.</span></span> <span data-ttu-id="fd18a-131">Asegúrese de que todas las máquinas usadas en la administración de máquinas virtuales de Hyper-V usan los bits más recientes de Windows Server 2008 R2 SP1.</span><span class="sxs-lookup"><span data-stu-id="fd18a-131">Ensure that all machines used in the management of Hyper-V virtual machines are using the latest Windows Server 2008 R2 SP1 bits.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="fd18a-132">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="fd18a-132">Links to Other Resources</span></span>

-   [<span data-ttu-id="fd18a-133">Memoria dinámica que va a entrar en el blog de Hyper-V</span><span class="sxs-lookup"><span data-stu-id="fd18a-133">Dynamic Memory Coming To Hyper-V blog</span></span>](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [<span data-ttu-id="fd18a-134">Usar el proveedor WMI de Hyper-V</span><span class="sxs-lookup"><span data-stu-id="fd18a-134">Using the Hyper-V WMI Provider</span></span>](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a><span data-ttu-id="fd18a-135">Declinación de responsabilidades</span><span class="sxs-lookup"><span data-stu-id="fd18a-135">Disclaimer</span></span>

<span data-ttu-id="fd18a-136">La información contenida en este documento se relaciona con el producto de software de versión preliminar que se puede modificar sustancialmente antes de la primera versión comercial.</span><span class="sxs-lookup"><span data-stu-id="fd18a-136">The information contained in this document relates to prerelease software product that may be substantially modified before its first commercial release.</span></span> <span data-ttu-id="fd18a-137">En consecuencia, es posible que la información no describa o refleje con precisión el producto de software cuando se lance por primera vez.</span><span class="sxs-lookup"><span data-stu-id="fd18a-137">Accordingly, the information may not accurately describe or reflect the software product when first commercially released.</span></span> <span data-ttu-id="fd18a-138">Este documento es meramente informativo.</span><span class="sxs-lookup"><span data-stu-id="fd18a-138">This document is for informational purposes only.</span></span> <span data-ttu-id="fd18a-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span><span class="sxs-lookup"><span data-stu-id="fd18a-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span></span>

 

 

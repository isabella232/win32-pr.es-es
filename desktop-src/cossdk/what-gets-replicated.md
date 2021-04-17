---
description: Lo que se replica
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: Lo que se replica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2739cb0ff615ddc38f30a7aa9b0a572be5e28a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705315"
---
# <a name="what-gets-replicated"></a><span data-ttu-id="0bd15-103">Lo que se replica</span><span class="sxs-lookup"><span data-stu-id="0bd15-103">What Gets Replicated</span></span>

## <a name="applications"></a><span data-ttu-id="0bd15-104">APLICACIONES</span><span class="sxs-lookup"><span data-stu-id="0bd15-104">Applications</span></span>

<span data-ttu-id="0bd15-105">Todas las aplicaciones instaladas en el equipo de origen se replican, excepto las siguientes:</span><span class="sxs-lookup"><span data-stu-id="0bd15-105">All applications installed on the source computer are replicated except for the following:</span></span>

<dl> <dt>

<span data-ttu-id="0bd15-106"><span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Elementos y dependencias de aplicaciones que no son COM +</span><span class="sxs-lookup"><span data-stu-id="0bd15-106"><span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Non-COM+ application elements and dependencies</span></span>
</dt> <dd>

<span data-ttu-id="0bd15-107">El administrador es responsable de replicar todo aquello del que depende una aplicación COM+ pero que no forma parte correctamente de la propia aplicación, como archivos de datos y archivos dll.</span><span class="sxs-lookup"><span data-stu-id="0bd15-107">The administrator is responsible for replicating anything that a COM+ application depends on but which is not properly part of the application itself, such as data files and DLLs.</span></span> <span data-ttu-id="0bd15-108">COMREPL no replicará nada fuera de los elementos de la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="0bd15-108">COMREPL will not replicate anything outside of COM+ application elements.</span></span>

</dd> <dt>

<span data-ttu-id="0bd15-109"><span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>Aplicaciones preinstaladas de COM+</span><span class="sxs-lookup"><span data-stu-id="0bd15-109"><span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>COM+ preinstalled applications</span></span>
</dt> <dd>

<span data-ttu-id="0bd15-110">Las aplicaciones que usa COM+ y que se instalan a través del programa de instalación de COM+ no se replican.</span><span class="sxs-lookup"><span data-stu-id="0bd15-110">Applications that are used internally by COM+ and are installed via the COM+ setup program are not replicated.</span></span> <span data-ttu-id="0bd15-111">Entre ellas, figuran:</span><span class="sxs-lookup"><span data-stu-id="0bd15-111">These include the following:</span></span>

-   <span data-ttu-id="0bd15-112">Aplicación del sistema</span><span class="sxs-lookup"><span data-stu-id="0bd15-112">System application</span></span>
-   <span data-ttu-id="0bd15-113">Utilidades COM+</span><span class="sxs-lookup"><span data-stu-id="0bd15-113">COM+ utilities</span></span>
-   <span data-ttu-id="0bd15-114">Agente de escucha de cola de mensajes con problemas de entrega COM+</span><span class="sxs-lookup"><span data-stu-id="0bd15-114">COM+ QC Dead Letter Queue Listener</span></span>

</dd> <dt>

<span data-ttu-id="0bd15-115"><span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Aplicaciones creadas por IIS</span><span class="sxs-lookup"><span data-stu-id="0bd15-115"><span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Applications created by IIS</span></span>
</dt> <dd>

<span data-ttu-id="0bd15-116">Estas aplicaciones no se replican e incluyen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0bd15-116">These applications are not replicated and include the following:</span></span>

-   <span data-ttu-id="0bd15-117">Aplicaciones en proceso de IIS</span><span class="sxs-lookup"><span data-stu-id="0bd15-117">IIS in-process applications</span></span>
-   <span data-ttu-id="0bd15-118">Utilidades IIS</span><span class="sxs-lookup"><span data-stu-id="0bd15-118">IIS utilities</span></span>
-   <span data-ttu-id="0bd15-119">Todas las aplicaciones creadas para las raíces virtuales agrupadas o aisladas</span><span class="sxs-lookup"><span data-stu-id="0bd15-119">All applications created for isolated or pooled virtual roots</span></span>

</dd> </dl>

## <a name="computer-list"></a><span data-ttu-id="0bd15-120">Lista de equipos</span><span class="sxs-lookup"><span data-stu-id="0bd15-120">Computer List</span></span>

<span data-ttu-id="0bd15-121">Los equipos remotos nombrados en la carpeta **equipos** de la herramienta de administración de servicios de componentes no se replicarán desde el equipo de origen al de destino.</span><span class="sxs-lookup"><span data-stu-id="0bd15-121">The remote computers named in the **Computers** folder in the Component Services administration tool will not be replicated from source to target computer.</span></span>

## <a name="properties"></a><span data-ttu-id="0bd15-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0bd15-122">Properties</span></span>

<span data-ttu-id="0bd15-123">Se replican las siguientes propiedades de la colección **LocalComputer** :</span><span class="sxs-lookup"><span data-stu-id="0bd15-123">The following **LocalComputer** collection properties are replicated:</span></span>

-   <span data-ttu-id="0bd15-124">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="0bd15-124">TransactionTimeout</span></span>
-   <span data-ttu-id="0bd15-125">ResourcePoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="0bd15-125">ResourcePoolingEnabled</span></span>
-   <span data-ttu-id="0bd15-126">DCOMEnabled</span><span class="sxs-lookup"><span data-stu-id="0bd15-126">DCOMEnabled</span></span>
-   <span data-ttu-id="0bd15-127">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="0bd15-127">DefaultAuthenticationLevel</span></span>
-   <span data-ttu-id="0bd15-128">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="0bd15-128">DefaultImpersonationLevel</span></span>
-   <span data-ttu-id="0bd15-129">SecurityTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="0bd15-129">SecurityTrackingEnabled</span></span>
-   <span data-ttu-id="0bd15-130">CISEnabled</span><span class="sxs-lookup"><span data-stu-id="0bd15-130">CISEnabled</span></span>
-   <span data-ttu-id="0bd15-131">SecureReferencesEnabled</span><span class="sxs-lookup"><span data-stu-id="0bd15-131">SecureReferencesEnabled</span></span>
-   <span data-ttu-id="0bd15-132">InternetPortsListed</span><span class="sxs-lookup"><span data-stu-id="0bd15-132">InternetPortsListed</span></span>
-   <span data-ttu-id="0bd15-133">DeafultToInternetPorts</span><span class="sxs-lookup"><span data-stu-id="0bd15-133">DeafultToInternetPorts</span></span>
-   <span data-ttu-id="0bd15-134">Puertos</span><span class="sxs-lookup"><span data-stu-id="0bd15-134">Ports</span></span>
-   <span data-ttu-id="0bd15-135">RpcProxyEnabled</span><span class="sxs-lookup"><span data-stu-id="0bd15-135">RpcProxyEnabled</span></span>

<span data-ttu-id="0bd15-136">Las siguientes propiedades de la colección **LocalComputer** no se replican:</span><span class="sxs-lookup"><span data-stu-id="0bd15-136">The following **LocalComputer** collection properties are not replicated:</span></span>

-   <span data-ttu-id="0bd15-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="0bd15-137">Description</span></span>
-   <span data-ttu-id="0bd15-138">ApplicationProxyRSN</span><span class="sxs-lookup"><span data-stu-id="0bd15-138">ApplicationProxyRSN</span></span>
-   <span data-ttu-id="0bd15-139">IsRouter</span><span class="sxs-lookup"><span data-stu-id="0bd15-139">IsRouter</span></span>

<span data-ttu-id="0bd15-140">Para obtener descripciones de las propiedades de la colección **LocalComputer** , vea [**LocalComputer**](localcomputer.md).</span><span class="sxs-lookup"><span data-stu-id="0bd15-140">For descriptions of the **LocalComputer** collection properties, see [**LocalComputer**](localcomputer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bd15-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0bd15-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bd15-142">Administración de archivos</span><span class="sxs-lookup"><span data-stu-id="0bd15-142">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="0bd15-143">Registro e informes de errores</span><span class="sxs-lookup"><span data-stu-id="0bd15-143">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="0bd15-144">Fases de replicación</span><span class="sxs-lookup"><span data-stu-id="0bd15-144">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="0bd15-145">Usar COMREPL</span><span class="sxs-lookup"><span data-stu-id="0bd15-145">Using COMREPL</span></span>](using-comrepl.md)
</dt> </dl>

 

 




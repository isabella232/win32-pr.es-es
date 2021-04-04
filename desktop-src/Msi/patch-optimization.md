---
description: Windows Installer puede optimizar la aplicación de revisiones para reducir el tiempo necesario para aplicar revisiones a las aplicaciones instaladas.
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: Optimización de revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86215855bb02314d7eb54c774541b0a2086c7c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908705"
---
# <a name="patch-optimization"></a><span data-ttu-id="2f626-103">Optimización de revisiones</span><span class="sxs-lookup"><span data-stu-id="2f626-103">Patch Optimization</span></span>

<span data-ttu-id="2f626-104">Windows Installer puede optimizar la aplicación de revisiones para reducir el tiempo necesario para aplicar revisiones a las aplicaciones instaladas.</span><span class="sxs-lookup"><span data-stu-id="2f626-104">Windows Installer can optimize patching to reduce the time that is required to apply patches to installed applications.</span></span>

<span data-ttu-id="2f626-105">**Windows Installer 2,0:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="2f626-105">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="2f626-106">En el caso de las versiones de Windows Installer publicadas antes de Windows Installer 3,0, la aplicación de revisiones ejecuta una instalación de reparación completa de la aplicación, lo que puede tardar mucho más tiempo.</span><span class="sxs-lookup"><span data-stu-id="2f626-106">For versions of Windows Installer released before Windows Installer 3.0, patching runs a complete repair installation of the application, which can take significantly more time.</span></span>

<span data-ttu-id="2f626-107">**Windows Installer 3,0 y versiones posteriores:** El proceso de aplicación de revisiones solo cambia las partes de una aplicación que se modifican mediante una revisión.</span><span class="sxs-lookup"><span data-stu-id="2f626-107">**Windows Installer 3.0 and later:** The patching process only changes the parts of an application that are modified by a patch.</span></span>

<span data-ttu-id="2f626-108">**Windows Installer 3,1 y versiones posteriores:** A partir de Windows Installer 3,1, la optimización de revisiones requiere que todas las revisiones de la transacción tengan la propiedad OptimizedInstallMode establecida en 1 (uno) en la [tabla MsiPatchMetadata](msipatchmetadata-table.md).</span><span class="sxs-lookup"><span data-stu-id="2f626-108">**Windows Installer 3.1 and later:** Beginning with Windows Installer 3.1, patch optimization requires that all patches in the transaction have the OptimizedInstallMode property set to 1 (one) in the [MsiPatchMetadata Table](msipatchmetadata-table.md).</span></span>

<span data-ttu-id="2f626-109">Si una revisión solo modifica las tablas siguientes, Windows Installer 3,0 o una versión posterior omite las acciones asociadas a las demás tablas, incluso si dichas acciones se muestran en las tablas de secuencias del paquete de instalación original de la aplicación (archivo. msi).</span><span class="sxs-lookup"><span data-stu-id="2f626-109">If a patch only modifies the following tables, Windows Installer 3.0 or later skips the actions that are associated with all the other tables, even if those actions are listed in the sequence tables of the original application installation package (.msi file).</span></span>

-   [<span data-ttu-id="2f626-110">AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="2f626-110">AdminExecuteSequence</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="2f626-111">AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="2f626-111">AdminUISequence</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="2f626-112">Condition</span><span class="sxs-lookup"><span data-stu-id="2f626-112">Condition</span></span>](condition-table.md)
-   [<span data-ttu-id="2f626-113">CustomAction</span><span class="sxs-lookup"><span data-stu-id="2f626-113">CustomAction</span></span>](customaction-table.md)
-   [<span data-ttu-id="2f626-114">Archivo</span><span class="sxs-lookup"><span data-stu-id="2f626-114">File</span></span>](file-table.md)
-   [<span data-ttu-id="2f626-115">FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="2f626-115">FileSFPCatalog</span></span>](filesfpcatalog-table.md)
-   [<span data-ttu-id="2f626-116">InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="2f626-116">InstallExecuteSequence</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="2f626-117">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="2f626-117">InstallUISequence</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="2f626-118">Elementos multimedia</span><span class="sxs-lookup"><span data-stu-id="2f626-118">Media</span></span>](media-table.md)
-   [<span data-ttu-id="2f626-119">MoveFile</span><span class="sxs-lookup"><span data-stu-id="2f626-119">MoveFile</span></span>](movefile-table.md)
-   [<span data-ttu-id="2f626-120">MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="2f626-120">MsiAssembly</span></span>](msiassembly-table.md)
-   [<span data-ttu-id="2f626-121">MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="2f626-121">MsiDigitalCertificate</span></span>](msidigitalcertificate-table.md)
-   [<span data-ttu-id="2f626-122">MsiDigitalSignature</span><span class="sxs-lookup"><span data-stu-id="2f626-122">MsiDigitalSignature</span></span>](msidigitalsignature-table.md)
-   [<span data-ttu-id="2f626-123">MsiFileHash</span><span class="sxs-lookup"><span data-stu-id="2f626-123">MsiFileHash</span></span>](msifilehash-table.md)
-   [<span data-ttu-id="2f626-124">MsiPatchHeaders</span><span class="sxs-lookup"><span data-stu-id="2f626-124">MsiPatchHeaders</span></span>](msipatchheaders-table.md)
-   [<span data-ttu-id="2f626-125">Revisión</span><span class="sxs-lookup"><span data-stu-id="2f626-125">Patch</span></span>](patch-table.md)
-   [<span data-ttu-id="2f626-126">PatchPackage</span><span class="sxs-lookup"><span data-stu-id="2f626-126">PatchPackage</span></span>](patchpackage-table.md)
-   [<span data-ttu-id="2f626-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2f626-127">Property</span></span>](property-table.md)
-   [<span data-ttu-id="2f626-128">Registro</span><span class="sxs-lookup"><span data-stu-id="2f626-128">Registry</span></span>](registry-table.md)
-   [<span data-ttu-id="2f626-129">SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="2f626-129">SFPCatalog</span></span>](sfpcatalog-table.md)
-   [<span data-ttu-id="2f626-130">TypeLib</span><span class="sxs-lookup"><span data-stu-id="2f626-130">TypeLib</span></span>](typelib-table.md)
-   [<span data-ttu-id="2f626-131">\_Columnas</span><span class="sxs-lookup"><span data-stu-id="2f626-131">\_Columns</span></span>](-columns-table.md)
-   [<span data-ttu-id="2f626-132">\_Almacenamientos</span><span class="sxs-lookup"><span data-stu-id="2f626-132">\_Storages</span></span>](-storages-table.md)
-   [<span data-ttu-id="2f626-133">\_Secuencias</span><span class="sxs-lookup"><span data-stu-id="2f626-133">\_Streams</span></span>](-streams-table.md)
-   [<span data-ttu-id="2f626-134">\_Tablas</span><span class="sxs-lookup"><span data-stu-id="2f626-134">\_Tables</span></span>](-tables-table.md)
-   [<span data-ttu-id="2f626-135">\_Tabla TransformView</span><span class="sxs-lookup"><span data-stu-id="2f626-135">\_TransformView Table</span></span>](-transformview-table.md)
-   [<span data-ttu-id="2f626-136">\_Validación</span><span class="sxs-lookup"><span data-stu-id="2f626-136">\_Validation</span></span>](-validation-table.md)

<span data-ttu-id="2f626-137">Para desactivar la opción de optimización de revisiones, use la directiva [DisableFlyWeightPatching](disableflyweightpatching.md) .</span><span class="sxs-lookup"><span data-stu-id="2f626-137">To turn off the patch optimization option, use the [DisableFlyWeightPatching](disableflyweightpatching.md) policy.</span></span>

 

 




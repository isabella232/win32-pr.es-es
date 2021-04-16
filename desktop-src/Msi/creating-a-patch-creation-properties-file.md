---
description: Para reproducir el paquete de revisión de ejemplo, necesita una herramienta de software capaz de crear y editar un paquete de revisión de Windows Installer.
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: Crear un archivo de propiedades de creación de revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2775f8521731b43264df315ae05a874e37dd3ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669926"
---
# <a name="creating-a-patch-creation-properties-file"></a><span data-ttu-id="03f9b-103">Crear un archivo de propiedades de creación de revisiones</span><span class="sxs-lookup"><span data-stu-id="03f9b-103">Creating a Patch Creation Properties File</span></span>

<span data-ttu-id="03f9b-104">Para reproducir el paquete de revisión de ejemplo, necesita una herramienta de software capaz de crear y editar un paquete de revisión de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="03f9b-104">To reproduce the sample patch package, you need a software tool capable of creating and editing a Windows Installer patch package.</span></span> <span data-ttu-id="03f9b-105">Hay disponibles varias herramientas de creación de paquetes de revisiones de fabricantes de software independientes.</span><span class="sxs-lookup"><span data-stu-id="03f9b-105">Several patch package creation tools are available from independent software vendors.</span></span> <span data-ttu-id="03f9b-106">En el ejemplo que se describe en las secciones siguientes se usa un editor de base de datos de Windows Installer denominado orca para crear un archivo de propiedades de creación de revisiones (extensión. PCP).</span><span class="sxs-lookup"><span data-stu-id="03f9b-106">The example discussed in the following sections uses a Windows Installer database editor called Orca to author a patch creation properties file (.pcp extension).</span></span> <span data-ttu-id="03f9b-107">El archivo. PCP se puede usar con las utilidades [Msimsp.exe](msimsp-exe.md) y [Patchwiz.dll](patchwiz-dll.md) para generar un paquete de revisión de Windows Installer (extensión. msp).</span><span class="sxs-lookup"><span data-stu-id="03f9b-107">The .pcp file may be used with the utilities [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) to generate a Windows Installer patch package (.msp extension).</span></span> <span data-ttu-id="03f9b-108">Orca, Msimsp.exe y Patchwiz.dll se proporcionan en los [componentes Windows SDK para los programadores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="03f9b-108">Orca, Msimsp.exe, and Patchwiz.dll are provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="03f9b-109">También se proporciona un archivo de propiedades de creación de revisiones en blanco, template. PCP, con el SDK.</span><span class="sxs-lookup"><span data-stu-id="03f9b-109">A blank patch creation properties file, template.pcp, is also provided with the SDK.</span></span> <span data-ttu-id="03f9b-110">Haga una copia de template. PCP y cambie el nombre de esta copia MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="03f9b-110">Make a copy of template.pcp and rename this copy MNP2000.pcp.</span></span> <span data-ttu-id="03f9b-111">Use Orca u otro editor de bases de datos para especificar los datos siguientes en la tabla de propiedades de MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="03f9b-111">Use Orca or another database editor to enter the following data into the Properties table of MNP2000.pcp.</span></span> <span data-ttu-id="03f9b-112">La tabla de propiedades contiene la configuración global del paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="03f9b-112">The Properties table contains global settings for the patch package.</span></span>

[<span data-ttu-id="03f9b-113">Propiedades de tabla</span><span class="sxs-lookup"><span data-stu-id="03f9b-113">Properties Table</span></span>](properties-table-patchwiz-dll-.md)



| <span data-ttu-id="03f9b-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="03f9b-114">Name</span></span>                               | <span data-ttu-id="03f9b-115">Value</span><span class="sxs-lookup"><span data-stu-id="03f9b-115">Value</span></span>                                  |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="03f9b-116">AllowProductCodeMismatches</span><span class="sxs-lookup"><span data-stu-id="03f9b-116">AllowProductCodeMismatches</span></span>         | <span data-ttu-id="03f9b-117">1</span><span class="sxs-lookup"><span data-stu-id="03f9b-117">1</span></span>                                      |
| <span data-ttu-id="03f9b-118">AllowProductVersionMajorMismatches</span><span class="sxs-lookup"><span data-stu-id="03f9b-118">AllowProductVersionMajorMismatches</span></span> | <span data-ttu-id="03f9b-119">1</span><span class="sxs-lookup"><span data-stu-id="03f9b-119">1</span></span>                                      |
| <span data-ttu-id="03f9b-120">ApiPatchingSymbolFlags</span><span class="sxs-lookup"><span data-stu-id="03f9b-120">ApiPatchingSymbolFlags</span></span>             | <span data-ttu-id="03f9b-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="03f9b-121">0x00000000</span></span>                             |
| <span data-ttu-id="03f9b-122">DontRemoveTempFolderWhenFinished</span><span class="sxs-lookup"><span data-stu-id="03f9b-122">DontRemoveTempFolderWhenFinished</span></span>   | <span data-ttu-id="03f9b-123">1</span><span class="sxs-lookup"><span data-stu-id="03f9b-123">1</span></span>                                      |
| <span data-ttu-id="03f9b-124">IncludeWholeFilesOnly</span><span class="sxs-lookup"><span data-stu-id="03f9b-124">IncludeWholeFilesOnly</span></span>              | <span data-ttu-id="03f9b-125">0</span><span class="sxs-lookup"><span data-stu-id="03f9b-125">0</span></span>                                      |
| <span data-ttu-id="03f9b-126">ListOfPatchGUIDsToReplace</span><span class="sxs-lookup"><span data-stu-id="03f9b-126">ListOfPatchGUIDsToReplace</span></span>          |                                        |
| <span data-ttu-id="03f9b-127">ListOfTargetProductCodes</span><span class="sxs-lookup"><span data-stu-id="03f9b-127">ListOfTargetProductCodes</span></span>           | \*                                     |
| <span data-ttu-id="03f9b-128">PatchGUID</span><span class="sxs-lookup"><span data-stu-id="03f9b-128">PatchGUID</span></span>                          | <span data-ttu-id="03f9b-129">{5406B219-A1AC-4BC4-8695-72292C8195AC}</span><span class="sxs-lookup"><span data-stu-id="03f9b-129">{5406B219-A1AC-4BC4-8695-72292C8195AC}</span></span> |
| <span data-ttu-id="03f9b-130">PatchOutputPath</span><span class="sxs-lookup"><span data-stu-id="03f9b-130">PatchOutputPath</span></span>                    | <span data-ttu-id="03f9b-131">c: \\ salida. MSP</span><span class="sxs-lookup"><span data-stu-id="03f9b-131">c:\\output.msp</span></span>                         |
| <span data-ttu-id="03f9b-132">PatchSourceList</span><span class="sxs-lookup"><span data-stu-id="03f9b-132">PatchSourceList</span></span>                    | <span data-ttu-id="03f9b-133">PatchSourceList</span><span class="sxs-lookup"><span data-stu-id="03f9b-133">PatchSourceList</span></span>                        |



 

<span data-ttu-id="03f9b-134">Use el editor de base de datos para escribir los siguientes datos en la tabla ImageFamilies de MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="03f9b-134">Use the database editor to enter the following data into the ImageFamilies table of MNP2000.pcp.</span></span> <span data-ttu-id="03f9b-135">La tabla ImageFamilies contiene información que se va a agregar a la [tabla de medios](media-table.md) durante la revisión.</span><span class="sxs-lookup"><span data-stu-id="03f9b-135">The ImageFamilies table contains information to be added to the [Media table](media-table.md) during patching.</span></span>

[<span data-ttu-id="03f9b-136">Tabla ImageFamilies</span><span class="sxs-lookup"><span data-stu-id="03f9b-136">ImageFamilies Table</span></span>](imagefamilies-table-patchwiz-dll-.md)



| <span data-ttu-id="03f9b-137">Familia</span><span class="sxs-lookup"><span data-stu-id="03f9b-137">Family</span></span>  | <span data-ttu-id="03f9b-138">MediaSrcPropName</span><span class="sxs-lookup"><span data-stu-id="03f9b-138">MediaSrcPropName</span></span> | <span data-ttu-id="03f9b-139">MediaDiskId</span><span class="sxs-lookup"><span data-stu-id="03f9b-139">MediaDiskId</span></span> | <span data-ttu-id="03f9b-140">FileSequenceStart</span><span class="sxs-lookup"><span data-stu-id="03f9b-140">FileSequenceStart</span></span> | <span data-ttu-id="03f9b-141">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="03f9b-141">DiskPrompt</span></span> | <span data-ttu-id="03f9b-142">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="03f9b-142">VolumeLabel</span></span> |
|---------|------------------|-------------|-------------------|------------|-------------|
| <span data-ttu-id="03f9b-143">MNPapps</span><span class="sxs-lookup"><span data-stu-id="03f9b-143">MNPapps</span></span> | <span data-ttu-id="03f9b-144">MNPSrcPropName</span><span class="sxs-lookup"><span data-stu-id="03f9b-144">MNPSrcPropName</span></span>   | <span data-ttu-id="03f9b-145">2</span><span class="sxs-lookup"><span data-stu-id="03f9b-145">2</span></span>           | <span data-ttu-id="03f9b-146">1000</span><span class="sxs-lookup"><span data-stu-id="03f9b-146">1000</span></span>              |            |             |



 

<span data-ttu-id="03f9b-147">Escriba los datos siguientes en la tabla UpgradedImages de MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="03f9b-147">Enter the following data into the UpgradedImages table of MNP2000.pcp.</span></span> <span data-ttu-id="03f9b-148">La tabla UpgradedImages contiene información sobre la imagen actualizada que ha creado en la sección [planeación de una pequeña revisión de actualización](planning-a-small-update-patch.md).</span><span class="sxs-lookup"><span data-stu-id="03f9b-148">The UpgradedImages table contains information about the Upgraded image you created in [Planning a Small Update Patch](planning-a-small-update-patch.md).</span></span>

[<span data-ttu-id="03f9b-149">Tabla UpgradedImages</span><span class="sxs-lookup"><span data-stu-id="03f9b-149">UpgradedImages Table</span></span>](upgradedimages-table-patchwiz-dll-.md)



| <span data-ttu-id="03f9b-150">Upgraded</span><span class="sxs-lookup"><span data-stu-id="03f9b-150">Upgraded</span></span>   | <span data-ttu-id="03f9b-151">Rutamsi</span><span class="sxs-lookup"><span data-stu-id="03f9b-151">MsiPath</span></span>                                           | <span data-ttu-id="03f9b-152">PatchMsiPath</span><span class="sxs-lookup"><span data-stu-id="03f9b-152">PatchMsiPath</span></span> | <span data-ttu-id="03f9b-153">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="03f9b-153">SymbolPaths</span></span> | <span data-ttu-id="03f9b-154">Familia</span><span class="sxs-lookup"><span data-stu-id="03f9b-154">Family</span></span>  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| <span data-ttu-id="03f9b-155">MNP \_ fijo</span><span class="sxs-lookup"><span data-stu-id="03f9b-155">MNP\_fixed</span></span> | <span data-ttu-id="03f9b-156">C: \\ Nota \_ revisión del instalador \\ \\ actualizada \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="03f9b-156">C:\\Note\_Installer\\Patch\\Upgraded\\MNP2000.msi</span></span> |              |             | <span data-ttu-id="03f9b-157">MNPapps</span><span class="sxs-lookup"><span data-stu-id="03f9b-157">MNPapps</span></span> |



 

<span data-ttu-id="03f9b-158">Escriba los datos siguientes en la tabla TargetImages de MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="03f9b-158">Enter the following data into the TargetImages table of MNP2000.pcp.</span></span> <span data-ttu-id="03f9b-159">La tabla TargetImages contiene información sobre la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="03f9b-159">The TargetImages table contains information about the Target image.</span></span>

[<span data-ttu-id="03f9b-160">Tabla TargetImages</span><span class="sxs-lookup"><span data-stu-id="03f9b-160">TargetImages Table</span></span>](targetimages-table-patchwiz-dll-.md)



| <span data-ttu-id="03f9b-161">Destino</span><span class="sxs-lookup"><span data-stu-id="03f9b-161">Target</span></span>     | <span data-ttu-id="03f9b-162">Rutamsi</span><span class="sxs-lookup"><span data-stu-id="03f9b-162">MsiPath</span></span>                                         | <span data-ttu-id="03f9b-163">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="03f9b-163">SymbolPaths</span></span> | <span data-ttu-id="03f9b-164">Upgraded</span><span class="sxs-lookup"><span data-stu-id="03f9b-164">Upgraded</span></span>   | <span data-ttu-id="03f9b-165">Pedido</span><span class="sxs-lookup"><span data-stu-id="03f9b-165">Order</span></span> | <span data-ttu-id="03f9b-166">ProductValidateFlags</span><span class="sxs-lookup"><span data-stu-id="03f9b-166">ProductValidateFlags</span></span> | <span data-ttu-id="03f9b-167">IgnoreMissingSrcFiles</span><span class="sxs-lookup"><span data-stu-id="03f9b-167">IgnoreMissingSrcFiles</span></span> |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| <span data-ttu-id="03f9b-168">Error de MNP \_</span><span class="sxs-lookup"><span data-stu-id="03f9b-168">MNP\_error</span></span> | <span data-ttu-id="03f9b-169">C: \\ tenga en cuenta el \_ destino de revisión del instalador \\ \\ \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="03f9b-169">C:\\Note\_Installer\\Patch\\Target\\MNP2000.msi</span></span> |             | <span data-ttu-id="03f9b-170">MNP \_ fijo</span><span class="sxs-lookup"><span data-stu-id="03f9b-170">MNP\_fixed</span></span> | <span data-ttu-id="03f9b-171">1</span><span class="sxs-lookup"><span data-stu-id="03f9b-171">1</span></span>     |                      | <span data-ttu-id="03f9b-172">0</span><span class="sxs-lookup"><span data-stu-id="03f9b-172">0</span></span>                     |



 

<span data-ttu-id="03f9b-173">En el paquete de revisión de ejemplo, deje en blanco las siguientes tablas en MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="03f9b-173">For the sample patch package, leave the following tables in MNP2000.pcp blank.</span></span>

[<span data-ttu-id="03f9b-174">\_Tabla OptionalData UpgradedFiles</span><span class="sxs-lookup"><span data-stu-id="03f9b-174">UpgradedFiles\_OptionalData Table</span></span>](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[<span data-ttu-id="03f9b-175">Tabla FamilyFileRanges</span><span class="sxs-lookup"><span data-stu-id="03f9b-175">FamilyFileRanges Table</span></span>](familyfileranges-table-patchwiz-dll-.md)

[<span data-ttu-id="03f9b-176">\_Tabla OptionalData TargetFiles</span><span class="sxs-lookup"><span data-stu-id="03f9b-176">TargetFiles\_OptionalData Table</span></span>](targetfiles-optionaldata-table-patchwiz-dll-.md)

[<span data-ttu-id="03f9b-177">Tabla ExternalFiles</span><span class="sxs-lookup"><span data-stu-id="03f9b-177">ExternalFiles Table</span></span>](externalfiles-table-patchwiz-dll-.md)

[<span data-ttu-id="03f9b-178">Tabla UpgradedFilesToIgnore</span><span class="sxs-lookup"><span data-stu-id="03f9b-178">UpgradedFilesToIgnore Table</span></span>](upgradedfilestoignore-table-patchwiz-dll-.md)

[<span data-ttu-id="03f9b-179">Continuar</span><span class="sxs-lookup"><span data-stu-id="03f9b-179">Continue</span></span>](generating-a-patch-package.md)

 

 




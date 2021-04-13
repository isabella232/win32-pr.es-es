---
description: Para generar un paquete de revisión, se recomienda usar una herramienta de creación de revisiones como Msimsp.exe y Patchwiz.dll.
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6dc1135a9e2c09bb8a96e041f77bae39f0057ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279327"
---
# <a name="patchwizdll"></a><span data-ttu-id="a389f-103">Patchwiz.dll</span><span class="sxs-lookup"><span data-stu-id="a389f-103">Patchwiz.dll</span></span>

<span data-ttu-id="a389f-104">Para generar un paquete de revisión, se recomienda usar una herramienta de creación de revisiones como [Msimsp.exe](msimsp-exe.md) y Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="a389f-104">To generate a patch package, it is recommended that you use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) and Patchwiz.dll.</span></span> <span data-ttu-id="a389f-105">Patchwiz.dll versión 4,0 es compatible con los paquetes y las revisiones que se crearon con versiones anteriores de la Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="a389f-105">Patchwiz.dll version 4.0 is compatible with packages and patches that were authored using earlier versions of the Patchwiz.dll.</span></span> <span data-ttu-id="a389f-106">La herramienta Patchwiz.dll solo está disponible en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="a389f-106">The Patchwiz.dll tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="a389f-107">Patchwiz.dll versión 4,0 tiene una nueva función, [UiCreatePatchPackageEx (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), que extiende la funcionalidad de [UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="a389f-107">Patchwiz.dll version 4.0 has one new function, [UiCreatePatchPackageEx (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), that extends the functionality of [UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md).</span></span> <span data-ttu-id="a389f-108">Estas funciones toman un archivo de propiedades de creación de revisiones (archivo. PCP) y generan un [paquete de revisión](patch-packages.md)del instalador.</span><span class="sxs-lookup"><span data-stu-id="a389f-108">These functions take a patch creation properties file (.pcp file) and generate an installer [Patch Package](patch-packages.md).</span></span>

<span data-ttu-id="a389f-109">El archivo. PCP es un archivo de base de datos binario con el mismo formato que una base de datos de Windows Installer (archivo. msi), pero con un esquema de base de datos diferente.</span><span class="sxs-lookup"><span data-stu-id="a389f-109">The .pcp file is a binary database file with the same format as a Windows Installer database (.msi file), but with a different database schema.</span></span> <span data-ttu-id="a389f-110">Por lo tanto, se puede crear un archivo. PCP con las mismas herramientas que se usan para una base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="a389f-110">Therefore a .pcp file can be authored by using the same tools used for an installer database.</span></span>

<span data-ttu-id="a389f-111">Puede crear un archivo. PCP mediante un editor de tablas como [Orca.exe](orca-exe.md) para escribir información en la base de datos en blanco. el PCP proporcionado con el Windows Installer SDK, template. PCP.</span><span class="sxs-lookup"><span data-stu-id="a389f-111">You can create a .pcp file by using a table editor such as [Orca.exe](orca-exe.md) to enter information into the blank .pcp database provided with the Windows Installer SDK, Template.pcp.</span></span> <span data-ttu-id="a389f-112">Para obtener más información, vea [un pequeño ejemplo de revisión de actualización](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="a389f-112">For more information, see [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="a389f-113">Las tablas de base de datos siguientes son necesarias en cada archivo. PCP:</span><span class="sxs-lookup"><span data-stu-id="a389f-113">The following database tables are required in every .pcp file:</span></span>

-   [<span data-ttu-id="a389f-114">Tabla de propiedades (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="a389f-114">Properties Table (Patchwiz.dll)</span></span>](properties-table-patchwiz-dll-.md)
-   [<span data-ttu-id="a389f-115">Tabla ImageFamilies (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="a389f-115">ImageFamilies Table (Patchwiz.dll)</span></span>](imagefamilies-table-patchwiz-dll-.md)
-   [<span data-ttu-id="a389f-116">Tabla UpgradedImages (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="a389f-116">UpgradedImages Table (Patchwiz.dll)</span></span>](upgradedimages-table-patchwiz-dll-.md)
-   [<span data-ttu-id="a389f-117">Tabla TargetImages (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="a389f-117">TargetImages Table (Patchwiz.dll)</span></span>](targetimages-table-patchwiz-dll-.md)

<span data-ttu-id="a389f-118">Las tablas de base de datos siguientes son opcionales:</span><span class="sxs-lookup"><span data-stu-id="a389f-118">The following database tables are optional:</span></span>

-   [<span data-ttu-id="a389f-119">UpgradedFiles \_ OptionalData (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="a389f-119">UpgradedFiles\_OptionalData Table (Patchwiz.dll)</span></span>](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [<span data-ttu-id="a389f-120">Tabla FamilyFileRanges (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="a389f-120">FamilyFileRanges Table (Patchwiz.dll)</span></span>](familyfileranges-table-patchwiz-dll-.md)
-   [<span data-ttu-id="a389f-121">TargetFiles \_ OptionalData (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="a389f-121">TargetFiles\_OptionalData Table (Patchwiz.dll)</span></span>](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [<span data-ttu-id="a389f-122">Tabla ExternalFiles (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="a389f-122">ExternalFiles Table (Patchwiz.dll)</span></span>](externalfiles-table-patchwiz-dll-.md)
-   [<span data-ttu-id="a389f-123">Tabla UpgradedFilesToIgnore (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="a389f-123">UpgradedFilesToIgnore Table (Patchwiz.dll)</span></span>](upgradedfilestoignore-table-patchwiz-dll-.md)

<span data-ttu-id="a389f-124">La tabla siguiente es necesaria en los archivos. PCP que tienen un valor de MinimumRequiredMsiVersion igual a 300 en la tabla de [propiedades](properties-table-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="a389f-124">The following table is required in .pcp files that have a MinimumRequiredMsiVersion equal to 300 in the [Properties](properties-table-patchwiz-dll-.md) table.</span></span>

-   [<span data-ttu-id="a389f-125">Tabla PatchMetadata (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="a389f-125">PatchMetadata Table (Patchwiz.dll)</span></span>](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> <span data-ttu-id="a389f-126">La tabla es opcional si MinimumRequiredMsiVersion no es igual a 300.</span><span class="sxs-lookup"><span data-stu-id="a389f-126">The table is optional if MinimumRequiredMsiVersion is not equal to 300.</span></span>

 

<span data-ttu-id="a389f-127">La versión de Patchwiz.dll publicada con Windows Installer 3,0 puede generar automáticamente información de secuenciación de revisiones y agregarla a la [tabla MsiPatchSequence](msipatchsequence-table.md) de una nueva revisión.</span><span class="sxs-lookup"><span data-stu-id="a389f-127">The version of Patchwiz.dll released with Windows Installer 3.0 can automatically generate patch sequencing information and add it to the [MsiPatchSequence Table](msipatchsequence-table.md) of a new patch.</span></span> <span data-ttu-id="a389f-128">La [tabla PatchSequence](patchsequence-table--patchwiz-dll-.md) se puede usar para agregar manualmente la información de secuenciación de revisiones a la tabla MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="a389f-128">The [PatchSequence Table](patchsequence-table--patchwiz-dll-.md) can be used to manually add patch sequencing information the MsiPatchSequence Table.</span></span> <span data-ttu-id="a389f-129">Para obtener más información, vea [generar información de secuencia de revisión](generating-patch-sequence-information---patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="a389f-129">For more information, see [Generating Patch Sequence Information](generating-patch-sequence-information---patchwiz-dll-.md).</span></span>

<span data-ttu-id="a389f-130">A partir de Patchwiz.dll versión 2,0, puede aumentar la velocidad de la creación posterior de revisiones mediante el [almacenamiento en caché de la información de revisión (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="a389f-130">Beginning with Patchwiz.dll version 2.0, you can increase the speed of subsequent patch creation by using [Patch Information Caching (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).</span></span>

<span data-ttu-id="a389f-131">El uso de símbolos públicos para los archivos binarios de imagen de destino y actualización puede reducir el tamaño de las revisiones binarias en aproximadamente una mitad.</span><span class="sxs-lookup"><span data-stu-id="a389f-131">Using public symbols for your target and upgrade image binaries can reduce binary patch sizes by approximately one half.</span></span> <span data-ttu-id="a389f-132">Para obtener más información, vea [usar símbolos para reducir el tamaño de las revisiones binarias](using-symbols-to-reduce-binary-patch-size.md).</span><span class="sxs-lookup"><span data-stu-id="a389f-132">For more information, see [Using Symbols to Reduce Binary Patch Size](using-symbols-to-reduce-binary-patch-size.md).</span></span>

<span data-ttu-id="a389f-133">Puede especificar que se conserven que se sobrescriban determinadas regiones del archivo de destino durante la revisión y que se retenga la información de esas regiones.</span><span class="sxs-lookup"><span data-stu-id="a389f-133">You can specify that certain regions of the target file be preserved from being overwritten during patching and that the information in those regions be retained.</span></span> <span data-ttu-id="a389f-134">Para obtener más información, consulte [aplicar revisiones a las regiones seleccionadas de un archivo](patching-selected-regions-of-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="a389f-134">For more information, see [Patching Selected Regions of a File](patching-selected-regions-of-a-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a389f-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a389f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a389f-136">Versiones publicadas, herramientas y redistribuibles</span><span class="sxs-lookup"><span data-stu-id="a389f-136">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 




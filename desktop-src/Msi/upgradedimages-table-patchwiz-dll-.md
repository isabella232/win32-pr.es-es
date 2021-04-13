---
description: La tabla UpgradedImages contiene información sobre las imágenes actualizadas del producto.
ms.assetid: f4ee2cc8-8a49-4e4a-b8cf-b4ae2bc7e753
title: Tabla UpgradedImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48dcecc94786cbe783f21e6e005b645586f2e894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361390"
---
# <a name="upgradedimages-table-patchwizdll"></a><span data-ttu-id="0e928-103">Tabla UpgradedImages (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="0e928-103">UpgradedImages Table (Patchwiz.dll)</span></span>

<span data-ttu-id="0e928-104">La tabla UpgradedImages contiene información sobre las imágenes actualizadas del producto.</span><span class="sxs-lookup"><span data-stu-id="0e928-104">The UpgradedImages table contains information about the upgraded images of the product.</span></span> <span data-ttu-id="0e928-105">La imagen actualizada debe ser una imagen de instalación totalmente descomprimida de la versión más reciente del producto, por ejemplo, una imagen administrativa o una imagen de instalación sin comprimir de un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="0e928-105">The upgraded image should be a fully uncompressed setup image of the latest version of the product, for example, an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="0e928-106">Un paquete de revisión de Windows Installer actualiza una imagen de destino en una imagen actualizada.</span><span class="sxs-lookup"><span data-stu-id="0e928-106">A Windows Installer patch package updates a target image into an upgraded image.</span></span> <span data-ttu-id="0e928-107">La tabla UpgradedImages es necesaria en la base de datos de creación de revisiones (archivo. PCP) y se usa en [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="0e928-107">The UpgradedImages table is required in the patch creation database (.pcp file) and is used by [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span></span>

<span data-ttu-id="0e928-108">Se requiere una tabla UpgradedImages que contenga al menos un registro en cada base de datos de creación de revisiones (archivo. PCP).</span><span class="sxs-lookup"><span data-stu-id="0e928-108">An UpgradedImages table containing at least one record is required in every patch creation database (.pcp file).</span></span> <span data-ttu-id="0e928-109">Esta tabla la usa [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="0e928-109">This table is used by [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span></span>

<span data-ttu-id="0e928-110">La tabla UpgradedImages tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="0e928-110">The UpgradedImages table has the following columns.</span></span>



| <span data-ttu-id="0e928-111">Columna</span><span class="sxs-lookup"><span data-stu-id="0e928-111">Column</span></span>       | <span data-ttu-id="0e928-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e928-112">Type</span></span> | <span data-ttu-id="0e928-113">Clave</span><span class="sxs-lookup"><span data-stu-id="0e928-113">Key</span></span> | <span data-ttu-id="0e928-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="0e928-114">Nullable</span></span> |
|--------------|------|-----|----------|
| <span data-ttu-id="0e928-115">Upgraded</span><span class="sxs-lookup"><span data-stu-id="0e928-115">Upgraded</span></span>     | <span data-ttu-id="0e928-116">text</span><span class="sxs-lookup"><span data-stu-id="0e928-116">text</span></span> | <span data-ttu-id="0e928-117">Y</span><span class="sxs-lookup"><span data-stu-id="0e928-117">Y</span></span>   | <span data-ttu-id="0e928-118">N</span><span class="sxs-lookup"><span data-stu-id="0e928-118">N</span></span>        |
| <span data-ttu-id="0e928-119">Rutamsi</span><span class="sxs-lookup"><span data-stu-id="0e928-119">MsiPath</span></span>      | <span data-ttu-id="0e928-120">text</span><span class="sxs-lookup"><span data-stu-id="0e928-120">text</span></span> |     | <span data-ttu-id="0e928-121">N</span><span class="sxs-lookup"><span data-stu-id="0e928-121">N</span></span>        |
| <span data-ttu-id="0e928-122">PatchMsiPath</span><span class="sxs-lookup"><span data-stu-id="0e928-122">PatchMsiPath</span></span> | <span data-ttu-id="0e928-123">text</span><span class="sxs-lookup"><span data-stu-id="0e928-123">text</span></span> |     | <span data-ttu-id="0e928-124">Y</span><span class="sxs-lookup"><span data-stu-id="0e928-124">Y</span></span>        |
| <span data-ttu-id="0e928-125">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="0e928-125">SymbolPaths</span></span>  | <span data-ttu-id="0e928-126">text</span><span class="sxs-lookup"><span data-stu-id="0e928-126">text</span></span> |     | <span data-ttu-id="0e928-127">Y</span><span class="sxs-lookup"><span data-stu-id="0e928-127">Y</span></span>        |
| <span data-ttu-id="0e928-128">Familia</span><span class="sxs-lookup"><span data-stu-id="0e928-128">Family</span></span>       | <span data-ttu-id="0e928-129">text</span><span class="sxs-lookup"><span data-stu-id="0e928-129">text</span></span> |     | <span data-ttu-id="0e928-130">N</span><span class="sxs-lookup"><span data-stu-id="0e928-130">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0e928-131">Columnas</span><span class="sxs-lookup"><span data-stu-id="0e928-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0e928-132"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Actualizado</span><span class="sxs-lookup"><span data-stu-id="0e928-132"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="0e928-133">El campo actualizado es un identificador arbitrario para conectar las imágenes de destino con una imagen actualizada del producto.</span><span class="sxs-lookup"><span data-stu-id="0e928-133">The Upgraded field is an arbitrary identifier to connect the target images with an upgraded image of the product.</span></span>

</dd> <dt>

<span data-ttu-id="0e928-134"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>Rutamsi</span><span class="sxs-lookup"><span data-stu-id="0e928-134"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span></span>
</dt> <dd>

<span data-ttu-id="0e928-135">Este campo especifica la ruta de acceso completa, incluido el nombre de archivo, en la ubicación del archivo. msi de la imagen actualizada.</span><span class="sxs-lookup"><span data-stu-id="0e928-135">This field specifies the full path, including the file name, to the location of the .msi file for the upgraded image.</span></span> <span data-ttu-id="0e928-136">Esta es la ubicación de los archivos de origen de la imagen actualizada.</span><span class="sxs-lookup"><span data-stu-id="0e928-136">This is the location of the source files for the upgraded image.</span></span>

</dd> <dt>

<span data-ttu-id="0e928-137"><span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath</span><span class="sxs-lookup"><span data-stu-id="0e928-137"><span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath</span></span>
</dt> <dd>

<span data-ttu-id="0e928-138">El patchMsiPath opcional apunta a una copia modificada de la base de datos de instalación actualizada que contiene la creación adicional específica del proceso de instalación de la revisión.</span><span class="sxs-lookup"><span data-stu-id="0e928-138">The optional patchMsiPath points to a modified copy of the upgraded installation database that contains additional authoring specific to the patch installation process.</span></span> <span data-ttu-id="0e928-139">Por ejemplo, cuadros de diálogo adicionales o acciones personalizadas condicionadas en la propiedad [**patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="0e928-139">For example, additional dialogs or custom actions conditioned on the [**PATCH**](patch.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="0e928-140"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="0e928-140"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="0e928-141">Una lista delimitada por punto y coma de carpetas en las que se van a buscar archivos de símbolos que se pueden usar para optimizar la generación de la revisión binaria.</span><span class="sxs-lookup"><span data-stu-id="0e928-141">A semicolon delimited list of folders that are to be searched for symbol files that may be used to optimize the generation of the binary patch.</span></span> <span data-ttu-id="0e928-142">Tenga en cuenta que no se busca en los subdirectorios de las carpetas especificadas en este campo.</span><span class="sxs-lookup"><span data-stu-id="0e928-142">Note that the subdirectories of folders specified in this field are not searched.</span></span> <span data-ttu-id="0e928-143">Una revisión binaria optimizada puede ser menor.</span><span class="sxs-lookup"><span data-stu-id="0e928-143">An optimized binary patch may be smaller.</span></span> <span data-ttu-id="0e928-144">Visual C++ debe estar instalado en el equipo que genera la revisión y que se usa para crear los archivos de símbolos.</span><span class="sxs-lookup"><span data-stu-id="0e928-144">Visual C++ must be installed on the computer generating the patch and used to create the symbol files.</span></span> <span data-ttu-id="0e928-145">Este campo es opcional y el instalador crea una revisión binaria incluso si no se especifica ningún archivo de símbolos o si los archivos de símbolos dejan de estar disponibles para Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="0e928-145">This field is optional, and the installer creates a binary patch even if no symbol files are specified or if the symbol files become unavailable to Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="0e928-146"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Familia</span><span class="sxs-lookup"><span data-stu-id="0e928-146"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="0e928-147">Clave externa en la [tabla ImageFamilies](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="0e928-147">Foreign key into the [ImageFamilies table](imagefamilies-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="0e928-148">Cada imagen actualizada debe pertenecer a una sola familia.</span><span class="sxs-lookup"><span data-stu-id="0e928-148">Each upgraded image must belong to only one family.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e928-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e928-149">Remarks</span></span>

<span data-ttu-id="0e928-150">Aunque cada imagen actualizada se puede agrupar en una familia de imágenes independiente, la agrupación de imágenes actualizadas que compartan archivos juntos puede hacer que el archivo. MSP sea más pequeño.</span><span class="sxs-lookup"><span data-stu-id="0e928-150">Although each upgraded image can be grouped into a separate image family, grouping upgraded images that share files together may make the .msp smaller.</span></span>

<span data-ttu-id="0e928-151">Esta tabla acepta las variables de entorno como rutas de acceso a partir de la versión 4,0 de Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="0e928-151">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

 

 




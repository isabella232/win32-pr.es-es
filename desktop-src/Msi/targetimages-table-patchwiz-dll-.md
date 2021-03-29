---
description: La tabla TargetImages contiene información sobre las imágenes de destino del producto. Un paquete de revisión de Windows Installer actualiza una imagen de destino en una imagen actualizada.
ms.assetid: 4681715e-9918-4d7b-8f33-1cca2bb34eb7
title: Tabla TargetImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bbb8e7bae92fbc25b217808aaae709f079d65dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913069"
---
# <a name="targetimages-table-patchwizdll"></a><span data-ttu-id="b3b9d-104">Tabla TargetImages (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="b3b9d-104">TargetImages Table (Patchwiz.dll)</span></span>

<span data-ttu-id="b3b9d-105">La tabla TargetImages contiene información sobre las imágenes de destino del producto.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-105">The TargetImages table contains information about the target images of the product.</span></span> <span data-ttu-id="b3b9d-106">Un paquete de revisión de Windows Installer actualiza una imagen de destino en una imagen actualizada.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-106">A Windows Installer patch package updates a target image into an upgraded image.</span></span>

<span data-ttu-id="b3b9d-107">Se requiere una tabla TargetImages que contenga al menos un registro en cada base de datos de creación de revisiones (archivo. PCP).</span><span class="sxs-lookup"><span data-stu-id="b3b9d-107">A TargetImages table containing at least one record is required in every patch creation database (.pcp file).</span></span> <span data-ttu-id="b3b9d-108">La función [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) usa esta tabla.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-108">This table is used by the [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="b3b9d-109">La tabla TargetImages tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-109">The TargetImages table has the following columns.</span></span>



| <span data-ttu-id="b3b9d-110">Columna</span><span class="sxs-lookup"><span data-stu-id="b3b9d-110">Column</span></span>                | <span data-ttu-id="b3b9d-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3b9d-111">Type</span></span>    | <span data-ttu-id="b3b9d-112">Clave</span><span class="sxs-lookup"><span data-stu-id="b3b9d-112">Key</span></span> | <span data-ttu-id="b3b9d-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="b3b9d-113">Nullable</span></span> |
|-----------------------|---------|-----|----------|
| <span data-ttu-id="b3b9d-114">Destino</span><span class="sxs-lookup"><span data-stu-id="b3b9d-114">Target</span></span>                | <span data-ttu-id="b3b9d-115">text</span><span class="sxs-lookup"><span data-stu-id="b3b9d-115">text</span></span>    | <span data-ttu-id="b3b9d-116">Y</span><span class="sxs-lookup"><span data-stu-id="b3b9d-116">Y</span></span>   | <span data-ttu-id="b3b9d-117">N</span><span class="sxs-lookup"><span data-stu-id="b3b9d-117">N</span></span>        |
| <span data-ttu-id="b3b9d-118">Rutamsi</span><span class="sxs-lookup"><span data-stu-id="b3b9d-118">MsiPath</span></span>               | <span data-ttu-id="b3b9d-119">text</span><span class="sxs-lookup"><span data-stu-id="b3b9d-119">text</span></span>    |     | <span data-ttu-id="b3b9d-120">N</span><span class="sxs-lookup"><span data-stu-id="b3b9d-120">N</span></span>        |
| <span data-ttu-id="b3b9d-121">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="b3b9d-121">SymbolPaths</span></span>           | <span data-ttu-id="b3b9d-122">text</span><span class="sxs-lookup"><span data-stu-id="b3b9d-122">text</span></span>    |     | <span data-ttu-id="b3b9d-123">Y</span><span class="sxs-lookup"><span data-stu-id="b3b9d-123">Y</span></span>        |
| <span data-ttu-id="b3b9d-124">Upgraded</span><span class="sxs-lookup"><span data-stu-id="b3b9d-124">Upgraded</span></span>              | <span data-ttu-id="b3b9d-125">text</span><span class="sxs-lookup"><span data-stu-id="b3b9d-125">text</span></span>    |     | <span data-ttu-id="b3b9d-126">N</span><span class="sxs-lookup"><span data-stu-id="b3b9d-126">N</span></span>        |
| <span data-ttu-id="b3b9d-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="b3b9d-127">Order</span></span>                 | <span data-ttu-id="b3b9d-128">integer</span><span class="sxs-lookup"><span data-stu-id="b3b9d-128">integer</span></span> |     | <span data-ttu-id="b3b9d-129">N</span><span class="sxs-lookup"><span data-stu-id="b3b9d-129">N</span></span>        |
| <span data-ttu-id="b3b9d-130">ProductValidateFlags</span><span class="sxs-lookup"><span data-stu-id="b3b9d-130">ProductValidateFlags</span></span>  | <span data-ttu-id="b3b9d-131">text</span><span class="sxs-lookup"><span data-stu-id="b3b9d-131">text</span></span>    |     | <span data-ttu-id="b3b9d-132">Y</span><span class="sxs-lookup"><span data-stu-id="b3b9d-132">Y</span></span>        |
| <span data-ttu-id="b3b9d-133">IgnoreMissingSrcFiles</span><span class="sxs-lookup"><span data-stu-id="b3b9d-133">IgnoreMissingSrcFiles</span></span> | <span data-ttu-id="b3b9d-134">integer</span><span class="sxs-lookup"><span data-stu-id="b3b9d-134">integer</span></span> |     | <span data-ttu-id="b3b9d-135">N</span><span class="sxs-lookup"><span data-stu-id="b3b9d-135">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b3b9d-136">Columnas</span><span class="sxs-lookup"><span data-stu-id="b3b9d-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b3b9d-137"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Dirigir</span><span class="sxs-lookup"><span data-stu-id="b3b9d-137"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="b3b9d-138">Identificador de una imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-138">Identifier for a target image.</span></span> <span data-ttu-id="b3b9d-139">El paquete de revisión actualiza la imagen de destino especificada en esta columna a la imagen actualizada especificada en la columna actualizada.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-139">The patch package updates the target image specified in this column to the upgraded image specified in the Upgraded column.</span></span> <span data-ttu-id="b3b9d-140">Hay una o varias imágenes de destino para cada imagen actualizada.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-140">There are one or more target images for each upgraded image.</span></span> <span data-ttu-id="b3b9d-141">La imagen de destino debe ser una imagen de instalación totalmente descomprimida del producto, como una imagen administrativa o una imagen de instalación sin comprimir en un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-141">The target image must be a fully uncompressed setup image of the product, such as an administrative image or an uncompressed setup image on a CD-ROM.</span></span> <span data-ttu-id="b3b9d-142">Tenga en cuenta que la función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) no genera revisiones binarias para los archivos de los archivadores.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-142">Note that the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function does not generate binary patches for files in cabinets.</span></span> <span data-ttu-id="b3b9d-143">El valor de este campo se usa con el valor del campo actualizado para generar los nombres de las transformaciones que el instalador agrega al paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-143">The value in this field is used with the value in the Upgraded field to generate the names of the transforms that the installer adds to the patch package.</span></span>

</dd> <dt>

<span data-ttu-id="b3b9d-144"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>Rutamsi</span><span class="sxs-lookup"><span data-stu-id="b3b9d-144"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span></span>
</dt> <dd>

<span data-ttu-id="b3b9d-145">Este campo especifica la ruta de acceso completa, incluido el nombre de archivo, en la ubicación del archivo. msi de la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-145">This field specifies the full path, including the file name, to the location of the .msi file for the target image.</span></span> <span data-ttu-id="b3b9d-146">Esta es la ubicación de los archivos de origen de la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-146">This is the location of the source files for the target image.</span></span>

</dd> <dt>

<span data-ttu-id="b3b9d-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="b3b9d-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="b3b9d-148">Una lista delimitada por punto y coma de carpetas en las que se van a buscar archivos de símbolos que se pueden usar para optimizar la generación de la revisión binaria.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-148">A semicolon delimited list of folders that are to be searched for symbol files that may be used to optimize the generation of the binary patch.</span></span> <span data-ttu-id="b3b9d-149">Tenga en cuenta que no se busca en los subdirectorios de las carpetas especificadas en este campo.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-149">Note that the subdirectories of folders specified in this field are not searched.</span></span> <span data-ttu-id="b3b9d-150">Una revisión binaria optimizada puede ser menor.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-150">An optimized binary patch may be smaller.</span></span> <span data-ttu-id="b3b9d-151">Microsoft Visual C++ debe estar instalado en el equipo que genera la revisión y que se usa para crear los archivos de símbolos.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-151">Microsoft Visual C++ must be installed on the computer generating the patch and used to create the symbol files.</span></span> <span data-ttu-id="b3b9d-152">Este campo es opcional y el instalador crea una revisión binaria incluso si no se especifica ningún archivo de símbolos o si los archivos de símbolos dejan de estar disponibles para Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-152">This field is optional, and the installer creates a binary patch even if no symbol files are specified or if the symbol files become unavailable to Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="b3b9d-153"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Actualizado</span><span class="sxs-lookup"><span data-stu-id="b3b9d-153"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="b3b9d-154">Clave externa para la columna actualizada de la [tabla UpgradedImages](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="b3b9d-154">Foreign key to the Upgraded column of the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="b3b9d-155">La función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) omite cualquier imagen actualizada a la que no haga referencia al menos un registro de la tabla TargetImages.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-155">The [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function ignores any upgraded image that is not referenced by at least one record of the TargetImages table.</span></span>

</dd> <dt>

<span data-ttu-id="b3b9d-156"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Orden</span><span class="sxs-lookup"><span data-stu-id="b3b9d-156"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="b3b9d-157">Orden relativo de la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-157">Relative order of the target image.</span></span> <span data-ttu-id="b3b9d-158">Dado que se pueden revisar varios destinos en una imagen actualizada, el campo orden proporciona un medio para secuenciar las transformaciones en la lista de transformaciones de revisiones.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-158">Because multiple targets can be patched to an upgraded image, the Order field provides a means to sequence the transforms in the patch transforms list.</span></span> <span data-ttu-id="b3b9d-159">Normalmente, el orden es de la imagen más antigua a la más reciente.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-159">Commonly, the order is from oldest to newest image.</span></span>

</dd> <dt>

<span data-ttu-id="b3b9d-160"><span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags</span><span class="sxs-lookup"><span data-stu-id="b3b9d-160"><span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags</span></span>
</dt> <dd>

<span data-ttu-id="b3b9d-161">El campo ProductValidateFlags se usa para especificar la comprobación del producto a fin de evitar aplicar transformaciones irrelevantes.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-161">The ProductValidateFlags field is used to specify product checking to avoid applying irrelevant transforms.</span></span> <span data-ttu-id="b3b9d-162">El valor especificado en este campo debe ser un entero hexadecimal de 8 dígitos y uno de los valores válidos para el parámetro *iValidation* de la función [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) .</span><span class="sxs-lookup"><span data-stu-id="b3b9d-162">The value entered in this field must be an 8-digit hex integer and one of the valid values for the *iValidation* parameter of the [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) function.</span></span> <span data-ttu-id="b3b9d-163">El valor predeterminado es 0x00000922, que es igual a **MSITRANSFORM \_ Validate \_ UPDATEVERSION**  +  **MSITRANSFORM \_ Validate \_ NEWEQUALBASEVERSION**  +  **MSITRANSFORM \_ Validate \_ UPGRADECODE**  +  **MSITRANSFORM \_ Validate \_ Product**.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-163">The default value is 0x00000922 which equals **MSITRANSFORM\_VALIDATE\_UPDATEVERSION** + **MSITRANSFORM\_VALIDATE\_NEWEQUALBASEVERSION** + **MSITRANSFORM\_VALIDATE\_UPGRADECODE** + **MSITRANSFORM\_VALIDATE\_PRODUCT**.</span></span>

</dd> <dt>

<span data-ttu-id="b3b9d-164"><span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles</span><span class="sxs-lookup"><span data-stu-id="b3b9d-164"><span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles</span></span>
</dt> <dd>

<span data-ttu-id="b3b9d-165">Si este campo se establece en un valor distinto de cero, el instalador omite los archivos que faltan de la imagen de destino y quedan sin modificar durante la revisión.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-165">If this field is set to a nonzero value, files missing from the target image are ignored by the installer and left unchanged during patching.</span></span> <span data-ttu-id="b3b9d-166">Esto permite realizar revisiones sin necesidad de toda la imagen; solo se requieren los archivos modificados del producto y el archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-166">This enables patches to be made without requiring the entire image; only the changed files of the product and the .msi file are required.</span></span> <span data-ttu-id="b3b9d-167">Esto puede reducir el tiempo necesario para generar la revisión.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-167">This may reduce the time required to generate the patch.</span></span>

> [!Note]  
> <span data-ttu-id="b3b9d-168">No use el valor IgnoreMissingSrcFiles con TrustMsi establecido en 1 en la [tabla de propiedades](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="b3b9d-168">Do not use the IgnoreMissingSrcFiles value with TrustMsi set to 1 in the [Properties Table](properties-table-patchwiz-dll-.md).</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3b9d-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3b9d-169">Remarks</span></span>

<span data-ttu-id="b3b9d-170">Esta tabla acepta las variables de entorno como rutas de acceso a partir de la versión 4,0 de Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="b3b9d-170">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

 

 




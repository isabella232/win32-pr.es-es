---
description: La tabla ExternalFiles contiene información sobre archivos específicos que no forman parte de una imagen de destino normal.
ms.assetid: c75591c2-5266-4a99-8104-53815f6550e2
title: Tabla ExternalFiles (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f0002961408be9f43685ef40cd2ccff729e48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544286"
---
# <a name="externalfiles-table-patchwizdll"></a><span data-ttu-id="b688a-103">Tabla ExternalFiles (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="b688a-103">ExternalFiles Table (Patchwiz.dll)</span></span>

<span data-ttu-id="b688a-104">La tabla ExternalFiles contiene información sobre archivos específicos que no forman parte de una imagen de destino normal.</span><span class="sxs-lookup"><span data-stu-id="b688a-104">The ExternalFiles table contains information about specific files that are not part of a regular target image.</span></span> <span data-ttu-id="b688a-105">Estos archivos pueden existir en productos que han sido actualizados por otro producto, actualización o revisión.</span><span class="sxs-lookup"><span data-stu-id="b688a-105">These files may exist in products that have been updated by another product, upgrade, or patch.</span></span> <span data-ttu-id="b688a-106">Esta tabla es opcional en la base de datos de creación de revisiones (archivo. PCP) y la usa la función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="b688a-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="b688a-107">La tabla ExternalFiles tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="b688a-107">The ExternalFiles table has the following columns.</span></span>



| <span data-ttu-id="b688a-108">Columna</span><span class="sxs-lookup"><span data-stu-id="b688a-108">Column</span></span>        | <span data-ttu-id="b688a-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b688a-109">Type</span></span>    | <span data-ttu-id="b688a-110">Clave</span><span class="sxs-lookup"><span data-stu-id="b688a-110">Key</span></span> | <span data-ttu-id="b688a-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="b688a-111">Nullable</span></span> |
|---------------|---------|-----|----------|
| <span data-ttu-id="b688a-112">Familia</span><span class="sxs-lookup"><span data-stu-id="b688a-112">Family</span></span>        | <span data-ttu-id="b688a-113">text</span><span class="sxs-lookup"><span data-stu-id="b688a-113">text</span></span>    | <span data-ttu-id="b688a-114">Y</span><span class="sxs-lookup"><span data-stu-id="b688a-114">Y</span></span>   | <span data-ttu-id="b688a-115">N</span><span class="sxs-lookup"><span data-stu-id="b688a-115">N</span></span>        |
| <span data-ttu-id="b688a-116">FTK</span><span class="sxs-lookup"><span data-stu-id="b688a-116">FTK</span></span>           | <span data-ttu-id="b688a-117">text</span><span class="sxs-lookup"><span data-stu-id="b688a-117">text</span></span>    | <span data-ttu-id="b688a-118">Y</span><span class="sxs-lookup"><span data-stu-id="b688a-118">Y</span></span>   | <span data-ttu-id="b688a-119">N</span><span class="sxs-lookup"><span data-stu-id="b688a-119">N</span></span>        |
| <span data-ttu-id="b688a-120">FilePath</span><span class="sxs-lookup"><span data-stu-id="b688a-120">FilePath</span></span>      | <span data-ttu-id="b688a-121">text</span><span class="sxs-lookup"><span data-stu-id="b688a-121">text</span></span>    | <span data-ttu-id="b688a-122">Y</span><span class="sxs-lookup"><span data-stu-id="b688a-122">Y</span></span>   | <span data-ttu-id="b688a-123">N</span><span class="sxs-lookup"><span data-stu-id="b688a-123">N</span></span>        |
| <span data-ttu-id="b688a-124">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="b688a-124">SymbolPaths</span></span>   | <span data-ttu-id="b688a-125">text</span><span class="sxs-lookup"><span data-stu-id="b688a-125">text</span></span>    |     | <span data-ttu-id="b688a-126">Y</span><span class="sxs-lookup"><span data-stu-id="b688a-126">Y</span></span>        |
| <span data-ttu-id="b688a-127">IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="b688a-127">IgnoreOffsets</span></span> | <span data-ttu-id="b688a-128">text</span><span class="sxs-lookup"><span data-stu-id="b688a-128">text</span></span>    |     | <span data-ttu-id="b688a-129">Y</span><span class="sxs-lookup"><span data-stu-id="b688a-129">Y</span></span>        |
| <span data-ttu-id="b688a-130">IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="b688a-130">IgnoreLengths</span></span> | <span data-ttu-id="b688a-131">text</span><span class="sxs-lookup"><span data-stu-id="b688a-131">text</span></span>    |     | <span data-ttu-id="b688a-132">Y</span><span class="sxs-lookup"><span data-stu-id="b688a-132">Y</span></span>        |
| <span data-ttu-id="b688a-133">RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="b688a-133">RetainOffsets</span></span> | <span data-ttu-id="b688a-134">text</span><span class="sxs-lookup"><span data-stu-id="b688a-134">text</span></span>    |     | <span data-ttu-id="b688a-135">N</span><span class="sxs-lookup"><span data-stu-id="b688a-135">N</span></span>        |
| <span data-ttu-id="b688a-136">Pedido</span><span class="sxs-lookup"><span data-stu-id="b688a-136">Order</span></span>         | <span data-ttu-id="b688a-137">integer</span><span class="sxs-lookup"><span data-stu-id="b688a-137">integer</span></span> |     | <span data-ttu-id="b688a-138">Y</span><span class="sxs-lookup"><span data-stu-id="b688a-138">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b688a-139">Columnas</span><span class="sxs-lookup"><span data-stu-id="b688a-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b688a-140"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Familia</span><span class="sxs-lookup"><span data-stu-id="b688a-140"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="b688a-141">Clave externa para la columna Family de la [tabla ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="b688a-141">Foreign key to the Family column of the [ImageFamilies Table (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="b688a-142"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="b688a-142"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="b688a-143">Clave externa en la [tabla de archivos](file-table.md) del archivo. msi de la imagen actualizada.</span><span class="sxs-lookup"><span data-stu-id="b688a-143">Foreign key into [File table](file-table.md) of the .msi file of the upgraded image.</span></span>

</dd> <dt>

<span data-ttu-id="b688a-144"><span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>FilePath</span><span class="sxs-lookup"><span data-stu-id="b688a-144"><span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>FilePath</span></span>
</dt> <dd>

<span data-ttu-id="b688a-145">Ruta de acceso completa del archivo externo, incluido el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="b688a-145">Full path of the external file including the file name.</span></span> <span data-ttu-id="b688a-146">El campo FilePath se usa para buscar el archivo especificado en la columna FTK.</span><span class="sxs-lookup"><span data-stu-id="b688a-146">FilePath field is used to locate the file specified in the FTK column.</span></span>

</dd> <dt>

<span data-ttu-id="b688a-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="b688a-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="b688a-148">Ruta de acceso completa busca archivos de símbolos del archivo especificado en la columna FTK.</span><span class="sxs-lookup"><span data-stu-id="b688a-148">Full path searched for symbol files of the file specified in the FTK column.</span></span>

</dd> <dt>

<span data-ttu-id="b688a-149"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="b688a-149"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span></span>
</dt> <dd>

<span data-ttu-id="b688a-150">El valor de este campo es una lista delimitada por comas de números de desplazamiento de intervalo para los intervalos que se van a omitir en el archivo externo.</span><span class="sxs-lookup"><span data-stu-id="b688a-150">The value in this field is a comma-delimited list of range offset numbers for the ranges to be ignored in the external file.</span></span> <span data-ttu-id="b688a-151">El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna IgnoreLengths.</span><span class="sxs-lookup"><span data-stu-id="b688a-151">The order and number of the ranges in the list must match the items in the IgnoreLengths column.</span></span> <span data-ttu-id="b688a-152">Esta columna es opcional.</span><span class="sxs-lookup"><span data-stu-id="b688a-152">This column is optional.</span></span>

<span data-ttu-id="b688a-153">Los valores pueden ser decimales o hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="b688a-153">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="b688a-154">[Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x".</span><span class="sxs-lookup"><span data-stu-id="b688a-154">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="b688a-155">Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONGs.</span><span class="sxs-lookup"><span data-stu-id="b688a-155">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="b688a-156"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="b688a-156"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span></span>
</dt> <dd>

<span data-ttu-id="b688a-157">El valor de este campo es una lista delimitada por comas de longitudes de intervalo en bytes para los intervalos que se van a omitir en el archivo externo.</span><span class="sxs-lookup"><span data-stu-id="b688a-157">The value in this field is a comma-delimited list of range lengths in bytes for the ranges to be ignored in the external file.</span></span> <span data-ttu-id="b688a-158">El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna IgnoreOffsets.</span><span class="sxs-lookup"><span data-stu-id="b688a-158">The order and number of the ranges in the list must match the items in the IgnoreOffsets column.</span></span> <span data-ttu-id="b688a-159">Esta columna es opcional.</span><span class="sxs-lookup"><span data-stu-id="b688a-159">This column is optional.</span></span>

<span data-ttu-id="b688a-160">Los valores pueden ser decimales o hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="b688a-160">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="b688a-161">[Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x".</span><span class="sxs-lookup"><span data-stu-id="b688a-161">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="b688a-162">Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONGs.</span><span class="sxs-lookup"><span data-stu-id="b688a-162">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="b688a-163"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="b688a-163"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="b688a-164">El valor de este campo es una lista delimitada por comas de números de desplazamiento de intervalo para los intervalos que se van a conservar en el archivo externo.</span><span class="sxs-lookup"><span data-stu-id="b688a-164">The value in this field is a comma-delimited list of range offset numbers for the ranges to be retained in the External file.</span></span> <span data-ttu-id="b688a-165">El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna RetainOffsets del registro correspondiente en la [tabla FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="b688a-165">The order and number of the ranges in the list must match the items in the RetainOffsets column of the corresponding record in the [FamilyFileRanges Table (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md).</span></span>

<span data-ttu-id="b688a-166">Los valores pueden ser decimales o hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="b688a-166">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="b688a-167">[Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x".</span><span class="sxs-lookup"><span data-stu-id="b688a-167">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="b688a-168">Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONGs.</span><span class="sxs-lookup"><span data-stu-id="b688a-168">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="b688a-169"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Orden</span><span class="sxs-lookup"><span data-stu-id="b688a-169"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="b688a-170">Si se especifican dos o más versiones para el mismo archivo externo, la tabla puede contener varios registros con valores coincidentes en los campos FTK y Family.</span><span class="sxs-lookup"><span data-stu-id="b688a-170">If two or more versions are specified for the same external file, the table may contain multiple records with matching values in the FTK and Family fields.</span></span> <span data-ttu-id="b688a-171">En este caso, el campo orden puede especificar el orden de los archivos externos que se utilizarán al crear la revisión.</span><span class="sxs-lookup"><span data-stu-id="b688a-171">In this case, the Order field may specify the order of external files to use when creating the patch.</span></span> <span data-ttu-id="b688a-172">El orden es de la versión más antigua a la más reciente.</span><span class="sxs-lookup"><span data-stu-id="b688a-172">The order is from the oldest to the most recent version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b688a-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b688a-173">Remarks</span></span>

<span data-ttu-id="b688a-174">Esta tabla acepta las variables de entorno como rutas de acceso a partir de la versión 4,0 de Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="b688a-174">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b688a-175">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b688a-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b688a-176">Aplicar revisiones a las regiones seleccionadas de un archivo</span><span class="sxs-lookup"><span data-stu-id="b688a-176">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 




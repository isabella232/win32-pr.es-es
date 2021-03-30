---
description: La \_ tabla TargetFiles OptionalData contiene información sobre los archivos específicos de una imagen de destino. Esta tabla es opcional en la base de datos de creación de revisiones (archivo. PCP) y la usa la función UiCreatePatchPackageEx.
ms.assetid: 577b1674-1e44-42e1-b011-c0fb561b514c
title: Tabla TargetFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859ac2e03f68c28eff5ebf7f5afa2bf53ab69299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002362"
---
# <a name="targetfiles_optionaldata-table-patchwizdll"></a><span data-ttu-id="5dbd3-104">TargetFiles \_ OptionalData (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="5dbd3-104">TargetFiles\_OptionalData Table (Patchwiz.dll)</span></span>

<span data-ttu-id="5dbd3-105">La \_ tabla TargetFiles OptionalData contiene información sobre los archivos específicos de una imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-105">The TargetFiles\_OptionalData table contains information about specific files in a target image.</span></span> <span data-ttu-id="5dbd3-106">Esta tabla es opcional en la base de datos de creación de revisiones (archivo. PCP) y la usa la función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="5dbd3-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="5dbd3-107">La \_ tabla TargetFiles OptionalData tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-107">The TargetFiles\_OptionalData table has the following columns.</span></span>



| <span data-ttu-id="5dbd3-108">Columna</span><span class="sxs-lookup"><span data-stu-id="5dbd3-108">Column</span></span>        | <span data-ttu-id="5dbd3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5dbd3-109">Type</span></span> | <span data-ttu-id="5dbd3-110">Clave</span><span class="sxs-lookup"><span data-stu-id="5dbd3-110">Key</span></span> | <span data-ttu-id="5dbd3-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="5dbd3-111">Nullable</span></span> |
|---------------|------|-----|----------|
| <span data-ttu-id="5dbd3-112">Destino</span><span class="sxs-lookup"><span data-stu-id="5dbd3-112">Target</span></span>        | <span data-ttu-id="5dbd3-113">text</span><span class="sxs-lookup"><span data-stu-id="5dbd3-113">text</span></span> | <span data-ttu-id="5dbd3-114">Y</span><span class="sxs-lookup"><span data-stu-id="5dbd3-114">Y</span></span>   | <span data-ttu-id="5dbd3-115">N</span><span class="sxs-lookup"><span data-stu-id="5dbd3-115">N</span></span>        |
| <span data-ttu-id="5dbd3-116">FTK</span><span class="sxs-lookup"><span data-stu-id="5dbd3-116">FTK</span></span>           | <span data-ttu-id="5dbd3-117">text</span><span class="sxs-lookup"><span data-stu-id="5dbd3-117">text</span></span> | <span data-ttu-id="5dbd3-118">Y</span><span class="sxs-lookup"><span data-stu-id="5dbd3-118">Y</span></span>   | <span data-ttu-id="5dbd3-119">N</span><span class="sxs-lookup"><span data-stu-id="5dbd3-119">N</span></span>        |
| <span data-ttu-id="5dbd3-120">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="5dbd3-120">SymbolPaths</span></span>   | <span data-ttu-id="5dbd3-121">text</span><span class="sxs-lookup"><span data-stu-id="5dbd3-121">text</span></span> |     | <span data-ttu-id="5dbd3-122">Y</span><span class="sxs-lookup"><span data-stu-id="5dbd3-122">Y</span></span>        |
| <span data-ttu-id="5dbd3-123">IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="5dbd3-123">IgnoreOffsets</span></span> | <span data-ttu-id="5dbd3-124">text</span><span class="sxs-lookup"><span data-stu-id="5dbd3-124">text</span></span> |     | <span data-ttu-id="5dbd3-125">Y</span><span class="sxs-lookup"><span data-stu-id="5dbd3-125">Y</span></span>        |
| <span data-ttu-id="5dbd3-126">IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="5dbd3-126">IgnoreLengths</span></span> | <span data-ttu-id="5dbd3-127">text</span><span class="sxs-lookup"><span data-stu-id="5dbd3-127">text</span></span> |     | <span data-ttu-id="5dbd3-128">Y</span><span class="sxs-lookup"><span data-stu-id="5dbd3-128">Y</span></span>        |
| <span data-ttu-id="5dbd3-129">RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="5dbd3-129">RetainOffsets</span></span> | <span data-ttu-id="5dbd3-130">text</span><span class="sxs-lookup"><span data-stu-id="5dbd3-130">text</span></span> |     | <span data-ttu-id="5dbd3-131">Y</span><span class="sxs-lookup"><span data-stu-id="5dbd3-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="5dbd3-132">Columnas</span><span class="sxs-lookup"><span data-stu-id="5dbd3-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="5dbd3-133"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Dirigir</span><span class="sxs-lookup"><span data-stu-id="5dbd3-133"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="5dbd3-134">Clave externa para la columna de destino de la [tabla TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="5dbd3-134">Foreign key to the Target column of the [TargetImages Table (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dbd3-135"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="5dbd3-135"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="5dbd3-136">Clave externa en la [tabla de archivos](file-table.md) de la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-136">Foreign key into the [File table](file-table.md) of target image.</span></span>

</dd> <dt>

<span data-ttu-id="5dbd3-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="5dbd3-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="5dbd3-138">El valor de este campo se agrega a la lista de carpetas delimitada por punto y coma de la columna SymbolPaths de la [tabla TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) cuando se genera la revisión, y se puede usar para agregar archivos de símbolos para un archivo específico.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-138">The value in this field is added to the semicolon delimited list of folders in the SymbolPaths column of the [TargetImages Table (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) when the patch is generated, and can be used to add symbol files for a specific file.</span></span>

</dd> <dt>

<span data-ttu-id="5dbd3-139"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="5dbd3-139"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span></span>
</dt> <dd>

<span data-ttu-id="5dbd3-140">El valor de este campo es una lista delimitada por comas de números de desplazamiento de intervalo para los intervalos que se van a omitir en el archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-140">The value in this field is a comma delimited list of range offset numbers for the ranges to be ignored in the Target file.</span></span> <span data-ttu-id="5dbd3-141">El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna IgnoreLengths.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-141">The order and number of the ranges in the list must match the items in the IgnoreLengths column.</span></span> <span data-ttu-id="5dbd3-142">Esta columna es opcional.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-142">This column is optional.</span></span>

<span data-ttu-id="5dbd3-143">Los valores pueden ser decimales o hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-143">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="5dbd3-144">[Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x".</span><span class="sxs-lookup"><span data-stu-id="5dbd3-144">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="5dbd3-145">Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONGs.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-145">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="5dbd3-146"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="5dbd3-146"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span></span>
</dt> <dd>

<span data-ttu-id="5dbd3-147">El valor de este campo es una lista delimitada por comas de longitudes de intervalo en bytes para los intervalos que se van a omitir en el archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-147">The value in this field is a comma delimited list of range lengths in bytes for the ranges to be ignored in the Target file.</span></span> <span data-ttu-id="5dbd3-148">El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna IgnoreOffsets.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-148">The order and number of the ranges in the list must match the items in the IgnoreOffsets column.</span></span> <span data-ttu-id="5dbd3-149">Esta columna es opcional.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-149">This column is optional.</span></span>

<span data-ttu-id="5dbd3-150">Los valores pueden ser decimales o hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-150">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="5dbd3-151">[Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x".</span><span class="sxs-lookup"><span data-stu-id="5dbd3-151">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="5dbd3-152">Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONGs.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-152">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="5dbd3-153"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="5dbd3-153"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="5dbd3-154">El valor de este campo es una lista delimitada por comas de números de desplazamiento de intervalo para los intervalos que se van a conservar en el archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-154">The value in this field is a comma delimited list of range offset numbers for the ranges to be retained in the Target file.</span></span> <span data-ttu-id="5dbd3-155">El orden y el número de los intervalos de la lista debe coincidir con los elementos de la columna RetainOffsets del registro correspondiente en la [tabla FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)</span><span class="sxs-lookup"><span data-stu-id="5dbd3-155">The order and number of the ranges in the list must match the items in the RetainOffsets column of the corresponding record in the [FamilyFileRanges Table (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)</span></span>

<span data-ttu-id="5dbd3-156">Los valores pueden ser decimales o hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-156">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="5dbd3-157">[Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x".</span><span class="sxs-lookup"><span data-stu-id="5dbd3-157">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="5dbd3-158">Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONGs.</span><span class="sxs-lookup"><span data-stu-id="5dbd3-158">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="5dbd3-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5dbd3-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dbd3-160">Aplicar revisiones a las regiones seleccionadas de un archivo</span><span class="sxs-lookup"><span data-stu-id="5dbd3-160">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 




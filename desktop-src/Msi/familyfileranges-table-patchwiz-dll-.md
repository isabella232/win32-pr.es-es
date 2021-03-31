---
description: La tabla FamilyFileRanges contiene información sobre determinados archivos de una imagen actualizada con intervalos que nunca deben sobrescribirse.
ms.assetid: 2e77605a-d909-4a17-977c-18281a96c36c
title: Tabla FamilyFileRanges (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2940d45d82efae3e61842ee0f6b4e46e3f77ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155524"
---
# <a name="familyfileranges-table-patchwizdll"></a><span data-ttu-id="25df8-103">Tabla FamilyFileRanges (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="25df8-103">FamilyFileRanges Table (Patchwiz.dll)</span></span>

<span data-ttu-id="25df8-104">La tabla FamilyFileRanges contiene información sobre determinados archivos de una imagen actualizada con intervalos que nunca deben sobrescribirse.</span><span class="sxs-lookup"><span data-stu-id="25df8-104">The FamilyFileRanges table contains information about particular files of an upgraded image with ranges that should never be overwritten.</span></span> <span data-ttu-id="25df8-105">Esta tabla es opcional en la base de datos de creación de revisiones (archivo. PCP) y la usa la función [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="25df8-105">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="25df8-106">La tabla FamilyFileRanges tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="25df8-106">The FamilyFileRanges table has the following columns.</span></span>



| <span data-ttu-id="25df8-107">Columna</span><span class="sxs-lookup"><span data-stu-id="25df8-107">Column</span></span>        | <span data-ttu-id="25df8-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="25df8-108">Type</span></span> | <span data-ttu-id="25df8-109">Clave</span><span class="sxs-lookup"><span data-stu-id="25df8-109">Key</span></span> | <span data-ttu-id="25df8-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="25df8-110">Nullable</span></span> |
|---------------|------|-----|----------|
| <span data-ttu-id="25df8-111">Familia</span><span class="sxs-lookup"><span data-stu-id="25df8-111">Family</span></span>        | <span data-ttu-id="25df8-112">text</span><span class="sxs-lookup"><span data-stu-id="25df8-112">text</span></span> | <span data-ttu-id="25df8-113">Y</span><span class="sxs-lookup"><span data-stu-id="25df8-113">Y</span></span>   | <span data-ttu-id="25df8-114">N</span><span class="sxs-lookup"><span data-stu-id="25df8-114">N</span></span>        |
| <span data-ttu-id="25df8-115">FTK</span><span class="sxs-lookup"><span data-stu-id="25df8-115">FTK</span></span>           | <span data-ttu-id="25df8-116">text</span><span class="sxs-lookup"><span data-stu-id="25df8-116">text</span></span> | <span data-ttu-id="25df8-117">Y</span><span class="sxs-lookup"><span data-stu-id="25df8-117">Y</span></span>   | <span data-ttu-id="25df8-118">N</span><span class="sxs-lookup"><span data-stu-id="25df8-118">N</span></span>        |
| <span data-ttu-id="25df8-119">RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="25df8-119">RetainOffsets</span></span> | <span data-ttu-id="25df8-120">text</span><span class="sxs-lookup"><span data-stu-id="25df8-120">text</span></span> |     | <span data-ttu-id="25df8-121">N</span><span class="sxs-lookup"><span data-stu-id="25df8-121">N</span></span>        |
| <span data-ttu-id="25df8-122">RetainLengths</span><span class="sxs-lookup"><span data-stu-id="25df8-122">RetainLengths</span></span> | <span data-ttu-id="25df8-123">text</span><span class="sxs-lookup"><span data-stu-id="25df8-123">text</span></span> |     | <span data-ttu-id="25df8-124">N</span><span class="sxs-lookup"><span data-stu-id="25df8-124">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="25df8-125">Columnas</span><span class="sxs-lookup"><span data-stu-id="25df8-125">Columns</span></span>

<dl> <dt>

<span data-ttu-id="25df8-126"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Familia</span><span class="sxs-lookup"><span data-stu-id="25df8-126"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="25df8-127">Clave externa para la columna Family de la [tabla ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="25df8-127">Foreign key to the Family column of the [ImageFamilies Table (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="25df8-128"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="25df8-128"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="25df8-129">Clave externa en las [tablas de archivos](file-table.md) de todas las imágenes actualizadas de la familia de imágenes.</span><span class="sxs-lookup"><span data-stu-id="25df8-129">Foreign key into the [File tables](file-table.md) of all the upgraded images in the image family.</span></span>

</dd> <dt>

<span data-ttu-id="25df8-130"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="25df8-130"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="25df8-131">Desplazamiento de los intervalos que no se pueden sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="25df8-131">The offset of the ranges that cannot be overwritten.</span></span> <span data-ttu-id="25df8-132">El valor de este campo es una lista de los números de desplazamiento de intervalo para los intervalos que no se van a sobrescribir en los archivos de destino.</span><span class="sxs-lookup"><span data-stu-id="25df8-132">The value in this field is a list of the range offset numbers for ranges that are not to be overwritten in the target files.</span></span> <span data-ttu-id="25df8-133">El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna RetainLengths.</span><span class="sxs-lookup"><span data-stu-id="25df8-133">The order and number of the ranges in the list must match the items in the RetainLengths column.</span></span>

<span data-ttu-id="25df8-134">Los valores pueden ser decimales o hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="25df8-134">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="25df8-135">[Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x".</span><span class="sxs-lookup"><span data-stu-id="25df8-135">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="25df8-136">Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONGs.</span><span class="sxs-lookup"><span data-stu-id="25df8-136">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="25df8-137"><span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths</span><span class="sxs-lookup"><span data-stu-id="25df8-137"><span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths</span></span>
</dt> <dd>

<span data-ttu-id="25df8-138">La longitud en bytes de los intervalos que no se pueden sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="25df8-138">The length in bytes of the ranges that cannot be overwritten.</span></span> <span data-ttu-id="25df8-139">El valor de este campo es una lista de números de longitud de intervalo para los intervalos que se conservan en los archivos de destino.</span><span class="sxs-lookup"><span data-stu-id="25df8-139">The value in this field is a list of range length numbers for ranges to retain in target files.</span></span> <span data-ttu-id="25df8-140">El orden y el número de los intervalos de la lista deben coincidir con los elementos de la columna RetainOffsets.</span><span class="sxs-lookup"><span data-stu-id="25df8-140">The order and number of the ranges in the list must match the items in the RetainOffsets column.</span></span>

<span data-ttu-id="25df8-141">Los valores pueden ser decimales o hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="25df8-141">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="25df8-142">[Patchwiz.dll](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x".</span><span class="sxs-lookup"><span data-stu-id="25df8-142">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="25df8-143">Las columnas son columnas de cadena y Patchwiz.dll convertirá los valores en ULONGs.</span><span class="sxs-lookup"><span data-stu-id="25df8-143">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25df8-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25df8-144">Remarks</span></span>

<span data-ttu-id="25df8-145">Los desplazamientos y las longitudes especificados en RetainOffsets y RetainLengths no deben especificar intervalos superpuestos.</span><span class="sxs-lookup"><span data-stu-id="25df8-145">The offsets and lengths entered in RetainOffsets and RetainLengths must not specify overlapping ranges.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25df8-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="25df8-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25df8-147">Aplicar revisiones a las regiones seleccionadas de un archivo</span><span class="sxs-lookup"><span data-stu-id="25df8-147">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 




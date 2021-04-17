---
description: ICE32 valida que las claves y las claves externas del archivo. msi tienen el mismo tamaño y tipos de definición de columna.
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d6ff9e4de592ac073050b357aff0c63d984f0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667756"
---
# <a name="ice32"></a><span data-ttu-id="fc54a-103">ICE32</span><span class="sxs-lookup"><span data-stu-id="fc54a-103">ICE32</span></span>

<span data-ttu-id="fc54a-104">ICE32 valida que las claves y las claves externas del archivo. msi tienen el mismo tamaño y tipos de definición de columna.</span><span class="sxs-lookup"><span data-stu-id="fc54a-104">ICE32 validates that keys and foreign keys in the .msi file are of the same size and column definition types.</span></span> <span data-ttu-id="fc54a-105">Esta acción personalizada de ICE realiza la comparación mediante la [ \_ tabla de validación](-validation-table.md) y usando los tipos de definición devueltos por [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo).</span><span class="sxs-lookup"><span data-stu-id="fc54a-105">This ICE custom action makes the comparison using the [\_Validation table](-validation-table.md) and using the definition types that are returned by [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo).</span></span> <span data-ttu-id="fc54a-106">Para obtener más información, vea [formato de definición de columna](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="fc54a-106">For more information, see [Column Definition Format](column-definition-format.md).</span></span>

## <a name="result"></a><span data-ttu-id="fc54a-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="fc54a-107">Result</span></span>

<span data-ttu-id="fc54a-108">ICE32 expone errores si el archivo. msi contiene claves externas a claves de una longitud de columna o un tipo de datos de columna diferentes.</span><span class="sxs-lookup"><span data-stu-id="fc54a-108">ICE32 posts errors if the .msi file contains any foreign keys to keys of a different column length or column data type.</span></span>

## <a name="example"></a><span data-ttu-id="fc54a-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc54a-109">Example</span></span>

<span data-ttu-id="fc54a-110">ICE32 expone dos errores para el ejemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="fc54a-110">ICE32 posts two errors for the example shown:</span></span>

-   <span data-ttu-id="fc54a-111">Hay una clave externa y una clave definidas que difieren en tamaño.</span><span class="sxs-lookup"><span data-stu-id="fc54a-111">There is a foreign key and key defined that differ in size.</span></span>
-   <span data-ttu-id="fc54a-112">Hay una clave externa y una clave definidas que difieren en su tipo de definición.</span><span class="sxs-lookup"><span data-stu-id="fc54a-112">There is a foreign key and key defined that differ in their definition type.</span></span>

<span data-ttu-id="fc54a-113">[ \_ Tabla de validación](-validation-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="fc54a-113">[\_Validation Table](-validation-table.md) (partial)</span></span>



| <span data-ttu-id="fc54a-114">Tabla</span><span class="sxs-lookup"><span data-stu-id="fc54a-114">Table</span></span> | <span data-ttu-id="fc54a-115">Columna</span><span class="sxs-lookup"><span data-stu-id="fc54a-115">Column</span></span>  | <span data-ttu-id="fc54a-116">KeyTable</span><span class="sxs-lookup"><span data-stu-id="fc54a-116">KeyTable</span></span> | <span data-ttu-id="fc54a-117">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="fc54a-117">KeyColumn</span></span> |
|-------|---------|----------|-----------|
| <span data-ttu-id="fc54a-118">Archivo</span><span class="sxs-lookup"><span data-stu-id="fc54a-118">File</span></span>  | <span data-ttu-id="fc54a-119">Version</span><span class="sxs-lookup"><span data-stu-id="fc54a-119">Version</span></span> | <span data-ttu-id="fc54a-120">Archivo</span><span class="sxs-lookup"><span data-stu-id="fc54a-120">File</span></span>     | <span data-ttu-id="fc54a-121">1</span><span class="sxs-lookup"><span data-stu-id="fc54a-121">1</span></span>         |
| <span data-ttu-id="fc54a-122">Flap</span><span class="sxs-lookup"><span data-stu-id="fc54a-122">Flap</span></span>  | <span data-ttu-id="fc54a-123">Column8</span><span class="sxs-lookup"><span data-stu-id="fc54a-123">Column8</span></span> | <span data-ttu-id="fc54a-124">Flap</span><span class="sxs-lookup"><span data-stu-id="fc54a-124">Flap</span></span>     | <span data-ttu-id="fc54a-125">1</span><span class="sxs-lookup"><span data-stu-id="fc54a-125">1</span></span>         |



 

<span data-ttu-id="fc54a-126">Definiciones de columna (Partial)</span><span class="sxs-lookup"><span data-stu-id="fc54a-126">Column Definitions (partial)</span></span>



| <span data-ttu-id="fc54a-127">Tabla</span><span class="sxs-lookup"><span data-stu-id="fc54a-127">Table</span></span> | <span data-ttu-id="fc54a-128">Columna</span><span class="sxs-lookup"><span data-stu-id="fc54a-128">Column</span></span>  | <span data-ttu-id="fc54a-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc54a-129">Type</span></span> | <span data-ttu-id="fc54a-130">Size</span><span class="sxs-lookup"><span data-stu-id="fc54a-130">Size</span></span> |
|-------|---------|------|------|
| <span data-ttu-id="fc54a-131">Archivo</span><span class="sxs-lookup"><span data-stu-id="fc54a-131">File</span></span>  | <span data-ttu-id="fc54a-132">Archivo</span><span class="sxs-lookup"><span data-stu-id="fc54a-132">File</span></span>    | <span data-ttu-id="fc54a-133">s</span><span class="sxs-lookup"><span data-stu-id="fc54a-133">s</span></span>    | <span data-ttu-id="fc54a-134">72</span><span class="sxs-lookup"><span data-stu-id="fc54a-134">72</span></span>   |
| <span data-ttu-id="fc54a-135">Archivo</span><span class="sxs-lookup"><span data-stu-id="fc54a-135">File</span></span>  | <span data-ttu-id="fc54a-136">Versión</span><span class="sxs-lookup"><span data-stu-id="fc54a-136">Version</span></span> | <span data-ttu-id="fc54a-137">S</span><span class="sxs-lookup"><span data-stu-id="fc54a-137">S</span></span>    | <span data-ttu-id="fc54a-138">32</span><span class="sxs-lookup"><span data-stu-id="fc54a-138">32</span></span>   |
| <span data-ttu-id="fc54a-139">Flap</span><span class="sxs-lookup"><span data-stu-id="fc54a-139">Flap</span></span>  | <span data-ttu-id="fc54a-140">Columna1</span><span class="sxs-lookup"><span data-stu-id="fc54a-140">Column1</span></span> | <span data-ttu-id="fc54a-141">i</span><span class="sxs-lookup"><span data-stu-id="fc54a-141">i</span></span>    | <span data-ttu-id="fc54a-142">2</span><span class="sxs-lookup"><span data-stu-id="fc54a-142">2</span></span>    |
| <span data-ttu-id="fc54a-143">Flap</span><span class="sxs-lookup"><span data-stu-id="fc54a-143">Flap</span></span>  | <span data-ttu-id="fc54a-144">Column8</span><span class="sxs-lookup"><span data-stu-id="fc54a-144">Column8</span></span> | <span data-ttu-id="fc54a-145">S</span><span class="sxs-lookup"><span data-stu-id="fc54a-145">S</span></span>    | <span data-ttu-id="fc54a-146">32</span><span class="sxs-lookup"><span data-stu-id="fc54a-146">32</span></span>   |



 

<span data-ttu-id="fc54a-147">La columna versión de la tabla de archivos puede ser una clave externa a otro archivo de la tabla de archivos.</span><span class="sxs-lookup"><span data-stu-id="fc54a-147">The Version column of the File table can be a foreign key to another file in the File table.</span></span> <span data-ttu-id="fc54a-148">Esto ocurre con los archivos complementarios.</span><span class="sxs-lookup"><span data-stu-id="fc54a-148">This occurs with companion files.</span></span> <span data-ttu-id="fc54a-149">Sin embargo, la columna versión solo permite una longitud de cadena de 32, mientras que la columna archivo permite una longitud de cadena de 72.</span><span class="sxs-lookup"><span data-stu-id="fc54a-149">However, the Version column only allows a string length 32, whereas the File column allows a string length 72.</span></span> <span data-ttu-id="fc54a-150">Para corregir este error, cambie las longitudes de cadena para que coincidan.</span><span class="sxs-lookup"><span data-stu-id="fc54a-150">To fix this error change the string lengths to match.</span></span>

<span data-ttu-id="fc54a-151">Hay una clave externa y una clave definidas que difieren en sus tipos de definición.</span><span class="sxs-lookup"><span data-stu-id="fc54a-151">There is a foreign key and key defined that differ in their definition types.</span></span> <span data-ttu-id="fc54a-152">Column8 de la tabla flap aparece como una clave externa a Columna1.</span><span class="sxs-lookup"><span data-stu-id="fc54a-152">Column8 of the Flap Table is listed as a foreign key to Column1.</span></span> <span data-ttu-id="fc54a-153">Column8 es una columna de cadena y Column1 es una columna de tipo entero.</span><span class="sxs-lookup"><span data-stu-id="fc54a-153">Column8 is a string column and Column1 is an integer column.</span></span> <span data-ttu-id="fc54a-154">Se deben definir los pares de clave externa y de clave para que sus tipos de datos coincidan.</span><span class="sxs-lookup"><span data-stu-id="fc54a-154">The foreign key and key pairs must be defined so that their data types match.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc54a-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc54a-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc54a-156">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="fc54a-156">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




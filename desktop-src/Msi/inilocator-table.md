---
description: La tabla IniLocator contiene la información necesaria para buscar un archivo o directorio mediante un archivo. ini o para buscar una entrada. ini determinada. El archivo. ini debe estar presente en el directorio predeterminado de Microsoft Windows.
ms.assetid: 5a3c6077-34ef-48c8-b4e6-ecb1deb40f96
title: Tabla IniLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89583a2d69fd88dd4b5624920e2374aa7e203103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652571"
---
# <a name="inilocator-table"></a><span data-ttu-id="f52d3-104">Tabla IniLocator</span><span class="sxs-lookup"><span data-stu-id="f52d3-104">IniLocator Table</span></span>

<span data-ttu-id="f52d3-105">La tabla IniLocator contiene la información necesaria para buscar un archivo o directorio mediante un archivo. ini o para buscar una entrada. ini determinada.</span><span class="sxs-lookup"><span data-stu-id="f52d3-105">The IniLocator table holds the information needed to search for a file or directory using an .ini file or to search for a particular .ini entry itself.</span></span> <span data-ttu-id="f52d3-106">El archivo. ini debe estar presente en el directorio predeterminado de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f52d3-106">The .ini file must be present in the default Microsoft Windows directory.</span></span>

<span data-ttu-id="f52d3-107">La tabla IniLocator tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="f52d3-107">The IniLocator table has the following columns.</span></span>



| <span data-ttu-id="f52d3-108">Columna</span><span class="sxs-lookup"><span data-stu-id="f52d3-108">Column</span></span>      | <span data-ttu-id="f52d3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f52d3-109">Type</span></span>                         | <span data-ttu-id="f52d3-110">Clave</span><span class="sxs-lookup"><span data-stu-id="f52d3-110">Key</span></span> | <span data-ttu-id="f52d3-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="f52d3-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="f52d3-112">Signatura\_</span><span class="sxs-lookup"><span data-stu-id="f52d3-112">Signature\_</span></span> | [<span data-ttu-id="f52d3-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="f52d3-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="f52d3-114">Y</span><span class="sxs-lookup"><span data-stu-id="f52d3-114">Y</span></span>   | <span data-ttu-id="f52d3-115">N</span><span class="sxs-lookup"><span data-stu-id="f52d3-115">N</span></span>        |
| <span data-ttu-id="f52d3-116">FileName</span><span class="sxs-lookup"><span data-stu-id="f52d3-116">FileName</span></span>    | [<span data-ttu-id="f52d3-117">FileName</span><span class="sxs-lookup"><span data-stu-id="f52d3-117">FileName</span></span>](text.md)         | <span data-ttu-id="f52d3-118">N</span><span class="sxs-lookup"><span data-stu-id="f52d3-118">N</span></span>   | <span data-ttu-id="f52d3-119">N</span><span class="sxs-lookup"><span data-stu-id="f52d3-119">N</span></span>        |
| <span data-ttu-id="f52d3-120">Sección</span><span class="sxs-lookup"><span data-stu-id="f52d3-120">Section</span></span>     | [<span data-ttu-id="f52d3-121">Texto</span><span class="sxs-lookup"><span data-stu-id="f52d3-121">Text</span></span>](text.md)             | <span data-ttu-id="f52d3-122">N</span><span class="sxs-lookup"><span data-stu-id="f52d3-122">N</span></span>   | <span data-ttu-id="f52d3-123">N</span><span class="sxs-lookup"><span data-stu-id="f52d3-123">N</span></span>        |
| <span data-ttu-id="f52d3-124">Clave</span><span class="sxs-lookup"><span data-stu-id="f52d3-124">Key</span></span>         | [<span data-ttu-id="f52d3-125">Texto</span><span class="sxs-lookup"><span data-stu-id="f52d3-125">Text</span></span>](text.md)             | <span data-ttu-id="f52d3-126">N</span><span class="sxs-lookup"><span data-stu-id="f52d3-126">N</span></span>   | <span data-ttu-id="f52d3-127">N</span><span class="sxs-lookup"><span data-stu-id="f52d3-127">N</span></span>        |
| <span data-ttu-id="f52d3-128">Campo</span><span class="sxs-lookup"><span data-stu-id="f52d3-128">Field</span></span>       | [<span data-ttu-id="f52d3-129">Entero</span><span class="sxs-lookup"><span data-stu-id="f52d3-129">Integer</span></span>](integer.md)       | <span data-ttu-id="f52d3-130">N</span><span class="sxs-lookup"><span data-stu-id="f52d3-130">N</span></span>   | <span data-ttu-id="f52d3-131">Y</span><span class="sxs-lookup"><span data-stu-id="f52d3-131">Y</span></span>        |
| <span data-ttu-id="f52d3-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="f52d3-132">Type</span></span>        | [<span data-ttu-id="f52d3-133">Entero</span><span class="sxs-lookup"><span data-stu-id="f52d3-133">Integer</span></span>](integer.md)       | <span data-ttu-id="f52d3-134">N</span><span class="sxs-lookup"><span data-stu-id="f52d3-134">N</span></span>   | <span data-ttu-id="f52d3-135">Y</span><span class="sxs-lookup"><span data-stu-id="f52d3-135">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f52d3-136">Columnas</span><span class="sxs-lookup"><span data-stu-id="f52d3-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f52d3-137"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatura\_</span><span class="sxs-lookup"><span data-stu-id="f52d3-137"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="f52d3-138">Una clave externa en la primera columna de la [tabla de firma](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="f52d3-138">An external key into the first column of the [Signature table](signature-table.md).</span></span> <span data-ttu-id="f52d3-139">La firma \_ representa una firma única y también es la clave externa en la columna uno de la tabla de signatura.</span><span class="sxs-lookup"><span data-stu-id="f52d3-139">The Signature\_ represents a unique signature and is also the external key into column one of the Signature table.</span></span> <span data-ttu-id="f52d3-140">Si esta firma está presente en la tabla de firmas, la búsqueda es para un archivo.</span><span class="sxs-lookup"><span data-stu-id="f52d3-140">If this signature is present in the Signature table, then the search is for a file.</span></span> <span data-ttu-id="f52d3-141">Si esta clave no está presente en la tabla de firmas y el valor de la columna Type es **msidbLocatorTypeRawValue**, la búsqueda es para la entrada. ini especificada por la tabla IniLocator.</span><span class="sxs-lookup"><span data-stu-id="f52d3-141">If this key is absent from the Signature table, and the value of the Type column is **msidbLocatorTypeRawValue**, the search is for the .ini entry specified by the IniLocator table.</span></span> <span data-ttu-id="f52d3-142">En caso contrario, la búsqueda es para un directorio especificado por la tabla IniLocator.</span><span class="sxs-lookup"><span data-stu-id="f52d3-142">Otherwise the search is for a directory specified by the IniLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="f52d3-143"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extensión</span><span class="sxs-lookup"><span data-stu-id="f52d3-143"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="f52d3-144">Nombre del archivo. ini.</span><span class="sxs-lookup"><span data-stu-id="f52d3-144">The .ini file name.</span></span>

</dd> <dt>

<span data-ttu-id="f52d3-145"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Transversal</span><span class="sxs-lookup"><span data-stu-id="f52d3-145"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="f52d3-146">Nombre de sección dentro del archivo. ini.</span><span class="sxs-lookup"><span data-stu-id="f52d3-146">Section name within the .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="f52d3-147"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave</span><span class="sxs-lookup"><span data-stu-id="f52d3-147"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="f52d3-148">Valor de clave dentro de la sección.</span><span class="sxs-lookup"><span data-stu-id="f52d3-148">Key value within the section.</span></span>

</dd> <dt>

<span data-ttu-id="f52d3-149"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>Campo</span><span class="sxs-lookup"><span data-stu-id="f52d3-149"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>Field</span></span>
</dt> <dd>

<span data-ttu-id="f52d3-150">Campo de la línea. ini.</span><span class="sxs-lookup"><span data-stu-id="f52d3-150">The field in the .ini line.</span></span> <span data-ttu-id="f52d3-151">Si el campo es null o 0, se leerá toda la línea.</span><span class="sxs-lookup"><span data-stu-id="f52d3-151">If Field is Null or 0, then the entire line is read.</span></span> <span data-ttu-id="f52d3-152">Debe ser un número no negativo.</span><span class="sxs-lookup"><span data-stu-id="f52d3-152">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="f52d3-153"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Automáticamente</span><span class="sxs-lookup"><span data-stu-id="f52d3-153"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="f52d3-154">Un valor que determina si el valor de. ini es una ubicación de archivo, una ubicación de directorio o un valor de. ini sin formato.</span><span class="sxs-lookup"><span data-stu-id="f52d3-154">A value that determines whether the .ini value is a file location, a directory location, or raw .ini value.</span></span>

<span data-ttu-id="f52d3-155">En la tabla siguiente se enumeran los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="f52d3-155">The following table lists valid values.</span></span> <span data-ttu-id="f52d3-156">Si no está presente, el tipo se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="f52d3-156">If absent, Type is set to be 1.</span></span>



| <span data-ttu-id="f52d3-157">Constante</span><span class="sxs-lookup"><span data-stu-id="f52d3-157">Constant</span></span>                      | <span data-ttu-id="f52d3-158">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="f52d3-158">Hexadecimal</span></span> | <span data-ttu-id="f52d3-159">Decimal</span><span class="sxs-lookup"><span data-stu-id="f52d3-159">Decimal</span></span> | <span data-ttu-id="f52d3-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="f52d3-160">Description</span></span>           |
|-------------------------------|-------------|---------|-----------------------|
| <span data-ttu-id="f52d3-161">**msidbLocatorTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="f52d3-161">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="f52d3-162">0x000</span><span class="sxs-lookup"><span data-stu-id="f52d3-162">0x000</span></span>       | <span data-ttu-id="f52d3-163">0</span><span class="sxs-lookup"><span data-stu-id="f52d3-163">0</span></span>       | <span data-ttu-id="f52d3-164">Ubicación del directorio.</span><span class="sxs-lookup"><span data-stu-id="f52d3-164">A directory location.</span></span> |
| <span data-ttu-id="f52d3-165">**msidbLocatorTypeFileName**</span><span class="sxs-lookup"><span data-stu-id="f52d3-165">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="f52d3-166">0x001</span><span class="sxs-lookup"><span data-stu-id="f52d3-166">0x001</span></span>       | <span data-ttu-id="f52d3-167">1</span><span class="sxs-lookup"><span data-stu-id="f52d3-167">1</span></span>       | <span data-ttu-id="f52d3-168">Ubicación del archivo.</span><span class="sxs-lookup"><span data-stu-id="f52d3-168">A file location.</span></span>      |
| <span data-ttu-id="f52d3-169">**msidbLocatorTypeRawValue**</span><span class="sxs-lookup"><span data-stu-id="f52d3-169">**msidbLocatorTypeRawValue**</span></span>  | <span data-ttu-id="f52d3-170">0x002</span><span class="sxs-lookup"><span data-stu-id="f52d3-170">0x002</span></span>       | <span data-ttu-id="f52d3-171">2</span><span class="sxs-lookup"><span data-stu-id="f52d3-171">2</span></span>       | <span data-ttu-id="f52d3-172">Un valor de. ini sin formato.</span><span class="sxs-lookup"><span data-stu-id="f52d3-172">A raw .ini value.</span></span>     |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f52d3-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f52d3-173">Remarks</span></span>

<span data-ttu-id="f52d3-174">Esta tabla se usa con la [tabla AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="f52d3-174">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="f52d3-175">Por lo general, las columnas de esta tabla no están localizadas.</span><span class="sxs-lookup"><span data-stu-id="f52d3-175">This table's columns are generally not localized.</span></span> <span data-ttu-id="f52d3-176">Si un autor decide buscar productos en varios idiomas, puede haber una entrada independiente incluida en la tabla para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="f52d3-176">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="f52d3-177">El texto localizado asociado para la presentación o el registro de progreso se especifica en la [tabla ActionText](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="f52d3-177">Associated localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="f52d3-178">Vea [Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="f52d3-178">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="f52d3-179">Validación</span><span class="sxs-lookup"><span data-stu-id="f52d3-179">Validation</span></span>

<dl>

[<span data-ttu-id="f52d3-180">ICE03</span><span class="sxs-lookup"><span data-stu-id="f52d3-180">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f52d3-181">ICE06</span><span class="sxs-lookup"><span data-stu-id="f52d3-181">ICE06</span></span>](ice06.md)  
</dl>

 

 




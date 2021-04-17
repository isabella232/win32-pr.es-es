---
description: La tabla Signature contiene la información que identifica de forma única una firma de archivo. Para obtener más información acerca de las firmas, consulte firmas digitales y Windows Installer.
ms.assetid: 4780356f-e02a-45d9-883c-4f84867dbdea
title: Tabla de firmas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efb75155c4c7b8ddf4a82706bc38f09d0af75260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678069"
---
# <a name="signature-table"></a><span data-ttu-id="02a46-104">Tabla de firmas</span><span class="sxs-lookup"><span data-stu-id="02a46-104">Signature Table</span></span>

<span data-ttu-id="02a46-105">La tabla Signature contiene la información que identifica de forma única una firma de archivo.</span><span class="sxs-lookup"><span data-stu-id="02a46-105">The Signature table holds the information that uniquely identifies a file signature.</span></span> <span data-ttu-id="02a46-106">Para obtener más información acerca de las firmas [, consulte firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="02a46-106">For more information regarding signatures see [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

<span data-ttu-id="02a46-107">La tabla de firmas tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="02a46-107">The Signature table has the following columns.</span></span>



| <span data-ttu-id="02a46-108">Columna</span><span class="sxs-lookup"><span data-stu-id="02a46-108">Column</span></span>     | <span data-ttu-id="02a46-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="02a46-109">Type</span></span>                               | <span data-ttu-id="02a46-110">Clave</span><span class="sxs-lookup"><span data-stu-id="02a46-110">Key</span></span> | <span data-ttu-id="02a46-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="02a46-111">Nullable</span></span> |
|------------|------------------------------------|-----|----------|
| <span data-ttu-id="02a46-112">Firma</span><span class="sxs-lookup"><span data-stu-id="02a46-112">Signature</span></span>  | [<span data-ttu-id="02a46-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="02a46-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="02a46-114">Y</span><span class="sxs-lookup"><span data-stu-id="02a46-114">Y</span></span>   | <span data-ttu-id="02a46-115">N</span><span class="sxs-lookup"><span data-stu-id="02a46-115">N</span></span>        |
| <span data-ttu-id="02a46-116">FileName</span><span class="sxs-lookup"><span data-stu-id="02a46-116">FileName</span></span>   | [<span data-ttu-id="02a46-117">Texto</span><span class="sxs-lookup"><span data-stu-id="02a46-117">Text</span></span>](text.md)                   | <span data-ttu-id="02a46-118">N</span><span class="sxs-lookup"><span data-stu-id="02a46-118">N</span></span>   | <span data-ttu-id="02a46-119">N</span><span class="sxs-lookup"><span data-stu-id="02a46-119">N</span></span>        |
| <span data-ttu-id="02a46-120">MinVersion</span><span class="sxs-lookup"><span data-stu-id="02a46-120">MinVersion</span></span> | [<span data-ttu-id="02a46-121">Texto</span><span class="sxs-lookup"><span data-stu-id="02a46-121">Text</span></span>](text.md)                   | <span data-ttu-id="02a46-122">N</span><span class="sxs-lookup"><span data-stu-id="02a46-122">N</span></span>   | <span data-ttu-id="02a46-123">Y</span><span class="sxs-lookup"><span data-stu-id="02a46-123">Y</span></span>        |
| <span data-ttu-id="02a46-124">MaxVersion</span><span class="sxs-lookup"><span data-stu-id="02a46-124">MaxVersion</span></span> | [<span data-ttu-id="02a46-125">Texto</span><span class="sxs-lookup"><span data-stu-id="02a46-125">Text</span></span>](text.md)                   | <span data-ttu-id="02a46-126">N</span><span class="sxs-lookup"><span data-stu-id="02a46-126">N</span></span>   | <span data-ttu-id="02a46-127">Y</span><span class="sxs-lookup"><span data-stu-id="02a46-127">Y</span></span>        |
| <span data-ttu-id="02a46-128">MinSize</span><span class="sxs-lookup"><span data-stu-id="02a46-128">MinSize</span></span>    | [<span data-ttu-id="02a46-129">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="02a46-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="02a46-130">N</span><span class="sxs-lookup"><span data-stu-id="02a46-130">N</span></span>   | <span data-ttu-id="02a46-131">Y</span><span class="sxs-lookup"><span data-stu-id="02a46-131">Y</span></span>        |
| <span data-ttu-id="02a46-132">MaxSize</span><span class="sxs-lookup"><span data-stu-id="02a46-132">MaxSize</span></span>    | [<span data-ttu-id="02a46-133">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="02a46-133">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="02a46-134">N</span><span class="sxs-lookup"><span data-stu-id="02a46-134">N</span></span>   | <span data-ttu-id="02a46-135">Y</span><span class="sxs-lookup"><span data-stu-id="02a46-135">Y</span></span>        |
| <span data-ttu-id="02a46-136">MinDate</span><span class="sxs-lookup"><span data-stu-id="02a46-136">MinDate</span></span>    | [<span data-ttu-id="02a46-137">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="02a46-137">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="02a46-138">N</span><span class="sxs-lookup"><span data-stu-id="02a46-138">N</span></span>   | <span data-ttu-id="02a46-139">Y</span><span class="sxs-lookup"><span data-stu-id="02a46-139">Y</span></span>        |
| <span data-ttu-id="02a46-140">MaxDate</span><span class="sxs-lookup"><span data-stu-id="02a46-140">MaxDate</span></span>    | [<span data-ttu-id="02a46-141">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="02a46-141">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="02a46-142">N</span><span class="sxs-lookup"><span data-stu-id="02a46-142">N</span></span>   | <span data-ttu-id="02a46-143">Y</span><span class="sxs-lookup"><span data-stu-id="02a46-143">Y</span></span>        |
| <span data-ttu-id="02a46-144">Idiomas</span><span class="sxs-lookup"><span data-stu-id="02a46-144">Languages</span></span>  | [<span data-ttu-id="02a46-145">Texto</span><span class="sxs-lookup"><span data-stu-id="02a46-145">Text</span></span>](text.md)                   | <span data-ttu-id="02a46-146">N</span><span class="sxs-lookup"><span data-stu-id="02a46-146">N</span></span>   | <span data-ttu-id="02a46-147">Y</span><span class="sxs-lookup"><span data-stu-id="02a46-147">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="02a46-148">Columnas</span><span class="sxs-lookup"><span data-stu-id="02a46-148">Columns</span></span>

<dl> <dt>

<span data-ttu-id="02a46-149"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signatura</span><span class="sxs-lookup"><span data-stu-id="02a46-149"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span></span>
</dt> <dd>

<span data-ttu-id="02a46-150">La columna de firma es una firma de archivo única.</span><span class="sxs-lookup"><span data-stu-id="02a46-150">The Signature column is a unique file signature.</span></span>

</dd> <dt>

<span data-ttu-id="02a46-151"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extensión</span><span class="sxs-lookup"><span data-stu-id="02a46-151"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="02a46-152">Nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="02a46-152">The name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="02a46-153"><span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion</span><span class="sxs-lookup"><span data-stu-id="02a46-153"><span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion</span></span>
</dt> <dd>

<span data-ttu-id="02a46-154">Versión mínima del archivo, con una comparación de idioma.</span><span class="sxs-lookup"><span data-stu-id="02a46-154">The minimum version of the file, with a language comparison.</span></span> <span data-ttu-id="02a46-155">Si se especifica este campo, el archivo debe tener una versión que sea al menos igual a MinVersion.</span><span class="sxs-lookup"><span data-stu-id="02a46-155">If this field is specified, then the file must have a version that is at least equal to MinVersion.</span></span> <span data-ttu-id="02a46-156">Si el archivo tiene una versión igual al valor del campo MinVersion pero el idioma especificado en la columna idiomas es distinto, el archivo no cumple los criterios de filtro de firma.</span><span class="sxs-lookup"><span data-stu-id="02a46-156">If the file has an equal version to the MinVersion field value but the language specified in the Languages column differs, the file does not satisfy the signature filter criteria.</span></span>

> [!Note]  
> <span data-ttu-id="02a46-157">El idioma especificado en la columna idiomas se usa en la comparación y no hay ninguna manera de omitir el idioma.</span><span class="sxs-lookup"><span data-stu-id="02a46-157">The language specified in the Languages column is used in the comparison and there is no way to ignore language.</span></span> <span data-ttu-id="02a46-158">Si desea que un archivo cumpla los requisitos de campo de MinVersion independientemente del idioma, debe escribir un valor en el campo MinVersion que sea uno menos que el valor real.</span><span class="sxs-lookup"><span data-stu-id="02a46-158">If you want a file to meet the MinVersion field requirement regardless of language, you must enter a value in the MinVersion field that is one less than the actual value.</span></span> <span data-ttu-id="02a46-159">Por ejemplo, si la versión mínima del filtro es 2.0.2600.1183, use 2.0.2600.1182 para buscar el archivo sin que coincida con la información de idioma.</span><span class="sxs-lookup"><span data-stu-id="02a46-159">For example, if the minimum version for the filter is 2.0.2600.1183, use 2.0.2600.1182 to find the file without matching the language information.</span></span>

 

</dd> <dt>

<span data-ttu-id="02a46-160"><span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion</span><span class="sxs-lookup"><span data-stu-id="02a46-160"><span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion</span></span>
</dt> <dd>

<span data-ttu-id="02a46-161">Versión máxima del archivo.</span><span class="sxs-lookup"><span data-stu-id="02a46-161">The maximum version of the file.</span></span> <span data-ttu-id="02a46-162">Si se especifica este campo, el archivo debe tener una versión que sea como más similar a MaxVersion.</span><span class="sxs-lookup"><span data-stu-id="02a46-162">If this field is specified, then the file must have a version that is at most equal to MaxVersion.</span></span>

</dd> <dt>

<span data-ttu-id="02a46-163"><span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize</span><span class="sxs-lookup"><span data-stu-id="02a46-163"><span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize</span></span>
</dt> <dd>

<span data-ttu-id="02a46-164">Tamaño mínimo del archivo.</span><span class="sxs-lookup"><span data-stu-id="02a46-164">The minimum size of the file.</span></span> <span data-ttu-id="02a46-165">Si se especifica este campo, el archivo en inspección debe tener un tamaño que sea al menos igual a MinSize.</span><span class="sxs-lookup"><span data-stu-id="02a46-165">If this field is specified, then the file under inspection must have a size that is at least equal to MinSize.</span></span> <span data-ttu-id="02a46-166">Debe ser un número no negativo.</span><span class="sxs-lookup"><span data-stu-id="02a46-166">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="02a46-167"><span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>Tamañomáximo</span><span class="sxs-lookup"><span data-stu-id="02a46-167"><span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize</span></span>
</dt> <dd>

<span data-ttu-id="02a46-168">Tamaño máximo del archivo.</span><span class="sxs-lookup"><span data-stu-id="02a46-168">The maximum size of the file.</span></span> <span data-ttu-id="02a46-169">Si se especifica este campo, el archivo que se está inspeccionando debe tener un tamaño que sea igual a MaxSize.</span><span class="sxs-lookup"><span data-stu-id="02a46-169">If this field is specified, then the file under inspection must have a size that is at most equal to MaxSize.</span></span> <span data-ttu-id="02a46-170">Debe ser un número no negativo.</span><span class="sxs-lookup"><span data-stu-id="02a46-170">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="02a46-171"><span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate</span><span class="sxs-lookup"><span data-stu-id="02a46-171"><span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate</span></span>
</dt> <dd>

<span data-ttu-id="02a46-172">Fecha y hora de modificación mínima del archivo.</span><span class="sxs-lookup"><span data-stu-id="02a46-172">The minimum modification date and time of the file.</span></span> <span data-ttu-id="02a46-173">Si se especifica este campo, el archivo en inspección debe tener una fecha y hora de modificación que sea al menos igual a MinDate.</span><span class="sxs-lookup"><span data-stu-id="02a46-173">If this field is specified, then the file under inspection must have a modification date and time that is at least equal to MinDate.</span></span> <span data-ttu-id="02a46-174">Debe ser un número no negativo.</span><span class="sxs-lookup"><span data-stu-id="02a46-174">This must be a non-negative number.</span></span> <span data-ttu-id="02a46-175">El formato de este campo es dos valores de 16 bits empaquetados de tipo **Word**.</span><span class="sxs-lookup"><span data-stu-id="02a46-175">The format of this field is two packed 16-bit values of type **WORD**.</span></span> <span data-ttu-id="02a46-176">El valor de **palabra** de orden superior especifica la fecha en formato de fecha de ms-dos.</span><span class="sxs-lookup"><span data-stu-id="02a46-176">The high order **WORD** value specifies the date in MS-DOS date format.</span></span> <span data-ttu-id="02a46-177">El valor de **palabra** de orden inferior especifica la hora en formato de hora de ms-dos.</span><span class="sxs-lookup"><span data-stu-id="02a46-177">The low order **WORD** value specifies the time in MS-DOS time format.</span></span> <span data-ttu-id="02a46-178">Un valor de 0 para el valor de hora representa la medianoche.</span><span class="sxs-lookup"><span data-stu-id="02a46-178">A value of 0 for the time value represents midnight.</span></span> <span data-ttu-id="02a46-179">Consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="02a46-179">See the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="02a46-180"><span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate</span><span class="sxs-lookup"><span data-stu-id="02a46-180"><span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate</span></span>
</dt> <dd>

<span data-ttu-id="02a46-181">La fecha de creación máxima del archivo.</span><span class="sxs-lookup"><span data-stu-id="02a46-181">The maximum creation date of the file.</span></span> <span data-ttu-id="02a46-182">Si se especifica este campo, el archivo que se inspecciona debe tener una fecha de creación igual a MaxDate.</span><span class="sxs-lookup"><span data-stu-id="02a46-182">If this field is specified, then the file under inspection must have a creation date that is at most equal to MaxDate.</span></span> <span data-ttu-id="02a46-183">Debe ser un número no negativo.</span><span class="sxs-lookup"><span data-stu-id="02a46-183">This must be a non-negative number.</span></span> <span data-ttu-id="02a46-184">El formato de este campo es dos valores de 16 bits empaquetados de tipo **Word**.</span><span class="sxs-lookup"><span data-stu-id="02a46-184">The format of this field is two packed 16-bit values of type **WORD**.</span></span> <span data-ttu-id="02a46-185">El valor de **palabra** de orden superior especifica la fecha en formato de fecha de ms-dos.</span><span class="sxs-lookup"><span data-stu-id="02a46-185">The high order **WORD** value specifies the date in MS-DOS date format.</span></span> <span data-ttu-id="02a46-186">El valor de **palabra** de orden inferior especifica la hora en formato de hora de ms-dos.</span><span class="sxs-lookup"><span data-stu-id="02a46-186">The low order **WORD** value specifies the time in MS-DOS time format.</span></span> <span data-ttu-id="02a46-187">Un valor de 0 para el valor de hora representa la medianoche.</span><span class="sxs-lookup"><span data-stu-id="02a46-187">A value of 0 for the time value represent midnight.</span></span> <span data-ttu-id="02a46-188">Consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="02a46-188">See the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="02a46-189"><span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Idiomas</span><span class="sxs-lookup"><span data-stu-id="02a46-189"><span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Languages</span></span>
</dt> <dd>

<span data-ttu-id="02a46-190">Idiomas admitidos por el archivo.</span><span class="sxs-lookup"><span data-stu-id="02a46-190">The languages supported by the file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02a46-191">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02a46-191">Remarks</span></span>

<span data-ttu-id="02a46-192">Esta tabla se usa con la [tabla AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="02a46-192">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="02a46-193">La firma se busca mediante la [tabla RegLocator](reglocator-table.md), la tabla [IniLocator](inilocator-table.md), la tabla [CompLocator](complocator-table.md)y la [tabla DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="02a46-193">The signature is searched for using the [RegLocator table](reglocator-table.md), the [IniLocator table](inilocator-table.md), the [CompLocator table](complocator-table.md), and the [DrLocator table](drlocator-table.md).</span></span> <span data-ttu-id="02a46-194">Por lo general, las columnas de esta tabla no están localizadas.</span><span class="sxs-lookup"><span data-stu-id="02a46-194">This table's columns are generally not localized.</span></span> <span data-ttu-id="02a46-195">Si un autor decide buscar productos en varios idiomas, puede haber una entrada independiente incluida en la tabla para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="02a46-195">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="02a46-196">La tabla de firmas suele seguir las [reglas de control de versiones de archivos](file-versioning-rules.md)Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="02a46-196">The Signature table generally follows the Windows Installer [File Versioning Rules](file-versioning-rules.md).</span></span> <span data-ttu-id="02a46-197">Los idiomas especificados en la columna Languages de la tabla Signature no se evalúan a menos que las versiones del archivo sean equivalentes.</span><span class="sxs-lookup"><span data-stu-id="02a46-197">Languages specified in the Languages column of the Signature table are not evaluated unless the file versions are equivalent.</span></span> <span data-ttu-id="02a46-198">La columna idiomas garantizará que un archivo sea de un idioma determinado si es de la versión solicitada.</span><span class="sxs-lookup"><span data-stu-id="02a46-198">The Languages column will ensure that a file is of a particular language if it is of the requested version.</span></span> <span data-ttu-id="02a46-199">No hay ningún método disponible para omitir la columna de idiomas.</span><span class="sxs-lookup"><span data-stu-id="02a46-199">There is no method available to ignore the Languages column.</span></span> <span data-ttu-id="02a46-200">Un valor NULL especificado en la columna Languages se trata como un archivo sin idioma y no coincide con la firma de archivo de un archivo con un idioma que aparece en la tabla Signature.</span><span class="sxs-lookup"><span data-stu-id="02a46-200">A NULL value entered in the Languages column is treated as a file without a language and does not match the file signature of a file with a language appearing in the Signature table.</span></span> <span data-ttu-id="02a46-201">En el siguiente ejemplo se busca una versión determinada de MSI.DLL.</span><span class="sxs-lookup"><span data-stu-id="02a46-201">The following example searches for a particular version of MSI.DLL.</span></span>

[<span data-ttu-id="02a46-202">Tabla DrLocator</span><span class="sxs-lookup"><span data-stu-id="02a46-202">DrLocator table</span></span>](drlocator-table.md)

| <span data-ttu-id="02a46-203">Signatura\_</span><span class="sxs-lookup"><span data-stu-id="02a46-203">Signature\_</span></span> | <span data-ttu-id="02a46-204">Parent</span><span class="sxs-lookup"><span data-stu-id="02a46-204">Parent</span></span> | <span data-ttu-id="02a46-205">Ruta</span><span class="sxs-lookup"><span data-stu-id="02a46-205">Path</span></span>                  | <span data-ttu-id="02a46-206">Profundidad</span><span class="sxs-lookup"><span data-stu-id="02a46-206">Depth</span></span> |
|-------------|--------|-----------------------|-------|
| <span data-ttu-id="02a46-207">MsiDll</span><span class="sxs-lookup"><span data-stu-id="02a46-207">MsiDll</span></span>      | <span data-ttu-id="02a46-208">acepta</span><span class="sxs-lookup"><span data-stu-id="02a46-208">{null}</span></span> | <span data-ttu-id="02a46-209">c: \\ Windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="02a46-209">c:\\windows\\system32</span></span> | <span data-ttu-id="02a46-210">0</span><span class="sxs-lookup"><span data-stu-id="02a46-210">0</span></span>     |



 

[<span data-ttu-id="02a46-211">Tabla AppSearch</span><span class="sxs-lookup"><span data-stu-id="02a46-211">AppSearch Table</span></span>](appsearch-table.md)



| <span data-ttu-id="02a46-212">Propiedad</span><span class="sxs-lookup"><span data-stu-id="02a46-212">Property</span></span> | <span data-ttu-id="02a46-213">Signatura\_</span><span class="sxs-lookup"><span data-stu-id="02a46-213">Signature\_</span></span> |
|----------|-------------|
| <span data-ttu-id="02a46-214">MSIDLL</span><span class="sxs-lookup"><span data-stu-id="02a46-214">MSIDLL</span></span>   | <span data-ttu-id="02a46-215">MsiDll</span><span class="sxs-lookup"><span data-stu-id="02a46-215">MsiDll</span></span>      |



 

<span data-ttu-id="02a46-216">Tabla de firmas</span><span class="sxs-lookup"><span data-stu-id="02a46-216">Signature table</span></span>



| <span data-ttu-id="02a46-217">Firma</span><span class="sxs-lookup"><span data-stu-id="02a46-217">Signature</span></span> | <span data-ttu-id="02a46-218">FileName</span><span class="sxs-lookup"><span data-stu-id="02a46-218">FileName</span></span> | <span data-ttu-id="02a46-219">MinVersion</span><span class="sxs-lookup"><span data-stu-id="02a46-219">MinVersion</span></span>    | <span data-ttu-id="02a46-220">MaxVersion</span><span class="sxs-lookup"><span data-stu-id="02a46-220">MaxVersion</span></span> | <span data-ttu-id="02a46-221">MinSize</span><span class="sxs-lookup"><span data-stu-id="02a46-221">MinSize</span></span> | <span data-ttu-id="02a46-222">MaxSize</span><span class="sxs-lookup"><span data-stu-id="02a46-222">MaxSize</span></span> | <span data-ttu-id="02a46-223">MinDate</span><span class="sxs-lookup"><span data-stu-id="02a46-223">MinDate</span></span> | <span data-ttu-id="02a46-224">MaxDate</span><span class="sxs-lookup"><span data-stu-id="02a46-224">MaxDate</span></span> | <span data-ttu-id="02a46-225">Idiomas</span><span class="sxs-lookup"><span data-stu-id="02a46-225">Languages</span></span> |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| <span data-ttu-id="02a46-226">MsiDll</span><span class="sxs-lookup"><span data-stu-id="02a46-226">MsiDll</span></span>    | <span data-ttu-id="02a46-227">msi.dll</span><span class="sxs-lookup"><span data-stu-id="02a46-227">msi.dll</span></span>  | <span data-ttu-id="02a46-228">2.0.2600.1106</span><span class="sxs-lookup"><span data-stu-id="02a46-228">2.0.2600.1106</span></span> | <span data-ttu-id="02a46-229">acepta</span><span class="sxs-lookup"><span data-stu-id="02a46-229">{null}</span></span>     | <span data-ttu-id="02a46-230">acepta</span><span class="sxs-lookup"><span data-stu-id="02a46-230">{null}</span></span>  | <span data-ttu-id="02a46-231">acepta</span><span class="sxs-lookup"><span data-stu-id="02a46-231">{null}</span></span>  | <span data-ttu-id="02a46-232">acepta</span><span class="sxs-lookup"><span data-stu-id="02a46-232">{null}</span></span>  | <span data-ttu-id="02a46-233">acepta</span><span class="sxs-lookup"><span data-stu-id="02a46-233">{null}</span></span>  | <span data-ttu-id="02a46-234">0</span><span class="sxs-lookup"><span data-stu-id="02a46-234">0</span></span>         |



 

<span data-ttu-id="02a46-235">En este caso, y en Windows XP SP1, la [acción AppSearch](appsearch-action.md) establece MSIDLL en c: \\ Windows \\ system32 \\msi.dll porque MSI.DLL es un archivo independiente del idioma.</span><span class="sxs-lookup"><span data-stu-id="02a46-235">In this case, and on Windows XP SP1, the [AppSearch action](appsearch-action.md) sets MSIDLL to c:\\windows\\system32\\msi.dll because MSI.DLL is a language neutral file.</span></span> <span data-ttu-id="02a46-236">Si el valor de la columna Languages se cambia de 0 a 1033, la acción AppSearch no puede encontrar el msi.dll coincidente y la propiedad MSIDLL no está definida.</span><span class="sxs-lookup"><span data-stu-id="02a46-236">If the value of the Languages column is changed from 0 to 1033, then the AppSearch action fails to find the matching msi.dll and the MSIDLL property is undefined.</span></span>

<span data-ttu-id="02a46-237">No se puede usar la tabla de firmas para realizar consultas solo en lenguajes.</span><span class="sxs-lookup"><span data-stu-id="02a46-237">You cannot use the Signature table to query on languages alone.</span></span> <span data-ttu-id="02a46-238">Para buscar diferentes versiones de idioma de un archivo, debe tener una entrada independiente en la tabla de firmas para cada versión de idioma.</span><span class="sxs-lookup"><span data-stu-id="02a46-238">To search for different language versions of a file, you must have a separate entry in the Signature table for each language version.</span></span> <span data-ttu-id="02a46-239">Si se proporcionan varios idiomas en la columna idiomas, la búsqueda es para un archivo que admita todos esos idiomas.</span><span class="sxs-lookup"><span data-stu-id="02a46-239">If multiple languages are provided in the Languages column, then the search is for a file that supports all of those languages.</span></span>

<span data-ttu-id="02a46-240">El formato de las columnas MinDate y MaxDate son dos valores de 16 bits empaquetados de tipo **Word**.</span><span class="sxs-lookup"><span data-stu-id="02a46-240">The format of MinDate and MaxDate columns are two packed 16-bit values of type **WORD**.</span></span>

<span data-ttu-id="02a46-241">**Palabra** de fecha</span><span class="sxs-lookup"><span data-stu-id="02a46-241">Date **WORD**</span></span>



| <span data-ttu-id="02a46-242">Bits</span><span class="sxs-lookup"><span data-stu-id="02a46-242">Bits</span></span> | <span data-ttu-id="02a46-243">Contenido</span><span class="sxs-lookup"><span data-stu-id="02a46-243">Content</span></span>                                             |
|------|-----------------------------------------------------|
| <span data-ttu-id="02a46-244">de 0 a 4</span><span class="sxs-lookup"><span data-stu-id="02a46-244">0–4</span></span>  | <span data-ttu-id="02a46-245">Día del mes (1-31)</span><span class="sxs-lookup"><span data-stu-id="02a46-245">Day of the month (1-31)</span></span>                             |
| <span data-ttu-id="02a46-246">5-8</span><span class="sxs-lookup"><span data-stu-id="02a46-246">5-8</span></span>  | <span data-ttu-id="02a46-247">Mes (1 = enero, 2 = febrero, etc.)</span><span class="sxs-lookup"><span data-stu-id="02a46-247">Month (1 = January, 2 = February, and so on)</span></span>        |
| <span data-ttu-id="02a46-248">9-15</span><span class="sxs-lookup"><span data-stu-id="02a46-248">9-15</span></span> | <span data-ttu-id="02a46-249">Desplazamiento de año desde 1980 (agregue 1980 para obtener el año real)</span><span class="sxs-lookup"><span data-stu-id="02a46-249">Year offset from 1980 (add 1980 to get actual year)</span></span> |



 

<span data-ttu-id="02a46-250">Hora- **palabra**</span><span class="sxs-lookup"><span data-stu-id="02a46-250">Time **WORD**</span></span>



| <span data-ttu-id="02a46-251">Bits</span><span class="sxs-lookup"><span data-stu-id="02a46-251">Bits</span></span>  | <span data-ttu-id="02a46-252">Contenido</span><span class="sxs-lookup"><span data-stu-id="02a46-252">Content</span></span>                     |
|-------|-----------------------------|
| <span data-ttu-id="02a46-253">de 0 a 4</span><span class="sxs-lookup"><span data-stu-id="02a46-253">0–4</span></span>   | <span data-ttu-id="02a46-254">Segundos divididos por 2</span><span class="sxs-lookup"><span data-stu-id="02a46-254">Seconds divided by 2</span></span>        |
| <span data-ttu-id="02a46-255">5-10</span><span class="sxs-lookup"><span data-stu-id="02a46-255">5-10</span></span>  | <span data-ttu-id="02a46-256">Minutos (0-59)</span><span class="sxs-lookup"><span data-stu-id="02a46-256">Minutes (0-59)</span></span>              |
| <span data-ttu-id="02a46-257">11-15</span><span class="sxs-lookup"><span data-stu-id="02a46-257">11-15</span></span> | <span data-ttu-id="02a46-258">Hora (0-23 en el reloj de 24 horas)</span><span class="sxs-lookup"><span data-stu-id="02a46-258">Hour(0-23 on 24 hour clock)</span></span> |



 

<span data-ttu-id="02a46-259">La fórmula para calcular los valores de los campos MinDate y MaxDate es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="02a46-259">The formula for calculating the MinDate and MaxDate field values is:</span></span>

<span data-ttu-id="02a46-260">((Año-1980) \* 512 + mes \* 32 + día) \* 65536 + horas \* 2048 + minutos \* 32 + segundos/2</span><span class="sxs-lookup"><span data-stu-id="02a46-260">( (Year - 1980) \* 512 + Month \* 32 + Day ) \* 65536 + Hours \* 2048 + Minutes \* 32 + Seconds/2</span></span>

## <a name="validation"></a><span data-ttu-id="02a46-261">Validación</span><span class="sxs-lookup"><span data-stu-id="02a46-261">Validation</span></span>

<dl>

[<span data-ttu-id="02a46-262">ICE03</span><span class="sxs-lookup"><span data-stu-id="02a46-262">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="02a46-263">ICE06</span><span class="sxs-lookup"><span data-stu-id="02a46-263">ICE06</span></span>](ice06.md)  
</dl>

 

 




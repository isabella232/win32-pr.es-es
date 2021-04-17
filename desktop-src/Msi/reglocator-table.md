---
description: La tabla RegLocator contiene la información necesaria para buscar un archivo o un directorio mediante el registro, o para buscar una entrada concreta del registro. Esta tabla tiene las columnas siguientes.
ms.assetid: dc88b083-cc1d-46d7-9be8-29ebbf3767a0
title: Tabla RegLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db5084b8c6fd8d10372759bdba65abbb4dfe7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667151"
---
# <a name="reglocator-table"></a><span data-ttu-id="41153-104">Tabla RegLocator</span><span class="sxs-lookup"><span data-stu-id="41153-104">RegLocator Table</span></span>

<span data-ttu-id="41153-105">La tabla RegLocator contiene la información necesaria para buscar un archivo o un directorio mediante el registro, o para buscar una entrada concreta del registro.</span><span class="sxs-lookup"><span data-stu-id="41153-105">The RegLocator table holds the information needed to search for a file or directory using the registry, or to search for a particular registry entry itself.</span></span> <span data-ttu-id="41153-106">Esta tabla tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="41153-106">This table has the following columns.</span></span>



| <span data-ttu-id="41153-107">Columna</span><span class="sxs-lookup"><span data-stu-id="41153-107">Column</span></span>      | <span data-ttu-id="41153-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="41153-108">Type</span></span>                         | <span data-ttu-id="41153-109">Clave</span><span class="sxs-lookup"><span data-stu-id="41153-109">Key</span></span> | <span data-ttu-id="41153-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="41153-110">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="41153-111">Signatura\_</span><span class="sxs-lookup"><span data-stu-id="41153-111">Signature\_</span></span> | [<span data-ttu-id="41153-112">Identificador</span><span class="sxs-lookup"><span data-stu-id="41153-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="41153-113">Y</span><span class="sxs-lookup"><span data-stu-id="41153-113">Y</span></span>   | <span data-ttu-id="41153-114">N</span><span class="sxs-lookup"><span data-stu-id="41153-114">N</span></span>        |
| <span data-ttu-id="41153-115">Root</span><span class="sxs-lookup"><span data-stu-id="41153-115">Root</span></span>        | [<span data-ttu-id="41153-116">Entero</span><span class="sxs-lookup"><span data-stu-id="41153-116">Integer</span></span>](integer.md)       | <span data-ttu-id="41153-117">N</span><span class="sxs-lookup"><span data-stu-id="41153-117">N</span></span>   | <span data-ttu-id="41153-118">N</span><span class="sxs-lookup"><span data-stu-id="41153-118">N</span></span>        |
| <span data-ttu-id="41153-119">Clave</span><span class="sxs-lookup"><span data-stu-id="41153-119">Key</span></span>         | [<span data-ttu-id="41153-120">RegPath</span><span class="sxs-lookup"><span data-stu-id="41153-120">RegPath</span></span>](regpath.md)       | <span data-ttu-id="41153-121">N</span><span class="sxs-lookup"><span data-stu-id="41153-121">N</span></span>   | <span data-ttu-id="41153-122">N</span><span class="sxs-lookup"><span data-stu-id="41153-122">N</span></span>        |
| <span data-ttu-id="41153-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="41153-123">Name</span></span>        | [<span data-ttu-id="41153-124">Formatea</span><span class="sxs-lookup"><span data-stu-id="41153-124">Formatted</span></span>](formatted.md)   | <span data-ttu-id="41153-125">N</span><span class="sxs-lookup"><span data-stu-id="41153-125">N</span></span>   | <span data-ttu-id="41153-126">Y</span><span class="sxs-lookup"><span data-stu-id="41153-126">Y</span></span>        |
| <span data-ttu-id="41153-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="41153-127">Type</span></span>        | [<span data-ttu-id="41153-128">Entero</span><span class="sxs-lookup"><span data-stu-id="41153-128">Integer</span></span>](integer.md)       | <span data-ttu-id="41153-129">N</span><span class="sxs-lookup"><span data-stu-id="41153-129">N</span></span>   | <span data-ttu-id="41153-130">Y</span><span class="sxs-lookup"><span data-stu-id="41153-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="41153-131">Columnas</span><span class="sxs-lookup"><span data-stu-id="41153-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="41153-132"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatura\_</span><span class="sxs-lookup"><span data-stu-id="41153-132"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="41153-133">El valor del campo Signature \_ representa una firma única que es una clave externa en la columna uno de la tabla [Signature](signature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="41153-133">The value in the Signature\_ field represents a unique signature that is an external key into column one of the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="41153-134">Si esta firma está presente en la tabla de firmas, la búsqueda es para un archivo.</span><span class="sxs-lookup"><span data-stu-id="41153-134">If this signature is present in the Signature table, the search is for a file.</span></span> <span data-ttu-id="41153-135">Si esta firma no está presente en la tabla de firmas y el valor de la columna Type es **msidbLocatorTypeRawValue**, la búsqueda es para el nombre de clave del registro al que apunta la tabla RegLocator.</span><span class="sxs-lookup"><span data-stu-id="41153-135">If this signature is absent from the Signature table, and the value of the Type column is **msidbLocatorTypeRawValue**, the search is for the registry key name pointed to by the RegLocator table.</span></span> <span data-ttu-id="41153-136">En caso contrario, la búsqueda es para un directorio al que apunta la tabla RegLocator.</span><span class="sxs-lookup"><span data-stu-id="41153-136">Otherwise the search is for a directory pointed to by the RegLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="41153-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Raíces</span><span class="sxs-lookup"><span data-stu-id="41153-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="41153-138">Clave raíz predefinida para el valor del registro.</span><span class="sxs-lookup"><span data-stu-id="41153-138">The predefined root key for the registry value.</span></span>



| <span data-ttu-id="41153-139">Constante</span><span class="sxs-lookup"><span data-stu-id="41153-139">Constant</span></span>                          | <span data-ttu-id="41153-140">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="41153-140">Hexadecimal</span></span> | <span data-ttu-id="41153-141">Decimal</span><span class="sxs-lookup"><span data-stu-id="41153-141">Decimal</span></span> | <span data-ttu-id="41153-142">Clave raíz</span><span class="sxs-lookup"><span data-stu-id="41153-142">Root key</span></span>             |
|-----------------------------------|-------------|---------|----------------------|
| <span data-ttu-id="41153-143">**msidbRegistryRootClassesRoot**</span><span class="sxs-lookup"><span data-stu-id="41153-143">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="41153-144">0x000</span><span class="sxs-lookup"><span data-stu-id="41153-144">0x000</span></span>       | <span data-ttu-id="41153-145">0</span><span class="sxs-lookup"><span data-stu-id="41153-145">0</span></span>       | <span data-ttu-id="41153-146">\_clase HKEY \_ raíz</span><span class="sxs-lookup"><span data-stu-id="41153-146">HKEY\_CLASSES\_ROOT</span></span>  |
| <span data-ttu-id="41153-147">**msidbRegistryRootCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="41153-147">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="41153-148">0x001</span><span class="sxs-lookup"><span data-stu-id="41153-148">0x001</span></span>       | <span data-ttu-id="41153-149">1</span><span class="sxs-lookup"><span data-stu-id="41153-149">1</span></span>       | <span data-ttu-id="41153-150">HKEY \_ Current \_ User</span><span class="sxs-lookup"><span data-stu-id="41153-150">HKEY\_CURRENT\_USER</span></span>  |
| <span data-ttu-id="41153-151">**msidbRegistryRootLocalMachine**</span><span class="sxs-lookup"><span data-stu-id="41153-151">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="41153-152">0x002</span><span class="sxs-lookup"><span data-stu-id="41153-152">0x002</span></span>       | <span data-ttu-id="41153-153">2</span><span class="sxs-lookup"><span data-stu-id="41153-153">2</span></span>       | <span data-ttu-id="41153-154">HKEY \_ local \_ Machine</span><span class="sxs-lookup"><span data-stu-id="41153-154">HKEY\_LOCAL\_MACHINE</span></span> |
| <span data-ttu-id="41153-155">**msidbRegistryRootUsers**</span><span class="sxs-lookup"><span data-stu-id="41153-155">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="41153-156">0x003</span><span class="sxs-lookup"><span data-stu-id="41153-156">0x003</span></span>       | <span data-ttu-id="41153-157">3</span><span class="sxs-lookup"><span data-stu-id="41153-157">3</span></span>       | <span data-ttu-id="41153-158">\_usuarios HKEY</span><span class="sxs-lookup"><span data-stu-id="41153-158">HKEY\_USERS</span></span>          |



 

</dd> <dt>

<span data-ttu-id="41153-159"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave</span><span class="sxs-lookup"><span data-stu-id="41153-159"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="41153-160">Clave para el valor del registro.</span><span class="sxs-lookup"><span data-stu-id="41153-160">The key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="41153-161"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="41153-161"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="41153-162">Nombre del valor del Registro.</span><span class="sxs-lookup"><span data-stu-id="41153-162">The registry value name.</span></span> <span data-ttu-id="41153-163">Si este valor es null, se recupera el valor del valor sin nombre o predeterminado de la clave, si existe.</span><span class="sxs-lookup"><span data-stu-id="41153-163">If this value is null, then the value from the key's unnamed or default value, if any, is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="41153-164"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Automáticamente</span><span class="sxs-lookup"><span data-stu-id="41153-164"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="41153-165">Un valor que determina si el valor del registro es un nombre de archivo, una ubicación de directorio o un valor de registro sin formato.</span><span class="sxs-lookup"><span data-stu-id="41153-165">A value that determines if the registry value is a file name, a directory location, or raw registry value.</span></span>

<span data-ttu-id="41153-166">En la tabla siguiente se enumeran los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="41153-166">The following table lists valid values.</span></span> <span data-ttu-id="41153-167">Establezca uno de los tres primeros valores y **msidbLocatorType64bit** si es necesario.</span><span class="sxs-lookup"><span data-stu-id="41153-167">Set one of the first three values and **msidbLocatorType64bit** if necessary.</span></span> <span data-ttu-id="41153-168">Si la entrada de este campo no está presente, el tipo se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="41153-168">If the entry in this field is absent, Type is set to be 1.</span></span>



| <span data-ttu-id="41153-169">Constante</span><span class="sxs-lookup"><span data-stu-id="41153-169">Constant</span></span>                      | <span data-ttu-id="41153-170">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="41153-170">Hexadecimal</span></span> | <span data-ttu-id="41153-171">Decimal</span><span class="sxs-lookup"><span data-stu-id="41153-171">Decimal</span></span> | <span data-ttu-id="41153-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="41153-172">Description</span></span>                                                                                                                                                        |
|-------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41153-173">**msidbLocatorTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="41153-173">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="41153-174">0x000</span><span class="sxs-lookup"><span data-stu-id="41153-174">0x000</span></span>       | <span data-ttu-id="41153-175">0</span><span class="sxs-lookup"><span data-stu-id="41153-175">0</span></span>       | <span data-ttu-id="41153-176">La ruta de acceso de la clave es un directorio.</span><span class="sxs-lookup"><span data-stu-id="41153-176">Key path is a directory.</span></span>                                                                                                                                           |
| <span data-ttu-id="41153-177">**msidbLocatorTypeFileName**</span><span class="sxs-lookup"><span data-stu-id="41153-177">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="41153-178">0x001</span><span class="sxs-lookup"><span data-stu-id="41153-178">0x001</span></span>       | <span data-ttu-id="41153-179">1</span><span class="sxs-lookup"><span data-stu-id="41153-179">1</span></span>       | <span data-ttu-id="41153-180">La ruta de acceso de la clave es un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="41153-180">Key path is a file name.</span></span>                                                                                                                                           |
| <span data-ttu-id="41153-181">**msidbLocatorTypeRawValue**</span><span class="sxs-lookup"><span data-stu-id="41153-181">**msidbLocatorTypeRawValue**</span></span>  | <span data-ttu-id="41153-182">0x002</span><span class="sxs-lookup"><span data-stu-id="41153-182">0x002</span></span>       | <span data-ttu-id="41153-183">2</span><span class="sxs-lookup"><span data-stu-id="41153-183">2</span></span>       | <span data-ttu-id="41153-184">La ruta de acceso de la clave es un valor del registro.</span><span class="sxs-lookup"><span data-stu-id="41153-184">Key path is a registry value.</span></span>                                                                                                                                      |
| <span data-ttu-id="41153-185">**msidbLocatorType64bit**</span><span class="sxs-lookup"><span data-stu-id="41153-185">**msidbLocatorType64bit**</span></span>     | <span data-ttu-id="41153-186">0x010</span><span class="sxs-lookup"><span data-stu-id="41153-186">0x010</span></span>       | <span data-ttu-id="41153-187">16</span><span class="sxs-lookup"><span data-stu-id="41153-187">16</span></span>      | <span data-ttu-id="41153-188">Establezca este bit para que el instalador busque en la parte 64 de bits del registro.</span><span class="sxs-lookup"><span data-stu-id="41153-188">Set this bit to have the installer search the 64-bit portion of the registry.</span></span> <span data-ttu-id="41153-189">No establezca este bit para que el instalador busque en la parte 32 de bits del registro.</span><span class="sxs-lookup"><span data-stu-id="41153-189">Do not set this bit to have the installer search the 32-bit portion of the registry.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41153-190">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41153-190">Remarks</span></span>

<span data-ttu-id="41153-191">Tenga en cuenta que si el valor del campo de tipo es **msidbLocatorTypeRawValue**, el instalador establece el valor de la propiedad especificada en el campo de propiedad de la tabla [AppSearch](appsearch-table.md) en el valor del registro.</span><span class="sxs-lookup"><span data-stu-id="41153-191">Note that if the value in the Type field is **msidbLocatorTypeRawValue**, the installer sets the value of the property specified in the Property field of the [AppSearch](appsearch-table.md) table to the registry value.</span></span> <span data-ttu-id="41153-192">El instalador agrega un prefijo al valor del registro que identifica el tipo de valor del registro.</span><span class="sxs-lookup"><span data-stu-id="41153-192">The installer adds a prefix to the registry value that identifies the type of registry value.</span></span> <span data-ttu-id="41153-193">Para obtener más información sobre los tipos de valores del registro, vea [tipos de valor del registro](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="41153-193">For more information about types of registry values, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>



| <span data-ttu-id="41153-194">Tipo de Registro</span><span class="sxs-lookup"><span data-stu-id="41153-194">Registry type</span></span>   | <span data-ttu-id="41153-195">Prefijo agregado por el instalador</span><span class="sxs-lookup"><span data-stu-id="41153-195">Prefix added by Installer</span></span>                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41153-196">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="41153-196">REG\_SZ</span></span>         | <span data-ttu-id="41153-197">Ninguno, pero si el primer carácter del valor del registro es \# , el instalador escapa el carácter prefijando otro \# .</span><span class="sxs-lookup"><span data-stu-id="41153-197">None, but if the first character of the registry value is \#, the installer escapes the character by prefixing a another \#.</span></span>            |
| <span data-ttu-id="41153-198">DWORD</span><span class="sxs-lookup"><span data-stu-id="41153-198">DWORD</span></span>           | <span data-ttu-id="41153-199">" \# " opcionalmente seguido de ' + ' o '-'</span><span class="sxs-lookup"><span data-stu-id="41153-199">"\#" optionally followed by '+' or '-'</span></span>                                                                                                  |
| <span data-ttu-id="41153-200">REG \_ expandir \_ SZ</span><span class="sxs-lookup"><span data-stu-id="41153-200">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="41153-201">"\#%"</span><span class="sxs-lookup"><span data-stu-id="41153-201">"\#%"</span></span>                                                                                                                                   |
| <span data-ttu-id="41153-202">REG \_ multi \_ SZ</span><span class="sxs-lookup"><span data-stu-id="41153-202">REG\_MULTI\_SZ</span></span>  | <span data-ttu-id="41153-203">NULL.</span><span class="sxs-lookup"><span data-stu-id="41153-203">Null.</span></span> <span data-ttu-id="41153-204">El instalador establece la propiedad en un valor que empieza con un valor NULL y termina con un valor null.</span><span class="sxs-lookup"><span data-stu-id="41153-204">The installer sets the property to a value beginning with a null and ending with a null.</span></span>                                          |
| <span data-ttu-id="41153-205">\_binario de reg</span><span class="sxs-lookup"><span data-stu-id="41153-205">REG\_BINARY</span></span>     | <span data-ttu-id="41153-206">" \# x" en el caso de reg \_ Binary, el instalador convierte y guarda cada dígito hexadecimal (recorte) como un carácter ASCII precedido por " \# x".</span><span class="sxs-lookup"><span data-stu-id="41153-206">"\#x" In case of REG\_BINARY, the installer converts and saves each hexadecimal digit (nibble) as an ASCII character prefixed by "\#x".</span></span> |



 

<span data-ttu-id="41153-207">Normalmente, las columnas de esta tabla no están localizadas.</span><span class="sxs-lookup"><span data-stu-id="41153-207">Typically, the columns in this table are not localized.</span></span> <span data-ttu-id="41153-208">Si un autor decide buscar productos en varios idiomas, debe haber una entrada independiente incluida en la tabla para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="41153-208">If an author decides to search for products in multiple languages, then there must be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="41153-209">Tenga en cuenta que no es posible usar la tabla RegLocator para comprobar solo la presencia de la clave.</span><span class="sxs-lookup"><span data-stu-id="41153-209">Note that it is not possible to use the RegLocator table to check only for the presence of the key.</span></span> <span data-ttu-id="41153-210">Sin embargo, puede buscar el valor predeterminado de una clave y recuperar su valor si no está vacío.</span><span class="sxs-lookup"><span data-stu-id="41153-210">However, you can search for the default value of a key and retrieve its value if it is not empty.</span></span>

<span data-ttu-id="41153-211">Para obtener más información, vea [Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="41153-211">For more information, see [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="41153-212">Validación</span><span class="sxs-lookup"><span data-stu-id="41153-212">Validation</span></span>

<dl>

[<span data-ttu-id="41153-213">ICE03</span><span class="sxs-lookup"><span data-stu-id="41153-213">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="41153-214">ICE06</span><span class="sxs-lookup"><span data-stu-id="41153-214">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="41153-215">ICE46</span><span class="sxs-lookup"><span data-stu-id="41153-215">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="41153-216">ICE80</span><span class="sxs-lookup"><span data-stu-id="41153-216">ICE80</span></span>](ice80.md)  
</dl>

 

 

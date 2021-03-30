---
description: La tabla del registro contiene la información del registro que la aplicación necesita para establecer en el registro del sistema.
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: Tabla del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16cb2084716ea8cb9830056808e9c6be7da667f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001870"
---
# <a name="registry-table"></a><span data-ttu-id="77097-103">Tabla del registro</span><span class="sxs-lookup"><span data-stu-id="77097-103">Registry Table</span></span>

<span data-ttu-id="77097-104">La tabla del registro contiene la información del registro que la aplicación necesita para establecer en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="77097-104">The Registry table holds the registry information that the application needs to set in the system registry.</span></span>

<span data-ttu-id="77097-105">La tabla del registro tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="77097-105">The Registry table has the following columns.</span></span>



| <span data-ttu-id="77097-106">Columna</span><span class="sxs-lookup"><span data-stu-id="77097-106">Column</span></span>      | <span data-ttu-id="77097-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="77097-107">Type</span></span>                         | <span data-ttu-id="77097-108">Clave</span><span class="sxs-lookup"><span data-stu-id="77097-108">Key</span></span> | <span data-ttu-id="77097-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="77097-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="77097-110">Registro</span><span class="sxs-lookup"><span data-stu-id="77097-110">Registry</span></span>    | [<span data-ttu-id="77097-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="77097-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="77097-112">Y</span><span class="sxs-lookup"><span data-stu-id="77097-112">Y</span></span>   | <span data-ttu-id="77097-113">N</span><span class="sxs-lookup"><span data-stu-id="77097-113">N</span></span>        |
| <span data-ttu-id="77097-114">Root</span><span class="sxs-lookup"><span data-stu-id="77097-114">Root</span></span>        | [<span data-ttu-id="77097-115">Entero</span><span class="sxs-lookup"><span data-stu-id="77097-115">Integer</span></span>](integer.md)       | <span data-ttu-id="77097-116">N</span><span class="sxs-lookup"><span data-stu-id="77097-116">N</span></span>   | <span data-ttu-id="77097-117">N</span><span class="sxs-lookup"><span data-stu-id="77097-117">N</span></span>        |
| <span data-ttu-id="77097-118">Clave</span><span class="sxs-lookup"><span data-stu-id="77097-118">Key</span></span>         | [<span data-ttu-id="77097-119">RegPath</span><span class="sxs-lookup"><span data-stu-id="77097-119">RegPath</span></span>](regpath.md)       | <span data-ttu-id="77097-120">N</span><span class="sxs-lookup"><span data-stu-id="77097-120">N</span></span>   | <span data-ttu-id="77097-121">N</span><span class="sxs-lookup"><span data-stu-id="77097-121">N</span></span>        |
| <span data-ttu-id="77097-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="77097-122">Name</span></span>        | [<span data-ttu-id="77097-123">Formatea</span><span class="sxs-lookup"><span data-stu-id="77097-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="77097-124">N</span><span class="sxs-lookup"><span data-stu-id="77097-124">N</span></span>   | <span data-ttu-id="77097-125">Y</span><span class="sxs-lookup"><span data-stu-id="77097-125">Y</span></span>        |
| <span data-ttu-id="77097-126">Value</span><span class="sxs-lookup"><span data-stu-id="77097-126">Value</span></span>       | [<span data-ttu-id="77097-127">Formatea</span><span class="sxs-lookup"><span data-stu-id="77097-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="77097-128">N</span><span class="sxs-lookup"><span data-stu-id="77097-128">N</span></span>   | <span data-ttu-id="77097-129">Y</span><span class="sxs-lookup"><span data-stu-id="77097-129">Y</span></span>        |
| <span data-ttu-id="77097-130">Componente\_</span><span class="sxs-lookup"><span data-stu-id="77097-130">Component\_</span></span> | [<span data-ttu-id="77097-131">Identificador</span><span class="sxs-lookup"><span data-stu-id="77097-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="77097-132">N</span><span class="sxs-lookup"><span data-stu-id="77097-132">N</span></span>   | <span data-ttu-id="77097-133">N</span><span class="sxs-lookup"><span data-stu-id="77097-133">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="77097-134">Columnas</span><span class="sxs-lookup"><span data-stu-id="77097-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="77097-135"><span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Del registro</span><span class="sxs-lookup"><span data-stu-id="77097-135"><span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Registry</span></span>
</dt> <dd>

<span data-ttu-id="77097-136">Clave principal que se usa para identificar un registro de registro.</span><span class="sxs-lookup"><span data-stu-id="77097-136">Primary key used to identify a registry record.</span></span>

</dd> <dt>

<span data-ttu-id="77097-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Raíces</span><span class="sxs-lookup"><span data-stu-id="77097-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="77097-138">Clave raíz predefinida para el valor del registro.</span><span class="sxs-lookup"><span data-stu-id="77097-138">The predefined root key for the registry value.</span></span> <span data-ttu-id="77097-139">Escriba un valor de-1 en este campo para que la clave raíz dependa del tipo de instalación.</span><span class="sxs-lookup"><span data-stu-id="77097-139">Enter a value of -1 in this field to make the root key dependent on the type of installation.</span></span> <span data-ttu-id="77097-140">Escriba uno de los otros valores de la tabla siguiente para forzar que el valor del registro se escriba en una clave raíz determinada.</span><span class="sxs-lookup"><span data-stu-id="77097-140">Enter one of the other values in the following table to force the registry value to be written under a particular root key.</span></span>



| <span data-ttu-id="77097-141">Constante</span><span class="sxs-lookup"><span data-stu-id="77097-141">Constant</span></span>                          | <span data-ttu-id="77097-142">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="77097-142">Hexadecimal</span></span> | <span data-ttu-id="77097-143">Decimal</span><span class="sxs-lookup"><span data-stu-id="77097-143">Decimal</span></span> | <span data-ttu-id="77097-144">Clave raíz</span><span class="sxs-lookup"><span data-stu-id="77097-144">Root key</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77097-145">(ninguno)</span><span class="sxs-lookup"><span data-stu-id="77097-145">(none)</span></span>                            | <span data-ttu-id="77097-146">\- 0x001</span><span class="sxs-lookup"><span data-stu-id="77097-146">\- 0x001</span></span>    | <span data-ttu-id="77097-147">-1</span><span class="sxs-lookup"><span data-stu-id="77097-147">-1</span></span>      | <span data-ttu-id="77097-148">Si se trata de una instalación por usuario, el valor del registro se escribe en **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="77097-148">If this is a per-user installation, the registry value is written under **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="77097-149">Si se trata de una instalación por equipo, el valor del registro se escribe en **HKEY \_ local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="77097-149">If this is a per-machine installation, the registry value is written under **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="77097-150">Tenga en cuenta que una instalación por equipo se especifica estableciendo la propiedad [**AllUsers**](allusers.md) en 1.</span><span class="sxs-lookup"><span data-stu-id="77097-150">Note that a per-machine installation is specified by setting the [**ALLUSERS**](allusers.md) property to 1.</span></span><br/>                |
| <span data-ttu-id="77097-151">**msidbRegistryRootClassesRoot**</span><span class="sxs-lookup"><span data-stu-id="77097-151">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="77097-152">0x000</span><span class="sxs-lookup"><span data-stu-id="77097-152">0x000</span></span>       | <span data-ttu-id="77097-153">0</span><span class="sxs-lookup"><span data-stu-id="77097-153">0</span></span>       | <span data-ttu-id="77097-154">**HKEY \_ CLASES \_ raíz** el instalador escribe o quita el valor de la **\\ clase HKCU Software \\ classes** durante la instalación en el [contexto de instalación](installation-context.md)por usuario.</span><span class="sxs-lookup"><span data-stu-id="77097-154">**HKEY\_CLASSES\_ROOT** The installer writes or removes the value from the **HKCU\\Software\\Classes** hive during installation in the per-user [installation context](installation-context.md).</span></span><br/> <span data-ttu-id="77097-155">El instalador escribe o quita el valor del subárbol **HKLM \\ software \\ classes** durante las instalaciones por máquina.</span><span class="sxs-lookup"><span data-stu-id="77097-155">The installer writes or removes the value from the **HKLM\\Software\\Classes** hive during per-machine installations.</span></span><br/> |
| <span data-ttu-id="77097-156">**msidbRegistryRootCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="77097-156">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="77097-157">0x001</span><span class="sxs-lookup"><span data-stu-id="77097-157">0x001</span></span>       | <span data-ttu-id="77097-158">1</span><span class="sxs-lookup"><span data-stu-id="77097-158">1</span></span>       | <span data-ttu-id="77097-159">**HKEY \_ Current \_ User**</span><span class="sxs-lookup"><span data-stu-id="77097-159">**HKEY\_CURRENT\_USER**</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="77097-160">**msidbRegistryRootLocalMachine**</span><span class="sxs-lookup"><span data-stu-id="77097-160">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="77097-161">0x002</span><span class="sxs-lookup"><span data-stu-id="77097-161">0x002</span></span>       | <span data-ttu-id="77097-162">2</span><span class="sxs-lookup"><span data-stu-id="77097-162">2</span></span>       | <span data-ttu-id="77097-163">**HKEY \_ local \_ Machine**</span><span class="sxs-lookup"><span data-stu-id="77097-163">**HKEY\_LOCAL\_MACHINE**</span></span>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="77097-164">**msidbRegistryRootUsers**</span><span class="sxs-lookup"><span data-stu-id="77097-164">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="77097-165">0x003</span><span class="sxs-lookup"><span data-stu-id="77097-165">0x003</span></span>       | <span data-ttu-id="77097-166">3</span><span class="sxs-lookup"><span data-stu-id="77097-166">3</span></span>       | <span data-ttu-id="77097-167">**\_usuarios HKEY**</span><span class="sxs-lookup"><span data-stu-id="77097-167">**HKEY\_USERS**</span></span>                                                                                                                                                                                                                                                                                                                              |



 

<span data-ttu-id="77097-168">Tenga en cuenta que se recomienda que las entradas del registro escritas en el subárbol **HKCU** hagan referencia a un componente que tenga establecido el bit RegistryKeyPath en la columna Attributes de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="77097-168">Note that it is recommended that registry entries written to the **HKCU** hive reference a component having the RegistryKeyPath bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="77097-169">Esto garantiza que el instalador escriba las entradas del registro necesarias cuando haya varios usuarios en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="77097-169">This ensures that the installer writes the necessary registry entries when there are multiple users on the same computer.</span></span>

</dd> <dt>

<span data-ttu-id="77097-170"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave</span><span class="sxs-lookup"><span data-stu-id="77097-170"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="77097-171">La clave localizable para el valor del registro.</span><span class="sxs-lookup"><span data-stu-id="77097-171">The localizable key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="77097-172"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="77097-172"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="77097-173">Esta columna contiene el nombre del valor del registro (localizable).</span><span class="sxs-lookup"><span data-stu-id="77097-173">This column contains the registry value name (localizable).</span></span> <span data-ttu-id="77097-174">Si es null, los datos especificados en la columna valor se escriben en la clave del registro predeterminada.</span><span class="sxs-lookup"><span data-stu-id="77097-174">If this is Null, then the data entered into the Value column are written to the default registry key.</span></span>

<span data-ttu-id="77097-175">Si la columna valor es null, las cadenas que se muestran en la tabla siguiente en la columna nombre tienen una importancia especial.</span><span class="sxs-lookup"><span data-stu-id="77097-175">If the Value column is Null, then the strings shown in the following table in the Name column have special significance.</span></span>



| <span data-ttu-id="77097-176">String</span><span class="sxs-lookup"><span data-stu-id="77097-176">String</span></span> | <span data-ttu-id="77097-177">Significado</span><span class="sxs-lookup"><span data-stu-id="77097-177">Meaning</span></span>                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | <span data-ttu-id="77097-178">La clave se creará, si no está presente, cuando se instale el componente.</span><span class="sxs-lookup"><span data-stu-id="77097-178">The key is to be created, if absent, when the component is installed.</span></span>                                                                                                                            |
| \-     | <span data-ttu-id="77097-179">La clave se eliminará, si está presente, con todos sus valores y subclaves, cuando se desinstale el componente.</span><span class="sxs-lookup"><span data-stu-id="77097-179">The key is to be deleted, if present, with all of its values and subkeys, when the component is uninstalled.</span></span>                                                                                     |
| \*     | <span data-ttu-id="77097-180">La clave se creará, si no está presente, cuando se instale el componente.</span><span class="sxs-lookup"><span data-stu-id="77097-180">The key is to be created, if absent, when the component is installed.</span></span> <span data-ttu-id="77097-181">Además, la clave se eliminará, si está presente, con todos sus valores y subclaves, cuando se desinstale el componente.</span><span class="sxs-lookup"><span data-stu-id="77097-181">Additionally, the key is to be deleted, if present, with all of its values and subkeys, when the component is uninstalled.</span></span> |



 

<span data-ttu-id="77097-182">Tenga en cuenta que se debe usar la [tabla RemoveRegistry](removeregistry-table.md) si se va a eliminar una clave del registro instalada, con sus valores y subclaves, cuando se instale el componente.</span><span class="sxs-lookup"><span data-stu-id="77097-182">Note that the [RemoveRegistry table](removeregistry-table.md) must be used if an installed registry key is to be deleted, with its values and subkeys, when the component is installed.</span></span>

</dd> <dt>

<span data-ttu-id="77097-183"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="77097-183"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="77097-184">Esta columna es el valor del registro localizable.</span><span class="sxs-lookup"><span data-stu-id="77097-184">This column is the localizable registry value.</span></span> <span data-ttu-id="77097-185">El campo tiene [formato](formatted.md).</span><span class="sxs-lookup"><span data-stu-id="77097-185">The field is [Formatted](formatted.md).</span></span> <span data-ttu-id="77097-186">Si el valor se adjunta a uno de los siguientes prefijos (es decir, \# % *Value*), el valor se interpreta como se describe en la tabla.</span><span class="sxs-lookup"><span data-stu-id="77097-186">If the value is attached to one of the following prefixes (i.e. \#%*value*) then the value is interpreted as described in the table.</span></span> <span data-ttu-id="77097-187">Tenga en cuenta que cada prefijo comienza con un signo de número ( \# ).</span><span class="sxs-lookup"><span data-stu-id="77097-187">Note that each prefix begins with a number sign (\#).</span></span> <span data-ttu-id="77097-188">Si el valor comienza con dos o más signos de número consecutivos ( \# ), el primero \# se omite y el valor se interpreta y se almacena como una cadena.</span><span class="sxs-lookup"><span data-stu-id="77097-188">If the value begins with two or more consecutive number signs (\#), the first \# is ignored and value is interpreted and stored as a string.</span></span>



| <span data-ttu-id="77097-189">Prefijo</span><span class="sxs-lookup"><span data-stu-id="77097-189">Prefix</span></span> | <span data-ttu-id="77097-190">Significado</span><span class="sxs-lookup"><span data-stu-id="77097-190">Meaning</span></span>                                                                        |
|--------|--------------------------------------------------------------------------------|
| <span data-ttu-id="77097-191">\#x1</span><span class="sxs-lookup"><span data-stu-id="77097-191">\#x</span></span>    | <span data-ttu-id="77097-192">El valor se interpreta y se almacena como un valor hexadecimal (REG \_ binario).</span><span class="sxs-lookup"><span data-stu-id="77097-192">The value is interpreted and stored as a hexadecimal value (REG\_BINARY).</span></span>      |
| \#%    | <span data-ttu-id="77097-193">El valor se interpreta y se almacena como una cadena expansible (REG \_ Expand \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="77097-193">The value is interpreted and stored as an expandable string (REG\_EXPAND\_SZ).</span></span> |
| \#     | <span data-ttu-id="77097-194">El valor se interpreta y se almacena como un entero (REG \_ DWORD).</span><span class="sxs-lookup"><span data-stu-id="77097-194">The value is interpreted and stored as an integer (REG\_DWORD).</span></span>                |



 

-   <span data-ttu-id="77097-195">Si el valor contiene la tilde de la secuencia \[ ~ \] , el valor se interpreta como una lista de cadenas delimitada por null (REG \_ multi \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="77097-195">If the value contains the sequence tilde \[~\], then the value is interpreted as a Null-delimited list of strings (REG\_MULTI\_SZ).</span></span> <span data-ttu-id="77097-196">Por ejemplo, para especificar una lista que contenga las tres cadenas a, b y c, use "a \[ ~ \] b \[ ~ \] c".</span><span class="sxs-lookup"><span data-stu-id="77097-196">For example, to specify a list containing the three strings a, b and c, use "a\[~\]b\[~\]c".</span></span>
-   <span data-ttu-id="77097-197">La secuencia \[ ~ \] dentro del valor separa las cadenas individuales y se interpreta y se almacena como un carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="77097-197">The sequence \[~\] within the value separates the individual strings and is interpreted and stored as a Null character.</span></span>
-   <span data-ttu-id="77097-198">Si \[ ~ \] precede a la lista de cadenas, las cadenas se anexarán a cualquier cadena de valor del registro existente.</span><span class="sxs-lookup"><span data-stu-id="77097-198">If a \[~\] precedes the string list, the strings are to be appended to any existing registry value strings.</span></span> <span data-ttu-id="77097-199">Si ya hay una cadena anexada en el valor del registro, se quita la repetición original de la cadena.</span><span class="sxs-lookup"><span data-stu-id="77097-199">If an appending string already occurs in the registry value, the original occurrence of the string is removed.</span></span>
-   <span data-ttu-id="77097-200">Si \[ ~ \] después del final de la lista de cadenas, las cadenas se anteponen a cualquier cadena de valor del registro existente.</span><span class="sxs-lookup"><span data-stu-id="77097-200">If a \[~\] follows the end of the string list, the strings are to be prepended to any existing registry value strings.</span></span> <span data-ttu-id="77097-201">Si ya hay una cadena anteponeda en el valor del registro, se quita la repetición original de la cadena.</span><span class="sxs-lookup"><span data-stu-id="77097-201">If a prepending string already occurs in the registry value, the original occurrence of the string is removed.</span></span>
-   <span data-ttu-id="77097-202">Si \[ ~ \] se encuentra al principio y al final, o al principio o al final de la lista de cadenas, las cadenas van a reemplazar cualquier cadena de valor del registro existente.</span><span class="sxs-lookup"><span data-stu-id="77097-202">If a \[~\] is at both the beginning and the end or at neither the beginning nor the end of the string list, the strings are to replace any existing registry value strings.</span></span>
-   <span data-ttu-id="77097-203">De lo contrario, el valor se interpreta y se almacena como una cadena (REG \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="77097-203">Otherwise, the value is interpreted and stored as a string (REG\_SZ).</span></span>

</dd> <dt>

<span data-ttu-id="77097-204"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="77097-204"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="77097-205">Clave externa en la primera columna de la [tabla de componentes](component-table.md) que hace referencia al componente que controla la instalación del valor del registro.</span><span class="sxs-lookup"><span data-stu-id="77097-205">External key into the first column of the [Component table](component-table.md) referencing the component that controls the installation of the registry value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77097-206">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77097-206">Remarks</span></span>

<span data-ttu-id="77097-207">Las acciones [WriteRegistryValues](writeregistryvalues-action.md) y [RemoveRegistryValues](removeregistryvalues-action.md) de [*las tablas de secuencia*](s-gly.md) procesan la información de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="77097-207">The [WriteRegistryValues](writeregistryvalues-action.md) and [RemoveRegistryValues](removeregistryvalues-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="77097-208">Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="77097-208">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="77097-209">La información del registro se escribe en el registro del sistema cuando se ha seleccionado el componente correspondiente para que se instale localmente o se ejecute desde el origen.</span><span class="sxs-lookup"><span data-stu-id="77097-209">The registry information is written out to the system registry when the corresponding component has been selected to be installed locally or run from source.</span></span>

<span data-ttu-id="77097-210">Tenga en cuenta que el instalador quita una clave del registro después de quitar el último valor o subclave de la clave.</span><span class="sxs-lookup"><span data-stu-id="77097-210">Note that the installer removes a registry key after removing the last value or subkey under the key.</span></span> <span data-ttu-id="77097-211">Para evitar que se quite una clave del Registro vacía al desinstalar, escriba un valor ficticio en la clave que necesita mantener y escriba + en la columna nombre.</span><span class="sxs-lookup"><span data-stu-id="77097-211">To prevent an empty registry key from being removed when uninstalling, write a dummy value under the key you need to keep and enter + in the Name column.</span></span> <span data-ttu-id="77097-212">Si \* está en la columna nombre, la clave se elimina, con todos sus valores y subclaves, cuando se quita el componente.</span><span class="sxs-lookup"><span data-stu-id="77097-212">If \* is in the Name column, the key is deleted, with all of its values and subkeys, when the component is removed.</span></span>

<span data-ttu-id="77097-213">Se puede utilizar una acción personalizada para agregar filas a la tabla del registro durante una operación de instalación, desinstalación o reparación.</span><span class="sxs-lookup"><span data-stu-id="77097-213">A custom action can be used to add rows to the Registry table during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="77097-214">Estas filas no se conservan en la tabla del registro y la información solo está disponible durante la transacción actual.</span><span class="sxs-lookup"><span data-stu-id="77097-214">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="77097-215">Por lo tanto, la acción personalizada se debe ejecutar en todas las transacciones de instalación, desinstalación o reparación que requieran la información de estas filas adicionales.</span><span class="sxs-lookup"><span data-stu-id="77097-215">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="77097-216">La acción personalizada debe ser anterior a las acciones [RemoveRegistryValues](removeregistryvalues-action.md) y [WriteRegistryValues](writeregistryvalues-action.md) en la secuencia de acción.</span><span class="sxs-lookup"><span data-stu-id="77097-216">The custom action must come before the [RemoveRegistryValues](removeregistryvalues-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions in the action sequence.</span></span>

<span data-ttu-id="77097-217">Para obtener información sobre cómo proteger una clave del registro, vea la [tabla MsiLockPermissionsEx](msilockpermissionsex-table.md) y la [tabla LockPermissions](lockpermissions-table.md).</span><span class="sxs-lookup"><span data-stu-id="77097-217">For information on how to secure a registry key see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) and [LockPermissions Table](lockpermissions-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="77097-218">Validación</span><span class="sxs-lookup"><span data-stu-id="77097-218">Validation</span></span>

<dl>

[<span data-ttu-id="77097-219">ICE02</span><span class="sxs-lookup"><span data-stu-id="77097-219">ICE02</span></span>](ice02.md)  
[<span data-ttu-id="77097-220">ICE03</span><span class="sxs-lookup"><span data-stu-id="77097-220">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="77097-221">ICE06</span><span class="sxs-lookup"><span data-stu-id="77097-221">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="77097-222">ICE32</span><span class="sxs-lookup"><span data-stu-id="77097-222">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="77097-223">ICE38</span><span class="sxs-lookup"><span data-stu-id="77097-223">ICE38</span></span>](ice38.md)  
[<span data-ttu-id="77097-224">ICE43</span><span class="sxs-lookup"><span data-stu-id="77097-224">ICE43</span></span>](ice43.md)  
[<span data-ttu-id="77097-225">ICE46</span><span class="sxs-lookup"><span data-stu-id="77097-225">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="77097-226">ICE49</span><span class="sxs-lookup"><span data-stu-id="77097-226">ICE49</span></span>](ice49.md)  
[<span data-ttu-id="77097-227">ICE53</span><span class="sxs-lookup"><span data-stu-id="77097-227">ICE53</span></span>](ice53.md)  
[<span data-ttu-id="77097-228">ICE55</span><span class="sxs-lookup"><span data-stu-id="77097-228">ICE55</span></span>](ice55.md)  
[<span data-ttu-id="77097-229">ICE57</span><span class="sxs-lookup"><span data-stu-id="77097-229">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="77097-230">ICE70</span><span class="sxs-lookup"><span data-stu-id="77097-230">ICE70</span></span>](ice70.md)  
[<span data-ttu-id="77097-231">ICE80</span><span class="sxs-lookup"><span data-stu-id="77097-231">ICE80</span></span>](ice80.md)  
</dl>

 

 





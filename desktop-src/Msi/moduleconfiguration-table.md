---
description: La tabla ModuleConfiguration identifica los atributos configurables del módulo. Esta tabla no se combina en la base de datos.
ms.assetid: 3b77cc23-c104-4adc-868c-3aa2b5794bc7
title: Tabla ModuleConfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa187c10b5d3376a9bec78eb897b4982445ff01f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277372"
---
# <a name="moduleconfiguration-table"></a><span data-ttu-id="aa87a-104">Tabla ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa87a-104">ModuleConfiguration Table</span></span>

<span data-ttu-id="aa87a-105">La tabla ModuleConfiguration identifica los atributos configurables del módulo.</span><span class="sxs-lookup"><span data-stu-id="aa87a-105">The ModuleConfiguration table identifies the configurable attributes of the module.</span></span> <span data-ttu-id="aa87a-106">Esta tabla no se combina en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="aa87a-106">This table is not merged into the database.</span></span>

<span data-ttu-id="aa87a-107">La tabla ModuleConfiguration tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="aa87a-107">The ModuleConfiguration table has the following columns.</span></span>



| <span data-ttu-id="aa87a-108">Columna</span><span class="sxs-lookup"><span data-stu-id="aa87a-108">Column</span></span>       | <span data-ttu-id="aa87a-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa87a-109">Type</span></span>                         | <span data-ttu-id="aa87a-110">Clave</span><span class="sxs-lookup"><span data-stu-id="aa87a-110">Key</span></span> | <span data-ttu-id="aa87a-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="aa87a-111">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="aa87a-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="aa87a-112">Name</span></span>         | [<span data-ttu-id="aa87a-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="aa87a-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="aa87a-114">Y</span><span class="sxs-lookup"><span data-stu-id="aa87a-114">Y</span></span>   | <span data-ttu-id="aa87a-115">N</span><span class="sxs-lookup"><span data-stu-id="aa87a-115">N</span></span>        |
| <span data-ttu-id="aa87a-116">Formato</span><span class="sxs-lookup"><span data-stu-id="aa87a-116">Format</span></span>       | [<span data-ttu-id="aa87a-117">Entero</span><span class="sxs-lookup"><span data-stu-id="aa87a-117">Integer</span></span>](integer.md)       | <span data-ttu-id="aa87a-118">N</span><span class="sxs-lookup"><span data-stu-id="aa87a-118">N</span></span>   | <span data-ttu-id="aa87a-119">N</span><span class="sxs-lookup"><span data-stu-id="aa87a-119">N</span></span>        |
| <span data-ttu-id="aa87a-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa87a-120">Type</span></span>         | [<span data-ttu-id="aa87a-121">Texto</span><span class="sxs-lookup"><span data-stu-id="aa87a-121">Text</span></span>](text.md)             | <span data-ttu-id="aa87a-122">N</span><span class="sxs-lookup"><span data-stu-id="aa87a-122">N</span></span>   | <span data-ttu-id="aa87a-123">Y</span><span class="sxs-lookup"><span data-stu-id="aa87a-123">Y</span></span>        |
| <span data-ttu-id="aa87a-124">ContextData</span><span class="sxs-lookup"><span data-stu-id="aa87a-124">ContextData</span></span>  | [<span data-ttu-id="aa87a-125">Texto</span><span class="sxs-lookup"><span data-stu-id="aa87a-125">Text</span></span>](text.md)             | <span data-ttu-id="aa87a-126">N</span><span class="sxs-lookup"><span data-stu-id="aa87a-126">N</span></span>   | <span data-ttu-id="aa87a-127">Y</span><span class="sxs-lookup"><span data-stu-id="aa87a-127">Y</span></span>        |
| <span data-ttu-id="aa87a-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="aa87a-128">DefaultValue</span></span> | [<span data-ttu-id="aa87a-129">Texto</span><span class="sxs-lookup"><span data-stu-id="aa87a-129">Text</span></span>](text.md)             | <span data-ttu-id="aa87a-130">N</span><span class="sxs-lookup"><span data-stu-id="aa87a-130">N</span></span>   | <span data-ttu-id="aa87a-131">Y</span><span class="sxs-lookup"><span data-stu-id="aa87a-131">Y</span></span>        |
| <span data-ttu-id="aa87a-132">Atributos</span><span class="sxs-lookup"><span data-stu-id="aa87a-132">Attributes</span></span>   | [<span data-ttu-id="aa87a-133">Entero</span><span class="sxs-lookup"><span data-stu-id="aa87a-133">Integer</span></span>](integer.md)       | <span data-ttu-id="aa87a-134">N</span><span class="sxs-lookup"><span data-stu-id="aa87a-134">N</span></span>   | <span data-ttu-id="aa87a-135">Y</span><span class="sxs-lookup"><span data-stu-id="aa87a-135">Y</span></span>        |
| <span data-ttu-id="aa87a-136">DisplayName</span><span class="sxs-lookup"><span data-stu-id="aa87a-136">DisplayName</span></span>  | [<span data-ttu-id="aa87a-137">Texto</span><span class="sxs-lookup"><span data-stu-id="aa87a-137">Text</span></span>](text.md)             | <span data-ttu-id="aa87a-138">N</span><span class="sxs-lookup"><span data-stu-id="aa87a-138">N</span></span>   | <span data-ttu-id="aa87a-139">Y</span><span class="sxs-lookup"><span data-stu-id="aa87a-139">Y</span></span>        |
| <span data-ttu-id="aa87a-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa87a-140">Description</span></span>  | [<span data-ttu-id="aa87a-141">Texto</span><span class="sxs-lookup"><span data-stu-id="aa87a-141">Text</span></span>](text.md)             | <span data-ttu-id="aa87a-142">N</span><span class="sxs-lookup"><span data-stu-id="aa87a-142">N</span></span>   | <span data-ttu-id="aa87a-143">Y</span><span class="sxs-lookup"><span data-stu-id="aa87a-143">Y</span></span>        |
| <span data-ttu-id="aa87a-144">HelpLocation</span><span class="sxs-lookup"><span data-stu-id="aa87a-144">HelpLocation</span></span> | [<span data-ttu-id="aa87a-145">Texto</span><span class="sxs-lookup"><span data-stu-id="aa87a-145">Text</span></span>](text.md)             | <span data-ttu-id="aa87a-146">N</span><span class="sxs-lookup"><span data-stu-id="aa87a-146">N</span></span>   | <span data-ttu-id="aa87a-147">Y</span><span class="sxs-lookup"><span data-stu-id="aa87a-147">Y</span></span>        |
| <span data-ttu-id="aa87a-148">HelpKeyword</span><span class="sxs-lookup"><span data-stu-id="aa87a-148">HelpKeyword</span></span>  | [<span data-ttu-id="aa87a-149">Texto</span><span class="sxs-lookup"><span data-stu-id="aa87a-149">Text</span></span>](text.md)             | <span data-ttu-id="aa87a-150">N</span><span class="sxs-lookup"><span data-stu-id="aa87a-150">N</span></span>   | <span data-ttu-id="aa87a-151">Y</span><span class="sxs-lookup"><span data-stu-id="aa87a-151">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="aa87a-152">Columnas</span><span class="sxs-lookup"><span data-stu-id="aa87a-152">Columns</span></span>

<dl> <dt>

<span data-ttu-id="aa87a-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="aa87a-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="aa87a-154">Este campo define el nombre del elemento configurable.</span><span class="sxs-lookup"><span data-stu-id="aa87a-154">This field defines the name of the configurable item.</span></span> <span data-ttu-id="aa87a-155">Se hace referencia a este nombre en la plantilla de formato en la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="aa87a-155">This name is referenced in the formatting template in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa87a-156"><span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Aplique</span><span class="sxs-lookup"><span data-stu-id="aa87a-156"><span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Format</span></span>
</dt> <dd>

<span data-ttu-id="aa87a-157">Esta columna especifica el formato de los datos que se van a cambiar.</span><span class="sxs-lookup"><span data-stu-id="aa87a-157">This column specifies the format of the data being changed.</span></span>



| <span data-ttu-id="aa87a-158">Formato</span><span class="sxs-lookup"><span data-stu-id="aa87a-158">Format</span></span>                                       | <span data-ttu-id="aa87a-159">Value</span><span class="sxs-lookup"><span data-stu-id="aa87a-159">Value</span></span> |
|----------------------------------------------|-------|
| [<span data-ttu-id="aa87a-160">Texto</span><span class="sxs-lookup"><span data-stu-id="aa87a-160">Text</span></span>](text-format-types.md)                | <span data-ttu-id="aa87a-161">0</span><span class="sxs-lookup"><span data-stu-id="aa87a-161">0</span></span>     |
| [<span data-ttu-id="aa87a-162">Clave</span><span class="sxs-lookup"><span data-stu-id="aa87a-162">Key</span></span>](key-format-types.md)                  | <span data-ttu-id="aa87a-163">1</span><span class="sxs-lookup"><span data-stu-id="aa87a-163">1</span></span>     |
| [<span data-ttu-id="aa87a-164">Entero</span><span class="sxs-lookup"><span data-stu-id="aa87a-164">Integer</span></span>](integer-format-types.md)          | <span data-ttu-id="aa87a-165">2</span><span class="sxs-lookup"><span data-stu-id="aa87a-165">2</span></span>     |
| [<span data-ttu-id="aa87a-166">Formato de campo de bits</span><span class="sxs-lookup"><span data-stu-id="aa87a-166">Bitfield Format</span></span>](bitfield-format-types.md) | <span data-ttu-id="aa87a-167">3</span><span class="sxs-lookup"><span data-stu-id="aa87a-167">3</span></span>     |



 

</dd> <dt>

<span data-ttu-id="aa87a-168"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Automáticamente</span><span class="sxs-lookup"><span data-stu-id="aa87a-168"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="aa87a-169">Esta columna especifica el tipo de los datos que se van a cambiar.</span><span class="sxs-lookup"><span data-stu-id="aa87a-169">This column specifies the type for the data being changed.</span></span> <span data-ttu-id="aa87a-170">Este tipo se utiliza para proporcionar un contexto para cualquier interfaz de usuario y no se utiliza en el proceso de mezcla.</span><span class="sxs-lookup"><span data-stu-id="aa87a-170">This type is used to provide a context for any user-interface and is not used in the merge process.</span></span> <span data-ttu-id="aa87a-171">Los valores válidos para esta columna dependen del valor de la columna formato.</span><span class="sxs-lookup"><span data-stu-id="aa87a-171">The valid values for this column depend on the value in the Format column.</span></span>

</dd> <dt>

<span data-ttu-id="aa87a-172"><span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData</span><span class="sxs-lookup"><span data-stu-id="aa87a-172"><span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData</span></span>
</dt> <dd>

<span data-ttu-id="aa87a-173">Esta columna especifica un contexto semántico para los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="aa87a-173">This column specifies a semantic context for the requested data.</span></span> <span data-ttu-id="aa87a-174">El tipo se utiliza para proporcionar un contexto para cualquier interfaz de usuario y no se utiliza en el proceso de mezcla.</span><span class="sxs-lookup"><span data-stu-id="aa87a-174">The type is used to provide a context for any user-interface and is not used in the merge process.</span></span> <span data-ttu-id="aa87a-175">Los valores válidos para esta columna dependen de los valores de las columnas Format y Type.</span><span class="sxs-lookup"><span data-stu-id="aa87a-175">The valid values for this column depend on the values in the Format and Type columns.</span></span>

</dd> <dt>

<span data-ttu-id="aa87a-176"><span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>DefaultValue</span><span class="sxs-lookup"><span data-stu-id="aa87a-176"><span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>DefaultValue</span></span>
</dt> <dd>

<span data-ttu-id="aa87a-177">Esta columna especifica un valor predeterminado para el elemento en este registro si la herramienta de combinación declina proporcionar un valor.</span><span class="sxs-lookup"><span data-stu-id="aa87a-177">This column specifies a default value for the item in this record if the merge tool declines to provide a value.</span></span> <span data-ttu-id="aa87a-178">Este valor debe tener el formato, el tipo y el contexto del elemento.</span><span class="sxs-lookup"><span data-stu-id="aa87a-178">This value must have the format, type, and context of the item.</span></span> <span data-ttu-id="aa87a-179">Si se trata de un elemento de formato de "clave", la clave externa debe ser una clave válida en las tablas del módulo.</span><span class="sxs-lookup"><span data-stu-id="aa87a-179">If this is a "Key" format item, the foreign key must be a valid key into the tables of the module.</span></span> <span data-ttu-id="aa87a-180">Null puede ser un valor válido para esta columna en función del elemento.</span><span class="sxs-lookup"><span data-stu-id="aa87a-180">Null may be a valid value for this column depending on the item.</span></span> <span data-ttu-id="aa87a-181">En el caso de los elementos de formato "Key", este valor se encuentra en [formato especial de CMsM](cmsm-special-format.md).</span><span class="sxs-lookup"><span data-stu-id="aa87a-181">For "Key" format items, this value is in [CMSM special format](cmsm-special-format.md).</span></span> <span data-ttu-id="aa87a-182">En el caso de todos los demás tipos, el valor se trata literalmente.</span><span class="sxs-lookup"><span data-stu-id="aa87a-182">For all other types, the value is treated literally.</span></span>

<span data-ttu-id="aa87a-183">Los autores de módulos deben asegurarse de que el módulo es válido en su estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="aa87a-183">Module authors must ensure that the module is valid in its default state.</span></span> <span data-ttu-id="aa87a-184">Esto garantiza que las versiones de Mergemod.dll anteriores a la versión 2,0 pueden seguir usando el módulo en su estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="aa87a-184">This ensures that versions of Mergemod.dll earlier than version 2.0 can still use the module in its default state.</span></span>

</dd> <dt>

<span data-ttu-id="aa87a-185"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Sus</span><span class="sxs-lookup"><span data-stu-id="aa87a-185"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="aa87a-186">Esta columna es un campo de bits que contiene los atributos de este elemento configurable.</span><span class="sxs-lookup"><span data-stu-id="aa87a-186">This column is a bit field containing attributes for this configurable item.</span></span> <span data-ttu-id="aa87a-187">NULL es equivalente a 0.</span><span class="sxs-lookup"><span data-stu-id="aa87a-187">Null is equivalent to 0.</span></span> <span data-ttu-id="aa87a-188">Todos los demás bits de esta columna se reservan para uso futuro y deben ser 0.</span><span class="sxs-lookup"><span data-stu-id="aa87a-188">All other bits in this column are reserved for future use and must be 0.</span></span>



| <span data-ttu-id="aa87a-189">Nombre</span><span class="sxs-lookup"><span data-stu-id="aa87a-189">Name</span></span>                             | <span data-ttu-id="aa87a-190">Decimal</span><span class="sxs-lookup"><span data-stu-id="aa87a-190">Decimal</span></span> | <span data-ttu-id="aa87a-191">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="aa87a-191">Hexadecimal</span></span> | <span data-ttu-id="aa87a-192">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa87a-192">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------|---------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa87a-193">msmConfigurableOptionKeyNoOrphan</span><span class="sxs-lookup"><span data-stu-id="aa87a-193">msmConfigurableOptionKeyNoOrphan</span></span> | <span data-ttu-id="aa87a-194">1</span><span class="sxs-lookup"><span data-stu-id="aa87a-194">1</span></span>       | <span data-ttu-id="aa87a-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="aa87a-195">0x00000001</span></span>  | <span data-ttu-id="aa87a-196">Este atributo solo se aplica a los registros que enumeran una clave externa en una tabla de módulos en su campo DefaultValue.</span><span class="sxs-lookup"><span data-stu-id="aa87a-196">This attribute only applies to records that list a foreign key to a module table in their DefaultValue field.</span></span> <span data-ttu-id="aa87a-197">La herramienta de combinación omite el atributo para los formatos distintos de los [tipos de formato de clave](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="aa87a-197">The merge tool ignores the attribute for any formats other than the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="aa87a-198">Los elementos que no aparecen en la [tabla ModuleSubstitution](modulesubstitution-table.md) se excluyen de la siguiente comprobación.</span><span class="sxs-lookup"><span data-stu-id="aa87a-198">Items not listed in the [ModuleSubstitution table](modulesubstitution-table.md) are excluded from the following check.</span></span> <span data-ttu-id="aa87a-199">La herramienta de combinación no combina la fila a la que hace referencia la columna DefaultValue en la base de datos de destino si se cumplen las siguientes condiciones después de completar todas las opciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="aa87a-199">The merge tool does not merge the row referenced by the DefaultValue column into the target database if the following conditions are satisfied after completing all configuration options.</span></span><br/> <span data-ttu-id="aa87a-200">Cada fila de la tabla ModuleConfiguration con el mismo DefaultValue tiene el valor de msmConfigurationItemsKeyNoOrphan establecido.</span><span class="sxs-lookup"><span data-stu-id="aa87a-200">Every row in the ModuleConfiguration table with the same DefaultValue has the msmConfigurationItemsKeyNoOrphan set.</span></span><br/> <span data-ttu-id="aa87a-201">Ninguna fila usa DefaultValue porque la herramienta de creación rechazó proporcionar un valor.</span><span class="sxs-lookup"><span data-stu-id="aa87a-201">No rows use the DefaultValue because the authoring tool declined to provide a value.</span></span><br/> <span data-ttu-id="aa87a-202">La herramienta de combinación combina la fila si se cumple alguna de las condiciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="aa87a-202">The merge tool merges the row if any of the following conditions are satisfied.</span></span><br/> <span data-ttu-id="aa87a-203">La herramienta de combinación encuentra cualquier fila que no tenga establecido msmConfigItemsKeyNoOrphan.</span><span class="sxs-lookup"><span data-stu-id="aa87a-203">The merge tool finds any row that does not have msmConfigItemsKeyNoOrphan set.</span></span><br/> <span data-ttu-id="aa87a-204">Si la herramienta de combinación encuentra una fila mediante DefaultValue porque la herramienta de creación rechazó proporcionar un valor.</span><span class="sxs-lookup"><span data-stu-id="aa87a-204">If the merge tool finds any row using DefaultValue because the authoring tool declined to provide a value.</span></span><br/> |
| <span data-ttu-id="aa87a-205">msmConfigurableOptionNonNullable</span><span class="sxs-lookup"><span data-stu-id="aa87a-205">msmConfigurableOptionNonNullable</span></span> | <span data-ttu-id="aa87a-206">2</span><span class="sxs-lookup"><span data-stu-id="aa87a-206">2</span></span>       | <span data-ttu-id="aa87a-207">0x00000002</span><span class="sxs-lookup"><span data-stu-id="aa87a-207">0x00000002</span></span>  | <span data-ttu-id="aa87a-208">Cuando se establece este atributo, NULL no es una respuesta válida para este elemento.</span><span class="sxs-lookup"><span data-stu-id="aa87a-208">When this attribute is set, null is not a valid response for this item.</span></span> <span data-ttu-id="aa87a-209">Este atributo no tiene ningún efecto en los [tipos de formato de entero](integer-format-types.md) o los tipos de formato de campo de [bits](bitfield-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="aa87a-209">This attribute has no effect for [Integer Format Types](integer-format-types.md) or [Bitfield Format Types](bitfield-format-types.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="aa87a-210"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>Mostrar</span><span class="sxs-lookup"><span data-stu-id="aa87a-210"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span></span>
</dt> <dd>

<span data-ttu-id="aa87a-211">Esta columna proporciona una breve descripción de este elemento que la herramienta de creación puede utilizar en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="aa87a-211">This column provides a short description of this item that the authoring tool may use in the user interface.</span></span> <span data-ttu-id="aa87a-212">Es posible que esta columna no esté localizada.</span><span class="sxs-lookup"><span data-stu-id="aa87a-212">This column may not be localized.</span></span> <span data-ttu-id="aa87a-213">Establezca esta columna en null para que el módulo solicite a la herramienta de creación que no exponga esta propiedad en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="aa87a-213">Set this column to null to have the module is request that the authoring tool not expose this property in the UI.</span></span> <span data-ttu-id="aa87a-214">La herramienta puede pasar por alto el valor de este campo.</span><span class="sxs-lookup"><span data-stu-id="aa87a-214">The tool may disregard the value in this field.</span></span>

</dd> <dt>

<span data-ttu-id="aa87a-215"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="aa87a-215"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="aa87a-216">Esta columna proporciona una descripción de este elemento que la herramienta de creación puede utilizar en los elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="aa87a-216">This column provides a description of this item that the authoring tool may use in UI elements.</span></span> <span data-ttu-id="aa87a-217">Esta cadena se puede localizar mediante la transformación de idioma del módulo.</span><span class="sxs-lookup"><span data-stu-id="aa87a-217">This string may be localized by the module's language transform.</span></span> <span data-ttu-id="aa87a-218">Esta columna puede ser null.</span><span class="sxs-lookup"><span data-stu-id="aa87a-218">This column may be null.</span></span>

</dd> <dt>

<span data-ttu-id="aa87a-219"><span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation</span><span class="sxs-lookup"><span data-stu-id="aa87a-219"><span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation</span></span>
</dt> <dd>

<span data-ttu-id="aa87a-220">Esta columna proporciona el nombre de un archivo de ayuda (sin la extensión. chm) o una lista de espacios de nombres de ayuda delimitados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="aa87a-220">This column provides either the name of a help file (without the .chm extension) or a semicolon delimited list of help namespaces.</span></span> <span data-ttu-id="aa87a-221">Esta columna puede ser null si no hay ayuda disponible.</span><span class="sxs-lookup"><span data-stu-id="aa87a-221">This column can be null if no help is available.</span></span> <span data-ttu-id="aa87a-222">Esta columna solo puede ser null si la columna HelpKeyword es NULL.</span><span class="sxs-lookup"><span data-stu-id="aa87a-222">This column can be null only if the HelpKeyword column is null.</span></span>

</dd> <dt>

<span data-ttu-id="aa87a-223"><span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword</span><span class="sxs-lookup"><span data-stu-id="aa87a-223"><span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword</span></span>
</dt> <dd>

<span data-ttu-id="aa87a-224">Esta columna proporciona una palabra clave en el archivo de ayuda o espacio de nombres de la columna HelpLocation.</span><span class="sxs-lookup"><span data-stu-id="aa87a-224">This column provides a keyword into the help file or namespace from the HelpLocation column.</span></span> <span data-ttu-id="aa87a-225">La interpretación de esta palabra clave depende de la columna HelpLocation.</span><span class="sxs-lookup"><span data-stu-id="aa87a-225">The interpretation of this keyword depends on the HelpLocation column.</span></span> <span data-ttu-id="aa87a-226">Esta columna puede ser null.</span><span class="sxs-lookup"><span data-stu-id="aa87a-226">This column may be null.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa87a-227">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa87a-227">Remarks</span></span>

<span data-ttu-id="aa87a-228">Los [módulos de combinación configurables](configurable-merge-modules.md)usan la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="aa87a-228">The ModuleConfiguration table is used by [Configurable Merge Modules](configurable-merge-modules.md).</span></span> <span data-ttu-id="aa87a-229">Se requiere Mergemod.dll 2,0 o una versión posterior para crear un módulo de combinación configurable.</span><span class="sxs-lookup"><span data-stu-id="aa87a-229">Mergemod.dll 2.0 or later is required to create a configurable merge module.</span></span>

<span data-ttu-id="aa87a-230">Para garantizar la compatibilidad con versiones anteriores de Mergemod.dll, la tabla ModuleConfiguration y la [tabla ModuleSubstitution](modulesubstitution-table.md) se deben agregar a la [tabla ModuleIgnoreTable](moduleignoretable-table.md) de cada módulo.</span><span class="sxs-lookup"><span data-stu-id="aa87a-230">To ensure compatibility with older versions of Mergemod.dll, the ModuleConfiguration table and [ModuleSubstitution table](modulesubstitution-table.md) should be added to the [ModuleIgnoreTable table](moduleignoretable-table.md) of every module.</span></span>

## <a name="validation"></a><span data-ttu-id="aa87a-231">Validación</span><span class="sxs-lookup"><span data-stu-id="aa87a-231">Validation</span></span>

<dl>

[<span data-ttu-id="aa87a-232">ICE03</span><span class="sxs-lookup"><span data-stu-id="aa87a-232">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="aa87a-233">ICE06</span><span class="sxs-lookup"><span data-stu-id="aa87a-233">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="aa87a-234">ICE25</span><span class="sxs-lookup"><span data-stu-id="aa87a-234">ICE25</span></span>](ice25.md)  
[<span data-ttu-id="aa87a-235">ICE45</span><span class="sxs-lookup"><span data-stu-id="aa87a-235">ICE45</span></span>](ice45.md)  
</dl>

 

 





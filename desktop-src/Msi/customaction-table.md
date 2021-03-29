---
description: La tabla CustomAction proporciona los medios para integrar el código personalizado y los datos en la instalación de. El origen del código que se ejecuta puede ser una secuencia contenida en la base de datos, un archivo instalado recientemente o un archivo ejecutable existente.
ms.assetid: 0f47abc1-4e06-4ddc-9ea1-9afb9f27d499
title: Tabla CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c8cbfa6500743e2a2ad89627447da1907f6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810393"
---
# <a name="customaction-table"></a><span data-ttu-id="24aee-104">Tabla CustomAction</span><span class="sxs-lookup"><span data-stu-id="24aee-104">CustomAction Table</span></span>

<span data-ttu-id="24aee-105">La tabla CustomAction proporciona los medios para integrar el código personalizado y los datos en la instalación de.</span><span class="sxs-lookup"><span data-stu-id="24aee-105">The CustomAction table provides the means of integrating custom code and data into the installation.</span></span> <span data-ttu-id="24aee-106">El origen del código que se ejecuta puede ser una secuencia contenida en la base de datos, un archivo instalado recientemente o un archivo ejecutable existente.</span><span class="sxs-lookup"><span data-stu-id="24aee-106">The source of the code that is executed can be a stream contained within the database, a recently installed file, or an existing executable file.</span></span>

<span data-ttu-id="24aee-107">La tabla CustomAction tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="24aee-107">The CustomAction table has the following columns.</span></span>



| <span data-ttu-id="24aee-108">Columna</span><span class="sxs-lookup"><span data-stu-id="24aee-108">Column</span></span>       | <span data-ttu-id="24aee-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="24aee-109">Type</span></span>                               | <span data-ttu-id="24aee-110">Clave</span><span class="sxs-lookup"><span data-stu-id="24aee-110">Key</span></span> | <span data-ttu-id="24aee-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="24aee-111">Nullable</span></span> |
|--------------|------------------------------------|-----|----------|
| <span data-ttu-id="24aee-112">Acción</span><span class="sxs-lookup"><span data-stu-id="24aee-112">Action</span></span>       | [<span data-ttu-id="24aee-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="24aee-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="24aee-114">Y</span><span class="sxs-lookup"><span data-stu-id="24aee-114">Y</span></span>   | <span data-ttu-id="24aee-115">N</span><span class="sxs-lookup"><span data-stu-id="24aee-115">N</span></span>        |
| <span data-ttu-id="24aee-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="24aee-116">Type</span></span>         | [<span data-ttu-id="24aee-117">Entero</span><span class="sxs-lookup"><span data-stu-id="24aee-117">Integer</span></span>](integer.md)             | <span data-ttu-id="24aee-118">N</span><span class="sxs-lookup"><span data-stu-id="24aee-118">N</span></span>   | <span data-ttu-id="24aee-119">N</span><span class="sxs-lookup"><span data-stu-id="24aee-119">N</span></span>        |
| <span data-ttu-id="24aee-120">Source</span><span class="sxs-lookup"><span data-stu-id="24aee-120">Source</span></span>       | [<span data-ttu-id="24aee-121">CustomSource</span><span class="sxs-lookup"><span data-stu-id="24aee-121">CustomSource</span></span>](customsource.md)   | <span data-ttu-id="24aee-122">N</span><span class="sxs-lookup"><span data-stu-id="24aee-122">N</span></span>   | <span data-ttu-id="24aee-123">Y</span><span class="sxs-lookup"><span data-stu-id="24aee-123">Y</span></span>        |
| <span data-ttu-id="24aee-124">Destino</span><span class="sxs-lookup"><span data-stu-id="24aee-124">Target</span></span>       | [<span data-ttu-id="24aee-125">Formatea</span><span class="sxs-lookup"><span data-stu-id="24aee-125">Formatted</span></span>](formatted.md)         | <span data-ttu-id="24aee-126">N</span><span class="sxs-lookup"><span data-stu-id="24aee-126">N</span></span>   | <span data-ttu-id="24aee-127">Y</span><span class="sxs-lookup"><span data-stu-id="24aee-127">Y</span></span>        |
| <span data-ttu-id="24aee-128">ExtendedType</span><span class="sxs-lookup"><span data-stu-id="24aee-128">ExtendedType</span></span> | [<span data-ttu-id="24aee-129">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="24aee-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="24aee-130">N</span><span class="sxs-lookup"><span data-stu-id="24aee-130">N</span></span>   | <span data-ttu-id="24aee-131">Y</span><span class="sxs-lookup"><span data-stu-id="24aee-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="24aee-132">Columnas</span><span class="sxs-lookup"><span data-stu-id="24aee-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="24aee-133"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar</span><span class="sxs-lookup"><span data-stu-id="24aee-133"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="24aee-134">Nombre de la acción.</span><span class="sxs-lookup"><span data-stu-id="24aee-134">Name of the action.</span></span> <span data-ttu-id="24aee-135">La acción normalmente aparece en una tabla de secuencia a menos que otra acción personalizada la llame.</span><span class="sxs-lookup"><span data-stu-id="24aee-135">The action normally appears in a sequence table unless it is called by another custom action.</span></span> <span data-ttu-id="24aee-136">Si el nombre coincide con cualquier acción integrada, nunca se llama a la acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="24aee-136">If the name matches any built-in action, then the custom action is never called.</span></span>

<span data-ttu-id="24aee-137">Clave de la tabla principal.</span><span class="sxs-lookup"><span data-stu-id="24aee-137">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="24aee-138"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Automáticamente</span><span class="sxs-lookup"><span data-stu-id="24aee-138"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="24aee-139">Campo de bits de marca que especifica el tipo básico de acción y opciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="24aee-139">A field of flag bits specifying the basic type of custom action and options.</span></span> <span data-ttu-id="24aee-140">Vea [lista de Resumen de todos los tipos de acción personalizados](summary-list-of-all-custom-action-types.md) para obtener una lista de los tipos básicos.</span><span class="sxs-lookup"><span data-stu-id="24aee-140">See [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a list of the basic types.</span></span> <span data-ttu-id="24aee-141">Vea [Opciones de procesamiento de devolución](custom-action-return-processing-options.md)de acción personalizada, [Opciones de programación](custom-action-execution-scheduling-options.md)de la ejecución de acciones personalizadas, [opción de destino oculto de acción personalizada](custom-action-hidden-target-option.md)y opciones de ejecución de la [acción personalizada In-Script](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="24aee-141">See [Custom Action Return Processing Options](custom-action-return-processing-options.md), [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md), [Custom Action Hidden Target Option](custom-action-hidden-target-option.md), and [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

</dd> <dt>

<span data-ttu-id="24aee-142"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Fuentes</span><span class="sxs-lookup"><span data-stu-id="24aee-142"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Source</span></span>
</dt> <dd>

<span data-ttu-id="24aee-143">Un nombre de propiedad o una clave externa en otra tabla.</span><span class="sxs-lookup"><span data-stu-id="24aee-143">A property name or external key into another table.</span></span> <span data-ttu-id="24aee-144">Para obtener una explicación de los posibles orígenes de acciones personalizadas, vea [Custom Action sources](custom-action-sources.md) y la [lista de Resumen de todos los tipos de acción personalizados](summary-list-of-all-custom-action-types.md).</span><span class="sxs-lookup"><span data-stu-id="24aee-144">For a discussion of the possible custom action sources, see [Custom Action Sources](custom-action-sources.md) and the [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md).</span></span> <span data-ttu-id="24aee-145">Por ejemplo, la columna de origen puede contener una clave externa en la primera columna de una de las tablas siguientes que contengan el origen del código de acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="24aee-145">For example, the Source column may contain an external key into the first column of one of the following tables containing the source of the custom action code.</span></span>

<span data-ttu-id="24aee-146">[Tabla del directorio](directory-table.md) para llamar a ejecutables existentes.</span><span class="sxs-lookup"><span data-stu-id="24aee-146">[Directory table](directory-table.md) for calling existing executables.</span></span>

<span data-ttu-id="24aee-147">[Tabla de archivos](file-table.md) para llamar a archivos ejecutables y dll que se acaban de instalar.</span><span class="sxs-lookup"><span data-stu-id="24aee-147">[File table](file-table.md) for calling executables and DLLs that have just been installed.</span></span>

<span data-ttu-id="24aee-148">[Tabla binaria](binary-table.md) para llamar a ejecutables, archivos dll y datos almacenados en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="24aee-148">[Binary table](binary-table.md) for calling executables, DLLs, and data stored in the database.</span></span>

<span data-ttu-id="24aee-149">[Tabla de propiedades](property-table.md) para llamar a ejecutables cuyas rutas de acceso están retenidas por una propiedad.</span><span class="sxs-lookup"><span data-stu-id="24aee-149">[Property table](property-table.md) for calling executables whose paths are held by a property.</span></span>

</dd> <dt>

<span data-ttu-id="24aee-150"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Dirigir</span><span class="sxs-lookup"><span data-stu-id="24aee-150"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="24aee-151">Parámetro de ejecución que depende del tipo básico de acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="24aee-151">An execution parameter that depends on the basic type of custom action.</span></span> <span data-ttu-id="24aee-152">Consulte la [lista de Resumen de todos los tipos de acciones personalizadas](summary-list-of-all-custom-action-types.md) para obtener una descripción de lo que se debe escribir en este campo para cada tipo de acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="24aee-152">See the [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a description of what should be entered in this field for each type of custom action.</span></span> <span data-ttu-id="24aee-153">Por ejemplo, este campo puede contener lo siguiente en función de la acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="24aee-153">For example, this field may contain the following depending on the custom action.</span></span>



| <span data-ttu-id="24aee-154">Destino</span><span class="sxs-lookup"><span data-stu-id="24aee-154">Target</span></span>                                    | <span data-ttu-id="24aee-155">Acción personalizada</span><span class="sxs-lookup"><span data-stu-id="24aee-155">Custom action</span></span>                         |
|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="24aee-156">Punto de entrada (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="24aee-156">Entry point (required)</span></span>                    | <span data-ttu-id="24aee-157">Llamar a un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="24aee-157">Calling a DLL.</span></span>                        |
| <span data-ttu-id="24aee-158">Nombre del archivo ejecutable con argumentos (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="24aee-158">Executable name with arguments (required)</span></span> | <span data-ttu-id="24aee-159">Llamar a un ejecutable existente.</span><span class="sxs-lookup"><span data-stu-id="24aee-159">Calling an existing executable.</span></span>       |
| <span data-ttu-id="24aee-160">Argumentos de la línea de comandos (opcional)</span><span class="sxs-lookup"><span data-stu-id="24aee-160">Command line arguments (optional)</span></span>         | <span data-ttu-id="24aee-161">Llamar a un archivo ejecutable recién instalado.</span><span class="sxs-lookup"><span data-stu-id="24aee-161">Calling an executable just installed.</span></span> |
| <span data-ttu-id="24aee-162">Nombre de archivo de destino (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="24aee-162">Target file name (required)</span></span>               | <span data-ttu-id="24aee-163">Crear un archivo a partir de datos personalizados.</span><span class="sxs-lookup"><span data-stu-id="24aee-163">Creating a file from custom data.</span></span>     |
| <span data-ttu-id="24aee-164">Null</span><span class="sxs-lookup"><span data-stu-id="24aee-164">Null</span></span>                                      | <span data-ttu-id="24aee-165">Ejecutar código de script.</span><span class="sxs-lookup"><span data-stu-id="24aee-165">Executing script code.</span></span>                |



 

</dd> <dt>

<span data-ttu-id="24aee-166"><span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType</span><span class="sxs-lookup"><span data-stu-id="24aee-166"><span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType</span></span>
</dt> <dd>

<span data-ttu-id="24aee-167">Escriba el valor de **msidbCustomActionTypePatchUninstall** en este campo para especificar una acción personalizada con la [opción de desinstalación de revisión de acción personalizada](custom-action-patch-uninstall-option.md).</span><span class="sxs-lookup"><span data-stu-id="24aee-167">Enter the **msidbCustomActionTypePatchUninstall** value in this field to specify a custom action with the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md).</span></span>

<span data-ttu-id="24aee-168">**[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="24aee-168">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="24aee-169">Esta opción está disponible a partir de Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="24aee-169">This option is available beginning with Windows Installer 4.5.</span></span>

</dd> </dl>

<span data-ttu-id="24aee-170">Para obtener más información, vea todos los temas de [acciones personalizadas](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="24aee-170">For more information, see all the topics under [Custom Actions](custom-actions.md).</span></span>

## <a name="validation"></a><span data-ttu-id="24aee-171">Validación</span><span class="sxs-lookup"><span data-stu-id="24aee-171">Validation</span></span>

<dl>

[<span data-ttu-id="24aee-172">ICE03</span><span class="sxs-lookup"><span data-stu-id="24aee-172">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="24aee-173">ICE06</span><span class="sxs-lookup"><span data-stu-id="24aee-173">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="24aee-174">ICE12</span><span class="sxs-lookup"><span data-stu-id="24aee-174">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="24aee-175">ICE27</span><span class="sxs-lookup"><span data-stu-id="24aee-175">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="24aee-176">ICE46</span><span class="sxs-lookup"><span data-stu-id="24aee-176">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="24aee-177">ICE63</span><span class="sxs-lookup"><span data-stu-id="24aee-177">ICE63</span></span>](ice63.md)  
[<span data-ttu-id="24aee-178">ICE68</span><span class="sxs-lookup"><span data-stu-id="24aee-178">ICE68</span></span>](ice68.md)  
[<span data-ttu-id="24aee-179">ICE72</span><span class="sxs-lookup"><span data-stu-id="24aee-179">ICE72</span></span>](ice72.md)  
[<span data-ttu-id="24aee-180">ICE75</span><span class="sxs-lookup"><span data-stu-id="24aee-180">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="24aee-181">ICE77</span><span class="sxs-lookup"><span data-stu-id="24aee-181">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="24aee-182">ICE80</span><span class="sxs-lookup"><span data-stu-id="24aee-182">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="24aee-183">ICE88</span><span class="sxs-lookup"><span data-stu-id="24aee-183">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="24aee-184">ICE93</span><span class="sxs-lookup"><span data-stu-id="24aee-184">ICE93</span></span>](ice93.md)  
</dl>

 

 




---
description: La tabla MsiAssembly y la tabla MsiAssemblyName especifican Windows Installer valores para los ensamblados de Common Language Runtime y los ensamblados Win32.
ms.assetid: cfe9a0a3-e40f-4c59-b2e4-ad7654528e3b
title: Tabla MsiAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12008682c82d7be20ed8713d8dc1c416f9c7065c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669846"
---
# <a name="msiassemblyname-table"></a><span data-ttu-id="a504a-103">Tabla MsiAssemblyName</span><span class="sxs-lookup"><span data-stu-id="a504a-103">MsiAssemblyName Table</span></span>

<span data-ttu-id="a504a-104">La tabla [MsiAssembly](msiassembly-table.md) y la tabla MsiAssemblyName especifican Windows Installer valores para los ensamblados de Common Language Runtime y los ensamblados Win32.</span><span class="sxs-lookup"><span data-stu-id="a504a-104">The [MsiAssembly Table](msiassembly-table.md) and MsiAssemblyName Table specify Windows Installer settings for common language runtime assemblies and Win32 assemblies.</span></span> <span data-ttu-id="a504a-105">Para obtener más información, vea [Instalar ensamblados en la caché global de ensamblados](installation-of-assemblies-to-the-global-assembly-cache.md) e [Instalar ensamblados Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="a504a-105">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="a504a-106">La tabla MsiAssemblyName especifica el esquema de los elementos de un nombre de caché de ensamblados seguro para un ensamblado de .NET Framework o Win32.</span><span class="sxs-lookup"><span data-stu-id="a504a-106">The MsiAssemblyName Table specifies the schema for the elements of a strong assembly cache name for a .NET Framework or Win32 assembly.</span></span> <span data-ttu-id="a504a-107">El nombre se construye anexando todos los elementos con la misma clave de componente \_ .</span><span class="sxs-lookup"><span data-stu-id="a504a-107">The name is constructed by appending all elements with the same Component\_ key.</span></span> <span data-ttu-id="a504a-108">Consulte el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a504a-108">See the following example.</span></span>

<span data-ttu-id="a504a-109">Windows Installer puede instalar ensamblados Win32 como [ensamblados en paralelo](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="a504a-109">Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="a504a-110">Para obtener más información, consulte la [API de ensamblados en paralelo](../sbscs/side-by-side-assembly-api.md).</span><span class="sxs-lookup"><span data-stu-id="a504a-110">For more information, see the [Side-by-Side Assembly API](../sbscs/side-by-side-assembly-api.md).</span></span>

<span data-ttu-id="a504a-111">La tabla MsiAssemblyName tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="a504a-111">The MsiAssemblyName Table has the following columns.</span></span>



| <span data-ttu-id="a504a-112">Columna</span><span class="sxs-lookup"><span data-stu-id="a504a-112">Column</span></span>      | <span data-ttu-id="a504a-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="a504a-113">Type</span></span>                         | <span data-ttu-id="a504a-114">Clave</span><span class="sxs-lookup"><span data-stu-id="a504a-114">Key</span></span> | <span data-ttu-id="a504a-115">Nullable</span><span class="sxs-lookup"><span data-stu-id="a504a-115">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="a504a-116">Componente\_</span><span class="sxs-lookup"><span data-stu-id="a504a-116">Component\_</span></span> | [<span data-ttu-id="a504a-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="a504a-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="a504a-118">Y</span><span class="sxs-lookup"><span data-stu-id="a504a-118">Y</span></span>   | <span data-ttu-id="a504a-119">N</span><span class="sxs-lookup"><span data-stu-id="a504a-119">N</span></span>        |
| <span data-ttu-id="a504a-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="a504a-120">Name</span></span>        | [<span data-ttu-id="a504a-121">Texto</span><span class="sxs-lookup"><span data-stu-id="a504a-121">Text</span></span>](text.md)             | <span data-ttu-id="a504a-122">Y</span><span class="sxs-lookup"><span data-stu-id="a504a-122">Y</span></span>   | <span data-ttu-id="a504a-123">N</span><span class="sxs-lookup"><span data-stu-id="a504a-123">N</span></span>        |
| <span data-ttu-id="a504a-124">Value</span><span class="sxs-lookup"><span data-stu-id="a504a-124">Value</span></span>       | [<span data-ttu-id="a504a-125">Texto</span><span class="sxs-lookup"><span data-stu-id="a504a-125">Text</span></span>](text.md)             | <span data-ttu-id="a504a-126">N</span><span class="sxs-lookup"><span data-stu-id="a504a-126">N</span></span>   | <span data-ttu-id="a504a-127">N</span><span class="sxs-lookup"><span data-stu-id="a504a-127">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a504a-128">Columnas</span><span class="sxs-lookup"><span data-stu-id="a504a-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a504a-129"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="a504a-129"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="a504a-130">Clave en la [tabla de componentes](component-table.md) que especifica el componente de Windows Installer que contiene este ensamblado.</span><span class="sxs-lookup"><span data-stu-id="a504a-130">Key into the [Component Table](component-table.md) that specifies the Windows Installer component that contains this assembly.</span></span>

</dd> <dt>

<span data-ttu-id="a504a-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="a504a-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="a504a-132">Nombre del atributo asociado con el valor especificado en la columna valor.</span><span class="sxs-lookup"><span data-stu-id="a504a-132">Name of the attribute associated with the value specified in the Value column.</span></span>

</dd> <dt>

<span data-ttu-id="a504a-133"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="a504a-133"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="a504a-134">Valor asociado al nombre especificado en la columna nombre.</span><span class="sxs-lookup"><span data-stu-id="a504a-134">Value associated with the name specified in the Name column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a504a-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a504a-135">Remarks</span></span>

<span data-ttu-id="a504a-136">La información que se crea en la tabla MsiAssemblyName debe coincidir con la información del archivo de manifiesto del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="a504a-136">The information authored into the MsiAssemblyName Table must match the information in the manifest file of the assembly.</span></span> <span data-ttu-id="a504a-137">Si la información de la tabla manifest y MsiAssemblyName no coinciden, la eliminación de la aplicación puede dejar el ensamblado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="a504a-137">If the information in the manifest and MsiAssemblyName Table do not match, removal of the application can leave the assembly on the computer.</span></span>

<span data-ttu-id="a504a-138">En el caso de los ensamblados Win32, debe haber una fila en la tabla MsiAssemblyName para cada una de las siguientes entradas en el campo Nombre: tipo, nombre, versión, idioma, publicKeyToken y processorArchitecture.</span><span class="sxs-lookup"><span data-stu-id="a504a-138">For Win32 assemblies there must be a row in the MsiAssemblyName Table for each of the following entries in the Name field: type, name, version, language, publicKeyToken and processorArchitecture.</span></span> <span data-ttu-id="a504a-139">El valor correspondiente para cada nombre se puede especificar en el campo de valor.</span><span class="sxs-lookup"><span data-stu-id="a504a-139">The corresponding value for each name can be entered into the Value field.</span></span> <span data-ttu-id="a504a-140">Los pares nombre-valor de la tabla MsiAssemblyName deben coincidir con los atributos Type, Name, version, Language, publicKeyToken y processorArchitecture en el manifiesto del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="a504a-140">The name-value pairs in MsiAssemblyName Table must match the type, name, version, language, publicKeyToken and processorArchitecture attributes in the manifest of the assembly.</span></span>

<span data-ttu-id="a504a-141">En el caso de los ensamblados de Common Language Runtime privados (.NET Frameworkversions 1,0 y 1,1), la tabla MsiAssemblyName debe incluir una fila para cada una de las siguientes entradas en el campo Nombre: nombre, versión y referencia cultural.</span><span class="sxs-lookup"><span data-stu-id="a504a-141">For private common language runtime assemblies (.NET Frameworkversions 1.0 and 1.1), the MsiAssemblyName Table must include a row for each of the following entries in the Name field: Name, Version, and Culture.</span></span> <span data-ttu-id="a504a-142">El valor correspondiente para cada nombre se puede especificar en el campo de valor.</span><span class="sxs-lookup"><span data-stu-id="a504a-142">The corresponding value for each Name can be entered into the Value field.</span></span>

<span data-ttu-id="a504a-143">En el caso de los ensamblados de Common Language Runtime globales (.NET Framework las versiones 1,0 y 1,1), la tabla MsiAssemblyName debe incluir una fila para cada una de las siguientes entradas en el campo Nombre: nombre, versión, referencia cultural y PublicKeyToken.</span><span class="sxs-lookup"><span data-stu-id="a504a-143">For global common language runtime assemblies (.NET Framework versions 1.0 and 1.1), the MsiAssemblyName Table must include a row for each of the following entries in the Name field: Name, Version, Culture, and PublicKeyToken.</span></span> <span data-ttu-id="a504a-144">El valor correspondiente para cada nombre se puede especificar en el campo de valor.</span><span class="sxs-lookup"><span data-stu-id="a504a-144">The corresponding value for each Name can be entered into the Value field.</span></span>

<span data-ttu-id="a504a-145">La versión .NET Framework 1,1 es la versión mínima que se puede usar para realizar una actualización en contexto de un ensamblado de Common Language Runtime global.</span><span class="sxs-lookup"><span data-stu-id="a504a-145">The .NET Framework version 1.1 is the minimum version that can be used to perform an in-place update of a global common language runtime assembly.</span></span> <span data-ttu-id="a504a-146">Puede comprobar la versión de la propiedad [**MsiNetAssemblySupport**](msinetassemblysupport.md) .</span><span class="sxs-lookup"><span data-stu-id="a504a-146">You can check the [**MsiNetAssemblySupport**](msinetassemblysupport.md) property for the version.</span></span> <span data-ttu-id="a504a-147">La tabla MsiAssemblyName también debe tener un campo FileVersion porque este tipo de actualización de ensamblado solo cambia la FileVersion.</span><span class="sxs-lookup"><span data-stu-id="a504a-147">The MsiAssemblyName Table must also have a FileVersion field because this type of assembly update only changes the FileVersion.</span></span> <span data-ttu-id="a504a-148">Para obtener más información, vea [Actualizar ensamblados](updating-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="a504a-148">For more information, see [Updating Assemblies](updating-assemblies.md).</span></span>

<span data-ttu-id="a504a-149">Por ejemplo, el manifiesto del ensamblado del componente a puede tener una sección assemblyIdentity como se indica a continuación para un ensamblado Win32.</span><span class="sxs-lookup"><span data-stu-id="a504a-149">For example, the assembly manifest for ComponentA might have an assemblyIdentity section as follows for a Win32 assembly.</span></span>

``` syntax
<assemblyIdentity type="win32" name="ms-sxstest-simple" version="1.0.0.0" language="en" publicKeyToken="1111111111222222" processorArchitecture="x86"/>
```

<span data-ttu-id="a504a-150">En este caso, rellene la tabla MsiAssemblyName como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="a504a-150">In this case, populate the MsiAssemblyName Table as follows.</span></span>



| <span data-ttu-id="a504a-151">Componente</span><span class="sxs-lookup"><span data-stu-id="a504a-151">Component</span></span>  | <span data-ttu-id="a504a-152">Nombre</span><span class="sxs-lookup"><span data-stu-id="a504a-152">Name</span></span>                  | <span data-ttu-id="a504a-153">Value</span><span class="sxs-lookup"><span data-stu-id="a504a-153">Value</span></span>             |
|------------|-----------------------|-------------------|
| <span data-ttu-id="a504a-154">Componentea</span><span class="sxs-lookup"><span data-stu-id="a504a-154">ComponentA</span></span> | <span data-ttu-id="a504a-155">type</span><span class="sxs-lookup"><span data-stu-id="a504a-155">type</span></span>                  | <span data-ttu-id="a504a-156">32</span><span class="sxs-lookup"><span data-stu-id="a504a-156">win32</span></span>             |
| <span data-ttu-id="a504a-157">Componentea</span><span class="sxs-lookup"><span data-stu-id="a504a-157">ComponentA</span></span> | <span data-ttu-id="a504a-158">name</span><span class="sxs-lookup"><span data-stu-id="a504a-158">name</span></span>                  | <span data-ttu-id="a504a-159">MS-sxstest: simple</span><span class="sxs-lookup"><span data-stu-id="a504a-159">ms-sxstest-simple</span></span> |
| <span data-ttu-id="a504a-160">Componentea</span><span class="sxs-lookup"><span data-stu-id="a504a-160">ComponentA</span></span> | <span data-ttu-id="a504a-161">version</span><span class="sxs-lookup"><span data-stu-id="a504a-161">version</span></span>               | <span data-ttu-id="a504a-162">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="a504a-162">1.0.0.0</span></span>           |
| <span data-ttu-id="a504a-163">Componentea</span><span class="sxs-lookup"><span data-stu-id="a504a-163">ComponentA</span></span> | <span data-ttu-id="a504a-164">language</span><span class="sxs-lookup"><span data-stu-id="a504a-164">language</span></span>              | <span data-ttu-id="a504a-165">en</span><span class="sxs-lookup"><span data-stu-id="a504a-165">en</span></span>                |
| <span data-ttu-id="a504a-166">Componentea</span><span class="sxs-lookup"><span data-stu-id="a504a-166">ComponentA</span></span> | <span data-ttu-id="a504a-167">publicKeyToken</span><span class="sxs-lookup"><span data-stu-id="a504a-167">publicKeyToken</span></span>        | <span data-ttu-id="a504a-168">1111111111222222</span><span class="sxs-lookup"><span data-stu-id="a504a-168">1111111111222222</span></span>  |
| <span data-ttu-id="a504a-169">Componentea</span><span class="sxs-lookup"><span data-stu-id="a504a-169">ComponentA</span></span> | <span data-ttu-id="a504a-170">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="a504a-170">processorArchitecture</span></span> | <span data-ttu-id="a504a-171">x86</span><span class="sxs-lookup"><span data-stu-id="a504a-171">x86</span></span>               |



 

## <a name="validation"></a><span data-ttu-id="a504a-172">Validación</span><span class="sxs-lookup"><span data-stu-id="a504a-172">Validation</span></span>

<dl>

[<span data-ttu-id="a504a-173">ICE03</span><span class="sxs-lookup"><span data-stu-id="a504a-173">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a504a-174">ICE06</span><span class="sxs-lookup"><span data-stu-id="a504a-174">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a504a-175">ICE32</span><span class="sxs-lookup"><span data-stu-id="a504a-175">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="a504a-176">ICE66</span><span class="sxs-lookup"><span data-stu-id="a504a-176">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="a504a-177">ICE83</span><span class="sxs-lookup"><span data-stu-id="a504a-177">ICE83</span></span>](ice83.md)  
</dl>

 

 

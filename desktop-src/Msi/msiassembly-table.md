---
description: La tabla MsiAssembly especifica la configuración de Windows Installer para los ensamblados de Microsoft .NET Framework y los ensamblados Win32. Para obtener más información, vea Instalar ensamblados en la caché global de ensamblados e instalar ensamblados Win32.
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: Tabla MsiAssembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b54bd6e58e2ff6d12c582309c23856a7bb825b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003049"
---
# <a name="msiassembly-table"></a><span data-ttu-id="c7302-104">Tabla MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="c7302-104">MsiAssembly Table</span></span>

<span data-ttu-id="c7302-105">La tabla MsiAssembly especifica la configuración de Windows Installer para los ensamblados de Microsoft .NET Framework y los ensamblados Win32.</span><span class="sxs-lookup"><span data-stu-id="c7302-105">The MsiAssembly Table specifies Windows Installer settings for Microsoft .NET Framework assemblies and Win32 assemblies.</span></span> <span data-ttu-id="c7302-106">Para obtener más información, vea [Instalar ensamblados en la caché global de ensamblados](installation-of-assemblies-to-the-global-assembly-cache.md) e [Instalar ensamblados Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="c7302-106">For more information, see [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="c7302-107">En Windows XP, Windows Installer puede instalar ensamblados Win32 como [ensamblados en paralelo](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="c7302-107">On Windows XP, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="c7302-108">Para obtener más información, consulte la [API de ensamblados en paralelo](../sbscs/side-by-side-assembly-api.md).</span><span class="sxs-lookup"><span data-stu-id="c7302-108">For more information, see the [Side-by-Side Assembly API](../sbscs/side-by-side-assembly-api.md).</span></span>

<span data-ttu-id="c7302-109">**Windows 2000:** Esta característica no se admite.</span><span class="sxs-lookup"><span data-stu-id="c7302-109">**Windows 2000:** This feature is not supported.</span></span>

<span data-ttu-id="c7302-110">La tabla MsiAssembly tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="c7302-110">The MsiAssembly Table has the following columns.</span></span>



| <span data-ttu-id="c7302-111">Columna</span><span class="sxs-lookup"><span data-stu-id="c7302-111">Column</span></span>            | <span data-ttu-id="c7302-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="c7302-112">Type</span></span>                         | <span data-ttu-id="c7302-113">Clave</span><span class="sxs-lookup"><span data-stu-id="c7302-113">Key</span></span> | <span data-ttu-id="c7302-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="c7302-114">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="c7302-115">Componente\_</span><span class="sxs-lookup"><span data-stu-id="c7302-115">Component\_</span></span>       | [<span data-ttu-id="c7302-116">Identificador</span><span class="sxs-lookup"><span data-stu-id="c7302-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="c7302-117">Y</span><span class="sxs-lookup"><span data-stu-id="c7302-117">Y</span></span>   | <span data-ttu-id="c7302-118">N</span><span class="sxs-lookup"><span data-stu-id="c7302-118">N</span></span>        |
| <span data-ttu-id="c7302-119">Característica\_</span><span class="sxs-lookup"><span data-stu-id="c7302-119">Feature\_</span></span>         | [<span data-ttu-id="c7302-120">Identificador</span><span class="sxs-lookup"><span data-stu-id="c7302-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="c7302-121">N</span><span class="sxs-lookup"><span data-stu-id="c7302-121">N</span></span>   | <span data-ttu-id="c7302-122">N</span><span class="sxs-lookup"><span data-stu-id="c7302-122">N</span></span>        |
| <span data-ttu-id="c7302-123">Manifiesto de archivo \_</span><span class="sxs-lookup"><span data-stu-id="c7302-123">File\_Manifest</span></span>    | [<span data-ttu-id="c7302-124">Identificador</span><span class="sxs-lookup"><span data-stu-id="c7302-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="c7302-125">N</span><span class="sxs-lookup"><span data-stu-id="c7302-125">N</span></span>   | <span data-ttu-id="c7302-126">Y</span><span class="sxs-lookup"><span data-stu-id="c7302-126">Y</span></span>        |
| <span data-ttu-id="c7302-127">Aplicación de archivo \_</span><span class="sxs-lookup"><span data-stu-id="c7302-127">File\_Application</span></span> | [<span data-ttu-id="c7302-128">Identificador</span><span class="sxs-lookup"><span data-stu-id="c7302-128">Identifier</span></span>](identifier.md) | <span data-ttu-id="c7302-129">N</span><span class="sxs-lookup"><span data-stu-id="c7302-129">N</span></span>   | <span data-ttu-id="c7302-130">Y</span><span class="sxs-lookup"><span data-stu-id="c7302-130">Y</span></span>        |
| <span data-ttu-id="c7302-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="c7302-131">Attributes</span></span>        | [<span data-ttu-id="c7302-132">Entero</span><span class="sxs-lookup"><span data-stu-id="c7302-132">Integer</span></span>](integer.md)       | <span data-ttu-id="c7302-133">N</span><span class="sxs-lookup"><span data-stu-id="c7302-133">N</span></span>   | <span data-ttu-id="c7302-134">Y</span><span class="sxs-lookup"><span data-stu-id="c7302-134">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c7302-135">Columnas</span><span class="sxs-lookup"><span data-stu-id="c7302-135">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c7302-136"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="c7302-136"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="c7302-137">Clave en la [tabla de componentes](component-table.md) que especifica el Windows Installer componente que contiene este ensamblado.</span><span class="sxs-lookup"><span data-stu-id="c7302-137">The key into the [Component Table](component-table.md) that specifies the Windows Installer component that contains this assembly.</span></span>

<span data-ttu-id="c7302-138">El valor de este campo no debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="c7302-138">The value in this field must not be set to null.</span></span> <span data-ttu-id="c7302-139">El campo de ruta de la [tabla de componentes](component-table.md) no debe ser null.</span><span class="sxs-lookup"><span data-stu-id="c7302-139">The component KeyPath field in the [Component Table](component-table.md) must not be null.</span></span>

<span data-ttu-id="c7302-140">En el caso de los ensamblados de Win32, la ruta de acceso de componente no puede ser el archivo de manifiesto especificado en el manifiesto de archivo \_ .</span><span class="sxs-lookup"><span data-stu-id="c7302-140">For Win32 assemblies, the component KeyPath cannot be the manifest file that is specified in File\_Manifest.</span></span> <span data-ttu-id="c7302-141">El manifiesto puede ser la ruta de la ruta de una .NET Framework o un ensamblado de directiva.</span><span class="sxs-lookup"><span data-stu-id="c7302-141">The manifest can be the keypath for a .NET Framework or policy assembly.</span></span>

</dd> <dt>

<span data-ttu-id="c7302-142"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Ofrecen\_</span><span class="sxs-lookup"><span data-stu-id="c7302-142"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="c7302-143">Clave en la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="c7302-143">Key into the [Feature Table](feature-table.md).</span></span>

<span data-ttu-id="c7302-144">Cuando la instalación de una característica debe instalar el ensamblado, Windows Installer instala la característica señalada por este campo.</span><span class="sxs-lookup"><span data-stu-id="c7302-144">When the assembly must be installed by a feature installation, Windows Installer installs the feature pointed to by this field.</span></span>

</dd> <dt>

<span data-ttu-id="c7302-145"><span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>Manifiesto de archivo \_</span><span class="sxs-lookup"><span data-stu-id="c7302-145"><span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>File\_Manifest</span></span>
</dt> <dd>

<span data-ttu-id="c7302-146">Una clave externa en la [tabla de archivos](file-table.md) que especifica el archivo que contiene el manifiesto de un ensamblado de .NET Framework o de Win32.</span><span class="sxs-lookup"><span data-stu-id="c7302-146">An external key into the [File Table](file-table.md) that specifies the file that contains the manifest for a .NET Framework assembly or Win32 assembly.</span></span>

<span data-ttu-id="c7302-147">En el caso de un ensamblado Win32, no especifique este archivo como el archivo de ruta de acceso de la clave de componente en el campo de ruta de clave de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="c7302-147">For a Win32 assembly, do not specify this file as the component key path file in the KeyPath field of the [Component Table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7302-148"><span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>Aplicación de archivo \_</span><span class="sxs-lookup"><span data-stu-id="c7302-148"><span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>File\_Application</span></span>
</dt> <dd>

<span data-ttu-id="c7302-149">Para instalar el ensamblado en una ubicación privada, escriba el archivo de ruta de acceso de la clave para el componente de ensamblado en este campo.</span><span class="sxs-lookup"><span data-stu-id="c7302-149">To install the assembly at a private location, enter the key path file for the assembly component in this field.</span></span>

<span data-ttu-id="c7302-150">Este es el valor que aparece en el campo de ruta de la ruta de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="c7302-150">This is the value that appears in the KeyPath field of the [Component Table](component-table.md).</span></span> <span data-ttu-id="c7302-151">Después, el instalador puede instalar el ensamblado en la estructura de directorios del componente que se especifica en la [tabla del directorio](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="c7302-151">The Installer can then install the assembly to the directory structure of the component that is specified in the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="c7302-152">Este campo debe ser null si el ensamblado se va a instalar en la caché global de ensamblados.</span><span class="sxs-lookup"><span data-stu-id="c7302-152">This field must be null if the assembly is to be installed into the global assembly cache.</span></span>

</dd> <dt>

<span data-ttu-id="c7302-153"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Sus</span><span class="sxs-lookup"><span data-stu-id="c7302-153"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="c7302-154">Escriba un valor de 1 (uno) para un ensamblado Win32.</span><span class="sxs-lookup"><span data-stu-id="c7302-154">Enter a value of 1 (one) for a Win32 assembly.</span></span> <span data-ttu-id="c7302-155">Escriba un valor de 0 (cero) para un ensamblado de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c7302-155">Enter a value of 0 (zero) for a .NET Framework assembly.</span></span>

<span data-ttu-id="c7302-156">Si la columna Attributes es NULL, el instalador trata el ensamblado como un ensamblado de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c7302-156">If the Attributes column is NULL, the Installer treats the assembly as a .NET Framework assembly.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7302-157">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7302-157">Remarks</span></span>

<span data-ttu-id="c7302-158">Si hay al menos una entrada en la tabla MsiAssembly, la [tabla InstallExecuteSequence](installexecutesequence-table.md) debe contener la [acción MsiPublishAssemblies](msipublishassemblies-action.md)y la [acción MsiUnpublishAssemblies](msiunpublishassemblies-action.md).</span><span class="sxs-lookup"><span data-stu-id="c7302-158">If there is at least one entry in the MsiAssembly Table, the [InstallExecuteSequence Table](installexecutesequence-table.md) must contain the [MsiPublishAssemblies Action](msipublishassemblies-action.md), and [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md).</span></span>

<span data-ttu-id="c7302-159">Dado que los ensamblados no se pueden revertir una vez confirmados, Windows Installer usa un proceso de instalación de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="c7302-159">Because assemblies cannot be rolled back after they are committed, Windows Installer uses a two-step installation process.</span></span> <span data-ttu-id="c7302-160">Las interfaces a los ensamblados se crean durante las operaciones de instalación generadas por la [acción MsiPublishAssemblies](msipublishassemblies-action.md).</span><span class="sxs-lookup"><span data-stu-id="c7302-160">The interfaces to the assemblies are created during the installation operations that are generated by the [MsiPublishAssemblies Action](msipublishassemblies-action.md).</span></span>

<span data-ttu-id="c7302-161">Los ensamblados no se confirman hasta que la ejecución de la [acción InstallFinalize](installfinalize-action.md)es correcta.</span><span class="sxs-lookup"><span data-stu-id="c7302-161">The assemblies are not committed until successful execution of the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="c7302-162">Esto significa que si crea una acción personalizada o un recurso que se basa en el ensamblado, se debe secuenciar después de la [acción InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="c7302-162">This means that if you author a custom action or resource that relies on the assembly, it must be sequenced after the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="c7302-163">Por ejemplo, si necesita iniciar un servicio que depende de un ensamblado en la caché de ensamblados global (GAC), debe programar el inicio de ese servicio después de la [acción InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="c7302-163">For example, if you need to start a service that depends on an assembly in the Global Assembly Cache (GAC), you must schedule the starting of that service after the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="c7302-164">Esto significa que no puede usar la [tabla ServiceControl](servicecontrol-table.md) para iniciar el servicio, sino que debe usar una acción personalizada que se secuenciará después de InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="c7302-164">This means you cannot use the [ServiceControl Table](servicecontrol-table.md) to start the service, instead you must use a custom action that is sequenced after InstallFinalize.</span></span>

## <a name="validation"></a><span data-ttu-id="c7302-165">Validación</span><span class="sxs-lookup"><span data-stu-id="c7302-165">Validation</span></span>

<dl>

[<span data-ttu-id="c7302-166">ICE03</span><span class="sxs-lookup"><span data-stu-id="c7302-166">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c7302-167">ICE06</span><span class="sxs-lookup"><span data-stu-id="c7302-167">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c7302-168">ICE32</span><span class="sxs-lookup"><span data-stu-id="c7302-168">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="c7302-169">ICE66</span><span class="sxs-lookup"><span data-stu-id="c7302-169">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="c7302-170">ICE83</span><span class="sxs-lookup"><span data-stu-id="c7302-170">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="c7302-171">ICE94</span><span class="sxs-lookup"><span data-stu-id="c7302-171">ICE94</span></span>](ice94.md)  
</dl>

 

 

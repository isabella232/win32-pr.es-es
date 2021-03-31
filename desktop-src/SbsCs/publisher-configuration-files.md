---
description: Un archivo de configuración de publicador es un archivo XML que redirige globalmente las aplicaciones y los ensamblados con una versión de un ensamblado en paralelo a otra versión del mismo ensamblado.
ms.assetid: b10752af-80a7-4027-b525-90333d0d010a
title: Archivos de configuración del publicador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc5d7d7b7ffdad3d1179a7f8c66a347d91e0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912506"
---
# <a name="publisher-configuration-files"></a><span data-ttu-id="5b30c-103">Archivos de configuración del publicador</span><span class="sxs-lookup"><span data-stu-id="5b30c-103">Publisher Configuration Files</span></span>

<span data-ttu-id="5b30c-104">Un archivo de configuración de publicador es un archivo XML que redirige globalmente las aplicaciones y los ensamblados con una versión de un ensamblado en paralelo a otra versión del mismo ensamblado.</span><span class="sxs-lookup"><span data-stu-id="5b30c-104">A publisher configuration file is an XML file that globally redirects applications and assemblies from using one version of a side-by-side assembly to another version of the same assembly.</span></span> <span data-ttu-id="5b30c-105">Normalmente, el publicador del ensamblado emite una corrección de seguridad o actualización compatible en cada ensamblado mediante la emisión de un archivo de configuración del publicador que se va a instalar junto con una actualización Service Pack.</span><span class="sxs-lookup"><span data-stu-id="5b30c-105">Typically, the publisher of the assembly issues a compatible update or security fix on a per-assembly basis by issuing a publisher configuration file to be installed along with a service pack update.</span></span> <span data-ttu-id="5b30c-106">Esto se conoce como [configuración del publicador](publisher-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="5b30c-106">This is referred to as [publisher configuration](publisher-configuration.md).</span></span> <span data-ttu-id="5b30c-107">Para obtener más información acerca de este tipo de [configuración](configuration.md) , consulte Configuración del publicador.</span><span class="sxs-lookup"><span data-stu-id="5b30c-107">For more information about this type of [configuration](configuration.md) see Publisher Configuration.</span></span>

<span data-ttu-id="5b30c-108">Los archivos de configuración del publicador tienen los siguientes elementos y atributos.</span><span class="sxs-lookup"><span data-stu-id="5b30c-108">Publisher configuration files have the following elements and attributes.</span></span> <span data-ttu-id="5b30c-109">Para obtener una lista completa del esquema XML, vea [esquema del archivo de configuración del publicador](publisher-configuration-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="5b30c-109">For a complete listing of the XML schema, see [Publisher Configuration File Schema](publisher-configuration-file-schema.md).</span></span>



| <span data-ttu-id="5b30c-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="5b30c-110">Element</span></span>               | <span data-ttu-id="5b30c-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="5b30c-111">Attributes</span></span>                | <span data-ttu-id="5b30c-112">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5b30c-112">Required</span></span> |
|-----------------------|---------------------------|----------|
| <span data-ttu-id="5b30c-113">**assembl**</span><span class="sxs-lookup"><span data-stu-id="5b30c-113">**assembly**</span></span>          |                           | <span data-ttu-id="5b30c-114">Sí</span><span class="sxs-lookup"><span data-stu-id="5b30c-114">Yes</span></span>      |
|                       | <span data-ttu-id="5b30c-115">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="5b30c-115">**manifestVersion**</span></span>       | <span data-ttu-id="5b30c-116">Sí</span><span class="sxs-lookup"><span data-stu-id="5b30c-116">Yes</span></span>      |
| <span data-ttu-id="5b30c-117">**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="5b30c-117">**assemblyIdentity**</span></span>  |                           | <span data-ttu-id="5b30c-118">Sí</span><span class="sxs-lookup"><span data-stu-id="5b30c-118">Yes</span></span>      |
|                       | <span data-ttu-id="5b30c-119">**type**</span><span class="sxs-lookup"><span data-stu-id="5b30c-119">**type**</span></span>                  | <span data-ttu-id="5b30c-120">Sí</span><span class="sxs-lookup"><span data-stu-id="5b30c-120">Yes</span></span>      |
|                       | <span data-ttu-id="5b30c-121">**name**</span><span class="sxs-lookup"><span data-stu-id="5b30c-121">**name**</span></span>                  | <span data-ttu-id="5b30c-122">Sí</span><span class="sxs-lookup"><span data-stu-id="5b30c-122">Yes</span></span>      |
|                       | <span data-ttu-id="5b30c-123">**language**</span><span class="sxs-lookup"><span data-stu-id="5b30c-123">**language**</span></span>              | <span data-ttu-id="5b30c-124">No</span><span class="sxs-lookup"><span data-stu-id="5b30c-124">No</span></span>       |
|                       | <span data-ttu-id="5b30c-125">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="5b30c-125">**processorArchitecture**</span></span> | <span data-ttu-id="5b30c-126">No</span><span class="sxs-lookup"><span data-stu-id="5b30c-126">No</span></span>       |
|                       | <span data-ttu-id="5b30c-127">**version**</span><span class="sxs-lookup"><span data-stu-id="5b30c-127">**version**</span></span>               | <span data-ttu-id="5b30c-128">Sí</span><span class="sxs-lookup"><span data-stu-id="5b30c-128">Yes</span></span>      |
|                       | <span data-ttu-id="5b30c-129">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="5b30c-129">**publicKeyToken**</span></span>        | <span data-ttu-id="5b30c-130">No</span><span class="sxs-lookup"><span data-stu-id="5b30c-130">No</span></span>       |
| <span data-ttu-id="5b30c-131">**pendiente**</span><span class="sxs-lookup"><span data-stu-id="5b30c-131">**dependency**</span></span>        |                           | <span data-ttu-id="5b30c-132">No</span><span class="sxs-lookup"><span data-stu-id="5b30c-132">No</span></span>       |
| <span data-ttu-id="5b30c-133">**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="5b30c-133">**dependentAssembly**</span></span> |                           | <span data-ttu-id="5b30c-134">No</span><span class="sxs-lookup"><span data-stu-id="5b30c-134">No</span></span>       |
| <span data-ttu-id="5b30c-135">**bindingRedirect**</span><span class="sxs-lookup"><span data-stu-id="5b30c-135">**bindingRedirect**</span></span>   |                           | <span data-ttu-id="5b30c-136">Sí</span><span class="sxs-lookup"><span data-stu-id="5b30c-136">Yes</span></span>      |
|                       | <span data-ttu-id="5b30c-137">**oldVersion**</span><span class="sxs-lookup"><span data-stu-id="5b30c-137">**oldVersion**</span></span>            | <span data-ttu-id="5b30c-138">Sí</span><span class="sxs-lookup"><span data-stu-id="5b30c-138">Yes</span></span>      |
|                       | <span data-ttu-id="5b30c-139">**newVersion**</span><span class="sxs-lookup"><span data-stu-id="5b30c-139">**newVersion**</span></span>            | <span data-ttu-id="5b30c-140">Sí</span><span class="sxs-lookup"><span data-stu-id="5b30c-140">Yes</span></span>      |



 

## <a name="file-location"></a><span data-ttu-id="5b30c-141">Ubicación del archivo</span><span class="sxs-lookup"><span data-stu-id="5b30c-141">File Location</span></span>

<span data-ttu-id="5b30c-142">Los archivos de configuración del publicador deben instalarse en la carpeta WinSxS.</span><span class="sxs-lookup"><span data-stu-id="5b30c-142">Publisher configuration files must be installed in the WinSxS folder.</span></span> <span data-ttu-id="5b30c-143">Normalmente se instalan como un archivo independiente, pero los archivos de configuración del publicador también se pueden incluir como un recurso en un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="5b30c-143">They are commonly installed as a separate file but publisher configuration files can also be included as a resource in a DLL.</span></span> <span data-ttu-id="5b30c-144">Un archivo de configuración de publicador no se puede incluir como un recurso en un archivo EXE.</span><span class="sxs-lookup"><span data-stu-id="5b30c-144">A publisher configuration file cannot be included as a resource in an EXE file.</span></span> <span data-ttu-id="5b30c-145">Un archivo EXE puede incluir un [manifiesto de aplicación](application-manifests.md) como un recurso.</span><span class="sxs-lookup"><span data-stu-id="5b30c-145">An EXE file may include an [application manifest](application-manifests.md) as a resource.</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="5b30c-146">Sintaxis de los nombres de archivo</span><span class="sxs-lookup"><span data-stu-id="5b30c-146">File Name Syntax</span></span>

<span data-ttu-id="5b30c-147">El nombre de archivo de un archivo de configuración de publicador tiene la *Directiva* de formulario. *principal*. *secundaria*. *AssemblyName* , donde *major* y *Minor* hacen referencia a las partes principales y secundarias de la [versión de ensamblado](assembly-versions.md) que se va a ver afectada.</span><span class="sxs-lookup"><span data-stu-id="5b30c-147">The file name of a publisher configuration file has the form *policy*.*major*.*minor*.*assemblyname* where *major* and *minor* refer to the major and minor parts of the [assembly version](assembly-versions.md) that is being affected.</span></span> <span data-ttu-id="5b30c-148">*AssemblyName* hace referencia al nombre del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="5b30c-148">The *assemblyname* refers to the name of the assembly.</span></span>

<span data-ttu-id="5b30c-149">Por ejemplo, un archivo de configuración de publicador para la versión 6,0 del ensamblado Microsoft. Windows. Common-Controls tendría el siguiente nombre:</span><span class="sxs-lookup"><span data-stu-id="5b30c-149">For example, a publisher configuration file for version 6.0 of the Microsoft.Windows.Common-Controls assembly would have the following name:</span></span>

<dl> <span data-ttu-id="5b30c-150">Policy. 6.0. Microsoft. Windows. Common-Controls</span><span class="sxs-lookup"><span data-stu-id="5b30c-150">policy.6.0.Microsoft.Windows.Common-Controls</span></span>  
</dl>

<span data-ttu-id="5b30c-151">No use archivos de configuración de directivas para incrementar la versión principal o secundaria de un ensamblado.</span><span class="sxs-lookup"><span data-stu-id="5b30c-151">Do not use policy configuration files to increment the major or minor version of an assembly.</span></span> <span data-ttu-id="5b30c-152">Por ejemplo, no redirija la versión 6.0.0.0 a 7.0.0.0 o 6.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="5b30c-152">For example, do not redirect version 6.0.0.0 to 7.0.0.0 or 6.1.0.0.</span></span> <span data-ttu-id="5b30c-153">Cuando una aplicación hace referencia a una versión de ensamblado, como 6.0.0.0, comprueba la presencia de cualquier archivo de configuración de directiva con las versiones principal y secundaria especificadas, por ejemplo, 6,0.</span><span class="sxs-lookup"><span data-stu-id="5b30c-153">When an application references an assembly version, such as 6.0.0.0, side-by-side checks for the presence of any policy configuration files with the specified major and minor versions, e.g. 6.0.</span></span> <span data-ttu-id="5b30c-154">A continuación, la aplicación se redirige a otra versión del ensamblado, por ejemplo 6.0.1.0.</span><span class="sxs-lookup"><span data-stu-id="5b30c-154">The application is then redirected to another version of the assembly, for example 6.0.1.0.</span></span> <span data-ttu-id="5b30c-155">Si un archivo de configuración del publicador incrementa la versión principal o secundaria de un ensamblado, la redirección posterior del ensamblado puede requerir la emisión de varios archivos de configuración de directivas.</span><span class="sxs-lookup"><span data-stu-id="5b30c-155">If a publisher configuration file increments the major or minor version of an assembly, subsequent redirection of the assembly may require issuing multiple policy configuration files.</span></span>

## <a name="elements"></a><span data-ttu-id="5b30c-156">Elementos</span><span class="sxs-lookup"><span data-stu-id="5b30c-156">Elements</span></span>

<dl> <dt>

<span data-ttu-id="5b30c-157"><span id="assembly"></span><span id="ASSEMBLY"></span>**assembl**</span><span class="sxs-lookup"><span data-stu-id="5b30c-157"><span id="assembly"></span><span id="ASSEMBLY"></span>**assembly**</span></span>
</dt> <dd>

<span data-ttu-id="5b30c-158">Elemento contenedor.</span><span class="sxs-lookup"><span data-stu-id="5b30c-158">A container element.</span></span> <span data-ttu-id="5b30c-159">Su primer subelemento debe ser **assemblyIdentity**.</span><span class="sxs-lookup"><span data-stu-id="5b30c-159">Its first subelement must be an **assemblyIdentity**.</span></span> <span data-ttu-id="5b30c-160">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5b30c-160">Required.</span></span>

<span data-ttu-id="5b30c-161">El elemento de ensamblado debe estar en el espacio de nombres **urn: schemas-microsoft-com: ASM. v1**.</span><span class="sxs-lookup"><span data-stu-id="5b30c-161">The assembly element must be in the namespace **urn:schemas-microsoft-com:asm.v1**.</span></span> <span data-ttu-id="5b30c-162">Los elementos secundarios del ensamblado también deben estar en este espacio de nombres, por herencia o mediante el etiquetado.</span><span class="sxs-lookup"><span data-stu-id="5b30c-162">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="5b30c-163">El elemento **Assembly** tiene los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="5b30c-163">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="5b30c-164">Atributo</span><span class="sxs-lookup"><span data-stu-id="5b30c-164">Attribute</span></span>           | <span data-ttu-id="5b30c-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b30c-165">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="5b30c-166">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="5b30c-166">**manifestVersion**</span></span> | <span data-ttu-id="5b30c-167">El atributo **manifestVersion** debe establecerse en 1,0.</span><span class="sxs-lookup"><span data-stu-id="5b30c-167">The **manifestVersion** attribute must be set to 1.0.</span></span> |



 

</dd> <dt>

<span data-ttu-id="5b30c-168"><span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="5b30c-168"><span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="5b30c-169">Describe e identifica de forma única un ensamblado en paralelo.</span><span class="sxs-lookup"><span data-stu-id="5b30c-169">Describes and uniquely identifies a side-by-side assembly.</span></span>

<span data-ttu-id="5b30c-170">Como primer subelemento de un elemento **Assembly** , **assemblyIdentity** describe el ensamblado en paralelo que tiene una o varias de sus dependencias de ensamblado cambiadas.</span><span class="sxs-lookup"><span data-stu-id="5b30c-170">As the first subelement of an **assembly** element, the **assemblyIdentity** describes the side-by-side assembly that is having one or more of its assembly dependencies changed.</span></span> <span data-ttu-id="5b30c-171">El archivo de configuración del publicador redirige las dependencias del ensamblado identificado.</span><span class="sxs-lookup"><span data-stu-id="5b30c-171">The publisher configuration file redirects the dependencies of the assembly identified.</span></span> <span data-ttu-id="5b30c-172">Por ejemplo, el siguiente **assemblyIdentity** indica que el archivo de configuración del publicador afecta a las dependencias del ensamblado de 6.0.0.0 x86 Microsoft. Windows. pop.</span><span class="sxs-lookup"><span data-stu-id="5b30c-172">For example, the following **assemblyIdentity** indicates that the publisher configuration file affects the dependencies of the x86 Microsoft.Windows.Pop 6.0.0.0 assembly.</span></span>

``` syntax
<assemblyIdentity 
     type="win32-policy" 
     publicKeyToken="0000000000000000" 
     name="policy.6.0.Microsoft.Windows.Pop" 
     version="2.1.0.0" 
     processorArchitecture="x86"/>
```

<span data-ttu-id="5b30c-173">Como primer subelemento de un elemento **dependentAssembly** , **assemblyIdentity** describe una dependencia del ensamblado en paralelo.</span><span class="sxs-lookup"><span data-stu-id="5b30c-173">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly dependency.</span></span> <span data-ttu-id="5b30c-174">El archivo de configuración del publicador vuelve a configurar la identidad de este ensamblado en paralelo necesario.</span><span class="sxs-lookup"><span data-stu-id="5b30c-174">The publisher configuration file reconfigures the identity of this required side-by-side assembly.</span></span> <span data-ttu-id="5b30c-175">El cambio se especifica en un **bindingRedirect**.</span><span class="sxs-lookup"><span data-stu-id="5b30c-175">The change is specified in a **bindingRedirect**.</span></span> <span data-ttu-id="5b30c-176">Por ejemplo, el siguiente **assemblyIdentity** cambia cualquier dependencia de la versión 2.0.0.0 de Microsoft. Windows. SampleAssembly a una dependencia de la versión de Microsoft. Windows. SampleAssembly 2.0.1.0.</span><span class="sxs-lookup"><span data-stu-id="5b30c-176">For example, the following **assemblyIdentity** changes any dependency on Microsoft.Windows.SampleAssembly version 2.0.0.0 to a dependency on Microsoft.Windows.SampleAssembly version 2.0.1.0.</span></span>

``` syntax
<dependency>
      <dependentAssembly>
         <assemblyIdentity 
type="win32" 
name="Microsoft.Windows.SampleAssembly"  
processorArchitecture="x86"
publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
</dependency>
```

<span data-ttu-id="5b30c-177">El elemento **assemblyIdentity** tiene los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="5b30c-177">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="5b30c-178">No tiene subelementos.</span><span class="sxs-lookup"><span data-stu-id="5b30c-178">It has no sub-elements.</span></span>



| <span data-ttu-id="5b30c-179">Atributo</span><span class="sxs-lookup"><span data-stu-id="5b30c-179">Attribute</span></span>                 | <span data-ttu-id="5b30c-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b30c-180">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b30c-181">**type**</span><span class="sxs-lookup"><span data-stu-id="5b30c-181">**type**</span></span>                  | <span data-ttu-id="5b30c-182">Especifica el tipo de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="5b30c-182">Specifies the assembly type.</span></span> <span data-ttu-id="5b30c-183">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5b30c-183">Required.</span></span> <span data-ttu-id="5b30c-184">En el **assemblyIdentity** para que el ensamblado se vea afectado, el valor del atributo **Type** debe establecerse en Win32-Policy.</span><span class="sxs-lookup"><span data-stu-id="5b30c-184">In the **assemblyIdentity** for the assembly being affected, the value of the **type** attribute must be set to win32-policy.</span></span> <span data-ttu-id="5b30c-185">El valor Win32-Policy debe estar en minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5b30c-185">The value win32-policy must be in all lowercase letters.</span></span><br/> <span data-ttu-id="5b30c-186">En el **assemblyIdentity** para la dependencia del ensamblado cambiante, el valor del atributo **Type** debe establecerse en Win32.</span><span class="sxs-lookup"><span data-stu-id="5b30c-186">In the **assemblyIdentity** for the changing assembly dependency, the value of the **type** attribute must be set to win32.</span></span> <span data-ttu-id="5b30c-187">El valor Win32 debe estar en minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5b30c-187">The value win32 must be in all lowercase letters.</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="5b30c-188">**name**</span><span class="sxs-lookup"><span data-stu-id="5b30c-188">**name**</span></span>                  | <span data-ttu-id="5b30c-189">Designa de forma única un ensamblado.</span><span class="sxs-lookup"><span data-stu-id="5b30c-189">Uniquely names an assembly.</span></span> <span data-ttu-id="5b30c-190">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5b30c-190">Required.</span></span> <span data-ttu-id="5b30c-191">En el **assemblyIdentity** para que el ensamblado se vea afectado, el nombre tiene la *Directiva* de formulario. *principal*. *secundaria*. *AssemblyName* donde *major* y *Minor* hacen referencia a las partes principales y secundarias de la [versión del ensamblado](assembly-versions.md).</span><span class="sxs-lookup"><span data-stu-id="5b30c-191">In the **assemblyIdentity** for the assembly being affected, name has the form *policy*.*major*.*minor*.*assemblyname* where *major* and *minor* refer to the major and minor parts of the [assembly version](assembly-versions.md).</span></span><br/> <span data-ttu-id="5b30c-192">En el **assemblyIdentity** para la dependencia del ensamblado cambiante, Name tiene el formato Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="5b30c-192">In the **assemblyIdentity** for the changing assembly dependency, name has the form Organization.Division.Name.</span></span> <span data-ttu-id="5b30c-193">Por ejemplo, Microsoft. Windows. MysampleApp.</span><span class="sxs-lookup"><span data-stu-id="5b30c-193">For example, Microsoft.Windows.MysampleApp.</span></span><br/>                                                                                                                                                                                 |
| <span data-ttu-id="5b30c-194">**language**</span><span class="sxs-lookup"><span data-stu-id="5b30c-194">**language**</span></span>              | <span data-ttu-id="5b30c-195">Identifica el idioma del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="5b30c-195">Identifies the language of the assembly.</span></span> <span data-ttu-id="5b30c-196">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5b30c-196">Optional.</span></span> <span data-ttu-id="5b30c-197">En el **assemblyIdentity** para que el ensamblado se vea afectado, si el ensamblado es específico del idioma, especifique el código de lenguaje DHTML.</span><span class="sxs-lookup"><span data-stu-id="5b30c-197">In the **assemblyIdentity** for the assembly being affected, if the assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="5b30c-198">Si el ensamblado es para uso internacional (idioma neutro), omita este atributo.</span><span class="sxs-lookup"><span data-stu-id="5b30c-198">If the assembly is for worldwide use (language neutral), omit this attribute.</span></span><br/> <span data-ttu-id="5b30c-199">En el **assemblyIdentity** para la dependencia del ensamblado cambiante, si el ensamblado es específico del idioma, especifique el código de lenguaje DHTML.</span><span class="sxs-lookup"><span data-stu-id="5b30c-199">In the **assemblyIdentity** for the changing assembly dependency, if the assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="5b30c-200">Si el ensamblado es para uso internacional (idioma neutro), establezca el valor como " \* ".</span><span class="sxs-lookup"><span data-stu-id="5b30c-200">If the assembly is for worldwide use (language neutral) set the value as "\*".</span></span><br/>                                                                                                                            |
| <span data-ttu-id="5b30c-201">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="5b30c-201">**processorArchitecture**</span></span> | <span data-ttu-id="5b30c-202">Especifica el procesador que ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5b30c-202">Specifies the processor running the application.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="5b30c-203">**version**</span><span class="sxs-lookup"><span data-stu-id="5b30c-203">**version**</span></span>               | <span data-ttu-id="5b30c-204">Especifica la versión del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="5b30c-204">Specifies the assembly version.</span></span> <span data-ttu-id="5b30c-205">Use la sintaxis de versión de cuatro partes: mmmm. nnnn. oooo. pppp</span><span class="sxs-lookup"><span data-stu-id="5b30c-205">Use four-part version syntax: mmmm.nnnn.oooo.pppp</span></span> <span data-ttu-id="5b30c-206">Solo se requiere en el **assemblyIdentity** de Def-context.</span><span class="sxs-lookup"><span data-stu-id="5b30c-206">Required only in the DEF-context **assemblyIdentity**.</span></span> <span data-ttu-id="5b30c-207">No especifique el atributo de versión en el **assemblyIdentity** de referencia.</span><span class="sxs-lookup"><span data-stu-id="5b30c-207">Do not specify the version attribute in the REF-context **assemblyIdentity**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="5b30c-208">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="5b30c-208">**publicKeyToken**</span></span>        | <span data-ttu-id="5b30c-209">Cadena hexadecimal de 16 caracteres que representa los últimos 8 bytes del hash SHA-1 de la clave pública con la que se firma el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="5b30c-209">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the assembly is signed.</span></span> <span data-ttu-id="5b30c-210">La clave pública que se usa para firmar el catálogo debe ser de 2048 bits o superior.</span><span class="sxs-lookup"><span data-stu-id="5b30c-210">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="5b30c-211">Se requiere un publicKeyToken para todos los ensamblados en paralelo compartidos.</span><span class="sxs-lookup"><span data-stu-id="5b30c-211">A publicKeyToken is required for all shared side-by-side assemblies.</span></span> <span data-ttu-id="5b30c-212">El publicKeyToken utilizado para el archivo de configuración del publicador debe ser la misma clave utilizada para el ensamblado firmado.</span><span class="sxs-lookup"><span data-stu-id="5b30c-212">The publicKeyToken used for the publisher configuration file should be the same key used for the signed assembly.</span></span> <span data-ttu-id="5b30c-213">Los archivos de configuración del publicador se pueden firmar con las mismas herramientas que se usan con los ensamblados, vea [ejemplo de firma de ensamblados](assembly-signing-example.md) y [crear archivos y catálogos firmados](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="5b30c-213">Publisher configuration files can be signed using the same tools as used with assemblies, see [Assembly Signing Example](assembly-signing-example.md) and [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span> |



 

</dd> <dt>

<span data-ttu-id="5b30c-214"><span id="dependency"></span><span id="DEPENDENCY"></span>**pendiente**</span><span class="sxs-lookup"><span data-stu-id="5b30c-214"><span id="dependency"></span><span id="DEPENDENCY"></span>**dependency**</span></span>
</dt> <dd>

<span data-ttu-id="5b30c-215">Un elemento contenedor opcional para al menos un elemento **dependentAssembly**.</span><span class="sxs-lookup"><span data-stu-id="5b30c-215">An optional container element for at least one **dependentAssembly**.</span></span> <span data-ttu-id="5b30c-216">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="5b30c-216">It has no attributes.</span></span>

</dd> <dt>

<span data-ttu-id="5b30c-217"><span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="5b30c-217"><span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**</span></span>
</dt> <dd>

<span data-ttu-id="5b30c-218">Cada **dependentAssembly** debe estar dentro de una **dependencia** exactamente.</span><span class="sxs-lookup"><span data-stu-id="5b30c-218">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="5b30c-219">Un **dependentAssembly** no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="5b30c-219">A **dependentAssembly** has no attributes.</span></span> <span data-ttu-id="5b30c-220">El primer subelemento de **dependentAssembly** debe ser un **assemblyIdentity** para que la configuración del publicador reconfigure el ensamblado en paralelo.</span><span class="sxs-lookup"><span data-stu-id="5b30c-220">The first subelement of **dependentAssembly** must be an **assemblyIdentity** for the side-by-side assembly being reconfigured by the publisher configuration.</span></span>

</dd> <dt>

<span data-ttu-id="5b30c-221"><span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**</span><span class="sxs-lookup"><span data-stu-id="5b30c-221"><span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**</span></span>
</dt> <dd>

<span data-ttu-id="5b30c-222">El elemento **bindingRedirect** contiene información de redirección para el enlace del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="5b30c-222">The **bindingRedirect** element contains redirection information for the binding of the assembly.</span></span>

<span data-ttu-id="5b30c-223">Este elemento tiene los atributos que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5b30c-223">This element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="5b30c-224">Atributo</span><span class="sxs-lookup"><span data-stu-id="5b30c-224">Attribute</span></span>      | <span data-ttu-id="5b30c-225">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b30c-225">Description</span></span>                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b30c-226">**oldVersion**</span><span class="sxs-lookup"><span data-stu-id="5b30c-226">**oldVersion**</span></span> | <span data-ttu-id="5b30c-227">Especifica la versión de ensamblado que se va a reemplazar y redirigir.</span><span class="sxs-lookup"><span data-stu-id="5b30c-227">Specifies the assembly version being overridden and redirected.</span></span> <span data-ttu-id="5b30c-228">Use la sintaxis de la versión de cuatro partes nnnnn. nnnnn. nnnnn. nnnnn.</span><span class="sxs-lookup"><span data-stu-id="5b30c-228">Use the four-part version syntax nnnnn.nnnnn.nnnnn.nnnnn.</span></span> <span data-ttu-id="5b30c-229">Especifique un intervalo de versiones por un guión sin espacios.</span><span class="sxs-lookup"><span data-stu-id="5b30c-229">Specify a range of versions by a dash with no spaces.</span></span> <span data-ttu-id="5b30c-230">Por ejemplo, 2.14.3.0 o 2.14.3.0 2.16.0.0.</span><span class="sxs-lookup"><span data-stu-id="5b30c-230">For example, 2.14.3.0 or 2.14.3.0 2.16.0.0.</span></span> <span data-ttu-id="5b30c-231">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5b30c-231">Required.</span></span> |
| <span data-ttu-id="5b30c-232">**newVersion**</span><span class="sxs-lookup"><span data-stu-id="5b30c-232">**newVersion**</span></span> | <span data-ttu-id="5b30c-233">Especifica la versión del ensamblado de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="5b30c-233">Specifies the replacement assembly version.</span></span> <span data-ttu-id="5b30c-234">Use la sintaxis de versión de cuatro partes nnnnn. nnnnn. nnnnn. nnnnn.</span><span class="sxs-lookup"><span data-stu-id="5b30c-234">Use four-part version syntax nnnnn.nnnnn.nnnnn.nnnnn.</span></span>                                                                                                                                     |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b30c-235">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b30c-235">Remarks</span></span>

<span data-ttu-id="5b30c-236">Los archivos de configuración del publicador no especifican archivos.</span><span class="sxs-lookup"><span data-stu-id="5b30c-236">Publisher configuration files do not specify files.</span></span> <span data-ttu-id="5b30c-237">Tenga en cuenta que los archivos de directivas específicos del idioma son independientes del archivo de configuración del publicador.</span><span class="sxs-lookup"><span data-stu-id="5b30c-237">Note that language-specific policy files are separate from the publisher configuration file.</span></span>

## <a name="example"></a><span data-ttu-id="5b30c-238">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5b30c-238">Example</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.6.0.Proseware.Research.SampleAssembly" version="1.0.1.0" language="en-us" processorArchitecture="x86"/>
<dependency>
<dependentAssembly>
<assemblyIdentity type="win32" publicKeyToken="0000000000000000" name="Proseware.Research.SampleAssembly" language="en-us" processorArchitecture="x86"/>
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.1.0"/>
</dependentAssembly>
</dependency>
</assembly>
```

 

 





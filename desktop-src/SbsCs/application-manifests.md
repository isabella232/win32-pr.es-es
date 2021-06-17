---
description: Un manifiesto de aplicación es un archivo XML que describe e identifica los ensamblados en paralelo, compartidos y privados, a los que debe enlazarse una aplicación en tiempo de ejecución.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Manifiestos de aplicación
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: 2fb7297310102134dfcacf0e5f0d907fbf3a3e0b
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230241"
---
# <a name="application-manifests"></a><span data-ttu-id="32c93-103">Manifiestos de aplicación</span><span class="sxs-lookup"><span data-stu-id="32c93-103">Application Manifests</span></span>

<span data-ttu-id="32c93-104">Un manifiesto de aplicación es un archivo XML que describe e identifica los ensamblados en paralelo, compartidos y privados, a los que debe enlazarse una aplicación en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="32c93-104">An application manifest is an XML file that describes and identifies the shared and private side-by-side assemblies that an application should bind to at run time.</span></span> <span data-ttu-id="32c93-105">Deben ser las mismas versiones de ensamblado utilizadas para probar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32c93-105">These should be the same assembly versions that were used to test the application.</span></span> <span data-ttu-id="32c93-106">Los manifiestos de aplicación también describen los metadatos para archivos privados de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32c93-106">Application manifests may also describe metadata for files that are private to the application.</span></span>

<span data-ttu-id="32c93-107">Para obtener una lista completa del esquema XML, vea [Esquema de archivo de manifiesto.](manifest-file-schema.md)</span><span class="sxs-lookup"><span data-stu-id="32c93-107">For a complete listing of the XML schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="32c93-108">Los manifiestos de aplicación tienen los siguientes elementos y atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-108">Application manifests have the following elements and attributes.</span></span>

| <span data-ttu-id="32c93-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="32c93-109">Element</span></span>                               | <span data-ttu-id="32c93-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="32c93-110">Attributes</span></span>                | <span data-ttu-id="32c93-111">Requerido</span><span class="sxs-lookup"><span data-stu-id="32c93-111">Required</span></span> |
|---------------------------------------|---------------------------|----------|
| <span data-ttu-id="32c93-112">**ensamblado**</span><span class="sxs-lookup"><span data-stu-id="32c93-112">**assembly**</span></span>                          |                           | <span data-ttu-id="32c93-113">Sí</span><span class="sxs-lookup"><span data-stu-id="32c93-113">Yes</span></span>      |
|                                       | <span data-ttu-id="32c93-114">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="32c93-114">**manifestVersion**</span></span>       | <span data-ttu-id="32c93-115">Sí</span><span class="sxs-lookup"><span data-stu-id="32c93-115">Yes</span></span>      |
| <span data-ttu-id="32c93-116">**noInherit**</span><span class="sxs-lookup"><span data-stu-id="32c93-116">**noInherit**</span></span>                         |                           | <span data-ttu-id="32c93-117">No</span><span class="sxs-lookup"><span data-stu-id="32c93-117">No</span></span>       |
| <span data-ttu-id="32c93-118">**Assemblyidentity**</span><span class="sxs-lookup"><span data-stu-id="32c93-118">**assemblyIdentity**</span></span>                  |                           | <span data-ttu-id="32c93-119">Sí</span><span class="sxs-lookup"><span data-stu-id="32c93-119">Yes</span></span>      |
|                                       | <span data-ttu-id="32c93-120">**type**</span><span class="sxs-lookup"><span data-stu-id="32c93-120">**type**</span></span>                  | <span data-ttu-id="32c93-121">Sí</span><span class="sxs-lookup"><span data-stu-id="32c93-121">Yes</span></span>      |
|                                       | <span data-ttu-id="32c93-122">**name**</span><span class="sxs-lookup"><span data-stu-id="32c93-122">**name**</span></span>                  | <span data-ttu-id="32c93-123">Sí</span><span class="sxs-lookup"><span data-stu-id="32c93-123">Yes</span></span>      |
|                                       | <span data-ttu-id="32c93-124">**language**</span><span class="sxs-lookup"><span data-stu-id="32c93-124">**language**</span></span>              | <span data-ttu-id="32c93-125">No</span><span class="sxs-lookup"><span data-stu-id="32c93-125">No</span></span>       |
|                                       | <span data-ttu-id="32c93-126">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="32c93-126">**processorArchitecture**</span></span> | <span data-ttu-id="32c93-127">No</span><span class="sxs-lookup"><span data-stu-id="32c93-127">No</span></span>       |
|                                       | <span data-ttu-id="32c93-128">**version**</span><span class="sxs-lookup"><span data-stu-id="32c93-128">**version**</span></span>               | <span data-ttu-id="32c93-129">Sí</span><span class="sxs-lookup"><span data-stu-id="32c93-129">Yes</span></span>      |
|                                       | <span data-ttu-id="32c93-130">**Publickeytoken**</span><span class="sxs-lookup"><span data-stu-id="32c93-130">**publicKeyToken**</span></span>        | <span data-ttu-id="32c93-131">No</span><span class="sxs-lookup"><span data-stu-id="32c93-131">No</span></span>       |
| <span data-ttu-id="32c93-132">**Compatibilidad**</span><span class="sxs-lookup"><span data-stu-id="32c93-132">**compatibility**</span></span>                     |                           | <span data-ttu-id="32c93-133">No</span><span class="sxs-lookup"><span data-stu-id="32c93-133">No</span></span>       |
| <span data-ttu-id="32c93-134">**application**</span><span class="sxs-lookup"><span data-stu-id="32c93-134">**application**</span></span>                       |                           | <span data-ttu-id="32c93-135">No</span><span class="sxs-lookup"><span data-stu-id="32c93-135">No</span></span>       |
| <span data-ttu-id="32c93-136">**supportedOS**</span><span class="sxs-lookup"><span data-stu-id="32c93-136">**supportedOS**</span></span>                       | <span data-ttu-id="32c93-137">**Id**</span><span class="sxs-lookup"><span data-stu-id="32c93-137">**Id**</span></span>                    | <span data-ttu-id="32c93-138">No</span><span class="sxs-lookup"><span data-stu-id="32c93-138">No</span></span>       |
| <span data-ttu-id="32c93-139">**maxversiontested**</span><span class="sxs-lookup"><span data-stu-id="32c93-139">**maxversiontested**</span></span>                  | <span data-ttu-id="32c93-140">**Id**</span><span class="sxs-lookup"><span data-stu-id="32c93-140">**Id**</span></span>                    | <span data-ttu-id="32c93-141">No</span><span class="sxs-lookup"><span data-stu-id="32c93-141">No</span></span>       |
| <span data-ttu-id="32c93-142">**Dependencia**</span><span class="sxs-lookup"><span data-stu-id="32c93-142">**dependency**</span></span>                        |                           | <span data-ttu-id="32c93-143">No</span><span class="sxs-lookup"><span data-stu-id="32c93-143">No</span></span>       |
| <span data-ttu-id="32c93-144">**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="32c93-144">**dependentAssembly**</span></span>                 |                           | <span data-ttu-id="32c93-145">No</span><span class="sxs-lookup"><span data-stu-id="32c93-145">No</span></span>       |
| <span data-ttu-id="32c93-146">**file**</span><span class="sxs-lookup"><span data-stu-id="32c93-146">**file**</span></span>                              |                           | <span data-ttu-id="32c93-147">No</span><span class="sxs-lookup"><span data-stu-id="32c93-147">No</span></span>       |
|                                       | <span data-ttu-id="32c93-148">**name**</span><span class="sxs-lookup"><span data-stu-id="32c93-148">**name**</span></span>                  | <span data-ttu-id="32c93-149">No</span><span class="sxs-lookup"><span data-stu-id="32c93-149">No</span></span>       |
|                                       | <span data-ttu-id="32c93-150">**hashalg**</span><span class="sxs-lookup"><span data-stu-id="32c93-150">**hashalg**</span></span>               | <span data-ttu-id="32c93-151">No</span><span class="sxs-lookup"><span data-stu-id="32c93-151">No</span></span>       |
|                                       | <span data-ttu-id="32c93-152">**hash**</span><span class="sxs-lookup"><span data-stu-id="32c93-152">**hash**</span></span>                  | <span data-ttu-id="32c93-153">No</span><span class="sxs-lookup"><span data-stu-id="32c93-153">No</span></span>       |
| <span data-ttu-id="32c93-154">**activeCodePage**</span><span class="sxs-lookup"><span data-stu-id="32c93-154">**activeCodePage**</span></span>                    |                           | <span data-ttu-id="32c93-155">No</span><span class="sxs-lookup"><span data-stu-id="32c93-155">No</span></span>       |
| <span data-ttu-id="32c93-156">**autoElevate**</span><span class="sxs-lookup"><span data-stu-id="32c93-156">**autoElevate**</span></span>                       |                           | <span data-ttu-id="32c93-157">No</span><span class="sxs-lookup"><span data-stu-id="32c93-157">No</span></span>       |
| <span data-ttu-id="32c93-158">**disableTheming**</span><span class="sxs-lookup"><span data-stu-id="32c93-158">**disableTheming**</span></span>                    |                           | <span data-ttu-id="32c93-159">No</span><span class="sxs-lookup"><span data-stu-id="32c93-159">No</span></span>       |
| <span data-ttu-id="32c93-160">**disableWindowFiltering**</span><span class="sxs-lookup"><span data-stu-id="32c93-160">**disableWindowFiltering**</span></span>            |                           | <span data-ttu-id="32c93-161">No</span><span class="sxs-lookup"><span data-stu-id="32c93-161">No</span></span>       |
| <span data-ttu-id="32c93-162">**pppAware**</span><span class="sxs-lookup"><span data-stu-id="32c93-162">**dpiAware**</span></span>                          |                           | <span data-ttu-id="32c93-163">No</span><span class="sxs-lookup"><span data-stu-id="32c93-163">No</span></span>       |
| <span data-ttu-id="32c93-164">**pppAwareness**</span><span class="sxs-lookup"><span data-stu-id="32c93-164">**dpiAwareness**</span></span>                      |                           | <span data-ttu-id="32c93-165">No</span><span class="sxs-lookup"><span data-stu-id="32c93-165">No</span></span>       |
| <span data-ttu-id="32c93-166">**gdiScaling**</span><span class="sxs-lookup"><span data-stu-id="32c93-166">**gdiScaling**</span></span>                        |                           | <span data-ttu-id="32c93-167">No</span><span class="sxs-lookup"><span data-stu-id="32c93-167">No</span></span>       |
| <span data-ttu-id="32c93-168">**highResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="32c93-168">**highResolutionScrollingAware**</span></span>      |                           | <span data-ttu-id="32c93-169">No</span><span class="sxs-lookup"><span data-stu-id="32c93-169">No</span></span>       |
| <span data-ttu-id="32c93-170">**longPathAware**</span><span class="sxs-lookup"><span data-stu-id="32c93-170">**longPathAware**</span></span>                     |                           | <span data-ttu-id="32c93-171">No</span><span class="sxs-lookup"><span data-stu-id="32c93-171">No</span></span>       |
| <span data-ttu-id="32c93-172">**printerDriverIsolation**</span><span class="sxs-lookup"><span data-stu-id="32c93-172">**printerDriverIsolation**</span></span>            |                           | <span data-ttu-id="32c93-173">No</span><span class="sxs-lookup"><span data-stu-id="32c93-173">No</span></span>       |
| <span data-ttu-id="32c93-174">**ultraHighResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="32c93-174">**ultraHighResolutionScrollingAware**</span></span> |                           | <span data-ttu-id="32c93-175">No</span><span class="sxs-lookup"><span data-stu-id="32c93-175">No</span></span>       |
| <span data-ttu-id="32c93-176">**msix**</span><span class="sxs-lookup"><span data-stu-id="32c93-176">**msix**</span></span>                              |                           | <span data-ttu-id="32c93-177">No</span><span class="sxs-lookup"><span data-stu-id="32c93-177">No</span></span>       |
| <span data-ttu-id="32c93-178">**heapType**</span><span class="sxs-lookup"><span data-stu-id="32c93-178">**heapType**</span></span>                          |                           | <span data-ttu-id="32c93-179">No</span><span class="sxs-lookup"><span data-stu-id="32c93-179">No</span></span>       |

## <a name="file-location"></a><span data-ttu-id="32c93-180">Ubicación del archivo</span><span class="sxs-lookup"><span data-stu-id="32c93-180">File Location</span></span>

<span data-ttu-id="32c93-181">Los manifiestos de aplicación deben incluirse como un recurso en el archivo EXE o dll de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32c93-181">Application manifests should be included as a resource in the application's EXE file or DLL.</span></span>

<span data-ttu-id="32c93-182">Para obtener más información, vea [Installing Side-by-side Assemblies](installing-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="32c93-182">For more information, see [Installing Side-by-side Assemblies](installing-side-by-side-assemblies.md).</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="32c93-183">Sintaxis de los nombres de archivo</span><span class="sxs-lookup"><span data-stu-id="32c93-183">File Name Syntax</span></span>

<span data-ttu-id="32c93-184">El nombre de un archivo de manifiesto de aplicación es el nombre del ejecutable de la aplicación seguido de .manifest.</span><span class="sxs-lookup"><span data-stu-id="32c93-184">The name of an application manifest file is the name of the application's executable followed by .manifest.</span></span>

<span data-ttu-id="32c93-185">Por ejemplo, un manifiesto de aplicación que hace referencia a example.exe o example.dll usaría la siguiente sintaxis de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="32c93-185">For example, an application manifest that refers to example.exe or example.dll would use the following file name syntax.</span></span> <span data-ttu-id="32c93-186">Puede omitir el identificador <*de recurso>* campo si el identificador de recurso es 1.</span><span class="sxs-lookup"><span data-stu-id="32c93-186">You can omit the <*resource ID*> field if resource ID is 1.</span></span>

<span data-ttu-id="32c93-187">**example.exe.<*id. de recurso*>.manifest**</span><span class="sxs-lookup"><span data-stu-id="32c93-187">**example.exe.<*resource ID*>.manifest**</span></span>

<span data-ttu-id="32c93-188">**example.dll.<*id. de recurso*>.manifest**</span><span class="sxs-lookup"><span data-stu-id="32c93-188">**example.dll.<*resource ID*>.manifest**</span></span>

## <a name="elements"></a><span data-ttu-id="32c93-189">Elementos</span><span class="sxs-lookup"><span data-stu-id="32c93-189">Elements</span></span>

<span data-ttu-id="32c93-190">Los nombres de elementos y atributos distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="32c93-190">Names of elements and attributes are case-sensitive.</span></span> <span data-ttu-id="32c93-191">Los valores de elementos y atributos no tienen en cuenta las mayúsculas y minúsculas, excepto el valor del atributo type.</span><span class="sxs-lookup"><span data-stu-id="32c93-191">The values of elements and attributes are case-insensitive, except for the value of the type attribute.</span></span>

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a><span data-ttu-id="32c93-192">ensamblado</span><span class="sxs-lookup"><span data-stu-id="32c93-192">assembly</span></span>

<span data-ttu-id="32c93-193">Elemento contenedor.</span><span class="sxs-lookup"><span data-stu-id="32c93-193">A container element.</span></span> <span data-ttu-id="32c93-194">Su primer subelemento debe ser **un elemento noInherit** **o assemblyIdentity.**</span><span class="sxs-lookup"><span data-stu-id="32c93-194">Its first subelement must be a **noInherit** or **assemblyIdentity** element.</span></span> <span data-ttu-id="32c93-195">Necesario.</span><span class="sxs-lookup"><span data-stu-id="32c93-195">Required.</span></span>

<span data-ttu-id="32c93-196">El **elemento** de ensamblado debe estar en el espacio de nombres "urn:schemas-microsoft-com:asm.v1".</span><span class="sxs-lookup"><span data-stu-id="32c93-196">The **assembly** element must be in the namespace "urn:schemas-microsoft-com:asm.v1".</span></span> <span data-ttu-id="32c93-197">Los elementos secundarios del ensamblado también deben estar en este espacio de nombres, mediante herencia o etiquetado.</span><span class="sxs-lookup"><span data-stu-id="32c93-197">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="32c93-198">El **elemento** assembly tiene los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-198">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="32c93-199">Atributo</span><span class="sxs-lookup"><span data-stu-id="32c93-199">Attribute</span></span>           | <span data-ttu-id="32c93-200">Descripción</span><span class="sxs-lookup"><span data-stu-id="32c93-200">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="32c93-201">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="32c93-201">**manifestVersion**</span></span> | <span data-ttu-id="32c93-202">El **atributo manifestVersion** debe establecerse en 1.0.</span><span class="sxs-lookup"><span data-stu-id="32c93-202">The **manifestVersion** attribute must be set to 1.0.</span></span> |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a><span data-ttu-id="32c93-203">noInherit</span><span class="sxs-lookup"><span data-stu-id="32c93-203">noInherit</span></span>

<span data-ttu-id="32c93-204">Incluya este elemento en un manifiesto de aplicación para establecer los contextos de activación [generados](activation-contexts.md) a partir del manifiesto con la marca "no inherit".</span><span class="sxs-lookup"><span data-stu-id="32c93-204">Include this element in an application manifest to set the [activation contexts](activation-contexts.md) generated from the manifest with the "no inherit" flag.</span></span> <span data-ttu-id="32c93-205">Cuando esta marca no se establece en un contexto de activación y el contexto de activación está activo, lo heredan los nuevos subprocesos en el mismo proceso, ventanas, procedimientos de ventana y llamadas a [procedimientos asincrónicos](/windows/desktop/Sync/asynchronous-procedure-calls).</span><span class="sxs-lookup"><span data-stu-id="32c93-205">When this flag is not set in an activation context, and the activation context is active, it is inherited by new threads in the same process, windows, window procedures, and [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span> <span data-ttu-id="32c93-206">Establecer esta marca impide que el nuevo objeto herede el contexto activo.</span><span class="sxs-lookup"><span data-stu-id="32c93-206">Setting this flag prevents the new object from inheriting the active context.</span></span>

<span data-ttu-id="32c93-207">El **elemento noInherit** es opcional y normalmente se omite.</span><span class="sxs-lookup"><span data-stu-id="32c93-207">The **noInherit** element is optional and typically omitted.</span></span> <span data-ttu-id="32c93-208">La mayoría de los ensamblados no funcionan correctamente mediante un contexto de activación que no hereda porque el ensamblado debe diseñarse explícitamente para administrar la propagación de su propio contexto de activación.</span><span class="sxs-lookup"><span data-stu-id="32c93-208">Most assemblies do not work correctly using a no-inherit activation context because the assembly must be explicitly designed to manage the propagation of their own activation context.</span></span> <span data-ttu-id="32c93-209">El uso del **elemento noInherit** requiere que los ensamblados dependientes a los que hace referencia el manifiesto de aplicación tengan **un elemento noInherit** en su manifiesto [de ensamblado.](assembly-manifests.md)</span><span class="sxs-lookup"><span data-stu-id="32c93-209">The use of the **noInherit** element requires that any dependent assemblies referenced by the application manifest have a **noInherit** element in their [assembly manifest](assembly-manifests.md).</span></span>

<span data-ttu-id="32c93-210">Si **noInherit se** usa en un manifiesto, debe ser el primer subelemento del **elemento de** ensamblado.</span><span class="sxs-lookup"><span data-stu-id="32c93-210">If **noInherit** is used in a manifest, it must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="32c93-211">El **elemento assemblyIdentity** debe ir inmediatamente después del **elemento noInherit.**</span><span class="sxs-lookup"><span data-stu-id="32c93-211">The **assemblyIdentity** element should come immediately after the **noInherit** element.</span></span> <span data-ttu-id="32c93-212">Si **no se usa noInherit,** **assemblyIdentity** debe ser el primer subelemento del **elemento de** ensamblado.</span><span class="sxs-lookup"><span data-stu-id="32c93-212">If **noInherit** is not used, **assemblyIdentity** must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="32c93-213">El **elemento noInherit** no tiene elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="32c93-213">The **noInherit** element has no child elements.</span></span> <span data-ttu-id="32c93-214">No es un elemento válido en los [manifiestos de ensamblado.](assembly-manifests.md)</span><span class="sxs-lookup"><span data-stu-id="32c93-214">It is not a valid element in [assembly manifests](assembly-manifests.md).</span></span>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a><span data-ttu-id="32c93-215">assemblyIdentity</span><span class="sxs-lookup"><span data-stu-id="32c93-215">assemblyIdentity</span></span>

<span data-ttu-id="32c93-216">Como primer subelemento de un elemento **de** ensamblado, **assemblyIdentity** describe e identifica de forma única la aplicación propietaria de este manifiesto de aplicación.</span><span class="sxs-lookup"><span data-stu-id="32c93-216">As the first subelement of an **assembly** element, **assemblyIdentity** describes and uniquely identifies the application owning this application manifest.</span></span> <span data-ttu-id="32c93-217">Como primer subelemento de un **elemento dependentAssembly,** **assemblyIdentity** describe un ensamblado en paralelo requerido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32c93-217">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="32c93-218">Tenga en cuenta que todos los ensamblados a los que se hace referencia en el manifiesto de aplicación requieren una **assemblyIdentity** que coincida exactamente con **assemblyIdentity** en el propio manifiesto de ensamblado del ensamblado al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="32c93-218">Note that every assembly referenced in the application manifest requires an **assemblyIdentity** that exactly matches the **assemblyIdentity** in the referenced assembly's own assembly manifest.</span></span>

<span data-ttu-id="32c93-219">El **elemento assemblyIdentity** tiene los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="32c93-219">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="32c93-220">No tiene subelementos.</span><span class="sxs-lookup"><span data-stu-id="32c93-220">It has no subelements.</span></span>

| <span data-ttu-id="32c93-221">Atributo</span><span class="sxs-lookup"><span data-stu-id="32c93-221">Attribute</span></span>                 | <span data-ttu-id="32c93-222">Descripción</span><span class="sxs-lookup"><span data-stu-id="32c93-222">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32c93-223">**type**</span><span class="sxs-lookup"><span data-stu-id="32c93-223">**type**</span></span>                  | <span data-ttu-id="32c93-224">Especifica el tipo de aplicación o ensamblado.</span><span class="sxs-lookup"><span data-stu-id="32c93-224">Specifies the application or assembly type.</span></span> <span data-ttu-id="32c93-225">El valor debe ser Win32 y todo en minúsculas.</span><span class="sxs-lookup"><span data-stu-id="32c93-225">The value must be Win32 and all in lower case.</span></span> <span data-ttu-id="32c93-226">Necesario.</span><span class="sxs-lookup"><span data-stu-id="32c93-226">Required.</span></span>                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="32c93-227">**name**</span><span class="sxs-lookup"><span data-stu-id="32c93-227">**name**</span></span>                  | <span data-ttu-id="32c93-228">Nombra de forma única la aplicación o el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="32c93-228">Uniquely names the application or assembly.</span></span> <span data-ttu-id="32c93-229">Use el formato siguiente para el nombre: Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="32c93-229">Use the following format for the name: Organization.Division.Name.</span></span> <span data-ttu-id="32c93-230">Por ejemplo, Microsoft.Windows.mysampleApp.</span><span class="sxs-lookup"><span data-stu-id="32c93-230">For example Microsoft.Windows.mysampleApp.</span></span> <span data-ttu-id="32c93-231">Necesario.</span><span class="sxs-lookup"><span data-stu-id="32c93-231">Required.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="32c93-232">**language**</span><span class="sxs-lookup"><span data-stu-id="32c93-232">**language**</span></span>              | <span data-ttu-id="32c93-233">Identifica el idioma de la aplicación o ensamblado.</span><span class="sxs-lookup"><span data-stu-id="32c93-233">Identifies the language of the application or assembly.</span></span> <span data-ttu-id="32c93-234">Opcional.</span><span class="sxs-lookup"><span data-stu-id="32c93-234">Optional.</span></span> <span data-ttu-id="32c93-235">Si la aplicación o el ensamblado son específicos del lenguaje, especifique el código de lenguaje DHTML.</span><span class="sxs-lookup"><span data-stu-id="32c93-235">If the application or assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="32c93-236">En **assemblyIdentity de una** aplicación destinada a uso internacional (idioma neutro) omita el atributo language.</span><span class="sxs-lookup"><span data-stu-id="32c93-236">In the **assemblyIdentity** of an application intended for worldwide use (language neutral) omit the language attribute.</span></span><br/> <span data-ttu-id="32c93-237">En un **ensambladoIdentidad de** un ensamblado destinado a uso internacional (idioma neutro) establezca el valor de language en " \* ".</span><span class="sxs-lookup"><span data-stu-id="32c93-237">In an **assemblyIdentity** of an assembly intended for worldwide use (language neutral) set the value of language to "\*".</span></span><br/> |
| <span data-ttu-id="32c93-238">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="32c93-238">**processorArchitecture**</span></span> | <span data-ttu-id="32c93-239">Especifica el procesador.</span><span class="sxs-lookup"><span data-stu-id="32c93-239">Specifies the processor.</span></span> <span data-ttu-id="32c93-240">Entre los valores válidos se incluyen `x86`, `amd64`, `arm` y `arm64`.</span><span class="sxs-lookup"><span data-stu-id="32c93-240">Valid values include `x86`, `amd64`, `arm` and `arm64`.</span></span> <span data-ttu-id="32c93-241">Opcional.</span><span class="sxs-lookup"><span data-stu-id="32c93-241">Optional.</span></span>                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="32c93-242">**version**</span><span class="sxs-lookup"><span data-stu-id="32c93-242">**version**</span></span>               | <span data-ttu-id="32c93-243">Especifica la versión de la aplicación o del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="32c93-243">Specifies the application or assembly version.</span></span> <span data-ttu-id="32c93-244">Use el formato de versión de cuatro partes: mmmmm.nnnnn.ooooo.ppppp.</span><span class="sxs-lookup"><span data-stu-id="32c93-244">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="32c93-245">Cada una de las partes separadas por puntos puede ser de 0 a 65535, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="32c93-245">Each of the parts separated by periods can be 0-65535 inclusive.</span></span> <span data-ttu-id="32c93-246">Para obtener más información, vea [Versiones de ensamblado.](assembly-versions.md)</span><span class="sxs-lookup"><span data-stu-id="32c93-246">For more information, see [Assembly Versions](assembly-versions.md).</span></span> <span data-ttu-id="32c93-247">Necesario.</span><span class="sxs-lookup"><span data-stu-id="32c93-247">Required.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="32c93-248">**Publickeytoken**</span><span class="sxs-lookup"><span data-stu-id="32c93-248">**publicKeyToken**</span></span>        | <span data-ttu-id="32c93-249">Cadena hexadecimal de 16 caracteres que representa los últimos 8 bytes del hash SHA-1 de la clave pública con la que se firma la aplicación o el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="32c93-249">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the application or assembly is signed.</span></span> <span data-ttu-id="32c93-250">La clave pública que se usa para firmar el catálogo debe ser de 2048 bits o superior.</span><span class="sxs-lookup"><span data-stu-id="32c93-250">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="32c93-251">Necesario para todos los ensamblados en paralelo compartidos.</span><span class="sxs-lookup"><span data-stu-id="32c93-251">Required for all shared side-by-side assemblies.</span></span>                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a><span data-ttu-id="32c93-252">compatibilidad</span><span class="sxs-lookup"><span data-stu-id="32c93-252">compatibility</span></span>

<span data-ttu-id="32c93-253">Contiene al menos una **aplicación**.</span><span class="sxs-lookup"><span data-stu-id="32c93-253">Contains at least one **application**.</span></span> <span data-ttu-id="32c93-254">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-254">It has no attributes.</span></span> <span data-ttu-id="32c93-255">Opcional.</span><span class="sxs-lookup"><span data-stu-id="32c93-255">Optional.</span></span> <span data-ttu-id="32c93-256">Los manifiestos de aplicación sin un elemento de compatibilidad tienen como valor predeterminado la compatibilidad de Windows Vista en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="32c93-256">Application manifests without a compatibility element default to Windows Vista compatibility on Windows 7.</span></span>

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a><span data-ttu-id="32c93-257">application</span><span class="sxs-lookup"><span data-stu-id="32c93-257">application</span></span>

<span data-ttu-id="32c93-258">Contiene al menos un **elemento supportedOS.**</span><span class="sxs-lookup"><span data-stu-id="32c93-258">Contains at least one **supportedOS** element.</span></span> <span data-ttu-id="32c93-259">A partir Windows 10, versión 1903, también puede contener un **elemento maxversiontested** opcional.</span><span class="sxs-lookup"><span data-stu-id="32c93-259">Starting in Windows 10, version 1903, it can also contain one optional **maxversiontested** element.</span></span> <span data-ttu-id="32c93-260">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-260">It has no attributes.</span></span> <span data-ttu-id="32c93-261">Opcional.</span><span class="sxs-lookup"><span data-stu-id="32c93-261">Optional.</span></span>

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a><span data-ttu-id="32c93-262">supportedOS</span><span class="sxs-lookup"><span data-stu-id="32c93-262">supportedOS</span></span>

<span data-ttu-id="32c93-263">El **elemento supportedOS** tiene el atributo siguiente.</span><span class="sxs-lookup"><span data-stu-id="32c93-263">The **supportedOS** element has the following attribute.</span></span> <span data-ttu-id="32c93-264">No tiene subelementos.</span><span class="sxs-lookup"><span data-stu-id="32c93-264">It has no subelements.</span></span>

| <span data-ttu-id="32c93-265">Atributo</span><span class="sxs-lookup"><span data-stu-id="32c93-265">Attribute</span></span> | <span data-ttu-id="32c93-266">Descripción</span><span class="sxs-lookup"><span data-stu-id="32c93-266">Description</span></span>   |
|-----------|-----------------------|
| <span data-ttu-id="32c93-267">**Id**</span><span class="sxs-lookup"><span data-stu-id="32c93-267">**Id**</span></span>    | <span data-ttu-id="32c93-268">Establezca el atributo Id en **{e2011457-1546-43c5-a5fe-008deee3d3f0}** para ejecutar la aplicación mediante la funcionalidad vista.</span><span class="sxs-lookup"><span data-stu-id="32c93-268">Set the Id attribute to **{e2011457-1546-43c5-a5fe-008deee3d3f0}** to run the application using Vista functionality.</span></span> <span data-ttu-id="32c93-269">Esto puede permitir que una aplicación diseñada para Windows Vista se ejecute en un sistema operativo posterior.</span><span class="sxs-lookup"><span data-stu-id="32c93-269">This can enable an application designed for Windows Vista to run on a later operating system.</span></span> <br/> <span data-ttu-id="32c93-270">Establezca el atributo Id en **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** para ejecutar la aplicación con la funcionalidad de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="32c93-270">Set the Id attribute to **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** to run the application using Windows 7 functionality.</span></span><br/> <span data-ttu-id="32c93-271">Las aplicaciones que admiten Windows Vista, Windows 7 y Windows 8 no requieren manifiestos independientes.</span><span class="sxs-lookup"><span data-stu-id="32c93-271">Applications that support Windows Vista, Windows 7, and Windows 8 functionality do not require separate manifests.</span></span> <span data-ttu-id="32c93-272">En este caso, agregue los GUID para todos los sistemas operativos Windows.</span><span class="sxs-lookup"><span data-stu-id="32c93-272">In this case, add the GUIDs for all the Windows operating systems.</span></span><br/> <span data-ttu-id="32c93-273">Para obtener información sobre el **comportamiento del** atributo Id en Windows, vea la guía Windows 8 y compatibilidad de Windows [Server 2012](https://www.microsoft.com/download/details.aspx?id=27416).</span><span class="sxs-lookup"><span data-stu-id="32c93-273">For info about the **Id** attribute behavior in Windows, see the [Windows 8 and Windows Server 2012 Compatibility Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).</span></span><br/> <span data-ttu-id="32c93-274">Los siguientes GUID se corresponden con los sistemas operativos indicados:</span><span class="sxs-lookup"><span data-stu-id="32c93-274">The following GUIDs correspond with the indicated operating systems:</span></span><br/> <span data-ttu-id="32c93-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 y Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="32c93-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 and Windows Server 2019</span></span><br/> <span data-ttu-id="32c93-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 y Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="32c93-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 and Windows Server 2012 R2</span></span><br/> <span data-ttu-id="32c93-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 y Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="32c93-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 and Windows Server 2012</span></span><br/> <span data-ttu-id="32c93-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 y Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="32c93-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 and Windows Server 2008 R2</span></span><br/> <span data-ttu-id="32c93-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista y Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32c93-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista and Windows Server 2008</span></span><br/> <span data-ttu-id="32c93-280">Para probar esto en Windows 7 o Windows 8.x, ejecute Monitor de recursos (resmon), vaya a la pestaña CPU, haga clic con el botón derecho en las etiquetas de columna, "Seleccionar columna..." y active "Contexto del sistema operativo".</span><span class="sxs-lookup"><span data-stu-id="32c93-280">You can test this on Windows 7 or Windows 8.x by running Resource Monitor (resmon), going to the CPU tab, right-clicking on the column labels, "Select Column...", and check "Operating System Context".</span></span> <span data-ttu-id="32c93-281">En Windows 8.x, también puede encontrar esta columna disponible en el Administrador de tareas (taskmgr).</span><span class="sxs-lookup"><span data-stu-id="32c93-281">On Windows 8.x, you can also find this column available in the Task Manager (taskmgr).</span></span> <span data-ttu-id="32c93-282">El contenido de la columna muestra el valor más alto encontrado o "Windows Vista" como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="32c93-282">The content of the column shows the highest value found or "Windows Vista" as the default.</span></span> <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a><span data-ttu-id="32c93-283">maxversiontested</span><span class="sxs-lookup"><span data-stu-id="32c93-283">maxversiontested</span></span>

<span data-ttu-id="32c93-284">El **elemento maxversiontested** especifica las versiones de Windows con las que se ha probado la aplicación a partir de la versión mínima del sistema operativo que admite la aplicación hasta la versión máxima.</span><span class="sxs-lookup"><span data-stu-id="32c93-284">The **maxversiontested** element specifies the versions of Windows that the application was tested against starting with the minimum OS version the application supports up to the maximum version.</span></span> <span data-ttu-id="32c93-285">El conjunto completo de versiones se puede encontrar [aquí.](https://developer.microsoft.com/windows/downloads/sdk-archive/)</span><span class="sxs-lookup"><span data-stu-id="32c93-285">The complete set of versions can be found [here](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span> <span data-ttu-id="32c93-286">Esto está pensado para que lo usen las aplicaciones de escritorio que usan islas [XAML](/windows/apps/desktop/modernize/xaml-islands) y que no se implementan en un paquete MSIX.</span><span class="sxs-lookup"><span data-stu-id="32c93-286">This is intended to be used by desktop applications that use [XAML Islands](/windows/apps/desktop/modernize/xaml-islands) and that are not deployed in an MSIX package.</span></span> <span data-ttu-id="32c93-287">Este elemento se admite en Windows 10, versión 1903 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="32c93-287">This element is supported in Windows 10, version 1903, and later versions.</span></span>

<span data-ttu-id="32c93-288">El **elemento maxversiontested** tiene el atributo siguiente.</span><span class="sxs-lookup"><span data-stu-id="32c93-288">The **maxversiontested** element has the following attribute.</span></span> <span data-ttu-id="32c93-289">No tiene subelementos.</span><span class="sxs-lookup"><span data-stu-id="32c93-289">It has no subelements.</span></span>

| <span data-ttu-id="32c93-290">Atributo</span><span class="sxs-lookup"><span data-stu-id="32c93-290">Attribute</span></span> | <span data-ttu-id="32c93-291">Descripción</span><span class="sxs-lookup"><span data-stu-id="32c93-291">Description</span></span>    |
|-----------|----------------|
| <span data-ttu-id="32c93-292">**Id**</span><span class="sxs-lookup"><span data-stu-id="32c93-292">**Id**</span></span>    | <span data-ttu-id="32c93-293">Establezca el atributo Id en una cadena de versión de 4 partes que especifique la versión máxima de Windows con la que se probó la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32c93-293">Set the Id attribute to a 4-part version string that specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="32c93-294">Por ejemplo, "10.0.18226.0".</span><span class="sxs-lookup"><span data-stu-id="32c93-294">For example, "10.0.18226.0".</span></span> |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a><span data-ttu-id="32c93-295">dependency</span><span class="sxs-lookup"><span data-stu-id="32c93-295">dependency</span></span>

<span data-ttu-id="32c93-296">Contiene al menos un **dependentAssembly**.</span><span class="sxs-lookup"><span data-stu-id="32c93-296">Contains at least one **dependentAssembly**.</span></span> <span data-ttu-id="32c93-297">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-297">It has no attributes.</span></span> <span data-ttu-id="32c93-298">Opcional.</span><span class="sxs-lookup"><span data-stu-id="32c93-298">Optional.</span></span>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a><span data-ttu-id="32c93-299">dependentAssembly</span><span class="sxs-lookup"><span data-stu-id="32c93-299">dependentAssembly</span></span>

<span data-ttu-id="32c93-300">El primer subelemento de **dependentAssembly** debe ser un **elemento assemblyIdentity** que describa un ensamblado en paralelo requerido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32c93-300">The first subelement of **dependentAssembly** must be an **assemblyIdentity** element that describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="32c93-301">Cada **dependentAssembly debe** estar dentro de exactamente una **dependencia**.</span><span class="sxs-lookup"><span data-stu-id="32c93-301">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="32c93-302">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-302">It has no attributes.</span></span>

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a><span data-ttu-id="32c93-303">archivo</span><span class="sxs-lookup"><span data-stu-id="32c93-303">file</span></span>

<span data-ttu-id="32c93-304">Especifica los archivos que son privados para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32c93-304">Specifies files that are private to the application.</span></span> <span data-ttu-id="32c93-305">Opcional.</span><span class="sxs-lookup"><span data-stu-id="32c93-305">Optional.</span></span>

<span data-ttu-id="32c93-306">El **elemento** file tiene los atributos que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="32c93-306">The **file** element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="32c93-307">Atributo</span><span class="sxs-lookup"><span data-stu-id="32c93-307">Attribute</span></span>   | <span data-ttu-id="32c93-308">Descripción</span><span class="sxs-lookup"><span data-stu-id="32c93-308">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32c93-309">**name**</span><span class="sxs-lookup"><span data-stu-id="32c93-309">**name**</span></span>    | <span data-ttu-id="32c93-310">Nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="32c93-310">Name of the file.</span></span> <span data-ttu-id="32c93-311">Por ejemplo, Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="32c93-311">For example, Comctl32.dll.</span></span>                                                            |
| <span data-ttu-id="32c93-312">**hashalg**</span><span class="sxs-lookup"><span data-stu-id="32c93-312">**hashalg**</span></span> | <span data-ttu-id="32c93-313">Algoritmo utilizado para crear un hash del archivo.</span><span class="sxs-lookup"><span data-stu-id="32c93-313">Algorithm used to create a hash of the file.</span></span> <span data-ttu-id="32c93-314">Este valor debe ser SHA1.</span><span class="sxs-lookup"><span data-stu-id="32c93-314">This value should be SHA1.</span></span>                                 |
| <span data-ttu-id="32c93-315">**hash**</span><span class="sxs-lookup"><span data-stu-id="32c93-315">**hash**</span></span>    | <span data-ttu-id="32c93-316">Hash del archivo al que se hace referencia por nombre.</span><span class="sxs-lookup"><span data-stu-id="32c93-316">A hash of the file referred to by name.</span></span> <span data-ttu-id="32c93-317">Cadena hexadecimal de longitud en función del algoritmo hash.</span><span class="sxs-lookup"><span data-stu-id="32c93-317">A hexadecimal string of length depending on the hash algorithm.</span></span> |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a><span data-ttu-id="32c93-318">activeCodePage</span><span class="sxs-lookup"><span data-stu-id="32c93-318">activeCodePage</span></span>

<span data-ttu-id="32c93-319">Forzar que un proceso use UTF-8 como página de códigos del proceso.</span><span class="sxs-lookup"><span data-stu-id="32c93-319">Force a process to use UTF-8 as the process code page.</span></span>

<span data-ttu-id="32c93-320">**activeCodePage se** agregó en la versión 1903 de Windows (actualización de mayo de 2019).</span><span class="sxs-lookup"><span data-stu-id="32c93-320">**activeCodePage** was added in Windows Version 1903 (May 2019 Update).</span></span> <span data-ttu-id="32c93-321">Puede declarar esta propiedad y establecer como destino o ejecutar en compilaciones anteriores de Windows, pero debe controlar la detección y conversión de páginas de códigos heredadas como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="32c93-321">You can declare this property and target/run on earlier Windows builds, but you must handle legacy code page detection and conversion as usual.</span></span> <span data-ttu-id="32c93-322">Consulte [Uso de la página de códigos UTF-8 para](/windows/uwp/design/globalizing/use-utf8-code-page) obtener más información.</span><span class="sxs-lookup"><span data-stu-id="32c93-322">See [Use the UTF-8 code page](/windows/uwp/design/globalizing/use-utf8-code-page) for details.</span></span>

<span data-ttu-id="32c93-323">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-323">This element has no attributes.</span></span> <span data-ttu-id="32c93-324">**UTF-8 solo** es un valor válido para **el elemento activeCodePage.**</span><span class="sxs-lookup"><span data-stu-id="32c93-324">**UTF-8** is only valid value for **activeCodePage** element.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2019/WindowsSettings"> 
      <activeCodePage>UTF-8</activeCodePage> 
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="autoElevate"></span><span id="autoelevate"></span><span id="AUTOELEVATE"></span>

### <a name="autoelevate"></a><span data-ttu-id="32c93-325">autoElevate</span><span class="sxs-lookup"><span data-stu-id="32c93-325">autoElevate</span></span>

<span data-ttu-id="32c93-326">Especifica si la elevación automática está habilitada.</span><span class="sxs-lookup"><span data-stu-id="32c93-326">Specifies whether auto elevate is enabled.</span></span> <span data-ttu-id="32c93-327">**TRUE** indica que está habilitado.</span><span class="sxs-lookup"><span data-stu-id="32c93-327">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="32c93-328">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-328">It has no attributes.</span></span>

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a><span data-ttu-id="32c93-329">disableTheming</span><span class="sxs-lookup"><span data-stu-id="32c93-329">disableTheming</span></span>

<span data-ttu-id="32c93-330">Especifica si se deshabilita la entrega de un tema a los elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="32c93-330">Specifies whether giving UI elements a theme is disabled.</span></span> <span data-ttu-id="32c93-331">**TRUE** indica deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="32c93-331">**TRUE** indicates disabled.</span></span> <span data-ttu-id="32c93-332">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-332">It has no attributes.</span></span>

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a><span data-ttu-id="32c93-333">disableWindowFiltering</span><span class="sxs-lookup"><span data-stu-id="32c93-333">disableWindowFiltering</span></span>

<span data-ttu-id="32c93-334">Especifica si se va a deshabilitar el filtrado de ventanas.</span><span class="sxs-lookup"><span data-stu-id="32c93-334">Specifies whether to disable window filtering.</span></span> <span data-ttu-id="32c93-335">**TRUE** deshabilita el filtrado de ventanas para que pueda enumerar las ventanas inmersivas desde el escritorio.</span><span class="sxs-lookup"><span data-stu-id="32c93-335">**TRUE** disables window filtering so you can enumerate immersive windows from the desktop.</span></span> <span data-ttu-id="32c93-336">**disableWindowFiltering** se agregó en Windows 8 y no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-336">**disableWindowFiltering** was added in Windows 8 and has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <disableWindowFiltering>true</disableWindowFiltering>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAware"></span><span id="dpiaware"></span><span id="DPIAWARE"></span>

### <a name="dpiaware"></a><span data-ttu-id="32c93-337">dpiAware</span><span class="sxs-lookup"><span data-stu-id="32c93-337">dpiAware</span></span>

<span data-ttu-id="32c93-338">Especifica si el proceso actual es compatible con puntos por pulgada (ppp).</span><span class="sxs-lookup"><span data-stu-id="32c93-338">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="32c93-339">**Windows 10, versión 1607:** El **elemento dpiAware** se omite si **el elemento dpiAwareness** está presente.</span><span class="sxs-lookup"><span data-stu-id="32c93-339">**Windows 10, version 1607:** The **dpiAware** element is ignored if the **dpiAwareness** element is present.</span></span> <span data-ttu-id="32c93-340">Puede incluir ambos elementos en un manifiesto si desea especificar un comportamiento diferente para Windows 10, versión 1607 que para una versión anterior del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="32c93-340">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="32c93-341">En la tabla siguiente se describe el comportamiento que se produce en función de la presencia del **elemento dpiAware** y el texto que contiene.</span><span class="sxs-lookup"><span data-stu-id="32c93-341">The following table describes the behavior that results based upon the presence of the **dpiAware** element and the text that it contains.</span></span> <span data-ttu-id="32c93-342">El texto del elemento no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="32c93-342">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="32c93-343">Estado del **elemento dpiAware**</span><span class="sxs-lookup"><span data-stu-id="32c93-343">State of the **dpiAware** element</span></span> | <span data-ttu-id="32c93-344">Descripción</span><span class="sxs-lookup"><span data-stu-id="32c93-344">Description</span></span>     |
|-----------------------------------|---------|
| <span data-ttu-id="32c93-345">Absent</span><span class="sxs-lookup"><span data-stu-id="32c93-345">Absent</span></span>                            | <span data-ttu-id="32c93-346">El proceso actual no es consciente de ppp de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="32c93-346">The current process is dpi unaware by default.</span></span> <span data-ttu-id="32c93-347">Puede cambiar esta configuración mediante programación llamando a la [**función SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**o SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)</span><span class="sxs-lookup"><span data-stu-id="32c93-347">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>                                                                                                                                                            |
| <span data-ttu-id="32c93-348">Contiene "true"</span><span class="sxs-lookup"><span data-stu-id="32c93-348">Contains "true"</span></span>                   | <span data-ttu-id="32c93-349">El proceso actual es compatible con ppp del sistema.</span><span class="sxs-lookup"><span data-stu-id="32c93-349">The current process is system dpi aware.</span></span>                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="32c93-350">Contiene "false"</span><span class="sxs-lookup"><span data-stu-id="32c93-350">Contains "false"</span></span>                  | <span data-ttu-id="32c93-351">**Windows Vista, Windows 7 y Windows 8:** El comportamiento es el mismo que cuando **pppAware** está ausente.</span><span class="sxs-lookup"><span data-stu-id="32c93-351">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="32c93-352">**Windows 8.1 y Windows 10:** El proceso actual no es consciente de los valores de ppp y no se puede cambiar esta configuración mediante programación llamando a la [**función SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**o SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)</span><span class="sxs-lookup"><span data-stu-id="32c93-352">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |
| <span data-ttu-id="32c93-353">Contiene "true/pm"</span><span class="sxs-lookup"><span data-stu-id="32c93-353">Contains "true/pm"</span></span>                | <span data-ttu-id="32c93-354">**Windows Vista, Windows 7 y Windows 8:** El proceso actual es compatible con ppp del sistema.</span><span class="sxs-lookup"><span data-stu-id="32c93-354">**Windows Vista, Windows 7 and Windows 8:** The current process is system dpi aware.</span></span><br/> <span data-ttu-id="32c93-355">**Windows 8.1 y Windows 10:** El proceso actual es compatible con ppp por monitor.</span><span class="sxs-lookup"><span data-stu-id="32c93-355">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="32c93-356">Contiene "por monitor"</span><span class="sxs-lookup"><span data-stu-id="32c93-356">Contains "per monitor"</span></span>            | <span data-ttu-id="32c93-357">**Windows Vista, Windows 7 y Windows 8:** El comportamiento es el mismo que cuando **pppAware** está ausente.</span><span class="sxs-lookup"><span data-stu-id="32c93-357">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="32c93-358">**Windows 8.1 y Windows 10:** El proceso actual es compatible con ppp por monitor.</span><span class="sxs-lookup"><span data-stu-id="32c93-358">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="32c93-359">Contiene cualquier otra cadena</span><span class="sxs-lookup"><span data-stu-id="32c93-359">Contains any other string</span></span>         | <span data-ttu-id="32c93-360">**Windows Vista, Windows 7 y Windows 8:** El comportamiento es el mismo que cuando **pppAware** está ausente.</span><span class="sxs-lookup"><span data-stu-id="32c93-360">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="32c93-361">**Windows 8.1 y Windows 10:** El proceso actual no es consciente de los valores de ppp y no se puede cambiar esta configuración mediante programación llamando a la [**función SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**o SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)</span><span class="sxs-lookup"><span data-stu-id="32c93-361">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |

<span data-ttu-id="32c93-362">Para obtener más información sobre la configuración de reconocimiento de ppp, vea [Comparación de los niveles de reconocimiento de PPP.](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))</span><span class="sxs-lookup"><span data-stu-id="32c93-362">For more information about dpi awareness settings, see [Comparison of DPI Awareness Levels](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

<span data-ttu-id="32c93-363">**pppAware** no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-363">**dpiAware** has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAwareness"></span><span id="dpiawareness"></span><span id="DPIAWARENESS"></span>

### <a name="dpiawareness"></a><span data-ttu-id="32c93-364">pppAwareness</span><span class="sxs-lookup"><span data-stu-id="32c93-364">dpiAwareness</span></span>

<span data-ttu-id="32c93-365">Especifica si el proceso actual es compatible con puntos por pulgada (ppp).</span><span class="sxs-lookup"><span data-stu-id="32c93-365">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="32c93-366">La versión mínima del sistema operativo que admite el **elemento dpiAwareness** Windows 10, versión 1607.</span><span class="sxs-lookup"><span data-stu-id="32c93-366">The minimum version of the operating system that supports the **dpiAwareness** element is Windows 10, version 1607.</span></span> <span data-ttu-id="32c93-367">Para las versiones que admiten **el elemento dpiAwareness,** **pppAwareness** invalida el **elemento dpiAware.**</span><span class="sxs-lookup"><span data-stu-id="32c93-367">For versions that support the **dpiAwareness** element, the **dpiAwareness** overrides the **dpiAware** element.</span></span> <span data-ttu-id="32c93-368">Puede incluir ambos elementos en un manifiesto si desea especificar un comportamiento diferente para Windows 10, versión 1607 que para una versión anterior del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="32c93-368">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="32c93-369">El **elemento dpiAwareness** puede contener un solo elemento o una lista de elementos separados por comas.</span><span class="sxs-lookup"><span data-stu-id="32c93-369">The **dpiAwareness** element can contain a single item or a list of comma-separated items.</span></span> <span data-ttu-id="32c93-370">En el último caso, se usa el primer elemento (situado más a la izquierda) de la lista reconocido por el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="32c93-370">In the latter case, the first (leftmost) item in the list recognized by the operating system is used.</span></span> <span data-ttu-id="32c93-371">De esta manera, puede especificar distintos comportamientos admitidos en futuras versiones del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="32c93-371">In this way, you can specify different behaviors supported in future Windows operating system versions.</span></span>

<span data-ttu-id="32c93-372">En la tabla siguiente se describe el comportamiento que se produce en función de la presencia del elemento **dpiAwareness** y el texto que contiene en su elemento reconocido situado más a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="32c93-372">The following table describes the behavior that results based upon the presence of the **dpiAwareness** element and the text that it contains in its leftmost recognized item.</span></span> <span data-ttu-id="32c93-373">El texto del elemento no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="32c93-373">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="32c93-374">**estado del elemento dpiAwareness:**</span><span class="sxs-lookup"><span data-stu-id="32c93-374">**dpiAwareness** element status:</span></span>        | <span data-ttu-id="32c93-375">Descripción</span><span class="sxs-lookup"><span data-stu-id="32c93-375">Description</span></span>                          |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="32c93-376">El elemento está ausente</span><span class="sxs-lookup"><span data-stu-id="32c93-376">Element is absent</span></span>                       | <span data-ttu-id="32c93-377">El **elemento dpiAware** especifica si el proceso tiene en cuenta los valores de ppp.</span><span class="sxs-lookup"><span data-stu-id="32c93-377">The **dpiAware** element specifies whether the process is dpi aware.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="32c93-378">No contiene elementos reconocidos</span><span class="sxs-lookup"><span data-stu-id="32c93-378">Contains no recognized items</span></span>            | <span data-ttu-id="32c93-379">El proceso actual no es consciente de ppp de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="32c93-379">The current process is dpi unaware by default.</span></span> <span data-ttu-id="32c93-380">Puede cambiar esta configuración mediante programación llamando a la [**función SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**o SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)</span><span class="sxs-lookup"><span data-stu-id="32c93-380">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span> |
| <span data-ttu-id="32c93-381">El primer elemento reconocido es "system"</span><span class="sxs-lookup"><span data-stu-id="32c93-381">First recognized item is "system"</span></span>       | <span data-ttu-id="32c93-382">El proceso actual es compatible con ppp del sistema.</span><span class="sxs-lookup"><span data-stu-id="32c93-382">The current process is system dpi aware.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="32c93-383">El primer elemento reconocido es "permonitor".</span><span class="sxs-lookup"><span data-stu-id="32c93-383">First recognized item is "permonitor"</span></span>   | <span data-ttu-id="32c93-384">El proceso actual es compatible con ppp por monitor.</span><span class="sxs-lookup"><span data-stu-id="32c93-384">The current process is per-monitor dpi aware.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="32c93-385">El primer elemento reconocido es "permonitorv2"</span><span class="sxs-lookup"><span data-stu-id="32c93-385">First recognized item is "permonitorv2"</span></span> | <span data-ttu-id="32c93-386">El proceso actual usa el contexto de reconocimiento de ppp por monitor-v2.</span><span class="sxs-lookup"><span data-stu-id="32c93-386">The current process uses the per-monitor-v2 dpi awareness context.</span></span> <span data-ttu-id="32c93-387">Este elemento solo se reconocerá en Windows 10 versión 1703 o posterior.</span><span class="sxs-lookup"><span data-stu-id="32c93-387">This item will only be recognized on Windows 10 version 1703 or later.</span></span>                                                                                              |
| <span data-ttu-id="32c93-388">El primer elemento reconocido es "no consciente"</span><span class="sxs-lookup"><span data-stu-id="32c93-388">First recognized item is "unaware"</span></span>      | <span data-ttu-id="32c93-389">El proceso actual no es consciente de los valores de ppp.</span><span class="sxs-lookup"><span data-stu-id="32c93-389">The current process is dpi unaware.</span></span> <span data-ttu-id="32c93-390">No **se** puede cambiar esta configuración mediante programación llamando a la [**función SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**o SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)</span><span class="sxs-lookup"><span data-stu-id="32c93-390">You **cannot** programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>      |

<span data-ttu-id="32c93-391">Para obtener más información sobre la configuración de reconocimiento de ppp compatible con este elemento, vea [RECONOCIMIENTO \_ de PPP](/windows/desktop/api/windef/ne-windef-dpi_awareness) y [CONTEXTO DE RECONOCIMIENTO DE \_ \_ PPP](/windows/desktop/hidpi/dpi-awareness-context).</span><span class="sxs-lookup"><span data-stu-id="32c93-391">For more information about dpi awareness settings supported by this element, see [DPI\_AWARENESS](/windows/desktop/api/windef/ne-windef-dpi_awareness) and [DPI\_AWARENESS\_CONTEXT](/windows/desktop/hidpi/dpi-awareness-context).</span></span>

<span data-ttu-id="32c93-392">**pppAwareness** no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-392">**dpiAwareness** has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <dpiAwareness>PerMonitorV2, unaware</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="gdiScaling"></span><span id="gdiscaling"></span><span id="GDISCALING"></span>

### <a name="gdiscaling"></a><span data-ttu-id="32c93-393">gdiScaling</span><span class="sxs-lookup"><span data-stu-id="32c93-393">gdiScaling</span></span>

<span data-ttu-id="32c93-394">Especifica si el escalado de GDI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="32c93-394">Specifies whether GDI scaling is enabled.</span></span> <span data-ttu-id="32c93-395">La versión mínima del sistema operativo que admite el **elemento gdiScaling** Windows 10 versión 1703.</span><span class="sxs-lookup"><span data-stu-id="32c93-395">The minimum version of the operating system that supports the **gdiScaling** element is Windows 10 version 1703.</span></span>

<span data-ttu-id="32c93-396">El marco GDI (interfaz de dispositivo gráfico) puede aplicar el escalado de PPP a primitivos y texto por monitor sin actualizaciones en la propia aplicación.</span><span class="sxs-lookup"><span data-stu-id="32c93-396">The GDI (graphics device interface) framework can apply DPI scaling to primitives and text on a per-monitor basis without updates to the application itself.</span></span> <span data-ttu-id="32c93-397">Esto puede ser útil para las aplicaciones GDI que ya no se actualizan activamente.</span><span class="sxs-lookup"><span data-stu-id="32c93-397">This can be useful for GDI applications no longer being actively updated.</span></span>

<span data-ttu-id="32c93-398">Este elemento no puede escalar gráficos no vectoriales (como mapas de bits, iconos o barras de herramientas).</span><span class="sxs-lookup"><span data-stu-id="32c93-398">Non-vector graphics (such as bitmaps, icons, or toolbars) cannot be scaled by this element.</span></span> <span data-ttu-id="32c93-399">Además, los gráficos y el texto que aparecen dentro de los mapas de bits creados dinámicamente por las aplicaciones tampoco se pueden escalar mediante este elemento.</span><span class="sxs-lookup"><span data-stu-id="32c93-399">In addition, graphics and text appearing within bitmaps dynamically constructed by applications also cannot be scaled by this element.</span></span>

<span data-ttu-id="32c93-400">**TRUE** indica que este elemento está habilitado.</span><span class="sxs-lookup"><span data-stu-id="32c93-400">**TRUE** indicates that this element is enabled.</span></span> <span data-ttu-id="32c93-401">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-401">It has no attributes.</span></span>


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2017/WindowsSettings">
      <gdiScaling>true</gdiScaling>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="highResolutionScrollingAware"></span><span id="highresolutionscrollingaware"></span><span id="HIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="highresolutionscrollingaware"></a><span data-ttu-id="32c93-402">highResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="32c93-402">highResolutionScrollingAware</span></span>

<span data-ttu-id="32c93-403">Especifica si está habilitado el desplazamiento de alta resolución.</span><span class="sxs-lookup"><span data-stu-id="32c93-403">Specifies whether high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="32c93-404">**TRUE** indica que está habilitado.</span><span class="sxs-lookup"><span data-stu-id="32c93-404">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="32c93-405">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-405">It has no attributes.</span></span>

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a><span data-ttu-id="32c93-406">longPathAware</span><span class="sxs-lookup"><span data-stu-id="32c93-406">longPathAware</span></span>

<span data-ttu-id="32c93-407">Habilita rutas de acceso largas **que superan MAX_PATH** longitud.</span><span class="sxs-lookup"><span data-stu-id="32c93-407">Enables long paths that exceed **MAX_PATH** in length.</span></span> <span data-ttu-id="32c93-408">Este elemento se admite en Windows 10, versión 1607 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="32c93-408">This element is supported in Windows 10, version 1607, and later.</span></span> <span data-ttu-id="32c93-409">Para obtener más información, consulte [este artículo](../fileio/maximum-file-path-limitation.md).</span><span class="sxs-lookup"><span data-stu-id="32c93-409">For more information, see [this article](../fileio/maximum-file-path-limitation.md).</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <ws2:longPathAware>true</ws2:longPathAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="printerDriverIsolation"></span><span id="printerdriverisolation"></span><span id="PRINTERDRIVERISOLATION"></span>

### <a name="printerdriverisolation"></a><span data-ttu-id="32c93-410">printerDriverIsolation</span><span class="sxs-lookup"><span data-stu-id="32c93-410">printerDriverIsolation</span></span>

<span data-ttu-id="32c93-411">Especifica si el aislamiento del controlador de impresora está habilitado.</span><span class="sxs-lookup"><span data-stu-id="32c93-411">Specifies whether printer driver isolation is enabled.</span></span> <span data-ttu-id="32c93-412">**TRUE** indica que está habilitado.</span><span class="sxs-lookup"><span data-stu-id="32c93-412">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="32c93-413">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-413">It has no attributes.</span></span> <span data-ttu-id="32c93-414">El aislamiento del controlador de impresora mejora la confiabilidad del servicio de impresión de Windows al permitir que los controladores de impresora se ejecuten en procesos independientes del proceso en el que se ejecuta el administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="32c93-414">Printer driver isolation improves the reliability of the Windows print service by enabling printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="32c93-415">Compatibilidad con el aislamiento del controlador de impresora iniciado en Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="32c93-415">Support for printer driver isolation started in Windows 7 and Windows Server 2008 R2.</span></span> <span data-ttu-id="32c93-416">Una aplicación puede declarar el aislamiento del controlador de impresora en su manifiesto de aplicación para aislarse del controlador de impresora y mejorar su confiabilidad.</span><span class="sxs-lookup"><span data-stu-id="32c93-416">An app can declare printer driver isolation in its app manifest to isolate itself from the printer driver and improve its reliability.</span></span> <span data-ttu-id="32c93-417">Es decir, la aplicación no se bloqueará si el controlador de impresora tiene un error.</span><span class="sxs-lookup"><span data-stu-id="32c93-417">That is, the app won't crash if the printer driver has an error.</span></span>


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <printerDriverIsolation>true</printerDriverIsolation>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="ultraHighResolutionScrollingAware"></span><span id="ultrahighresolutionscrollingaware"></span><span id="ULTRAHIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="ultrahighresolutionscrollingaware"></a><span data-ttu-id="32c93-418">ultraHighResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="32c93-418">ultraHighResolutionScrollingAware</span></span>

<span data-ttu-id="32c93-419">Especifica si está habilitado el desplazamiento de resolución ultra alta.</span><span class="sxs-lookup"><span data-stu-id="32c93-419">Specifies whether ultra-high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="32c93-420">**TRUE** indica que está habilitado.</span><span class="sxs-lookup"><span data-stu-id="32c93-420">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="32c93-421">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-421">It has no attributes.</span></span>

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a><span data-ttu-id="32c93-422">msix</span><span class="sxs-lookup"><span data-stu-id="32c93-422">msix</span></span>

<span data-ttu-id="32c93-423">Especifica la información de identidad de un [paquete MSIX disperso](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) para la aplicación actual.</span><span class="sxs-lookup"><span data-stu-id="32c93-423">Specifies the identity info of a [sparse MSIX package](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) for the current application.</span></span> <span data-ttu-id="32c93-424">Este elemento se admite en Windows 10, versión 2004 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="32c93-424">This element is supported in Windows 10, version 2004, and later versions.</span></span>

<span data-ttu-id="32c93-425">El **elemento msix** debe estar en el espacio de nombres `urn:schemas-microsoft-com:msix.v1` .</span><span class="sxs-lookup"><span data-stu-id="32c93-425">The **msix** element must be in the namespace `urn:schemas-microsoft-com:msix.v1`.</span></span> <span data-ttu-id="32c93-426">Tiene los atributos que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="32c93-426">It has the attributes shown in the following table.</span></span>

| <span data-ttu-id="32c93-427">Atributo</span><span class="sxs-lookup"><span data-stu-id="32c93-427">Attribute</span></span>   | <span data-ttu-id="32c93-428">Descripción</span><span class="sxs-lookup"><span data-stu-id="32c93-428">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32c93-429">**publisher**</span><span class="sxs-lookup"><span data-stu-id="32c93-429">**publisher**</span></span>    | <span data-ttu-id="32c93-430">Describe la información del publicador.</span><span class="sxs-lookup"><span data-stu-id="32c93-430">Describes the publisher information.</span></span> <span data-ttu-id="32c93-431">Este valor debe coincidir con el **atributo Publisher** del [elemento Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) del manifiesto de paquete disperso.</span><span class="sxs-lookup"><span data-stu-id="32c93-431">This value must match the **Publisher** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span> |
| <span data-ttu-id="32c93-432">**packageName**</span><span class="sxs-lookup"><span data-stu-id="32c93-432">**packageName**</span></span> | <span data-ttu-id="32c93-433">Describe el contenido del paquete.</span><span class="sxs-lookup"><span data-stu-id="32c93-433">Describes the contents of the package.</span></span> <span data-ttu-id="32c93-434">Este valor debe coincidir con **el atributo Name** del elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) del manifiesto de paquete disperso.</span><span class="sxs-lookup"><span data-stu-id="32c93-434">This value must match the **Name** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span>    |
| <span data-ttu-id="32c93-435">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="32c93-435">**applicationId**</span></span>    | <span data-ttu-id="32c93-436">Identificador único de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32c93-436">The unique identifier of the application.</span></span> <span data-ttu-id="32c93-437">Este valor debe coincidir con el **atributo Id** del [elemento Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) del manifiesto del paquete disperso.</span><span class="sxs-lookup"><span data-stu-id="32c93-437">This value must match the **Id** attribute in the [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) element in your sparse package manifest.</span></span>  |

```xml
<?xml version="1.0" encoding="utf-8"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1">
  <assemblyIdentity version="1.0.0.0" name="Contoso.PhotoStoreApp"/>
  <msix xmlns="urn:schemas-microsoft-com:msix.v1"
          publisher="CN=Contoso"
          packageName="ContosoPhotoStore"
          applicationId="ContosoPhotoStore"
        />
</assembly>
```

### <a name="heaptype"></a><span data-ttu-id="32c93-438">heapType</span><span class="sxs-lookup"><span data-stu-id="32c93-438">heapType</span></span>

<span data-ttu-id="32c93-439">Invalida la implementación predeterminada del montón para que las API de montón de [Win32](../Memory/heap-functions.md) las usen.</span><span class="sxs-lookup"><span data-stu-id="32c93-439">Overrides the default heap implementation for the [Win32 heap APIs](../Memory/heap-functions.md) to use.</span></span>

* <span data-ttu-id="32c93-440">El valor **SegmentHeap** indica que se usará el montón de segmentos.</span><span class="sxs-lookup"><span data-stu-id="32c93-440">The value **SegmentHeap** indicates that segment heap will be used.</span></span> <span data-ttu-id="32c93-441">El montón de segmentos es una implementación moderna del montón que generalmente reducirá el uso general de memoria.</span><span class="sxs-lookup"><span data-stu-id="32c93-441">Segment heap is a modern heap implementation that will generally reduce your overall memory usage.</span></span> <span data-ttu-id="32c93-442">Este elemento se admite en Windows 10, versión 2004 (compilación 19041) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="32c93-442">This element is supported in Windows 10, version 2004 (build 19041) and later.</span></span>
* <span data-ttu-id="32c93-443">Se omiten todos los demás valores.</span><span class="sxs-lookup"><span data-stu-id="32c93-443">All other values are ignored.</span></span>

<span data-ttu-id="32c93-444">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="32c93-444">This element has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2020/WindowsSettings">
      <heapType>SegmentHeap</heapType>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

## <a name="example"></a><span data-ttu-id="32c93-445">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="32c93-445">Example</span></span>

<span data-ttu-id="32c93-446">A continuación se muestra un ejemplo de un manifiesto de aplicación para una aplicación denominada MySampleApp.exe.</span><span class="sxs-lookup"><span data-stu-id="32c93-446">The following is an example of an application manifest for an application named MySampleApp.exe.</span></span> <span data-ttu-id="32c93-447">La aplicación consume el ensamblado SampleAssembly en paralelo.</span><span class="sxs-lookup"><span data-stu-id="32c93-447">The application consumes the SampleAssembly side-by-side assembly.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">

  <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--This Id value indicates the application supports Windows Vista functionality -->
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--This Id value indicates the application supports Windows 7 functionality-->
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--This Id value indicates the application supports Windows 8 functionality-->
          <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
        <!--This Id value indicates the application supports Windows 8.1 functionality-->
          <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
      </application> 
  </compatibility>

  <assemblyIdentity type="win32" 
                    name="myOrganization.myDivision.mySampleApp" 
                    version="6.0.0.0" 
                    processorArchitecture="x86" 
                    publicKeyToken="0000000000000000"
  />
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" 
                        name="Proseware.Research.SampleAssembly" 
                        version="6.0.0.0" 
                        processorArchitecture="X86" 
                        publicKeyToken="0000000000000000" 
                        language="*"
      />
    </dependentAssembly>
  </dependency>
</assembly>
```

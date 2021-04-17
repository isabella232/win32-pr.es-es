---
description: Un manifiesto de aplicación es un archivo XML que describe e identifica los ensamblados en paralelo, compartidos y privados, a los que debe enlazarse una aplicación en tiempo de ejecución.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Manifiestos de aplicación
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: cb065bc4d6d29f4142c23cdd91c83769e2fb9b87
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "105653121"
---
# <a name="application-manifests"></a><span data-ttu-id="2cacb-103">Manifiestos de aplicación</span><span class="sxs-lookup"><span data-stu-id="2cacb-103">Application Manifests</span></span>

<span data-ttu-id="2cacb-104">Un manifiesto de aplicación es un archivo XML que describe e identifica los ensamblados en paralelo, compartidos y privados, a los que debe enlazarse una aplicación en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2cacb-104">An application manifest is an XML file that describes and identifies the shared and private side-by-side assemblies that an application should bind to at run time.</span></span> <span data-ttu-id="2cacb-105">Deben ser las mismas versiones de ensamblado utilizadas para probar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2cacb-105">These should be the same assembly versions that were used to test the application.</span></span> <span data-ttu-id="2cacb-106">Los manifiestos de aplicación también describen los metadatos para archivos privados de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2cacb-106">Application manifests may also describe metadata for files that are private to the application.</span></span>

<span data-ttu-id="2cacb-107">Para obtener una lista completa del esquema XML, consulte [esquema del archivo de manifiesto](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="2cacb-107">For a complete listing of the XML schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="2cacb-108">Los manifiestos de aplicación tienen los siguientes elementos y atributos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-108">Application manifests have the following elements and attributes.</span></span>

| <span data-ttu-id="2cacb-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="2cacb-109">Element</span></span>                               | <span data-ttu-id="2cacb-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="2cacb-110">Attributes</span></span>                | <span data-ttu-id="2cacb-111">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2cacb-111">Required</span></span> |
|---------------------------------------|---------------------------|----------|
| <span data-ttu-id="2cacb-112">**assembl**</span><span class="sxs-lookup"><span data-stu-id="2cacb-112">**assembly**</span></span>                          |                           | <span data-ttu-id="2cacb-113">Sí</span><span class="sxs-lookup"><span data-stu-id="2cacb-113">Yes</span></span>      |
|                                       | <span data-ttu-id="2cacb-114">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="2cacb-114">**manifestVersion**</span></span>       | <span data-ttu-id="2cacb-115">Sí</span><span class="sxs-lookup"><span data-stu-id="2cacb-115">Yes</span></span>      |
| <span data-ttu-id="2cacb-116">**noInherit**</span><span class="sxs-lookup"><span data-stu-id="2cacb-116">**noInherit**</span></span>                         |                           | <span data-ttu-id="2cacb-117">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-117">No</span></span>       |
| <span data-ttu-id="2cacb-118">**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="2cacb-118">**assemblyIdentity**</span></span>                  |                           | <span data-ttu-id="2cacb-119">Sí</span><span class="sxs-lookup"><span data-stu-id="2cacb-119">Yes</span></span>      |
|                                       | <span data-ttu-id="2cacb-120">**type**</span><span class="sxs-lookup"><span data-stu-id="2cacb-120">**type**</span></span>                  | <span data-ttu-id="2cacb-121">Sí</span><span class="sxs-lookup"><span data-stu-id="2cacb-121">Yes</span></span>      |
|                                       | <span data-ttu-id="2cacb-122">**name**</span><span class="sxs-lookup"><span data-stu-id="2cacb-122">**name**</span></span>                  | <span data-ttu-id="2cacb-123">Sí</span><span class="sxs-lookup"><span data-stu-id="2cacb-123">Yes</span></span>      |
|                                       | <span data-ttu-id="2cacb-124">**language**</span><span class="sxs-lookup"><span data-stu-id="2cacb-124">**language**</span></span>              | <span data-ttu-id="2cacb-125">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-125">No</span></span>       |
|                                       | <span data-ttu-id="2cacb-126">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="2cacb-126">**processorArchitecture**</span></span> | <span data-ttu-id="2cacb-127">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-127">No</span></span>       |
|                                       | <span data-ttu-id="2cacb-128">**version**</span><span class="sxs-lookup"><span data-stu-id="2cacb-128">**version**</span></span>               | <span data-ttu-id="2cacb-129">Sí</span><span class="sxs-lookup"><span data-stu-id="2cacb-129">Yes</span></span>      |
|                                       | <span data-ttu-id="2cacb-130">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="2cacb-130">**publicKeyToken**</span></span>        | <span data-ttu-id="2cacb-131">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-131">No</span></span>       |
| <span data-ttu-id="2cacb-132">**compatibilidad**</span><span class="sxs-lookup"><span data-stu-id="2cacb-132">**compatibility**</span></span>                     |                           | <span data-ttu-id="2cacb-133">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-133">No</span></span>       |
| <span data-ttu-id="2cacb-134">**application**</span><span class="sxs-lookup"><span data-stu-id="2cacb-134">**application**</span></span>                       |                           | <span data-ttu-id="2cacb-135">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-135">No</span></span>       |
| <span data-ttu-id="2cacb-136">**supportos**</span><span class="sxs-lookup"><span data-stu-id="2cacb-136">**supportedOS**</span></span>                       | <span data-ttu-id="2cacb-137">**Id**</span><span class="sxs-lookup"><span data-stu-id="2cacb-137">**Id**</span></span>                    | <span data-ttu-id="2cacb-138">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-138">No</span></span>       |
| <span data-ttu-id="2cacb-139">**maxversiontested**</span><span class="sxs-lookup"><span data-stu-id="2cacb-139">**maxversiontested**</span></span>                  | <span data-ttu-id="2cacb-140">**Id**</span><span class="sxs-lookup"><span data-stu-id="2cacb-140">**Id**</span></span>                    | <span data-ttu-id="2cacb-141">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-141">No</span></span>       |
| <span data-ttu-id="2cacb-142">**pendiente**</span><span class="sxs-lookup"><span data-stu-id="2cacb-142">**dependency**</span></span>                        |                           | <span data-ttu-id="2cacb-143">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-143">No</span></span>       |
| <span data-ttu-id="2cacb-144">**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="2cacb-144">**dependentAssembly**</span></span>                 |                           | <span data-ttu-id="2cacb-145">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-145">No</span></span>       |
| <span data-ttu-id="2cacb-146">**file**</span><span class="sxs-lookup"><span data-stu-id="2cacb-146">**file**</span></span>                              |                           | <span data-ttu-id="2cacb-147">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-147">No</span></span>       |
|                                       | <span data-ttu-id="2cacb-148">**name**</span><span class="sxs-lookup"><span data-stu-id="2cacb-148">**name**</span></span>                  | <span data-ttu-id="2cacb-149">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-149">No</span></span>       |
|                                       | <span data-ttu-id="2cacb-150">**hashalg**</span><span class="sxs-lookup"><span data-stu-id="2cacb-150">**hashalg**</span></span>               | <span data-ttu-id="2cacb-151">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-151">No</span></span>       |
|                                       | <span data-ttu-id="2cacb-152">**hash**</span><span class="sxs-lookup"><span data-stu-id="2cacb-152">**hash**</span></span>                  | <span data-ttu-id="2cacb-153">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-153">No</span></span>       |
| <span data-ttu-id="2cacb-154">**activeCodePage**</span><span class="sxs-lookup"><span data-stu-id="2cacb-154">**activeCodePage**</span></span>                    |                           | <span data-ttu-id="2cacb-155">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-155">No</span></span>       |
| <span data-ttu-id="2cacb-156">**Elevación de privilegios**</span><span class="sxs-lookup"><span data-stu-id="2cacb-156">**autoElevate**</span></span>                       |                           | <span data-ttu-id="2cacb-157">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-157">No</span></span>       |
| <span data-ttu-id="2cacb-158">**disableTheming**</span><span class="sxs-lookup"><span data-stu-id="2cacb-158">**disableTheming**</span></span>                    |                           | <span data-ttu-id="2cacb-159">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-159">No</span></span>       |
| <span data-ttu-id="2cacb-160">**disableWindowFiltering**</span><span class="sxs-lookup"><span data-stu-id="2cacb-160">**disableWindowFiltering**</span></span>            |                           | <span data-ttu-id="2cacb-161">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-161">No</span></span>       |
| <span data-ttu-id="2cacb-162">**dpiAware**</span><span class="sxs-lookup"><span data-stu-id="2cacb-162">**dpiAware**</span></span>                          |                           | <span data-ttu-id="2cacb-163">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-163">No</span></span>       |
| <span data-ttu-id="2cacb-164">**dpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="2cacb-164">**dpiAwareness**</span></span>                      |                           | <span data-ttu-id="2cacb-165">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-165">No</span></span>       |
| <span data-ttu-id="2cacb-166">**gdiScaling**</span><span class="sxs-lookup"><span data-stu-id="2cacb-166">**gdiScaling**</span></span>                        |                           | <span data-ttu-id="2cacb-167">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-167">No</span></span>       |
| <span data-ttu-id="2cacb-168">**highResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="2cacb-168">**highResolutionScrollingAware**</span></span>      |                           | <span data-ttu-id="2cacb-169">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-169">No</span></span>       |
| <span data-ttu-id="2cacb-170">**longPathAware**</span><span class="sxs-lookup"><span data-stu-id="2cacb-170">**longPathAware**</span></span>                     |                           | <span data-ttu-id="2cacb-171">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-171">No</span></span>       |
| <span data-ttu-id="2cacb-172">**printerDriverIsolation**</span><span class="sxs-lookup"><span data-stu-id="2cacb-172">**printerDriverIsolation**</span></span>            |                           | <span data-ttu-id="2cacb-173">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-173">No</span></span>       |
| <span data-ttu-id="2cacb-174">**ultraHighResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="2cacb-174">**ultraHighResolutionScrollingAware**</span></span> |                           | <span data-ttu-id="2cacb-175">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-175">No</span></span>       |
| <span data-ttu-id="2cacb-176">**msix**</span><span class="sxs-lookup"><span data-stu-id="2cacb-176">**msix**</span></span>                              |                           | <span data-ttu-id="2cacb-177">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-177">No</span></span>       |
| <span data-ttu-id="2cacb-178">**heapType**</span><span class="sxs-lookup"><span data-stu-id="2cacb-178">**heapType**</span></span>                          |                           | <span data-ttu-id="2cacb-179">No</span><span class="sxs-lookup"><span data-stu-id="2cacb-179">No</span></span>       |

## <a name="file-location"></a><span data-ttu-id="2cacb-180">Ubicación del archivo</span><span class="sxs-lookup"><span data-stu-id="2cacb-180">File Location</span></span>

<span data-ttu-id="2cacb-181">Los manifiestos de aplicación deben incluirse como un recurso en el archivo EXE o DLL de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2cacb-181">Application manifests should be included as a resource in the application's EXE file or DLL.</span></span>

<span data-ttu-id="2cacb-182">Para obtener más información, vea [Instalar ensamblados en paralelo](installing-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="2cacb-182">For more information, see [Installing Side-by-side Assemblies](installing-side-by-side-assemblies.md).</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="2cacb-183">Sintaxis de los nombres de archivo</span><span class="sxs-lookup"><span data-stu-id="2cacb-183">File Name Syntax</span></span>

<span data-ttu-id="2cacb-184">El nombre de un archivo de manifiesto de aplicación es el nombre del ejecutable de la aplicación seguido de. manifest.</span><span class="sxs-lookup"><span data-stu-id="2cacb-184">The name of an application manifest file is the name of the application's executable followed by .manifest.</span></span>

<span data-ttu-id="2cacb-185">Por ejemplo, un manifiesto de aplicación que hace referencia a example.exe o example.dll utilizaría la siguiente sintaxis de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="2cacb-185">For example, an application manifest that refers to example.exe or example.dll would use the following file name syntax.</span></span> <span data-ttu-id="2cacb-186">Puede omitir el campo <ID. de *recurso*> si el identificador de recurso es 1.</span><span class="sxs-lookup"><span data-stu-id="2cacb-186">You can omit the <*resource ID*> field if resource ID is 1.</span></span>

<span data-ttu-id="2cacb-187">**ID. de *recurso* deexample.exe. <>. manifest**</span><span class="sxs-lookup"><span data-stu-id="2cacb-187">**example.exe.<*resource ID*>.manifest**</span></span>

<span data-ttu-id="2cacb-188">**ID. de *recurso* deexample.dll. <>. manifest**</span><span class="sxs-lookup"><span data-stu-id="2cacb-188">**example.dll.<*resource ID*>.manifest**</span></span>

## <a name="elements"></a><span data-ttu-id="2cacb-189">Elementos</span><span class="sxs-lookup"><span data-stu-id="2cacb-189">Elements</span></span>

<span data-ttu-id="2cacb-190">Los nombres de los elementos y atributos distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2cacb-190">Names of elements and attributes are case-sensitive.</span></span> <span data-ttu-id="2cacb-191">Los valores de los elementos y atributos no distinguen mayúsculas de minúsculas, excepto el valor del atributo type.</span><span class="sxs-lookup"><span data-stu-id="2cacb-191">The values of elements and attributes are case-insensitive, except for the value of the type attribute.</span></span>

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a><span data-ttu-id="2cacb-192">ensamblado</span><span class="sxs-lookup"><span data-stu-id="2cacb-192">assembly</span></span>

<span data-ttu-id="2cacb-193">Elemento contenedor.</span><span class="sxs-lookup"><span data-stu-id="2cacb-193">A container element.</span></span> <span data-ttu-id="2cacb-194">Su primer subelemento debe ser un elemento **NoInherit** o **assemblyIdentity** .</span><span class="sxs-lookup"><span data-stu-id="2cacb-194">Its first subelement must be a **noInherit** or **assemblyIdentity** element.</span></span> <span data-ttu-id="2cacb-195">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2cacb-195">Required.</span></span>

<span data-ttu-id="2cacb-196">El elemento de **ensamblado** debe estar en el espacio de nombres "urn: schemas-microsoft-com: ASM. v1".</span><span class="sxs-lookup"><span data-stu-id="2cacb-196">The **assembly** element must be in the namespace "urn:schemas-microsoft-com:asm.v1".</span></span> <span data-ttu-id="2cacb-197">Los elementos secundarios del ensamblado también deben estar en este espacio de nombres, por herencia o mediante el etiquetado.</span><span class="sxs-lookup"><span data-stu-id="2cacb-197">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="2cacb-198">El elemento **Assembly** tiene los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="2cacb-198">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="2cacb-199">Atributo</span><span class="sxs-lookup"><span data-stu-id="2cacb-199">Attribute</span></span>           | <span data-ttu-id="2cacb-200">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cacb-200">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="2cacb-201">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="2cacb-201">**manifestVersion**</span></span> | <span data-ttu-id="2cacb-202">El atributo **manifestVersion** debe establecerse en 1,0.</span><span class="sxs-lookup"><span data-stu-id="2cacb-202">The **manifestVersion** attribute must be set to 1.0.</span></span> |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a><span data-ttu-id="2cacb-203">noInherit</span><span class="sxs-lookup"><span data-stu-id="2cacb-203">noInherit</span></span>

<span data-ttu-id="2cacb-204">Incluya este elemento en un manifiesto de aplicación para establecer los [contextos de activación](activation-contexts.md) generados a partir del manifiesto con la marca "no heredado".</span><span class="sxs-lookup"><span data-stu-id="2cacb-204">Include this element in an application manifest to set the [activation contexts](activation-contexts.md) generated from the manifest with the "no inherit" flag.</span></span> <span data-ttu-id="2cacb-205">Cuando esta marca no se establece en un contexto de activación y el contexto de activación está activo, lo heredan los nuevos subprocesos en el mismo proceso, ventanas, procedimientos de ventana y [llamadas a procedimientos asincrónicos](/windows/desktop/Sync/asynchronous-procedure-calls).</span><span class="sxs-lookup"><span data-stu-id="2cacb-205">When this flag is not set in an activation context, and the activation context is active, it is inherited by new threads in the same process, windows, window procedures, and [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span> <span data-ttu-id="2cacb-206">Al establecer esta marca, se evita que el nuevo objeto herede el contexto activo.</span><span class="sxs-lookup"><span data-stu-id="2cacb-206">Setting this flag prevents the new object from inheriting the active context.</span></span>

<span data-ttu-id="2cacb-207">El elemento **NoInherit** es opcional y se suele omitir.</span><span class="sxs-lookup"><span data-stu-id="2cacb-207">The **noInherit** element is optional and typically omitted.</span></span> <span data-ttu-id="2cacb-208">La mayoría de los ensamblados no funcionan correctamente utilizando un contexto de activación no heredado porque el ensamblado debe diseñarse explícitamente para administrar la propagación de su propio contexto de activación.</span><span class="sxs-lookup"><span data-stu-id="2cacb-208">Most assemblies do not work correctly using a no-inherit activation context because the assembly must be explicitly designed to manage the propagation of their own activation context.</span></span> <span data-ttu-id="2cacb-209">El uso del elemento **NoInherit** requiere que todos los ensamblados dependientes a los que hace referencia el manifiesto de aplicación tengan un elemento **NoInherit** en el [manifiesto del ensamblado](assembly-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="2cacb-209">The use of the **noInherit** element requires that any dependent assemblies referenced by the application manifest have a **noInherit** element in their [assembly manifest](assembly-manifests.md).</span></span>

<span data-ttu-id="2cacb-210">Si se utiliza **NoInherit** en un manifiesto, debe ser el primer subelemento del elemento **Assembly** .</span><span class="sxs-lookup"><span data-stu-id="2cacb-210">If **noInherit** is used in a manifest, it must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="2cacb-211">El elemento **assemblyIdentity** debe aparecer inmediatamente después del elemento **NoInherit** .</span><span class="sxs-lookup"><span data-stu-id="2cacb-211">The **assemblyIdentity** element should come immediately after the **noInherit** element.</span></span> <span data-ttu-id="2cacb-212">Si no se utiliza **NoInherit** , **assemblyIdentity** debe ser el primer subelemento del elemento **Assembly** .</span><span class="sxs-lookup"><span data-stu-id="2cacb-212">If **noInherit** is not used, **assemblyIdentity** must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="2cacb-213">El elemento **NoInherit** no tiene elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="2cacb-213">The **noInherit** element has no child elements.</span></span> <span data-ttu-id="2cacb-214">No es un elemento válido en los [manifiestos de ensamblado](assembly-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="2cacb-214">It is not a valid element in [assembly manifests](assembly-manifests.md).</span></span>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a><span data-ttu-id="2cacb-215">assemblyIdentity</span><span class="sxs-lookup"><span data-stu-id="2cacb-215">assemblyIdentity</span></span>

<span data-ttu-id="2cacb-216">Como primer subelemento de un elemento **Assembly** , **assemblyIdentity** describe e identifica de forma única la aplicación que posee este manifiesto de aplicación.</span><span class="sxs-lookup"><span data-stu-id="2cacb-216">As the first subelement of an **assembly** element, **assemblyIdentity** describes and uniquely identifies the application owning this application manifest.</span></span> <span data-ttu-id="2cacb-217">Como primer subelemento de un elemento **dependentAssembly** , **assemblyIdentity** describe un ensamblado en paralelo requerido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2cacb-217">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="2cacb-218">Tenga en cuenta que cada ensamblado al que se hace referencia en el manifiesto de aplicación requiere **assemblyIdentity** que coincida exactamente con el **assemblyIdentity** en el manifiesto del ensamblado del ensamblado al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="2cacb-218">Note that every assembly referenced in the application manifest requires an **assemblyIdentity** that exactly matches the **assemblyIdentity** in the referenced assembly's own assembly manifest.</span></span>

<span data-ttu-id="2cacb-219">El elemento **assemblyIdentity** tiene los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="2cacb-219">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="2cacb-220">No tiene subelementos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-220">It has no subelements.</span></span>

| <span data-ttu-id="2cacb-221">Atributo</span><span class="sxs-lookup"><span data-stu-id="2cacb-221">Attribute</span></span>                 | <span data-ttu-id="2cacb-222">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cacb-222">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cacb-223">**type**</span><span class="sxs-lookup"><span data-stu-id="2cacb-223">**type**</span></span>                  | <span data-ttu-id="2cacb-224">Especifica el tipo de aplicación o ensamblado.</span><span class="sxs-lookup"><span data-stu-id="2cacb-224">Specifies the application or assembly type.</span></span> <span data-ttu-id="2cacb-225">El valor debe ser Win32 y todo en minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2cacb-225">The value must be Win32 and all in lower case.</span></span> <span data-ttu-id="2cacb-226">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2cacb-226">Required.</span></span>                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="2cacb-227">**name**</span><span class="sxs-lookup"><span data-stu-id="2cacb-227">**name**</span></span>                  | <span data-ttu-id="2cacb-228">Designa de forma exclusiva la aplicación o el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="2cacb-228">Uniquely names the application or assembly.</span></span> <span data-ttu-id="2cacb-229">Use el siguiente formato para el nombre: Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="2cacb-229">Use the following format for the name: Organization.Division.Name.</span></span> <span data-ttu-id="2cacb-230">Por ejemplo, Microsoft. Windows. mysampleApp.</span><span class="sxs-lookup"><span data-stu-id="2cacb-230">For example Microsoft.Windows.mysampleApp.</span></span> <span data-ttu-id="2cacb-231">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2cacb-231">Required.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="2cacb-232">**language**</span><span class="sxs-lookup"><span data-stu-id="2cacb-232">**language**</span></span>              | <span data-ttu-id="2cacb-233">Identifica el idioma de la aplicación o del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="2cacb-233">Identifies the language of the application or assembly.</span></span> <span data-ttu-id="2cacb-234">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2cacb-234">Optional.</span></span> <span data-ttu-id="2cacb-235">Si la aplicación o el ensamblado son específicos del idioma, especifique el código de lenguaje DHTML.</span><span class="sxs-lookup"><span data-stu-id="2cacb-235">If the application or assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="2cacb-236">En el **assemblyIdentity** de una aplicación diseñada para uso internacional (idioma neutro), omita el atributo de idioma.</span><span class="sxs-lookup"><span data-stu-id="2cacb-236">In the **assemblyIdentity** of an application intended for worldwide use (language neutral) omit the language attribute.</span></span><br/> <span data-ttu-id="2cacb-237">En un **assemblyIdentity** de un ensamblado diseñado para uso internacional (idioma neutro) establezca el valor de Language en " \* ".</span><span class="sxs-lookup"><span data-stu-id="2cacb-237">In an **assemblyIdentity** of an assembly intended for worldwide use (language neutral) set the value of language to "\*".</span></span><br/> |
| <span data-ttu-id="2cacb-238">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="2cacb-238">**processorArchitecture**</span></span> | <span data-ttu-id="2cacb-239">Especifica el procesador.</span><span class="sxs-lookup"><span data-stu-id="2cacb-239">Specifies the processor.</span></span> <span data-ttu-id="2cacb-240">Entre los valores válidos se incluyen `x86`, `amd64`, `arm` y `arm64`.</span><span class="sxs-lookup"><span data-stu-id="2cacb-240">Valid values include `x86`, `amd64`, `arm` and `arm64`.</span></span> <span data-ttu-id="2cacb-241">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2cacb-241">Optional.</span></span>                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2cacb-242">**version**</span><span class="sxs-lookup"><span data-stu-id="2cacb-242">**version**</span></span>               | <span data-ttu-id="2cacb-243">Especifica la versión de la aplicación o del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="2cacb-243">Specifies the application or assembly version.</span></span> <span data-ttu-id="2cacb-244">Use el formato de versión de cuatro partes: mmmmm. nnnnn. ooooo. ppppp.</span><span class="sxs-lookup"><span data-stu-id="2cacb-244">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="2cacb-245">Cada una de las partes separadas por puntos puede ser 0-65535, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="2cacb-245">Each of the parts separated by periods can be 0-65535 inclusive.</span></span> <span data-ttu-id="2cacb-246">Para obtener más información, vea [versiones de ensamblado](assembly-versions.md).</span><span class="sxs-lookup"><span data-stu-id="2cacb-246">For more information, see [Assembly Versions](assembly-versions.md).</span></span> <span data-ttu-id="2cacb-247">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2cacb-247">Required.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="2cacb-248">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="2cacb-248">**publicKeyToken**</span></span>        | <span data-ttu-id="2cacb-249">Cadena hexadecimal de 16 caracteres que representa los últimos 8 bytes del hash SHA-1 de la clave pública con la que se firma la aplicación o el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="2cacb-249">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the application or assembly is signed.</span></span> <span data-ttu-id="2cacb-250">La clave pública que se usa para firmar el catálogo debe ser de 2048 bits o superior.</span><span class="sxs-lookup"><span data-stu-id="2cacb-250">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="2cacb-251">Se requiere para todos los ensamblados en paralelo compartidos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-251">Required for all shared side-by-side assemblies.</span></span>                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a><span data-ttu-id="2cacb-252">compatibilidad</span><span class="sxs-lookup"><span data-stu-id="2cacb-252">compatibility</span></span>

<span data-ttu-id="2cacb-253">Contiene al menos una **aplicación**.</span><span class="sxs-lookup"><span data-stu-id="2cacb-253">Contains at least one **application**.</span></span> <span data-ttu-id="2cacb-254">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-254">It has no attributes.</span></span> <span data-ttu-id="2cacb-255">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2cacb-255">Optional.</span></span> <span data-ttu-id="2cacb-256">Los manifiestos de aplicación sin un elemento de compatibilidad tienen como valor predeterminado la compatibilidad con Windows Vista en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2cacb-256">Application manifests without a compatibility element default to Windows Vista compatibility on Windows 7.</span></span>

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a><span data-ttu-id="2cacb-257">application</span><span class="sxs-lookup"><span data-stu-id="2cacb-257">application</span></span>

<span data-ttu-id="2cacb-258">Contiene al menos un elemento **admitido** .</span><span class="sxs-lookup"><span data-stu-id="2cacb-258">Contains at least one **supportedOS** element.</span></span> <span data-ttu-id="2cacb-259">A partir de Windows 10, versión 1903, también puede contener un elemento **maxversiontested** opcional.</span><span class="sxs-lookup"><span data-stu-id="2cacb-259">Starting in Windows 10, version 1903, it can also contain one optional **maxversiontested** element.</span></span> <span data-ttu-id="2cacb-260">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-260">It has no attributes.</span></span> <span data-ttu-id="2cacb-261">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2cacb-261">Optional.</span></span>

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a><span data-ttu-id="2cacb-262">supportos</span><span class="sxs-lookup"><span data-stu-id="2cacb-262">supportedOS</span></span>

<span data-ttu-id="2cacb-263">El elemento **supportos** tiene el siguiente atributo.</span><span class="sxs-lookup"><span data-stu-id="2cacb-263">The **supportedOS** element has the following attribute.</span></span> <span data-ttu-id="2cacb-264">No tiene subelementos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-264">It has no subelements.</span></span>

| <span data-ttu-id="2cacb-265">Atributo</span><span class="sxs-lookup"><span data-stu-id="2cacb-265">Attribute</span></span> | <span data-ttu-id="2cacb-266">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cacb-266">Description</span></span>   |
|-----------|-----------------------|
| <span data-ttu-id="2cacb-267">**Id**</span><span class="sxs-lookup"><span data-stu-id="2cacb-267">**Id**</span></span>    | <span data-ttu-id="2cacb-268">Establezca el atributo ID en **{e2011457-1546-43c5-a5fe-008deee3d3f0}** para ejecutar la aplicación mediante la funcionalidad de vista.</span><span class="sxs-lookup"><span data-stu-id="2cacb-268">Set the Id attribute to **{e2011457-1546-43c5-a5fe-008deee3d3f0}** to run the application using Vista functionality.</span></span> <span data-ttu-id="2cacb-269">Esto puede permitir que una aplicación diseñada para Windows Vista se ejecute en un sistema operativo posterior.</span><span class="sxs-lookup"><span data-stu-id="2cacb-269">This can enable an application designed for Windows Vista to run on a later operating system.</span></span> <br/> <span data-ttu-id="2cacb-270">Establezca el atributo ID en **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** para ejecutar la aplicación mediante la funcionalidad de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2cacb-270">Set the Id attribute to **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** to run the application using Windows 7 functionality.</span></span><br/> <span data-ttu-id="2cacb-271">Las aplicaciones que admiten la funcionalidad de Windows Vista, Windows 7 y Windows 8 no requieren manifiestos independientes.</span><span class="sxs-lookup"><span data-stu-id="2cacb-271">Applications that support Windows Vista, Windows 7, and Windows 8 functionality do not require separate manifests.</span></span> <span data-ttu-id="2cacb-272">En este caso, agregue los GUID para todos los sistemas operativos Windows.</span><span class="sxs-lookup"><span data-stu-id="2cacb-272">In this case, add the GUIDs for all the Windows operating systems.</span></span><br/> <span data-ttu-id="2cacb-273">Para obtener información sobre el comportamiento del atributo **ID** en Windows, vea la guía de compatibilidad de Windows [8 y Windows Server 2012](https://www.microsoft.com/download/details.aspx?id=27416).</span><span class="sxs-lookup"><span data-stu-id="2cacb-273">For info about the **Id** attribute behavior in Windows, see the [Windows 8 and Windows Server 2012 Compatibility Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).</span></span><br/> <span data-ttu-id="2cacb-274">Los siguientes GUID corresponden a los sistemas operativos indicados:</span><span class="sxs-lookup"><span data-stu-id="2cacb-274">The following GUIDs correspond with the indicated operating systems:</span></span><br/> <span data-ttu-id="2cacb-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, windows Server 2016 y windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="2cacb-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 and Windows Server 2019</span></span><br/> <span data-ttu-id="2cacb-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 y Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2cacb-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 and Windows Server 2012 R2</span></span><br/> <span data-ttu-id="2cacb-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 y windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2cacb-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 and Windows Server 2012</span></span><br/> <span data-ttu-id="2cacb-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 y windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2cacb-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 and Windows Server 2008 R2</span></span><br/> <span data-ttu-id="2cacb-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista y windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2cacb-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista and Windows Server 2008</span></span><br/> <span data-ttu-id="2cacb-280">Para probarlo en Windows 7 o Windows 8. x, ejecute Monitor de recursos (resmon), vaya a la pestaña CPU, haga clic con el botón derecho en las etiquetas de columna, "Seleccionar columna..." y seleccione "contexto del sistema operativo".</span><span class="sxs-lookup"><span data-stu-id="2cacb-280">You can test this on Windows 7 or Windows 8.x by running Resource Monitor (resmon), going to the CPU tab, right-clicking on the column labels, "Select Column...", and check "Operating System Context".</span></span> <span data-ttu-id="2cacb-281">En Windows 8. x, también puede encontrar esta columna disponible en el administrador de tareas (taskmgr).</span><span class="sxs-lookup"><span data-stu-id="2cacb-281">On Windows 8.x, you can also find this column available in the Task Manager (taskmgr).</span></span> <span data-ttu-id="2cacb-282">El contenido de la columna muestra el valor más alto encontrado o "Windows Vista" como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2cacb-282">The content of the column shows the highest value found or "Windows Vista" as the default.</span></span> <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a><span data-ttu-id="2cacb-283">maxversiontested</span><span class="sxs-lookup"><span data-stu-id="2cacb-283">maxversiontested</span></span>

<span data-ttu-id="2cacb-284">El elemento **maxversiontested** especifica la versión máxima de Windows con la que se probó la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2cacb-284">The **maxversiontested** element specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="2cacb-285">Esto está pensado para que lo usen las aplicaciones de escritorio que usan [islas XAML](/windows/apps/desktop/modernize/xaml-islands) y que no se implementan en un paquete MSIX.</span><span class="sxs-lookup"><span data-stu-id="2cacb-285">This is intended to be used by desktop applications that use [XAML Islands](/windows/apps/desktop/modernize/xaml-islands) and that are not deployed in an MSIX package.</span></span> <span data-ttu-id="2cacb-286">Este elemento es compatible con Windows 10, la versión 1903 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2cacb-286">This element is supported in Windows 10, version 1903, and later versions.</span></span>

<span data-ttu-id="2cacb-287">El elemento **maxversiontested** tiene el siguiente atributo.</span><span class="sxs-lookup"><span data-stu-id="2cacb-287">The **maxversiontested** element has the following attribute.</span></span> <span data-ttu-id="2cacb-288">No tiene subelementos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-288">It has no subelements.</span></span>

| <span data-ttu-id="2cacb-289">Atributo</span><span class="sxs-lookup"><span data-stu-id="2cacb-289">Attribute</span></span> | <span data-ttu-id="2cacb-290">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cacb-290">Description</span></span>    |
|-----------|----------------|
| <span data-ttu-id="2cacb-291">**Id**</span><span class="sxs-lookup"><span data-stu-id="2cacb-291">**Id**</span></span>    | <span data-ttu-id="2cacb-292">Establezca el atributo ID en una cadena de versión de cuatro partes que especifique la versión máxima de Windows con la que se probó la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2cacb-292">Set the Id attribute to a 4-part version string that specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="2cacb-293">Por ejemplo, "10.0.18226.0".</span><span class="sxs-lookup"><span data-stu-id="2cacb-293">For example, "10.0.18226.0".</span></span> |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a><span data-ttu-id="2cacb-294">dependency</span><span class="sxs-lookup"><span data-stu-id="2cacb-294">dependency</span></span>

<span data-ttu-id="2cacb-295">Contiene al menos un **dependentAssembly**.</span><span class="sxs-lookup"><span data-stu-id="2cacb-295">Contains at least one **dependentAssembly**.</span></span> <span data-ttu-id="2cacb-296">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-296">It has no attributes.</span></span> <span data-ttu-id="2cacb-297">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2cacb-297">Optional.</span></span>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a><span data-ttu-id="2cacb-298">dependentAssembly</span><span class="sxs-lookup"><span data-stu-id="2cacb-298">dependentAssembly</span></span>

<span data-ttu-id="2cacb-299">El primer subelemento de **dependentAssembly** debe ser un elemento **assemblyIdentity** que describe un ensamblado en paralelo requerido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2cacb-299">The first subelement of **dependentAssembly** must be an **assemblyIdentity** element that describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="2cacb-300">Cada **dependentAssembly** debe estar dentro de una **dependencia** exactamente.</span><span class="sxs-lookup"><span data-stu-id="2cacb-300">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="2cacb-301">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-301">It has no attributes.</span></span>

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a><span data-ttu-id="2cacb-302">archivo</span><span class="sxs-lookup"><span data-stu-id="2cacb-302">file</span></span>

<span data-ttu-id="2cacb-303">Especifica los archivos que son privados para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2cacb-303">Specifies files that are private to the application.</span></span> <span data-ttu-id="2cacb-304">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2cacb-304">Optional.</span></span>

<span data-ttu-id="2cacb-305">El elemento **File** tiene los atributos que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2cacb-305">The **file** element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="2cacb-306">Atributo</span><span class="sxs-lookup"><span data-stu-id="2cacb-306">Attribute</span></span>   | <span data-ttu-id="2cacb-307">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cacb-307">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cacb-308">**name**</span><span class="sxs-lookup"><span data-stu-id="2cacb-308">**name**</span></span>    | <span data-ttu-id="2cacb-309">Nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="2cacb-309">Name of the file.</span></span> <span data-ttu-id="2cacb-310">Por ejemplo, Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="2cacb-310">For example, Comctl32.dll.</span></span>                                                            |
| <span data-ttu-id="2cacb-311">**hashalg**</span><span class="sxs-lookup"><span data-stu-id="2cacb-311">**hashalg**</span></span> | <span data-ttu-id="2cacb-312">Algoritmo usado para crear un hash del archivo.</span><span class="sxs-lookup"><span data-stu-id="2cacb-312">Algorithm used to create a hash of the file.</span></span> <span data-ttu-id="2cacb-313">Este valor debe ser SHA1.</span><span class="sxs-lookup"><span data-stu-id="2cacb-313">This value should be SHA1.</span></span>                                 |
| <span data-ttu-id="2cacb-314">**hash**</span><span class="sxs-lookup"><span data-stu-id="2cacb-314">**hash**</span></span>    | <span data-ttu-id="2cacb-315">Un hash del archivo al que se hace referencia por nombre.</span><span class="sxs-lookup"><span data-stu-id="2cacb-315">A hash of the file referred to by name.</span></span> <span data-ttu-id="2cacb-316">Cadena hexadecimal de longitud según el algoritmo hash.</span><span class="sxs-lookup"><span data-stu-id="2cacb-316">A hexadecimal string of length depending on the hash algorithm.</span></span> |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a><span data-ttu-id="2cacb-317">activeCodePage</span><span class="sxs-lookup"><span data-stu-id="2cacb-317">activeCodePage</span></span>

<span data-ttu-id="2cacb-318">Fuerce que un proceso use UTF-8 como página de códigos del proceso.</span><span class="sxs-lookup"><span data-stu-id="2cacb-318">Force a process to use UTF-8 as the process code page.</span></span>

<span data-ttu-id="2cacb-319">**activeCodePage** se agregó en la versión 1903 de Windows (actualización 2019 de mayo).</span><span class="sxs-lookup"><span data-stu-id="2cacb-319">**activeCodePage** was added in Windows Version 1903 (May 2019 Update).</span></span> <span data-ttu-id="2cacb-320">Puede declarar esta propiedad y destino o ejecutar en compilaciones anteriores de Windows, pero debe administrar la detección y conversión de páginas de códigos heredadas como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="2cacb-320">You can declare this property and target/run on earlier Windows builds, but you must handle legacy code page detection and conversion as usual.</span></span> <span data-ttu-id="2cacb-321">Consulte [usar la página de códigos UTF-8](/windows/uwp/design/globalizing/use-utf8-code-page) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="2cacb-321">See [Use the UTF-8 code page](/windows/uwp/design/globalizing/use-utf8-code-page) for details.</span></span>

<span data-ttu-id="2cacb-322">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-322">This element has no attributes.</span></span> <span data-ttu-id="2cacb-323">**UTF-8** es solo un valor válido para el elemento **activeCodePage** .</span><span class="sxs-lookup"><span data-stu-id="2cacb-323">**UTF-8** is only valid value for **activeCodePage** element.</span></span>

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

### <a name="autoelevate"></a><span data-ttu-id="2cacb-324">Elevación de privilegios</span><span class="sxs-lookup"><span data-stu-id="2cacb-324">autoElevate</span></span>

<span data-ttu-id="2cacb-325">Especifica si la elevación automática está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2cacb-325">Specifies whether auto elevate is enabled.</span></span> <span data-ttu-id="2cacb-326">**True** indica que está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2cacb-326">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="2cacb-327">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-327">It has no attributes.</span></span>

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a><span data-ttu-id="2cacb-328">disableTheming</span><span class="sxs-lookup"><span data-stu-id="2cacb-328">disableTheming</span></span>

<span data-ttu-id="2cacb-329">Especifica si los elementos de la interfaz de usuario que proporcionan un tema están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="2cacb-329">Specifies whether giving UI elements a theme is disabled.</span></span> <span data-ttu-id="2cacb-330">**True** indica deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="2cacb-330">**TRUE** indicates disabled.</span></span> <span data-ttu-id="2cacb-331">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-331">It has no attributes.</span></span>

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a><span data-ttu-id="2cacb-332">disableWindowFiltering</span><span class="sxs-lookup"><span data-stu-id="2cacb-332">disableWindowFiltering</span></span>

<span data-ttu-id="2cacb-333">Especifica si se va a deshabilitar el filtrado de ventanas.</span><span class="sxs-lookup"><span data-stu-id="2cacb-333">Specifies whether to disable window filtering.</span></span> <span data-ttu-id="2cacb-334">**True** deshabilita el filtrado de ventanas para que pueda enumerar las ventanas envolventes del escritorio.</span><span class="sxs-lookup"><span data-stu-id="2cacb-334">**TRUE** disables window filtering so you can enumerate immersive windows from the desktop.</span></span> <span data-ttu-id="2cacb-335">**disableWindowFiltering** se agregó en Windows 8 y no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-335">**disableWindowFiltering** was added in Windows 8 and has no attributes.</span></span>

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

### <a name="dpiaware"></a><span data-ttu-id="2cacb-336">dpiAware</span><span class="sxs-lookup"><span data-stu-id="2cacb-336">dpiAware</span></span>

<span data-ttu-id="2cacb-337">Especifica si el proceso actual tiene reconocimiento de puntos por pulgada (PPP).</span><span class="sxs-lookup"><span data-stu-id="2cacb-337">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="2cacb-338">**Windows 10, versión 1607:** El elemento **dpiAware** se omite si el elemento **dpiAwareness** está presente.</span><span class="sxs-lookup"><span data-stu-id="2cacb-338">**Windows 10, version 1607:** The **dpiAware** element is ignored if the **dpiAwareness** element is present.</span></span> <span data-ttu-id="2cacb-339">Puede incluir ambos elementos en un manifiesto si desea especificar un comportamiento diferente para Windows 10, versión 1607, que para una versión anterior del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2cacb-339">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="2cacb-340">En la tabla siguiente se describe el comportamiento que se produce en función de la presencia del elemento **dpiAware** y del texto que contiene.</span><span class="sxs-lookup"><span data-stu-id="2cacb-340">The following table describes the behavior that results based upon the presence of the **dpiAware** element and the text that it contains.</span></span> <span data-ttu-id="2cacb-341">El texto dentro del elemento no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2cacb-341">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="2cacb-342">Estado del elemento **dpiAware**</span><span class="sxs-lookup"><span data-stu-id="2cacb-342">State of the **dpiAware** element</span></span> | <span data-ttu-id="2cacb-343">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cacb-343">Description</span></span>     |
|-----------------------------------|---------|
| <span data-ttu-id="2cacb-344">Absent</span><span class="sxs-lookup"><span data-stu-id="2cacb-344">Absent</span></span>                            | <span data-ttu-id="2cacb-345">El proceso actual no es compatible con PPP de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2cacb-345">The current process is dpi unaware by default.</span></span> <span data-ttu-id="2cacb-346">Puede cambiar este valor mediante programación llamando a la función [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="2cacb-346">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>                                                                                                                                                            |
| <span data-ttu-id="2cacb-347">Contiene "true"</span><span class="sxs-lookup"><span data-stu-id="2cacb-347">Contains "true"</span></span>                   | <span data-ttu-id="2cacb-348">El proceso actual es compatible con PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="2cacb-348">The current process is system dpi aware.</span></span>                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="2cacb-349">Contiene "false"</span><span class="sxs-lookup"><span data-stu-id="2cacb-349">Contains "false"</span></span>                  | <span data-ttu-id="2cacb-350">**Windows Vista, Windows 7 y Windows 8:** El comportamiento es el mismo que cuando el **dpiAware** está ausente.</span><span class="sxs-lookup"><span data-stu-id="2cacb-350">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="2cacb-351">**Windows 8.1 y Windows 10:** El proceso actual no tiene en cuenta el valor de PPP y no se puede cambiar mediante programación con la llamada a la función [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="2cacb-351">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |
| <span data-ttu-id="2cacb-352">Contiene "true/PM"</span><span class="sxs-lookup"><span data-stu-id="2cacb-352">Contains "true/pm"</span></span>                | <span data-ttu-id="2cacb-353">**Windows Vista, Windows 7 y Windows 8:** El proceso actual es compatible con PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="2cacb-353">**Windows Vista, Windows 7 and Windows 8:** The current process is system dpi aware.</span></span><br/> <span data-ttu-id="2cacb-354">**Windows 8.1 y Windows 10:** El proceso actual es compatible con PPP por monitor.</span><span class="sxs-lookup"><span data-stu-id="2cacb-354">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="2cacb-355">Contiene "por monitor"</span><span class="sxs-lookup"><span data-stu-id="2cacb-355">Contains "per monitor"</span></span>            | <span data-ttu-id="2cacb-356">**Windows Vista, Windows 7 y Windows 8:** El comportamiento es el mismo que cuando el **dpiAware** está ausente.</span><span class="sxs-lookup"><span data-stu-id="2cacb-356">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="2cacb-357">**Windows 8.1 y Windows 10:** El proceso actual es compatible con PPP por monitor.</span><span class="sxs-lookup"><span data-stu-id="2cacb-357">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="2cacb-358">Contiene cualquier otra cadena</span><span class="sxs-lookup"><span data-stu-id="2cacb-358">Contains any other string</span></span>         | <span data-ttu-id="2cacb-359">**Windows Vista, Windows 7 y Windows 8:** El comportamiento es el mismo que cuando el **dpiAware** está ausente.</span><span class="sxs-lookup"><span data-stu-id="2cacb-359">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="2cacb-360">**Windows 8.1 y Windows 10:** El proceso actual no tiene en cuenta el valor de PPP y no se puede cambiar mediante programación con la llamada a la función [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="2cacb-360">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |

<span data-ttu-id="2cacb-361">Para obtener más información sobre la configuración de reconocimiento de PPP, consulte [comparación de los niveles de reconocimiento de PPP](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="2cacb-361">For more information about dpi awareness settings, see [Comparison of DPI Awareness Levels](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

<span data-ttu-id="2cacb-362">**dpiAware** no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-362">**dpiAware** has no attributes.</span></span>

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

### <a name="dpiawareness"></a><span data-ttu-id="2cacb-363">dpiAwareness</span><span class="sxs-lookup"><span data-stu-id="2cacb-363">dpiAwareness</span></span>

<span data-ttu-id="2cacb-364">Especifica si el proceso actual tiene reconocimiento de puntos por pulgada (PPP).</span><span class="sxs-lookup"><span data-stu-id="2cacb-364">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="2cacb-365">La versión mínima del sistema operativo que admite el elemento **dpiAwareness** es Windows 10, versión 1607.</span><span class="sxs-lookup"><span data-stu-id="2cacb-365">The minimum version of the operating system that supports the **dpiAwareness** element is Windows 10, version 1607.</span></span> <span data-ttu-id="2cacb-366">En el caso de las versiones que admiten el elemento **dpiAwareness** , el **dpiAwareness** invalida el elemento **dpiAware** .</span><span class="sxs-lookup"><span data-stu-id="2cacb-366">For versions that support the **dpiAwareness** element, the **dpiAwareness** overrides the **dpiAware** element.</span></span> <span data-ttu-id="2cacb-367">Puede incluir ambos elementos en un manifiesto si desea especificar un comportamiento diferente para Windows 10, versión 1607, que para una versión anterior del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2cacb-367">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="2cacb-368">El elemento **dpiAwareness** puede contener un único elemento o una lista de elementos separados por comas.</span><span class="sxs-lookup"><span data-stu-id="2cacb-368">The **dpiAwareness** element can contain a single item or a list of comma-separated items.</span></span> <span data-ttu-id="2cacb-369">En el último caso, se usa el primer elemento (situado más a la izquierda) de la lista reconocido por el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2cacb-369">In the latter case, the first (leftmost) item in the list recognized by the operating system is used.</span></span> <span data-ttu-id="2cacb-370">De esta forma, puede especificar diferentes comportamientos que se admiten en versiones futuras del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="2cacb-370">In this way, you can specify different behaviors supported in future Windows operating system versions.</span></span>

<span data-ttu-id="2cacb-371">En la tabla siguiente se describe el comportamiento que se produce en función de la presencia del elemento **dpiAwareness** y el texto que contiene en el elemento reconocido más a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="2cacb-371">The following table describes the behavior that results based upon the presence of the **dpiAwareness** element and the text that it contains in its leftmost recognized item.</span></span> <span data-ttu-id="2cacb-372">El texto dentro del elemento no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2cacb-372">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="2cacb-373">Estado del elemento **dpiAwareness** :</span><span class="sxs-lookup"><span data-stu-id="2cacb-373">**dpiAwareness** element status:</span></span>        | <span data-ttu-id="2cacb-374">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cacb-374">Description</span></span>                          |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="2cacb-375">Falta el elemento</span><span class="sxs-lookup"><span data-stu-id="2cacb-375">Element is absent</span></span>                       | <span data-ttu-id="2cacb-376">El elemento **dpiAware** especifica si el proceso es compatible con PPP.</span><span class="sxs-lookup"><span data-stu-id="2cacb-376">The **dpiAware** element specifies whether the process is dpi aware.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="2cacb-377">No contiene elementos reconocidos</span><span class="sxs-lookup"><span data-stu-id="2cacb-377">Contains no recognized items</span></span>            | <span data-ttu-id="2cacb-378">El proceso actual no es compatible con PPP de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2cacb-378">The current process is dpi unaware by default.</span></span> <span data-ttu-id="2cacb-379">Puede cambiar este valor mediante programación llamando a la función [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="2cacb-379">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span> |
| <span data-ttu-id="2cacb-380">El primer elemento reconocido es "System"</span><span class="sxs-lookup"><span data-stu-id="2cacb-380">First recognized item is "system"</span></span>       | <span data-ttu-id="2cacb-381">El proceso actual es compatible con PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="2cacb-381">The current process is system dpi aware.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="2cacb-382">El primer elemento reconocido es "permonitor"</span><span class="sxs-lookup"><span data-stu-id="2cacb-382">First recognized item is "permonitor"</span></span>   | <span data-ttu-id="2cacb-383">El proceso actual es compatible con PPP por monitor.</span><span class="sxs-lookup"><span data-stu-id="2cacb-383">The current process is per-monitor dpi aware.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="2cacb-384">El primer elemento reconocido es "permonitorv2"</span><span class="sxs-lookup"><span data-stu-id="2cacb-384">First recognized item is "permonitorv2"</span></span> | <span data-ttu-id="2cacb-385">El proceso actual utiliza el contexto de reconocimiento de PPP por monitor-V2.</span><span class="sxs-lookup"><span data-stu-id="2cacb-385">The current process uses the per-monitor-v2 dpi awareness context.</span></span> <span data-ttu-id="2cacb-386">Este elemento solo se reconocerá en la versión 1703 o posterior de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2cacb-386">This item will only be recognized on Windows 10 version 1703 or later.</span></span>                                                                                              |
| <span data-ttu-id="2cacb-387">El primer elemento reconocido es "no compatible"</span><span class="sxs-lookup"><span data-stu-id="2cacb-387">First recognized item is "unaware"</span></span>      | <span data-ttu-id="2cacb-388">El proceso actual no es compatible con PPP.</span><span class="sxs-lookup"><span data-stu-id="2cacb-388">The current process is dpi unaware.</span></span> <span data-ttu-id="2cacb-389">**No se puede** cambiar este valor mediante programación si se llama a la función [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="2cacb-389">You **cannot** programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>      |

<span data-ttu-id="2cacb-390">Para obtener más información sobre la configuración de reconocimiento de PPP compatible con este elemento, consulte [ \_ reconocimiento de PPP](/windows/desktop/api/windef/ne-windef-dpi_awareness) y [contexto de \_ reconocimiento \_ de PPP](/windows/desktop/hidpi/dpi-awareness-context).</span><span class="sxs-lookup"><span data-stu-id="2cacb-390">For more information about dpi awareness settings supported by this element, see [DPI\_AWARENESS](/windows/desktop/api/windef/ne-windef-dpi_awareness) and [DPI\_AWARENESS\_CONTEXT](/windows/desktop/hidpi/dpi-awareness-context).</span></span>

<span data-ttu-id="2cacb-391">**dpiAwareness** no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-391">**dpiAwareness** has no attributes.</span></span>

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

### <a name="gdiscaling"></a><span data-ttu-id="2cacb-392">gdiScaling</span><span class="sxs-lookup"><span data-stu-id="2cacb-392">gdiScaling</span></span>

<span data-ttu-id="2cacb-393">Especifica si está habilitado el escalado de GDI.</span><span class="sxs-lookup"><span data-stu-id="2cacb-393">Specifies whether GDI scaling is enabled.</span></span> <span data-ttu-id="2cacb-394">La versión mínima del sistema operativo que admite el elemento **gdiScaling** es Windows 10, versión 1703.</span><span class="sxs-lookup"><span data-stu-id="2cacb-394">The minimum version of the operating system that supports the **gdiScaling** element is Windows 10 version 1703.</span></span>

<span data-ttu-id="2cacb-395">El marco de trabajo GDI (interfaz de dispositivo gráfico) puede aplicar el ajuste de escala de PPP a primitivos y texto por monitor sin actualizaciones a la propia aplicación.</span><span class="sxs-lookup"><span data-stu-id="2cacb-395">The GDI (graphics device interface) framework can apply DPI scaling to primitives and text on a per-monitor basis without updates to the application itself.</span></span> <span data-ttu-id="2cacb-396">Esto puede ser útil para las aplicaciones GDI que ya no se actualizan de forma activa.</span><span class="sxs-lookup"><span data-stu-id="2cacb-396">This can be useful for GDI applications no longer being actively updated.</span></span>

<span data-ttu-id="2cacb-397">Este elemento no puede escalar los gráficos no vectoriales (por ejemplo, mapas de bits, iconos o barras de herramientas).</span><span class="sxs-lookup"><span data-stu-id="2cacb-397">Non-vector graphics (such as bitmaps, icons, or toolbars) cannot be scaled by this element.</span></span> <span data-ttu-id="2cacb-398">Además, este elemento no puede escalar los gráficos y el texto que aparecen en los mapas de bits construidos dinámicamente por las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2cacb-398">In addition, graphics and text appearing within bitmaps dynamically constructed by applications also cannot be scaled by this element.</span></span>

<span data-ttu-id="2cacb-399">**True** indica que este elemento está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2cacb-399">**TRUE** indicates that this element is enabled.</span></span> <span data-ttu-id="2cacb-400">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-400">It has no attributes.</span></span>


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

### <a name="highresolutionscrollingaware"></a><span data-ttu-id="2cacb-401">highResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="2cacb-401">highResolutionScrollingAware</span></span>

<span data-ttu-id="2cacb-402">Especifica si está habilitado el reconocimiento de alta resolución.</span><span class="sxs-lookup"><span data-stu-id="2cacb-402">Specifies whether high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="2cacb-403">**True** indica que está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2cacb-403">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="2cacb-404">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-404">It has no attributes.</span></span>

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a><span data-ttu-id="2cacb-405">longPathAware</span><span class="sxs-lookup"><span data-stu-id="2cacb-405">longPathAware</span></span>

<span data-ttu-id="2cacb-406">Habilita rutas de acceso largas que superan **MAX_PATH** de longitud.</span><span class="sxs-lookup"><span data-stu-id="2cacb-406">Enables long paths that exceed **MAX_PATH** in length.</span></span> <span data-ttu-id="2cacb-407">Este elemento es compatible con Windows 10, versión 1607 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2cacb-407">This element is supported in Windows 10, version 1607, and later.</span></span> <span data-ttu-id="2cacb-408">Para obtener más información, consulte [este artículo](../fileio/maximum-file-path-limitation.md).</span><span class="sxs-lookup"><span data-stu-id="2cacb-408">For more information, see [this article](../fileio/maximum-file-path-limitation.md).</span></span>

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

### <a name="printerdriverisolation"></a><span data-ttu-id="2cacb-409">printerDriverIsolation</span><span class="sxs-lookup"><span data-stu-id="2cacb-409">printerDriverIsolation</span></span>

<span data-ttu-id="2cacb-410">Especifica si está habilitado el aislamiento de controladores de impresora.</span><span class="sxs-lookup"><span data-stu-id="2cacb-410">Specifies whether printer driver isolation is enabled.</span></span> <span data-ttu-id="2cacb-411">**True** indica que está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2cacb-411">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="2cacb-412">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-412">It has no attributes.</span></span> <span data-ttu-id="2cacb-413">El aislamiento de controladores de impresora mejora la confiabilidad del servicio de impresión de Windows al permitir que los controladores de impresora se ejecuten en procesos independientes del proceso en el que se ejecuta el administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="2cacb-413">Printer driver isolation improves the reliability of the Windows print service by enabling printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="2cacb-414">Se ha iniciado la compatibilidad con el aislamiento de controladores de impresora en Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="2cacb-414">Support for printer driver isolation started in Windows 7 and Windows Server 2008 R2.</span></span> <span data-ttu-id="2cacb-415">Una aplicación puede declarar el aislamiento del controlador de impresora en el manifiesto de la aplicación para aislarse del controlador de la impresora y mejorar su confiabilidad.</span><span class="sxs-lookup"><span data-stu-id="2cacb-415">An app can declare printer driver isolation in its app manifest to isolate itself from the printer driver and improve its reliability.</span></span> <span data-ttu-id="2cacb-416">Es decir, la aplicación no se bloqueará si el controlador de impresora tiene un error.</span><span class="sxs-lookup"><span data-stu-id="2cacb-416">That is, the app won't crash if the printer driver has an error.</span></span>


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

### <a name="ultrahighresolutionscrollingaware"></a><span data-ttu-id="2cacb-417">ultraHighResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="2cacb-417">ultraHighResolutionScrollingAware</span></span>

<span data-ttu-id="2cacb-418">Especifica si está habilitado el reconocimiento de la resolución ultra alta.</span><span class="sxs-lookup"><span data-stu-id="2cacb-418">Specifies whether ultra-high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="2cacb-419">**True** indica que está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2cacb-419">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="2cacb-420">No tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-420">It has no attributes.</span></span>

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a><span data-ttu-id="2cacb-421">msix</span><span class="sxs-lookup"><span data-stu-id="2cacb-421">msix</span></span>

<span data-ttu-id="2cacb-422">Especifica la información de identidad de un [paquete MSIX disperso](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) para la aplicación actual.</span><span class="sxs-lookup"><span data-stu-id="2cacb-422">Specifies the identity info of a [sparse MSIX package](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) for the current application.</span></span> <span data-ttu-id="2cacb-423">Este elemento es compatible con Windows 10, la versión 2004 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2cacb-423">This element is supported in Windows 10, version 2004, and later versions.</span></span>

<span data-ttu-id="2cacb-424">El elemento **msix** debe estar en el espacio de nombres `urn:schemas-microsoft-com:msix.v1` .</span><span class="sxs-lookup"><span data-stu-id="2cacb-424">The **msix** element must be in the namespace `urn:schemas-microsoft-com:msix.v1`.</span></span> <span data-ttu-id="2cacb-425">Tiene los atributos que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2cacb-425">It has the attributes shown in the following table.</span></span>

| <span data-ttu-id="2cacb-426">Atributo</span><span class="sxs-lookup"><span data-stu-id="2cacb-426">Attribute</span></span>   | <span data-ttu-id="2cacb-427">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cacb-427">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cacb-428">**publisher**</span><span class="sxs-lookup"><span data-stu-id="2cacb-428">**publisher**</span></span>    | <span data-ttu-id="2cacb-429">Describe la información del publicador.</span><span class="sxs-lookup"><span data-stu-id="2cacb-429">Describes the publisher information.</span></span> <span data-ttu-id="2cacb-430">Este valor debe coincidir con el atributo **Publisher** en el elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) en el manifiesto del paquete disperso.</span><span class="sxs-lookup"><span data-stu-id="2cacb-430">This value must match the **Publisher** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span> |
| <span data-ttu-id="2cacb-431">**packageName**</span><span class="sxs-lookup"><span data-stu-id="2cacb-431">**packageName**</span></span> | <span data-ttu-id="2cacb-432">Describe el contenido del paquete.</span><span class="sxs-lookup"><span data-stu-id="2cacb-432">Describes the contents of the package.</span></span> <span data-ttu-id="2cacb-433">Este valor debe coincidir con el atributo **Name** del elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) en el manifiesto del paquete disperso.</span><span class="sxs-lookup"><span data-stu-id="2cacb-433">This value must match the **Name** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span>    |
| <span data-ttu-id="2cacb-434">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="2cacb-434">**applicationId**</span></span>    | <span data-ttu-id="2cacb-435">Identificador único de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2cacb-435">The unique identifier of the application.</span></span> <span data-ttu-id="2cacb-436">Este valor debe coincidir con el atributo **ID** del elemento [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) en el manifiesto del paquete disperso.</span><span class="sxs-lookup"><span data-stu-id="2cacb-436">This value must match the **Id** attribute in the [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) element in your sparse package manifest.</span></span>  |

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

### <a name="heaptype"></a><span data-ttu-id="2cacb-437">heapType</span><span class="sxs-lookup"><span data-stu-id="2cacb-437">heapType</span></span>

<span data-ttu-id="2cacb-438">Invalida la implementación de montón predeterminada para las [API del montón de Win32](../Memory/heap-functions.md) que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="2cacb-438">Overrides the default heap implementation for the [Win32 heap APIs](../Memory/heap-functions.md) to use.</span></span>

* <span data-ttu-id="2cacb-439">El valor **SegmentHeap** indica que se usará el montón del segmento.</span><span class="sxs-lookup"><span data-stu-id="2cacb-439">The value **SegmentHeap** indicates that segment heap will be used.</span></span> <span data-ttu-id="2cacb-440">El montón de segmentos es una implementación de montón moderna que normalmente reducirá el uso de memoria total.</span><span class="sxs-lookup"><span data-stu-id="2cacb-440">Segment heap is a modern heap implementation that will generally reduce your overall memory usage.</span></span> <span data-ttu-id="2cacb-441">Este elemento es compatible con Windows 10, versión 2004 (compilación 19041) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2cacb-441">This element is supported in Windows 10, version 2004 (build 19041) and later.</span></span>
* <span data-ttu-id="2cacb-442">Todos los demás valores se omiten.</span><span class="sxs-lookup"><span data-stu-id="2cacb-442">All other values are ignored.</span></span>

<span data-ttu-id="2cacb-443">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2cacb-443">This element has no attributes.</span></span>

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

## <a name="example"></a><span data-ttu-id="2cacb-444">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2cacb-444">Example</span></span>

<span data-ttu-id="2cacb-445">El siguiente es un ejemplo de un manifiesto de aplicación para una aplicación denominada MySampleApp.exe.</span><span class="sxs-lookup"><span data-stu-id="2cacb-445">The following is an example of an application manifest for an application named MySampleApp.exe.</span></span> <span data-ttu-id="2cacb-446">La aplicación consume el ensamblado en paralelo SampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="2cacb-446">The application consumes the SampleAssembly side-by-side assembly.</span></span>

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

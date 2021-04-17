---
title: Anotaciones de encabezado
description: Las anotaciones de encabezado describen cómo una función usa sus parámetros y el valor devuelto.
ms.assetid: 4f9e42b1-2fe4-4173-946e-ab1805a96b9e
keywords:
- Anotaciones del archivo de encabezado de la API de Windows
- anotaciones del archivo de encabezado
- Specstrings. h
- lenguaje de anotación estándar (SAL)
- _bcount
- _deref
- _deref_opt
- _ecount
- _full
- _in
- _inout
- _opt
- _out
- _part
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8535118383a97d6c48f19246ad24ce324e8bb528
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714430"
---
# <a name="header-annotations"></a><span data-ttu-id="06bc4-117">Anotaciones de encabezado</span><span class="sxs-lookup"><span data-stu-id="06bc4-117">Header Annotations</span></span>

<span data-ttu-id="06bc4-118">\[En este tema se describen las anotaciones admitidas en los encabezados de Windows a través de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="06bc4-118">\[This topic describes the annotations supported in the Windows headers through Windows 7.</span></span> <span data-ttu-id="06bc4-119">Si va a desarrollar para Windows 8, debe usar las anotaciones descritas en [anotaciones de sal]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]</span><span class="sxs-lookup"><span data-stu-id="06bc4-119">If you are developing for Windows 8, you should use the annotations described in [SAL Annotations]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]</span></span>

<span data-ttu-id="06bc4-120">Las anotaciones de encabezado describen cómo una función usa sus parámetros y el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="06bc4-120">Header annotations describe how a function uses its parameters and return value.</span></span> <span data-ttu-id="06bc4-121">Estas anotaciones se han agregado a muchos de los archivos de encabezado de Windows para ayudarle a asegurarse de que está llamando correctamente a la API de Windows.</span><span class="sxs-lookup"><span data-stu-id="06bc4-121">These annotations have been added to many of the Windows header files to help you ensure that you are calling the Windows API correctly.</span></span> <span data-ttu-id="06bc4-122">Si habilita el análisis de código, que está disponible a partir de Visual Studio 2005, el compilador producirá advertencias de nivel 6000 si no está llamando a estas funciones según el uso descrito a través de las anotaciones.</span><span class="sxs-lookup"><span data-stu-id="06bc4-122">If you enable code analysis, which is available starting with the Visual Studio 2005, the compiler will produce level 6000 warnings if you are not calling these functions per the usage described through the annotations.</span></span> <span data-ttu-id="06bc4-123">También puede agregar estas anotaciones en su propio código para asegurarse de que se llama correctamente.</span><span class="sxs-lookup"><span data-stu-id="06bc4-123">You can also add these annotations in your own code to ensure that it is being called correctly.</span></span> <span data-ttu-id="06bc4-124">Para habilitar el análisis de código en Visual Studio, consulte la documentación de su versión de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="06bc4-124">To enable code analysis in Visual Studio, see the documentation for your version of Visual Studio.</span></span>

<span data-ttu-id="06bc4-125">Estas anotaciones se definen en Specstrings. h.</span><span class="sxs-lookup"><span data-stu-id="06bc4-125">These annotations are defined in Specstrings.h.</span></span> <span data-ttu-id="06bc4-126">Se basan en primitivos que forman parte del lenguaje de anotación estándar (SAL) y se implementan mediante `_declspec("SAL_*")` .</span><span class="sxs-lookup"><span data-stu-id="06bc4-126">They are built on primitives that are part of the Standard Annotation Language (SAL) and implemented using `_declspec("SAL_*")`.</span></span>

<span data-ttu-id="06bc4-127">Hay dos clases de anotaciones: anotaciones de búfer y anotaciones avanzadas.</span><span class="sxs-lookup"><span data-stu-id="06bc4-127">There are two classes of annotations: buffer annotations and advanced annotations.</span></span>

## <a name="buffer-annotations"></a><span data-ttu-id="06bc4-128">Anotaciones de búfer</span><span class="sxs-lookup"><span data-stu-id="06bc4-128">Buffer Annotations</span></span>

<span data-ttu-id="06bc4-129">Las anotaciones de búfer describen cómo las funciones usan sus punteros y se pueden usar para detectar saturaciones del búfer.</span><span class="sxs-lookup"><span data-stu-id="06bc4-129">Buffer annotations describe how functions use their pointers and can be used to detect buffer overruns.</span></span> <span data-ttu-id="06bc4-130">Cada parámetro puede usar una anotación de búfer o cero.</span><span class="sxs-lookup"><span data-stu-id="06bc4-130">Each parameter may use zero or one buffer annotation.</span></span> <span data-ttu-id="06bc4-131">Una anotación de búfer se construye con un carácter de subrayado inicial y los componentes descritos en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="06bc4-131">A buffer annotation is constructed with a leading underscore and the components described in the following sections.</span></span>



| <span data-ttu-id="06bc4-132">Tamaño de búfer</span><span class="sxs-lookup"><span data-stu-id="06bc4-132">Buffer size</span></span>                                                                                  | <span data-ttu-id="06bc4-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="06bc4-133">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06bc4-134"><span id="_size_"></span><span id="_SIZE_"></span>(*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-134"><span id="_size_"></span><span id="_SIZE_"></span>(*size*)</span></span><br/>                        | <span data-ttu-id="06bc4-135">Especifica el tamaño total del búfer.</span><span class="sxs-lookup"><span data-stu-id="06bc4-135">Specifies the total size of the buffer.</span></span> <span data-ttu-id="06bc4-136">Se usa con \_ BCOUNT y \_ ecount; no se usa con \_ Part.</span><span class="sxs-lookup"><span data-stu-id="06bc4-136">Use with \_bcount and \_ecount; do not use with \_part.</span></span> <span data-ttu-id="06bc4-137">Este valor es el espacio accesible; puede ser menor que el espacio asignado.</span><span class="sxs-lookup"><span data-stu-id="06bc4-137">This value is the accessible space; it may be less than the allocated space.</span></span><br/> |
| <span data-ttu-id="06bc4-138"><span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-138"><span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*size*,*length*)</span></span><br/> | <span data-ttu-id="06bc4-139">Especifica el tamaño total y la longitud inicializada del búfer.</span><span class="sxs-lookup"><span data-stu-id="06bc4-139">Specifies the total size and initialized length of the buffer.</span></span> <span data-ttu-id="06bc4-140">Se usa con \_ BCOUNT \_ Part y \_ ecount \_ Part.</span><span class="sxs-lookup"><span data-stu-id="06bc4-140">Use with \_bcount\_part and \_ecount\_part.</span></span> <span data-ttu-id="06bc4-141">El tamaño total puede ser menor que el espacio asignado.</span><span class="sxs-lookup"><span data-stu-id="06bc4-141">The total size may be less than the allocated space.</span></span><br/>              |



 



| <span data-ttu-id="06bc4-142">Unidades de tamaño de búfer</span><span class="sxs-lookup"><span data-stu-id="06bc4-142">Buffer size units</span></span>                                                       | <span data-ttu-id="06bc4-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="06bc4-143">Description</span></span>                                |
|-------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="06bc4-144"><span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount</span><span class="sxs-lookup"><span data-stu-id="06bc4-144"><span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount</span></span><br/> | <span data-ttu-id="06bc4-145">El tamaño del búfer está en bytes.</span><span class="sxs-lookup"><span data-stu-id="06bc4-145">The buffer size is in bytes.</span></span><br/>    |
| <span data-ttu-id="06bc4-146"><span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount</span><span class="sxs-lookup"><span data-stu-id="06bc4-146"><span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount</span></span><br/> | <span data-ttu-id="06bc4-147">El tamaño del búfer está en elementos.</span><span class="sxs-lookup"><span data-stu-id="06bc4-147">The buffer size is in elements.</span></span><br/> |



 



| <span data-ttu-id="06bc4-148">Dirección</span><span class="sxs-lookup"><span data-stu-id="06bc4-148">Direction</span></span>                                                            | <span data-ttu-id="06bc4-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="06bc4-149">Description</span></span>                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06bc4-150"><span id="_in"></span><span id="_IN"></span>\_de</span><span class="sxs-lookup"><span data-stu-id="06bc4-150"><span id="_in"></span><span id="_IN"></span>\_in</span></span><br/>          | <span data-ttu-id="06bc4-151">La función Lee del búfer.</span><span class="sxs-lookup"><span data-stu-id="06bc4-151">The function reads from the buffer.</span></span> <span data-ttu-id="06bc4-152">El autor de la llamada proporciona el búfer y lo inicializa.</span><span class="sxs-lookup"><span data-stu-id="06bc4-152">The caller provides the buffer and initializes it.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="06bc4-153"><span id="_inout"></span><span id="_INOUT"></span>\_Inout</span><span class="sxs-lookup"><span data-stu-id="06bc4-153"><span id="_inout"></span><span id="_INOUT"></span>\_inout</span></span><br/> | <span data-ttu-id="06bc4-154">La función Lee y escribe en el búfer.</span><span class="sxs-lookup"><span data-stu-id="06bc4-154">The function both reads from and writes to buffer.</span></span> <span data-ttu-id="06bc4-155">El autor de la llamada proporciona el búfer y lo inicializa.</span><span class="sxs-lookup"><span data-stu-id="06bc4-155">The caller provides the buffer and initializes it.</span></span> <span data-ttu-id="06bc4-156">Si se usa con \_ deref, la función puede reasignar el búfer.</span><span class="sxs-lookup"><span data-stu-id="06bc4-156">If used with \_deref, the buffer may be reallocated by the function.</span></span><br/>                                      |
| <span data-ttu-id="06bc4-157"><span id="_out"></span><span id="_OUT"></span>\_enuncia</span><span class="sxs-lookup"><span data-stu-id="06bc4-157"><span id="_out"></span><span id="_OUT"></span>\_out</span></span><br/>       | <span data-ttu-id="06bc4-158">La función escribe en el búfer.</span><span class="sxs-lookup"><span data-stu-id="06bc4-158">The function writes to the buffer.</span></span> <span data-ttu-id="06bc4-159">Si se usa en el valor devuelto o con \_ deref, la función proporciona el búfer y lo inicializa.</span><span class="sxs-lookup"><span data-stu-id="06bc4-159">If used on the return value or with \_deref, the function provides the buffer and initializes it.</span></span> <span data-ttu-id="06bc4-160">De lo contrario, el autor de la llamada proporciona el búfer y la función lo inicializa.</span><span class="sxs-lookup"><span data-stu-id="06bc4-160">Otherwise, the caller provides the buffer and the function initializes it.</span></span><br/> |



 



| <span data-ttu-id="06bc4-161">Direccionamiento indirecto</span><span class="sxs-lookup"><span data-stu-id="06bc4-161">Indirection</span></span>                                                                       | <span data-ttu-id="06bc4-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="06bc4-162">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06bc4-163"><span id="_deref"></span><span id="_DEREF"></span>\_deref</span><span class="sxs-lookup"><span data-stu-id="06bc4-163"><span id="_deref"></span><span id="_DEREF"></span>\_deref</span></span><br/>              | <span data-ttu-id="06bc4-164">Desreferenciar el parámetro para obtener el puntero de búfer.</span><span class="sxs-lookup"><span data-stu-id="06bc4-164">Dereference the parameter to obtain the buffer pointer.</span></span> <span data-ttu-id="06bc4-165">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="06bc4-165">This parameter may not be **NULL**.</span></span><br/> |
| <span data-ttu-id="06bc4-166"><span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_deref \_ OPT</span><span class="sxs-lookup"><span data-stu-id="06bc4-166"><span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_deref\_opt</span></span><br/> | <span data-ttu-id="06bc4-167">Desreferenciar el parámetro para obtener el puntero de búfer.</span><span class="sxs-lookup"><span data-stu-id="06bc4-167">Dereference the parameter to obtain the buffer pointer.</span></span> <span data-ttu-id="06bc4-168">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="06bc4-168">This parameter can be **NULL**.</span></span><br/>     |



 



| <span data-ttu-id="06bc4-169">Inicialización</span><span class="sxs-lookup"><span data-stu-id="06bc4-169">Initialization</span></span>                                                    | <span data-ttu-id="06bc4-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="06bc4-170">Description</span></span>                                                                                                              |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06bc4-171"><span id="_full"></span><span id="_FULL"></span>\_total</span><span class="sxs-lookup"><span data-stu-id="06bc4-171"><span id="_full"></span><span id="_FULL"></span>\_full</span></span><br/> | <span data-ttu-id="06bc4-172">La función inicializa todo el búfer.</span><span class="sxs-lookup"><span data-stu-id="06bc4-172">The function initializes the entire buffer.</span></span> <span data-ttu-id="06bc4-173">Use solo con búferes de salida.</span><span class="sxs-lookup"><span data-stu-id="06bc4-173">Use only with output buffers.</span></span><br/>                                     |
| <span data-ttu-id="06bc4-174"><span id="_part"></span><span id="_PART"></span>\_referencia</span><span class="sxs-lookup"><span data-stu-id="06bc4-174"><span id="_part"></span><span id="_PART"></span>\_part</span></span><br/> | <span data-ttu-id="06bc4-175">La función inicializa parte del búfer y indica de forma explícita cuánto.</span><span class="sxs-lookup"><span data-stu-id="06bc4-175">The function initializes part of the buffer, and explicitly indicates how much.</span></span> <span data-ttu-id="06bc4-176">Use solo con búferes de salida.</span><span class="sxs-lookup"><span data-stu-id="06bc4-176">Use only with output buffers.</span></span><br/> |



 



| <span data-ttu-id="06bc4-177">Búfer requerido u opcional</span><span class="sxs-lookup"><span data-stu-id="06bc4-177">Required or optional buffer</span></span>                                    | <span data-ttu-id="06bc4-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="06bc4-178">Description</span></span>                                |
|----------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="06bc4-179"><span id="_opt"></span><span id="_OPT"></span>\_rechace</span><span class="sxs-lookup"><span data-stu-id="06bc4-179"><span id="_opt"></span><span id="_OPT"></span>\_opt</span></span><br/> | <span data-ttu-id="06bc4-180">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="06bc4-180">This parameter can be **NULL**.</span></span><br/> |



 

<span data-ttu-id="06bc4-181">En el ejemplo siguiente se muestran las anotaciones de la función **GetModuleFileName** .</span><span class="sxs-lookup"><span data-stu-id="06bc4-181">The following example shows the annotations for the **GetModuleFileName** function.</span></span> <span data-ttu-id="06bc4-182">El parámetro *hModule* es un parámetro de entrada opcional.</span><span class="sxs-lookup"><span data-stu-id="06bc4-182">The *hModule* parameter is an optional input parameter .</span></span> <span data-ttu-id="06bc4-183">El parámetro *lpFilename* es un parámetro de salida; su tamaño en caracteres se especifica mediante el parámetro *nSize* y su longitud incluye el carácter de terminación **null**.</span><span class="sxs-lookup"><span data-stu-id="06bc4-183">The *lpFilename* parameter is an output parameter; its size in characters is specified by the *nSize* parameter and its length includes the **null**-terminating character.</span></span> <span data-ttu-id="06bc4-184">El parámetro *nSize* es un parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="06bc4-184">The *nSize* parameter is an input parameter.</span></span>


```C++
DWORD
WINAPI
GetModuleFileName(
    __in_opt HMODULE hModule,
    __out_ecount_part(nSize, return + 1) LPTSTR lpFilename,
    __in DWORD nSize
    );
```



<span data-ttu-id="06bc4-185">A continuación se enumeran las anotaciones definidas en Specstrings. h.</span><span class="sxs-lookup"><span data-stu-id="06bc4-185">The following are the annotations defined in Specstrings.h.</span></span> <span data-ttu-id="06bc4-186">Utilice la información de las tablas anteriores para interpretar su significado.</span><span class="sxs-lookup"><span data-stu-id="06bc4-186">Use the information in the tables above to interpret their meaning.</span></span>

<span data-ttu-id="06bc4-187">__bcount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-187">__bcount(*size*)</span></span>  
<span data-ttu-id="06bc4-188">__bcount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-188">__bcount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-189">__deref_bcount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-189">__deref_bcount(*size*)</span></span>  
<span data-ttu-id="06bc4-190">__deref_bcount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-190">__deref_bcount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-191">__deref_ecount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-191">__deref_ecount(*size*)</span></span>  
<span data-ttu-id="06bc4-192">__deref_ecount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-192">__deref_ecount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-193">__deref_in</span><span class="sxs-lookup"><span data-stu-id="06bc4-193">__deref_in</span></span>  
<span data-ttu-id="06bc4-194">__deref_in_bcount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-194">__deref_in_bcount(*size*)</span></span>  
<span data-ttu-id="06bc4-195">__deref_in_bcount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-195">__deref_in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-196">__deref_in_ecount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-196">__deref_in_ecount(*size*)</span></span>  
<span data-ttu-id="06bc4-197">__deref_in_ecount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-197">__deref_in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-198">__deref_in_opt</span><span class="sxs-lookup"><span data-stu-id="06bc4-198">__deref_in_opt</span></span>  
<span data-ttu-id="06bc4-199">__deref_inout</span><span class="sxs-lookup"><span data-stu-id="06bc4-199">__deref_inout</span></span>  
<span data-ttu-id="06bc4-200">__deref_inout_bcount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-200">__deref_inout_bcount(*size*)</span></span>  
<span data-ttu-id="06bc4-201">__deref_inout_bcount_full (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-201">__deref_inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="06bc4-202">__deref_inout_bcount_full_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-202">__deref_inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-203">__deref_inout_bcount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-203">__deref_inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-204">__deref_inout_bcount_part (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-204">__deref_inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-205">__deref_inout_bcount_part_opt (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-205">__deref_inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-206">__deref_inout_ecount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-206">__deref_inout_ecount(*size*)</span></span>  
<span data-ttu-id="06bc4-207">__deref_inout_ecount_full (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-207">__deref_inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="06bc4-208">__deref_inout_ecount_full_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-208">__deref_inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-209">__deref_inout_ecount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-209">__deref_inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-210">__deref_inout_ecount_part (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-210">__deref_inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-211">__deref_inout_ecount_part_opt (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-211">__deref_inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-212">__deref_inout_opt</span><span class="sxs-lookup"><span data-stu-id="06bc4-212">__deref_inout_opt</span></span>  
<span data-ttu-id="06bc4-213">__deref_opt_bcount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-213">__deref_opt_bcount(*size*)</span></span>  
<span data-ttu-id="06bc4-214">__deref_opt_bcount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-214">__deref_opt_bcount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-215">__deref_opt_ecount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-215">__deref_opt_ecount(*size*)</span></span>  
<span data-ttu-id="06bc4-216">__deref_opt_ecount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-216">__deref_opt_ecount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-217">__deref_opt_in</span><span class="sxs-lookup"><span data-stu-id="06bc4-217">__deref_opt_in</span></span>  
<span data-ttu-id="06bc4-218">__deref_opt_in_bcount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-218">__deref_opt_in_bcount(*size*)</span></span>  
<span data-ttu-id="06bc4-219">__deref_opt_in_bcount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-219">__deref_opt_in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-220">__deref_opt_in_ecount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-220">__deref_opt_in_ecount(*size*)</span></span>  
<span data-ttu-id="06bc4-221">__deref_opt_in_ecount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-221">__deref_opt_in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-222">__deref_opt_in_opt</span><span class="sxs-lookup"><span data-stu-id="06bc4-222">__deref_opt_in_opt</span></span>  
<span data-ttu-id="06bc4-223">__deref_opt_inout</span><span class="sxs-lookup"><span data-stu-id="06bc4-223">__deref_opt_inout</span></span>  
<span data-ttu-id="06bc4-224">__deref_opt_inout_bcount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-224">__deref_opt_inout_bcount(*size*)</span></span>  
<span data-ttu-id="06bc4-225">__deref_opt_inout_bcount_full (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-225">__deref_opt_inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="06bc4-226">__deref_opt_inout_bcount_full_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-226">__deref_opt_inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-227">__deref_opt_inout_bcount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-227">__deref_opt_inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-228">__deref_opt_inout_bcount_part (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-228">__deref_opt_inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-229">__deref_opt_inout_bcount_part_opt (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-229">__deref_opt_inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-230">__deref_opt_inout_ecount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-230">__deref_opt_inout_ecount(*size*)</span></span>  
<span data-ttu-id="06bc4-231">__deref_opt_inout_ecount_full (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-231">__deref_opt_inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="06bc4-232">__deref_opt_inout_ecount_full_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-232">__deref_opt_inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-233">__deref_opt_inout_ecount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-233">__deref_opt_inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-234">__deref_opt_inout_ecount_part (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-234">__deref_opt_inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-235">__deref_opt_inout_ecount_part_opt (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-235">__deref_opt_inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-236">__deref_opt_inout_opt</span><span class="sxs-lookup"><span data-stu-id="06bc4-236">__deref_opt_inout_opt</span></span>  
<span data-ttu-id="06bc4-237">__deref_opt_out</span><span class="sxs-lookup"><span data-stu-id="06bc4-237">__deref_opt_out</span></span>  
<span data-ttu-id="06bc4-238">__deref_opt_out_bcount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-238">__deref_opt_out_bcount(*size*)</span></span>  
<span data-ttu-id="06bc4-239">__deref_opt_out_bcount_full (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-239">__deref_opt_out_bcount_full(*size*)</span></span>  
<span data-ttu-id="06bc4-240">__deref_opt_out_bcount_full_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-240">__deref_opt_out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-241">__deref_opt_out_bcount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-241">__deref_opt_out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-242">__deref_opt_out_bcount_part (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-242">__deref_opt_out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-243">__deref_opt_out_bcount_part_opt (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-243">__deref_opt_out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-244">__deref_opt_out_ecount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-244">__deref_opt_out_ecount(*size*)</span></span>  
<span data-ttu-id="06bc4-245">__deref_opt_out_ecount_full (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-245">__deref_opt_out_ecount_full(*size*)</span></span>  
<span data-ttu-id="06bc4-246">__deref_opt_out_ecount_full_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-246">__deref_opt_out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-247">__deref_opt_out_ecount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-247">__deref_opt_out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-248">__deref_opt_out_ecount_part (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-248">__deref_opt_out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-249">__deref_opt_out_ecount_part_opt (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-249">__deref_opt_out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-250">__deref_opt_out_opt</span><span class="sxs-lookup"><span data-stu-id="06bc4-250">__deref_opt_out_opt</span></span>  
<span data-ttu-id="06bc4-251">__deref_out</span><span class="sxs-lookup"><span data-stu-id="06bc4-251">__deref_out</span></span>  
<span data-ttu-id="06bc4-252">__deref_out_bcount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-252">__deref_out_bcount(*size*)</span></span>  
<span data-ttu-id="06bc4-253">__deref_out_bcount_full (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-253">__deref_out_bcount_full(*size*)</span></span>  
<span data-ttu-id="06bc4-254">__deref_out_bcount_full_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-254">__deref_out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-255">__deref_out_bcount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-255">__deref_out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-256">__deref_out_bcount_part (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-256">__deref_out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-257">__deref_out_bcount_part_opt (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-257">__deref_out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-258">__deref_out_ecount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-258">__deref_out_ecount(*size*)</span></span>  
<span data-ttu-id="06bc4-259">__deref_out_ecount_full (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-259">__deref_out_ecount_full(*size*)</span></span>  
<span data-ttu-id="06bc4-260">__deref_out_ecount_full_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-260">__deref_out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-261">__deref_out_ecount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-261">__deref_out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-262">__deref_out_ecount_part (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-262">__deref_out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-263">__deref_out_ecount_part_opt (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-263">__deref_out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-264">__deref_out_opt</span><span class="sxs-lookup"><span data-stu-id="06bc4-264">__deref_out_opt</span></span>  
<span data-ttu-id="06bc4-265">__ecount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-265">__ecount(*size*)</span></span>  
<span data-ttu-id="06bc4-266">__ecount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-266">__ecount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-267">__in</span><span class="sxs-lookup"><span data-stu-id="06bc4-267">__in</span></span>  
<span data-ttu-id="06bc4-268">__in_bcount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-268">__in_bcount(*size*)</span></span>  
<span data-ttu-id="06bc4-269">__in_bcount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-269">__in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-270">__in_ecount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-270">__in_ecount(*size*)</span></span>  
<span data-ttu-id="06bc4-271">__in_ecount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-271">__in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-272">__in_opt</span><span class="sxs-lookup"><span data-stu-id="06bc4-272">__in_opt</span></span>  
<span data-ttu-id="06bc4-273">__inout</span><span class="sxs-lookup"><span data-stu-id="06bc4-273">__inout</span></span>  
<span data-ttu-id="06bc4-274">__inout_bcount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-274">__inout_bcount(*size*)</span></span>  
<span data-ttu-id="06bc4-275">__inout_bcount_full (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-275">__inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="06bc4-276">__inout_bcount_full_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-276">__inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-277">__inout_bcount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-277">__inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-278">__inout_bcount_part (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-278">__inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-279">__inout_bcount_part_opt (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-279">__inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-280">__inout_ecount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-280">__inout_ecount(*size*)</span></span>  
<span data-ttu-id="06bc4-281">__inout_ecount_full (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-281">__inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="06bc4-282">__inout_ecount_full_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-282">__inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-283">__inout_ecount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-283">__inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-284">__inout_ecount_part (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-284">__inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-285">__inout_ecount_part_opt (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-285">__inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-286">__inout_opt</span><span class="sxs-lookup"><span data-stu-id="06bc4-286">__inout_opt</span></span>  
<span data-ttu-id="06bc4-287">__out</span><span class="sxs-lookup"><span data-stu-id="06bc4-287">__out</span></span>  
<span data-ttu-id="06bc4-288">__out_bcount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-288">__out_bcount(*size*)</span></span>  
<span data-ttu-id="06bc4-289">__out_bcount_full (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-289">__out_bcount_full(*size*)</span></span>  
<span data-ttu-id="06bc4-290">__out_bcount_full_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-290">__out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-291">__out_bcount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-291">__out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-292">__out_bcount_part (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-292">__out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-293">__out_bcount_part_opt (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-293">__out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-294">__out_ecount (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-294">__out_ecount(*size*)</span></span>  
<span data-ttu-id="06bc4-295">__out_ecount_full (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-295">__out_ecount_full(*size*)</span></span>  
<span data-ttu-id="06bc4-296">__out_ecount_full_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-296">__out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-297">__out_ecount_opt (*tamaño*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-297">__out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="06bc4-298">__out_ecount_part (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-298">__out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-299">__out_ecount_part_opt (*tamaño*,*longitud*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-299">__out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="06bc4-300">__out_opt</span><span class="sxs-lookup"><span data-stu-id="06bc4-300">__out_opt</span></span>  

## <a name="advanced-annotations"></a><span data-ttu-id="06bc4-301">Anotaciones avanzadas</span><span class="sxs-lookup"><span data-stu-id="06bc4-301">Advanced Annotations</span></span>

<span data-ttu-id="06bc4-302">Las anotaciones avanzadas proporcionan información adicional sobre el parámetro o el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="06bc4-302">Advanced annotations provide additional information about the parameter or return value.</span></span> <span data-ttu-id="06bc4-303">Cada parámetro o valor devuelto puede usar cero o una anotación avanzada.</span><span class="sxs-lookup"><span data-stu-id="06bc4-303">Each parameter or return value may use zero or one advanced annotation.</span></span>



| <span data-ttu-id="06bc4-304">Anotación</span><span class="sxs-lookup"><span data-stu-id="06bc4-304">Annotation</span></span>                                                                                                                                               | <span data-ttu-id="06bc4-305">Descripción</span><span class="sxs-lookup"><span data-stu-id="06bc4-305">Description</span></span>                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06bc4-306"><span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_bloqueos (*recurso*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-306"><span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocksOn(*resource*)</span></span><br/> | <span data-ttu-id="06bc4-307">Las funciones se bloquean en el recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="06bc4-307">The functions blocks on the specified resource.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="06bc4-308"><span id="__callback"></span><span id="__CALLBACK"></span>\_\_regreso</span><span class="sxs-lookup"><span data-stu-id="06bc4-308"><span id="__callback"></span><span id="__CALLBACK"></span>\_\_callback</span></span><br/>                                                                        | <span data-ttu-id="06bc4-309">La función se puede usar como un puntero de función.</span><span class="sxs-lookup"><span data-stu-id="06bc4-309">The function can be used as a function pointer.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="06bc4-310"><span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn</span><span class="sxs-lookup"><span data-stu-id="06bc4-310"><span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn</span></span><br/>                               | <span data-ttu-id="06bc4-311">Los llamadores deben comprobar el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="06bc4-311">Callers must check the return value.</span></span><br/>                                                                                                                                                                                                                                 |
| <span data-ttu-id="06bc4-312"><span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_cadena de formato \_</span><span class="sxs-lookup"><span data-stu-id="06bc4-312"><span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_format\_string</span></span><br/>                                                        | <span data-ttu-id="06bc4-313">El parámetro es una cadena que contiene marcadores% de estilo printf.</span><span class="sxs-lookup"><span data-stu-id="06bc4-313">The parameter is a string that contains printf-style % markers.</span></span><br/>                                                                                                                                                                                                      |
| <span data-ttu-id="06bc4-314"><span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_en \_ awcount (*expr*,*size*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-314"><span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_in\_awcount(*expr*,*size*)</span></span><br/>                            | <span data-ttu-id="06bc4-315">Si la expresión es true en la salida, el tamaño del búfer de entrada se especifica en bytes.</span><span class="sxs-lookup"><span data-stu-id="06bc4-315">If the expression is true at exit, the size of the input buffer is specified in bytes.</span></span> <span data-ttu-id="06bc4-316">Si la expresión es false, el tamaño se especifica en elementos.</span><span class="sxs-lookup"><span data-stu-id="06bc4-316">If the expression is false, the size is specified in elements.</span></span><br/>                                                                                                                |
| <span data-ttu-id="06bc4-317"><span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated</span><span class="sxs-lookup"><span data-stu-id="06bc4-317"><span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated</span></span><br/>                                          | <span data-ttu-id="06bc4-318">Se puede tener acceso al búfer hasta e incluir la primera secuencia de dos caracteres **nulos** o punteros.</span><span class="sxs-lookup"><span data-stu-id="06bc4-318">The buffer may be accessed up to and including the first sequence of two **null** characters or pointers.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="06bc4-319"><span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_NullTerminated</span><span class="sxs-lookup"><span data-stu-id="06bc4-319"><span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_nullterminated</span></span><br/>                                                      | <span data-ttu-id="06bc4-320">Se puede tener acceso al búfer hasta el primer carácter o puntero **nulo** o incluirlo.</span><span class="sxs-lookup"><span data-stu-id="06bc4-320">The buffer may be accessed up to and including the first **null** character or pointer.</span></span><br/>                                                                                                                                                                              |
| <span data-ttu-id="06bc4-321"><span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out \_ awcount (*expr*,*size*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-321"><span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out\_awcount(*expr*,*size*)</span></span><br/>                         | <span data-ttu-id="06bc4-322">Si la expresión es true en la salida, el tamaño del búfer de salida se especifica en bytes.</span><span class="sxs-lookup"><span data-stu-id="06bc4-322">If the expression is true at exit, the size of the output buffer is specified in bytes.</span></span> <span data-ttu-id="06bc4-323">Si la expresión es false, el tamaño se especifica en elementos.</span><span class="sxs-lookup"><span data-stu-id="06bc4-323">If the expression is false, the size is specified in elements.</span></span> <br/>                                                                                                              |
| <span data-ttu-id="06bc4-324"><span id="__override"></span><span id="__OVERRIDE"></span>\_\_estima</span><span class="sxs-lookup"><span data-stu-id="06bc4-324"><span id="__override"></span><span id="__OVERRIDE"></span>\_\_override</span></span><br/>                                                                        | <span data-ttu-id="06bc4-325">Especifica el comportamiento de invalidación de estilo C# para los métodos virtuales.</span><span class="sxs-lookup"><span data-stu-id="06bc4-325">Specifies C#-style override behavior for virtual methods.</span></span><br/>                                                                                                                                                                                                           |
| <span data-ttu-id="06bc4-326"><span id="__reserved"></span><span id="__RESERVED"></span>\_\_sector</span><span class="sxs-lookup"><span data-stu-id="06bc4-326"><span id="__reserved"></span><span id="__RESERVED"></span>\_\_reserved</span></span><br/>                                                                        | <span data-ttu-id="06bc4-327">El parámetro está reservado para un uso futuro y debe ser cero o **null**.</span><span class="sxs-lookup"><span data-stu-id="06bc4-327">The parameter is reserved for future use and must be zero or **NULL**.</span></span><br/>                                                                                                                                                                                               |
| <span data-ttu-id="06bc4-328"><span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_correcto (*expr*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-328"><span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_success(*expr*)</span></span><br/>                                                       | <span data-ttu-id="06bc4-329">Si la expresión es true en la salida, el autor de la llamada puede confiar en todas las garantías especificadas por otras anotaciones.</span><span class="sxs-lookup"><span data-stu-id="06bc4-329">If the expression is true at exit, the caller can rely on all guarantees specified by other annotations.</span></span> <span data-ttu-id="06bc4-330">Si la expresión es falsa, el autor de la llamada no puede confiar en las garantías.</span><span class="sxs-lookup"><span data-stu-id="06bc4-330">If the expression is false, the caller cannot rely on the guarantees.</span></span> <span data-ttu-id="06bc4-331">Esta anotación se agrega automáticamente a las funciones que devuelven un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06bc4-331">This annotation is automatically added to functions that return an **HRESULT** value.</span></span><br/> |
| <span data-ttu-id="06bc4-332"><span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix (*CType*)</span><span class="sxs-lookup"><span data-stu-id="06bc4-332"><span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix(*ctype*)</span></span><br/>                                                    | <span data-ttu-id="06bc4-333">Trate el parámetro como el tipo especificado en lugar de su tipo declarado.</span><span class="sxs-lookup"><span data-stu-id="06bc4-333">Treat the parameter as the specified type rather than its declared type.</span></span><br/>                                                                                                                                                                                             |



 

<span data-ttu-id="06bc4-334">En los siguientes ejemplos se muestra el búfer y las anotaciones avanzadas para las funciones [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa)y [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) .</span><span class="sxs-lookup"><span data-stu-id="06bc4-334">The following examples show the buffer and advanced annotations for the [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa), and [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) functions.</span></span>


```C++
__checkReturn
BOOL
WINAPI
DeleteTimerQueueTimer(
    __in_opt HANDLE TimerQueue,
    __in     HANDLE Timer,
    __in_opt HANDLE CompletionEvent
    );

BOOL
WINAPI
FreeEnvironmentStrings(
    __in __nullnullterminated LPTCH
    );

__callback
LONG
WINAPI
UnhandledExceptionFilter(
    __in struct _EXCEPTION_POINTERS *ExceptionInfo
    );

```



## <a name="related-topics"></a><span data-ttu-id="06bc4-335">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06bc4-335">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06bc4-336">Anotaciones SAL</span><span class="sxs-lookup"><span data-stu-id="06bc4-336">SAL Annotations</span></span>](/cpp/c-runtime-library/sal-annotations?view=vs-2019)
</dt> <dt>

[<span data-ttu-id="06bc4-337">Tutorial: Analizar código de C/C++ en previsión de defectos</span><span class="sxs-lookup"><span data-stu-id="06bc4-337">Walkthrough: Analyzing C/C++ Code for Defects</span></span>](/visualstudio/code-quality/walkthrough-analyzing-c-cpp-code-for-defects?view=vs-2015)
</dt> </dl>

 


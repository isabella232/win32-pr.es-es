---
title: Especificación de firmas de raíz en HLSL
description: Especificar firmas raíz en el modelo de sombreador de HLSL 5,1 es una alternativa a especificarlas en código de C++.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236876e22c3e1e0bb849ec1e1bc7d45692c900d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549073"
---
# <a name="specifying-root-signatures-in-hlsl"></a><span data-ttu-id="75d60-103">Especificación de firmas de raíz en HLSL</span><span class="sxs-lookup"><span data-stu-id="75d60-103">Specifying Root Signatures in HLSL</span></span>

<span data-ttu-id="75d60-104">Especificar firmas raíz en el modelo de sombreador de HLSL 5,1 es una alternativa a especificarlas en código de C++.</span><span class="sxs-lookup"><span data-stu-id="75d60-104">Specifying root signatures in HLSL Shader Model 5.1 is an alternative to specifying them in C++ code.</span></span>

-   [<span data-ttu-id="75d60-105">Una firma raíz HLSL de ejemplo</span><span class="sxs-lookup"><span data-stu-id="75d60-105">An example HLSL Root Signature</span></span>](#an-example-hlsl-root-signature)
    -   [<span data-ttu-id="75d60-106">Versión de firma raíz 1,0</span><span class="sxs-lookup"><span data-stu-id="75d60-106">Root Signature Version 1.0</span></span>](#root-signature-version-10)
    -   [<span data-ttu-id="75d60-107">Versión de firma raíz 1,1</span><span class="sxs-lookup"><span data-stu-id="75d60-107">Root Signature Version 1.1</span></span>](#root-signature-version-11)
-   [<span data-ttu-id="75d60-108">RootFlags</span><span class="sxs-lookup"><span data-stu-id="75d60-108">RootFlags</span></span>](#rootflags)
-   [<span data-ttu-id="75d60-109">Constantes raíz</span><span class="sxs-lookup"><span data-stu-id="75d60-109">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="75d60-110">Visibilidad</span><span class="sxs-lookup"><span data-stu-id="75d60-110">Visibility</span></span>](#visibility)
-   [<span data-ttu-id="75d60-111">CBV de nivel de raíz</span><span class="sxs-lookup"><span data-stu-id="75d60-111">Root-level CBV</span></span>](#root-level-cbv)
-   [<span data-ttu-id="75d60-112">SRV de nivel de raíz</span><span class="sxs-lookup"><span data-stu-id="75d60-112">Root-level SRV</span></span>](#root-level-srv)
-   [<span data-ttu-id="75d60-113">UAV de nivel de raíz</span><span class="sxs-lookup"><span data-stu-id="75d60-113">Root-level UAV</span></span>](#root-level-uav)
-   [<span data-ttu-id="75d60-114">Tabla de descriptores</span><span class="sxs-lookup"><span data-stu-id="75d60-114">Descriptor Table</span></span>](#descriptor-table)
-   [<span data-ttu-id="75d60-115">Muestra estática</span><span class="sxs-lookup"><span data-stu-id="75d60-115">Static Sampler</span></span>](#static-sampler)
-   [<span data-ttu-id="75d60-116">Compilar una firma raíz HLSL</span><span class="sxs-lookup"><span data-stu-id="75d60-116">Compiling an HLSL root signature</span></span>](#compiling-an-hlsl-root-signature)
-   [<span data-ttu-id="75d60-117">Manipular firmas raíz con el compilador FXC</span><span class="sxs-lookup"><span data-stu-id="75d60-117">Manipulating root signatures with the FXC compiler</span></span>](#manipulating-root-signatures-with-the-fxc-compiler)
-   [<span data-ttu-id="75d60-118">Notas</span><span class="sxs-lookup"><span data-stu-id="75d60-118">Notes</span></span>](#notes)
-   [<span data-ttu-id="75d60-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75d60-119">Related topics</span></span>](#related-topics)

## <a name="an-example-hlsl-root-signature"></a><span data-ttu-id="75d60-120">Una firma raíz HLSL de ejemplo</span><span class="sxs-lookup"><span data-stu-id="75d60-120">An example HLSL Root Signature</span></span>

<span data-ttu-id="75d60-121">Se puede especificar una firma raíz en HLSL como una cadena.</span><span class="sxs-lookup"><span data-stu-id="75d60-121">A root signature can be specified in HLSL as a string.</span></span> <span data-ttu-id="75d60-122">La cadena contiene una colección de cláusulas separadas por comas que describen los componentes constituyentes de la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="75d60-122">The string contains a collection of comma-separated clauses that describe root signature constituent components.</span></span> <span data-ttu-id="75d60-123">La firma raíz debe ser idéntica en los distintos sombreadores de cualquier objeto de estado de canalización (PSO).</span><span class="sxs-lookup"><span data-stu-id="75d60-123">The root signature should be identical across shaders for any one pipeline state object (PSO).</span></span> <span data-ttu-id="75d60-124">Este es un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="75d60-124">Here is an example:</span></span>

### <a name="root-signature-version-10"></a><span data-ttu-id="75d60-125">Versión de firma raíz 1,0</span><span class="sxs-lookup"><span data-stu-id="75d60-125">Root Signature Version 1.0</span></span>

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1), " \
              "SRV(t0), " \
              "UAV(u0, visibility = SHADER_VISIBILITY_GEOMETRY), " \
              "DescriptorTable( CBV(b0), " \
                               "UAV(u1, numDescriptors = 2), " \
                               "SRV(t1, numDescriptors = unbounded)), " \
              "DescriptorTable(Sampler(s0, numDescriptors = 2)), " \
              "RootConstants(num32BitConstants=1, b9), " \
              "DescriptorTable( UAV(u3), " \
                               "UAV(u4), " \
                               "UAV(u5, offset=1)), " \

              "StaticSampler(s2)," \
              "StaticSampler(s3, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

### <a name="root-signature-version-11"></a><span data-ttu-id="75d60-126">Versión de firma raíz 1,1</span><span class="sxs-lookup"><span data-stu-id="75d60-126">Root Signature Version 1.1</span></span>

<span data-ttu-id="75d60-127">La [versión 1,1 de la firma raíz](root-signature-version-1-1.md) habilita las optimizaciones del controlador en los datos y los descriptores de la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="75d60-127">[Root Signature Version 1.1](root-signature-version-1-1.md) enables driver optimizations on root signature descriptors and data.</span></span>

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1, flags = DATA_STATIC), " \
              "SRV(t0), " \
              "UAV(u0), " \
              "DescriptorTable( CBV(b1), " \
                               "SRV(t1, numDescriptors = 8, " \
                               "        flags = DESCRIPTORS_VOLATILE), " \
                               "UAV(u1, numDescriptors = unbounded, " \
                               "        flags = DESCRIPTORS_VOLATILE)), " \
              "DescriptorTable(Sampler(s0, space=1, numDescriptors = 4)), " \
              "RootConstants(num32BitConstants=3, b10), " \
              "StaticSampler(s1)," \
              "StaticSampler(s2, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

<span data-ttu-id="75d60-128">Esta definición proporcionaría la siguiente firma raíz:</span><span class="sxs-lookup"><span data-stu-id="75d60-128">This definition would give the following root signature, noting:</span></span>

-   <span data-ttu-id="75d60-129">El uso de parámetros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="75d60-129">The use of default parameters.</span></span>
-   <span data-ttu-id="75d60-130">B0 y (b0, Space = 1) no entran en conflicto</span><span class="sxs-lookup"><span data-stu-id="75d60-130">b0 and (b0, space=1) do not conflict</span></span>
-   <span data-ttu-id="75d60-131">U0 solo es visible para el sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="75d60-131">u0 is only visible to the geometry shader</span></span>
-   <span data-ttu-id="75d60-132">U4 y U5 tienen un alias en el mismo descriptor de un montón</span><span class="sxs-lookup"><span data-stu-id="75d60-132">u4 and u5 are aliased to the same descriptor in a heap</span></span>

![una firma raíz especificada mediante el lenguaje de sombreador de alto nivel](images/hlsl-root-signature.png)

<span data-ttu-id="75d60-134">El lenguaje de firma raíz de HLSL se corresponde estrechamente con las API de firma raíz de C++ y tiene una potencia expresiva equivalente.</span><span class="sxs-lookup"><span data-stu-id="75d60-134">The HLSL root signature language closely corresponds to the C++ root signature APIs and has equivalent expressive power.</span></span> <span data-ttu-id="75d60-135">La firma raíz se especifica como una secuencia de cláusulas, separadas por comas.</span><span class="sxs-lookup"><span data-stu-id="75d60-135">The root signature is specified as a sequence of clauses, separated by comma.</span></span> <span data-ttu-id="75d60-136">El orden de las cláusulas es importante, ya que el orden de análisis determina la posición de la ranura en la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="75d60-136">The order of clauses is important, as the order of parsing determines the slot position in the root signature.</span></span> <span data-ttu-id="75d60-137">Cada cláusula toma uno o varios parámetros con nombre.</span><span class="sxs-lookup"><span data-stu-id="75d60-137">Each clause takes one or more named parameters.</span></span> <span data-ttu-id="75d60-138">Sin embargo, el orden de los parámetros no es importante.</span><span class="sxs-lookup"><span data-stu-id="75d60-138">The order of parameters is not important, however.</span></span>

## <a name="rootflags"></a><span data-ttu-id="75d60-139">RootFlags</span><span class="sxs-lookup"><span data-stu-id="75d60-139">RootFlags</span></span>

<span data-ttu-id="75d60-140">La cláusula *RootFlags* opcional toma 0 (el valor predeterminado para indicar que no hay marcas) o uno o varios valores de marcas de raíz predefinidos, conectados mediante el \| operador o ' '.</span><span class="sxs-lookup"><span data-stu-id="75d60-140">The optional *RootFlags* clause takes either 0 (the default value to indicate no flags), or one or several of predefined root flags values, connected via the OR ‘\|’ operator.</span></span> <span data-ttu-id="75d60-141">Los valores de marca de raíz permitidos se definen mediante [**\_ \_ \_ marcas de firma raíz de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span><span class="sxs-lookup"><span data-stu-id="75d60-141">The allowed root flag values are defined by [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

<span data-ttu-id="75d60-142">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="75d60-142">For example:</span></span>

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a><span data-ttu-id="75d60-143">Constantes raíz</span><span class="sxs-lookup"><span data-stu-id="75d60-143">Root Constants</span></span>

<span data-ttu-id="75d60-144">La cláusula *RootConstants* especifica las constantes raíz en la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="75d60-144">The *RootConstants* clause specifies root constants in the root signature.</span></span> <span data-ttu-id="75d60-145">Dos parámetros obligatorios son: *num32BitConstants* y *bReg* (el registro correspondiente a *BaseShaderRegister* en las API de C++) de *CBuffer*.</span><span class="sxs-lookup"><span data-stu-id="75d60-145">Two mandatory parameters are: *num32BitConstants* and *bReg* (the register corresponding to *BaseShaderRegister* in C++ APIs) of the *cbuffer*.</span></span> <span data-ttu-id="75d60-146">Los parámetros Space (*RegisterSpace* en las API de c++) y Visibility (*ShaderVisibility* en c++) son opcionales y los valores predeterminados son:</span><span class="sxs-lookup"><span data-stu-id="75d60-146">The space (*RegisterSpace* in C++ APIs) and visibility (*ShaderVisibility* in C++) parameters are optional, and the default values are:</span></span>

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

<span data-ttu-id="75d60-147">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="75d60-147">For example:</span></span>

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a><span data-ttu-id="75d60-148">Visibilidad</span><span class="sxs-lookup"><span data-stu-id="75d60-148">Visibility</span></span>

<span data-ttu-id="75d60-149">Visibility es un parámetro opcional que puede tener uno de los valores de [**la \_ \_ visibilidad del sombreador D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span><span class="sxs-lookup"><span data-stu-id="75d60-149">Visibility is an optional parameter that can have one of the values from [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

<span data-ttu-id="75d60-150">\_La visibilidad del sombreador \_ difunde los argumentos raíz a todos los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="75d60-150">SHADER\_VISIBILITY\_ALL broadcasts the root arguments to all shaders.</span></span> <span data-ttu-id="75d60-151">En algunos equipos, esto no tiene ningún costo, pero en otro hardware hay un costo para bifurcar los datos a todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="75d60-151">On some hardware this has no cost, but on other hardware there is a cost to fork the data to all the shader stages.</span></span> <span data-ttu-id="75d60-152">La configuración de una de las opciones, como \_ el vértice de visibilidad del sombreador \_ , limita el argumento raíz a una sola etapa del sombreador.</span><span class="sxs-lookup"><span data-stu-id="75d60-152">Setting one of the options, such as SHADER\_VISIBILITY\_VERTEX, limits the root argument to a single shader stage.</span></span>

<span data-ttu-id="75d60-153">Establecer los argumentos raíz en fases del sombreador único permite usar el mismo nombre de enlace en diferentes fases.</span><span class="sxs-lookup"><span data-stu-id="75d60-153">Setting root arguments to single shader stages allows the same bind name to be used at different stages.</span></span> <span data-ttu-id="75d60-154">Por ejemplo, un enlace SRV de `t0,SHADER_VISIBILITY_VERTEX` y el enlace SRV de `t0,SHADER_VISIBILITY_PIXEL` serían válidos.</span><span class="sxs-lookup"><span data-stu-id="75d60-154">For example, an SRV binding of `t0,SHADER_VISIBILITY_VERTEX` and SRV binding of `t0,SHADER_VISIBILITY_PIXEL` would be valid.</span></span> <span data-ttu-id="75d60-155">Pero si la configuración de visibilidad era `t0,SHADER_VISIBILITY_ALL` para uno de los enlaces, la signatura raíz no sería válida.</span><span class="sxs-lookup"><span data-stu-id="75d60-155">But if the visibility setting was `t0,SHADER_VISIBILITY_ALL` for one of the bindings, the root signature would be invalid.</span></span>

## <a name="root-level-cbv"></a><span data-ttu-id="75d60-156">CBV de nivel de raíz</span><span class="sxs-lookup"><span data-stu-id="75d60-156">Root-level CBV</span></span>

<span data-ttu-id="75d60-157">La `CBV` cláusula (vista de búfer de constantes) especifica una entrada de registro del búfer de constantes de nivel de raíz.</span><span class="sxs-lookup"><span data-stu-id="75d60-157">The `CBV` (constant buffer view) clause specifies a root-level constant buffer b-register Reg entry.</span></span> <span data-ttu-id="75d60-158">Tenga en cuenta que se trata de una entrada escalar; no es posible especificar un intervalo para el nivel raíz.</span><span class="sxs-lookup"><span data-stu-id="75d60-158">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a><span data-ttu-id="75d60-159">SRV de nivel de raíz</span><span class="sxs-lookup"><span data-stu-id="75d60-159">Root-level SRV</span></span>

<span data-ttu-id="75d60-160">La `SRV` cláusula (vista de recursos del sombreador) especifica una entrada de registro de registro t-Register SRV de nivel de raíz.</span><span class="sxs-lookup"><span data-stu-id="75d60-160">The `SRV` (shader resource view) clause specifies a root-level SRV t-register Reg entry.</span></span> <span data-ttu-id="75d60-161">Tenga en cuenta que se trata de una entrada escalar; no es posible especificar un intervalo para el nivel raíz.</span><span class="sxs-lookup"><span data-stu-id="75d60-161">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a><span data-ttu-id="75d60-162">UAV de nivel de raíz</span><span class="sxs-lookup"><span data-stu-id="75d60-162">Root-level UAV</span></span>

<span data-ttu-id="75d60-163">La `UAV` cláusula (vista de acceso desordenado) especifica una entrada de registro de UAV u-Register reg de nivel de raíz.</span><span class="sxs-lookup"><span data-stu-id="75d60-163">The `UAV` (unordered access view) clause specifies a root-level UAV u-register Reg entry.</span></span> <span data-ttu-id="75d60-164">Tenga en cuenta que se trata de una entrada escalar; no es posible especificar un intervalo para el nivel raíz.</span><span class="sxs-lookup"><span data-stu-id="75d60-164">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="75d60-165">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="75d60-165">For example:</span></span>

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a><span data-ttu-id="75d60-166">Tabla de descriptores</span><span class="sxs-lookup"><span data-stu-id="75d60-166">Descriptor Table</span></span>

<span data-ttu-id="75d60-167">La `DescriptorTable` cláusula es en sí misma una lista de cláusulas de tabla de descriptores separadas por comas, así como un parámetro de visibilidad opcional.</span><span class="sxs-lookup"><span data-stu-id="75d60-167">The `DescriptorTable` clause is itself a list of comma-separated descriptor table clauses, as well as an optional visibility parameter.</span></span> <span data-ttu-id="75d60-168">Las cláusulas *DescriptorTable* incluyen CBV, SRV, UAV y muestreador.</span><span class="sxs-lookup"><span data-stu-id="75d60-168">The *DescriptorTable* clauses include CBV, SRV, UAV, and Sampler.</span></span> <span data-ttu-id="75d60-169">Tenga en cuenta que sus parámetros difieren de los de las cláusulas de nivel de raíz.</span><span class="sxs-lookup"><span data-stu-id="75d60-169">Note that their parameters differ from those of the root-level clauses.</span></span>

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

<span data-ttu-id="75d60-170">La tabla de descriptores `CBV` tiene la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="75d60-170">The Descriptor Table `CBV` has the following syntax:</span></span>

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="75d60-171">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="75d60-171">For example:</span></span>

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

<span data-ttu-id="75d60-172">El parámetro obligatorio *bReg* especifica el REG de inicio del intervalo de CBuffer.</span><span class="sxs-lookup"><span data-stu-id="75d60-172">The mandatory parameter *bReg* specifies the start Reg of the cbuffer range.</span></span> <span data-ttu-id="75d60-173">El parámetro *numDescriptors* especifica el número de descriptores en el intervalo de CBuffer contiguo; el valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="75d60-173">The *numDescriptors* parameter specifies the number of descriptors in the contiguous cbuffer range; the default value being 1.</span></span> <span data-ttu-id="75d60-174">La entrada declara un intervalo CBuffer ` [Reg, Reg + numDescriptors - 1]` , cuando *numDescriptors* es un número.</span><span class="sxs-lookup"><span data-stu-id="75d60-174">The entry declares a cbuffer range` [Reg, Reg + numDescriptors - 1]`, when *numDescriptors* is a number.</span></span> <span data-ttu-id="75d60-175">Si *numDescriptors* es igual a "unbounded", el intervalo es `[Reg, UINT_MAX]` , lo que significa que la aplicación debe asegurarse de que no hace referencia a un área fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="75d60-175">If *numDescriptors* is equal to "unbounded", the range is `[Reg, UINT_MAX]`, which means the app must ensure it is not referencing an out-of-bounds area.</span></span> <span data-ttu-id="75d60-176">El campo *offset* representa el parámetro *OffsetInDescriptorsFromTableStart* en las API de C++, es decir, el desplazamiento (en descriptores) desde el inicio de la tabla.</span><span class="sxs-lookup"><span data-stu-id="75d60-176">The *offset* field represents the *OffsetInDescriptorsFromTableStart* parameter in the C++ APIs, that is, the offset (in descriptors) from the start of the table.</span></span> <span data-ttu-id="75d60-177">Si el desplazamiento se establece en descriptor de \_ desplazamiento de intervalo \_ \_ Append (el valor predeterminado), significa que el intervalo está justo después del intervalo anterior.</span><span class="sxs-lookup"><span data-stu-id="75d60-177">If the offset is set to DESCRIPTOR\_RANGE\_OFFSET\_APPEND (the default), it means the range is directly after the previous range.</span></span> <span data-ttu-id="75d60-178">Sin embargo, la especificación de desplazamientos específicos permite que los intervalos se superpongan entre sí, lo que permite el alias del registro.</span><span class="sxs-lookup"><span data-stu-id="75d60-178">However, entering specific offsets does allow for ranges to overlap each other, allowing register aliasing.</span></span>

<span data-ttu-id="75d60-179">La tabla de descriptores `SRV` tiene la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="75d60-179">The Descriptor Table `SRV` has the following syntax:</span></span>

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="75d60-180">Esto es similar a la entrada de la tabla de descriptores `CBV` , salvo que el intervalo especificado es para las vistas de recursos del sombreador.</span><span class="sxs-lookup"><span data-stu-id="75d60-180">This is similar to the descriptor table `CBV` entry, except the specified range is for shader resource views.</span></span>

<span data-ttu-id="75d60-181">La tabla de descriptores `UAV` tiene la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="75d60-181">The Descriptor Table `UAV` has the following syntax:</span></span>

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="75d60-182">Esto es similar a la entrada de la tabla de descriptores `CBV` , salvo que el intervalo especificado es para las vistas de acceso desordenado.</span><span class="sxs-lookup"><span data-stu-id="75d60-182">This is similar to the descriptor table `CBV` entry, except the specified range is for unordered access views.</span></span>

<span data-ttu-id="75d60-183">La tabla de descriptores `Sampler` tiene la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="75d60-183">The Descriptor Table `Sampler` has the following syntax:</span></span>

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

<span data-ttu-id="75d60-184">Esto es similar a la entrada de la tabla de descriptores `CBV` , salvo que el intervalo especificado es para los muestreadores de sombreador.</span><span class="sxs-lookup"><span data-stu-id="75d60-184">This is similar to the descriptor table `CBV` entry, except the specified range is for shader samplers.</span></span> <span data-ttu-id="75d60-185">Tenga en cuenta que los muestreadores no se pueden combinar con otros tipos de descriptores en la misma tabla de descriptores (ya que se encuentran en un montón descriptor independiente).</span><span class="sxs-lookup"><span data-stu-id="75d60-185">Note that Samplers can’t be mixed with other types of descriptors in the same descriptor table (since they are in a separate descriptor heap).</span></span>

## <a name="static-sampler"></a><span data-ttu-id="75d60-186">Muestra estática</span><span class="sxs-lookup"><span data-stu-id="75d60-186">Static Sampler</span></span>

<span data-ttu-id="75d60-187">La muestra estática representa la estructura DESC de la [**\_ \_ muestra \_ estática D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .</span><span class="sxs-lookup"><span data-stu-id="75d60-187">The static sampler represents the [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span> <span data-ttu-id="75d60-188">El parámetro obligatorio para *StaticSampler* es un valor escalar de muestra s-Register reg. Otros parámetros son opcionales con los valores predeterminados que se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="75d60-188">The mandatory parameter for *StaticSampler* is a scalar, sampler s-register Reg. Other parameters are optional with default values shown below.</span></span> <span data-ttu-id="75d60-189">La mayoría de los campos aceptan un conjunto de enumeraciones predefinidas.</span><span class="sxs-lookup"><span data-stu-id="75d60-189">Most fields accept a set of predefined enums.</span></span>

``` syntax
StaticSampler( sReg,
              [ filter = FILTER_ANISOTROPIC, 
                addressU = TEXTURE_ADDRESS_WRAP,
                addressV = TEXTURE_ADDRESS_WRAP,
                addressW = TEXTURE_ADDRESS_WRAP,
                mipLODBias = 0.f,
                maxAnisotropy = 16,
                comparisonFunc = COMPARISON_LESS_EQUAL,
                borderColor = STATIC_BORDER_COLOR_OPAQUE_WHITE,
                minLOD = 0.f,         
                maxLOD = 3.402823466e+38f,
                space = 0, 
                visibility = SHADER_VISIBILITY_ALL ])
```

<span data-ttu-id="75d60-190">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="75d60-190">For example:</span></span>

``` syntax
StaticSampler(s4, filter=FILTER_MIN_MAG_MIP_LINEAR)
```

<span data-ttu-id="75d60-191">Las opciones de parámetro son muy similares a las llamadas de la API de C++, a excepción de *BorderColor*, que está restringida a una enumeración en HLSL.</span><span class="sxs-lookup"><span data-stu-id="75d60-191">The parameter options are very similar to the C++ API calls, except for *borderColor*, which is restricted to an enum in HLSL.</span></span>

<span data-ttu-id="75d60-192">El campo de filtro puede ser uno de [**D3D12 \_ Filter**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).</span><span class="sxs-lookup"><span data-stu-id="75d60-192">The filter field can be one of [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).</span></span>

<span data-ttu-id="75d60-193">Los campos de dirección pueden ser uno de [**los \_ \_ \_ modos de dirección de textura D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).</span><span class="sxs-lookup"><span data-stu-id="75d60-193">The address fields can each be one of [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).</span></span>

<span data-ttu-id="75d60-194">La función de comparación puede ser una de [**D3D12 \_ Comparison \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).</span><span class="sxs-lookup"><span data-stu-id="75d60-194">The comparison function can be one of [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).</span></span>

<span data-ttu-id="75d60-195">El campo de color del borde puede ser [**un \_ \_ \_ color de borde estático de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).</span><span class="sxs-lookup"><span data-stu-id="75d60-195">The border color field can be one of [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).</span></span>

<span data-ttu-id="75d60-196">La visibilidad puede ser una de las D3D12 de la [**\_ \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span><span class="sxs-lookup"><span data-stu-id="75d60-196">Visibility can be one of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

## <a name="compiling-an-hlsl-root-signature"></a><span data-ttu-id="75d60-197">Compilar una firma raíz HLSL</span><span class="sxs-lookup"><span data-stu-id="75d60-197">Compiling an HLSL root signature</span></span>

<span data-ttu-id="75d60-198">Hay dos mecanismos para compilar una firma raíz de HLSL.</span><span class="sxs-lookup"><span data-stu-id="75d60-198">There are two mechanisms to compile an HLSL root signature.</span></span> <span data-ttu-id="75d60-199">En primer lugar, es posible adjuntar una cadena de firma raíz a un sombreador determinado a través del atributo *RootSignature* (en el ejemplo siguiente, mediante el punto de entrada **MyRS1** ):</span><span class="sxs-lookup"><span data-stu-id="75d60-199">First, it is possible to attach a root signature string to a particular shader via the *RootSignature* attribute (in the following example, using the **MyRS1** entry point):</span></span>

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

<span data-ttu-id="75d60-200">El compilador creará y comprobará el BLOB de firma raíz para el sombreador y lo incrustará junto con el código de byte del sombreador en el BLOB de sombreador.</span><span class="sxs-lookup"><span data-stu-id="75d60-200">The compiler will create and verify the root signature blob for the shader and embed it alongside the shader byte code into the shader blob.</span></span> <span data-ttu-id="75d60-201">El compilador admite la sintaxis de firma raíz para el modelo de sombreador 5,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="75d60-201">The compiler supports root signature syntax for shader model 5.0 and higher.</span></span> <span data-ttu-id="75d60-202">Si una firma raíz está incrustada en un sombreador modelo de sombreador 5,0 y ese sombreador se envía al tiempo de ejecución de D3D11, en lugar de D3D12, la parte de la firma raíz se omitirá de forma silenciosa por D3D11.</span><span class="sxs-lookup"><span data-stu-id="75d60-202">If a root signature is embedded in a shader model 5.0 shader and that shader is sent to the D3D11 runtime, as opposed to D3D12, the root signature portion will get silently ignored by D3D11.</span></span>

<span data-ttu-id="75d60-203">El otro mecanismo consiste en crear un BLOB de firma raíz independiente, quizás para reutilizarlo con un gran conjunto de sombreadores, lo que ahorra espacio.</span><span class="sxs-lookup"><span data-stu-id="75d60-203">The other mechanism is to create a standalone root signature blob, perhaps to reuse it with a large set of shaders, saving space.</span></span> <span data-ttu-id="75d60-204">La [herramienta de compilador de efectos](/windows/desktop/direct3dtools/fxc) (FXC) admite los modelos de sombreador **rootsig \_ 1 \_ 0** y **rootsig \_ 1 \_ 1** .</span><span class="sxs-lookup"><span data-stu-id="75d60-204">The [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC) supports both **rootsig\_1\_0** and **rootsig\_1\_1** shader models.</span></span> <span data-ttu-id="75d60-205">El nombre de la cadena de definición se especifica mediante el argumento/E habitual.</span><span class="sxs-lookup"><span data-stu-id="75d60-205">The name of the define string is specified via the usual /E argument.</span></span> <span data-ttu-id="75d60-206">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="75d60-206">For example:</span></span>

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

<span data-ttu-id="75d60-207">Tenga en cuenta que la definición de la cadena de firma raíz también se puede pasar en la línea de comandos, por ejemplo,/D MyRS1 = "...".</span><span class="sxs-lookup"><span data-stu-id="75d60-207">Note that the root signature string define can also be passed on the command line, e.g, /D MyRS1=”…”.</span></span>

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a><span data-ttu-id="75d60-208">Manipular firmas raíz con el compilador FXC</span><span class="sxs-lookup"><span data-stu-id="75d60-208">Manipulating root signatures with the FXC compiler</span></span>

<span data-ttu-id="75d60-209">El compilador FXC crea el código de bytes del sombreador desde los archivos de código fuente HLSL.</span><span class="sxs-lookup"><span data-stu-id="75d60-209">The FXC compiler creates shader byte-code from HLSL source files.</span></span> <span data-ttu-id="75d60-210">Hay muchos parámetros opcionales para este compilador, consulte la herramienta de [compilador de efectos](/windows/desktop/direct3dtools/fxc).</span><span class="sxs-lookup"><span data-stu-id="75d60-210">There are a lot of optional parameters for this compiler, refer to the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc).</span></span>

<span data-ttu-id="75d60-211">Para administrar las firmas de raíz creadas por HLSL, en la tabla siguiente se proporcionan algunos ejemplos del uso de FXC.</span><span class="sxs-lookup"><span data-stu-id="75d60-211">For managing HLSL authored root signatures, the following table gives some examples of using FXC.</span></span>



| <span data-ttu-id="75d60-212">Línea</span><span class="sxs-lookup"><span data-stu-id="75d60-212">Line</span></span> | <span data-ttu-id="75d60-213">Línea de comandos</span><span class="sxs-lookup"><span data-stu-id="75d60-213">Command line</span></span>                                                                 | <span data-ttu-id="75d60-214">Descripción</span><span class="sxs-lookup"><span data-stu-id="75d60-214">Description</span></span>                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d60-215">1</span><span class="sxs-lookup"><span data-stu-id="75d60-215">1</span></span>    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | <span data-ttu-id="75d60-216">Compila un sombreador para el destino del sombreador de píxeles 5,1, el origen del sombreador se encuentra en el archivo shaderWithRootSig. HLSL, que incluye una firma raíz.</span><span class="sxs-lookup"><span data-stu-id="75d60-216">Compiles a shader for the pixel shader 5.1 target, the shader source is in the shaderWithRootSig.hlsl file, which includes a root signature.</span></span> <span data-ttu-id="75d60-217">El sombreador y la firma raíz se compilan como Blobs independientes en el archivo binario RS1. FXO.</span><span class="sxs-lookup"><span data-stu-id="75d60-217">The shader and root signature are compiled as separate blobs in the rs1.fxo binary file.</span></span>    |
| <span data-ttu-id="75d60-218">2</span><span class="sxs-lookup"><span data-stu-id="75d60-218">2</span></span>    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | <span data-ttu-id="75d60-219">Extrae la firma raíz del archivo creado por la línea 1, por lo que el archivo RS1. RS. FXO contiene solo una firma raíz.</span><span class="sxs-lookup"><span data-stu-id="75d60-219">Extracts the root signature from the file created by line 1, so the rs1.rs.fxo file contains just a root signature.</span></span>                                                                                                                      |
| <span data-ttu-id="75d60-220">3</span><span class="sxs-lookup"><span data-stu-id="75d60-220">3</span></span>    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | <span data-ttu-id="75d60-221">Quita la firma raíz del archivo creado por la línea 1, por lo que el archivo RS1. unsumed. FXO contiene un sombreador sin firma raíz.</span><span class="sxs-lookup"><span data-stu-id="75d60-221">Removes the root signature from the file created by line 1, so the rs1.stripped.fxo file contains a shader with no root signature.</span></span>                                                                                                       |
| <span data-ttu-id="75d60-222">4</span><span class="sxs-lookup"><span data-stu-id="75d60-222">4</span></span>    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | <span data-ttu-id="75d60-223">Combina un sombreador y una firma raíz que se encuentran en archivos independientes en un archivo binario que contiene ambos BLOBs.</span><span class="sxs-lookup"><span data-stu-id="75d60-223">Combines a shader and root signature that are in separate files into a binary file containing both blobs.</span></span> <span data-ttu-id="75d60-224">En este ejemplo, RS1. New. FX0 sería idéntico a RS1. FX0 en la línea 1.</span><span class="sxs-lookup"><span data-stu-id="75d60-224">In this example rs1.new.fx0 would be identical to rs1.fx0 in line 1.</span></span>                                                           |
| <span data-ttu-id="75d60-225">5</span><span class="sxs-lookup"><span data-stu-id="75d60-225">5</span></span>    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | <span data-ttu-id="75d60-226">Crea un archivo binario de firma raíz independiente a partir de un origen que puede contener más de una firma raíz.</span><span class="sxs-lookup"><span data-stu-id="75d60-226">Creates a stand-alone root signature binary file from a source that may contain more than just a root signature.</span></span> <span data-ttu-id="75d60-227">Observe el \_ \_ destino de rootsig 1 0 y que RS1 es el nombre de la cadena de macro de la firma raíz ( \# define) en el archivo HLSL.</span><span class="sxs-lookup"><span data-stu-id="75d60-227">Note the rootsig\_1\_0 target, and that RS1 is the name of the root signature (\#define) macro string in the HLSL file.</span></span> |



 

<span data-ttu-id="75d60-228">La funcionalidad disponible a través de FXC también está disponible mediante programación con la función [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="75d60-228">The functionality available through FXC is also available programmatically using the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) function.</span></span> <span data-ttu-id="75d60-229">Esta llamada compila un sombreador con una firma raíz o una firma raíz independiente (estableciendo el \_ destino rootsig 1 \_ 0).</span><span class="sxs-lookup"><span data-stu-id="75d60-229">This call compiles a shader with a root signature, or stand-alone root signature (setting the rootsig\_1\_0 target).</span></span> <span data-ttu-id="75d60-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) y [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) pueden extraer y adjuntar firmas raíz a un BLOB existente.</span><span class="sxs-lookup"><span data-stu-id="75d60-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) and [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) can extract and attach root signatures to an existing blob.</span></span><span data-ttu-id="75d60-231">\_La firma de raíz de blobs D3D \_ \_ se usa para especificar el tipo de parte del BLOB de firma raíz.</span><span class="sxs-lookup"><span data-stu-id="75d60-231">  D3D\_BLOB\_ROOT\_SIGNATURE is used to specify the root signature blob part type.</span></span> <span data-ttu-id="75d60-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) quita la firma raíz (mediante la marca de la \_ \_ firma raíz D3DCOMPILER \_ ) del BLOB.</span><span class="sxs-lookup"><span data-stu-id="75d60-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) removes the root signature (using the D3DCOMPILER\_STRIP\_ROOT\_SIGNATURE flag) from the blob.</span></span>

## <a name="notes"></a><span data-ttu-id="75d60-233">Notas</span><span class="sxs-lookup"><span data-stu-id="75d60-233">Notes</span></span>

> [!Note]  
> <span data-ttu-id="75d60-234">Mientras que la compilación sin conexión de los sombreadores es muy recomendable, si los sombreadores deben compilarse en tiempo de ejecución, consulte la sección Comentarios de [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).</span><span class="sxs-lookup"><span data-stu-id="75d60-234">Whereas the offline compilation of shaders is strongly recommended, if shaders have to be compiled at runtime, refer to the remarks for [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).</span></span>

 

> [!Note]  
> <span data-ttu-id="75d60-235">No es necesario cambiar los recursos de HLSL existentes para controlar las firmas raíz que se usarán con ellos.</span><span class="sxs-lookup"><span data-stu-id="75d60-235">Existing HLSL assets do not need to be changed to handle root signatures to be used with them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="75d60-236">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75d60-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75d60-237">Indexado dinámico mediante HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="75d60-237">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[<span data-ttu-id="75d60-238">Características del modelo de sombreador de HLSL 5,1 para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="75d60-238">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="75d60-239">Enlace de recursos</span><span class="sxs-lookup"><span data-stu-id="75d60-239">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="75d60-240">Enlace de recursos en HLSL</span><span class="sxs-lookup"><span data-stu-id="75d60-240">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="75d60-241">Firmas raíz</span><span class="sxs-lookup"><span data-stu-id="75d60-241">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="75d60-242">Modelo de sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="75d60-242">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="75d60-243">Valor de referencia de estarcido del sombreador especificado</span><span class="sxs-lookup"><span data-stu-id="75d60-243">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
</dt> <dt>

[<span data-ttu-id="75d60-244">Cargas de vista de acceso no ordenada con tipo</span><span class="sxs-lookup"><span data-stu-id="75d60-244">Typed Unordered Access View Loads</span></span>](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 
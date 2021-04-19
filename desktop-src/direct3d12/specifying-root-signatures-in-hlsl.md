---
title: Especificación de firmas de raíz en HLSL
description: Especificar firmas raíz en el modelo de sombreador HLSL 5.1 es una alternativa a especificarlas en código de C++.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dad0da9f84d68fc1acbf53332d1cae4075f0faa
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492287"
---
# <a name="specifying-root-signatures-in-hlsl"></a><span data-ttu-id="ec52f-103">Especificación de firmas de raíz en HLSL</span><span class="sxs-lookup"><span data-stu-id="ec52f-103">Specifying Root Signatures in HLSL</span></span>

<span data-ttu-id="ec52f-104">Especificar firmas raíz en el modelo de sombreador HLSL 5.1 es una alternativa a especificarlas en código de C++.</span><span class="sxs-lookup"><span data-stu-id="ec52f-104">Specifying root signatures in HLSL Shader Model 5.1 is an alternative to specifying them in C++ code.</span></span>

-   [<span data-ttu-id="ec52f-105">Una firma raíz HLSL de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec52f-105">An example HLSL Root Signature</span></span>](#an-example-hlsl-root-signature)
    -   [<span data-ttu-id="ec52f-106">Firma raíz versión 1.0</span><span class="sxs-lookup"><span data-stu-id="ec52f-106">Root Signature Version 1.0</span></span>](#root-signature-version-10)
    -   [<span data-ttu-id="ec52f-107">Versión 1.1 de la firma raíz</span><span class="sxs-lookup"><span data-stu-id="ec52f-107">Root Signature Version 1.1</span></span>](#root-signature-version-11)
-   [<span data-ttu-id="ec52f-108">RootFlags</span><span class="sxs-lookup"><span data-stu-id="ec52f-108">RootFlags</span></span>](#rootflags)
-   [<span data-ttu-id="ec52f-109">Constantes raíz</span><span class="sxs-lookup"><span data-stu-id="ec52f-109">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="ec52f-110">Visibilidad</span><span class="sxs-lookup"><span data-stu-id="ec52f-110">Visibility</span></span>](#visibility)
-   [<span data-ttu-id="ec52f-111">CBV de nivel raíz</span><span class="sxs-lookup"><span data-stu-id="ec52f-111">Root-level CBV</span></span>](#root-level-cbv)
-   [<span data-ttu-id="ec52f-112">SRV de nivel raíz</span><span class="sxs-lookup"><span data-stu-id="ec52f-112">Root-level SRV</span></span>](#root-level-srv)
-   [<span data-ttu-id="ec52f-113">UAV de nivel de raíz</span><span class="sxs-lookup"><span data-stu-id="ec52f-113">Root-level UAV</span></span>](#root-level-uav)
-   [<span data-ttu-id="ec52f-114">Tabla descriptor</span><span class="sxs-lookup"><span data-stu-id="ec52f-114">Descriptor Table</span></span>](#descriptor-table)
-   [<span data-ttu-id="ec52f-115">Sampler estático</span><span class="sxs-lookup"><span data-stu-id="ec52f-115">Static Sampler</span></span>](#static-sampler)
-   [<span data-ttu-id="ec52f-116">Compilación de una firma raíz HLSL</span><span class="sxs-lookup"><span data-stu-id="ec52f-116">Compiling an HLSL root signature</span></span>](#compiling-an-hlsl-root-signature)
-   [<span data-ttu-id="ec52f-117">Manipulación de firmas raíz con el compilador fxc</span><span class="sxs-lookup"><span data-stu-id="ec52f-117">Manipulating root signatures with the FXC compiler</span></span>](#manipulating-root-signatures-with-the-fxc-compiler)
-   [<span data-ttu-id="ec52f-118">Notas</span><span class="sxs-lookup"><span data-stu-id="ec52f-118">Notes</span></span>](#notes)
-   [<span data-ttu-id="ec52f-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ec52f-119">Related topics</span></span>](#related-topics)

## <a name="an-example-hlsl-root-signature"></a><span data-ttu-id="ec52f-120">Una firma raíz HLSL de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec52f-120">An example HLSL Root Signature</span></span>

<span data-ttu-id="ec52f-121">Una firma raíz se puede especificar en HLSL como una cadena.</span><span class="sxs-lookup"><span data-stu-id="ec52f-121">A root signature can be specified in HLSL as a string.</span></span> <span data-ttu-id="ec52f-122">La cadena contiene una colección de cláusulas separadas por comas que describen los componentes constituyentes de la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="ec52f-122">The string contains a collection of comma-separated clauses that describe root signature constituent components.</span></span> <span data-ttu-id="ec52f-123">La firma raíz debe ser idéntica entre sombreadores para cualquier objeto de estado de canalización (PSO).</span><span class="sxs-lookup"><span data-stu-id="ec52f-123">The root signature should be identical across shaders for any one pipeline state object (PSO).</span></span> <span data-ttu-id="ec52f-124">Este es un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ec52f-124">Here is an example:</span></span>

### <a name="root-signature-version-10"></a><span data-ttu-id="ec52f-125">Firma raíz versión 1.0</span><span class="sxs-lookup"><span data-stu-id="ec52f-125">Root Signature Version 1.0</span></span>

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

<span data-ttu-id="ec52f-126">Esta definición proporcionaría la siguiente firma raíz, y se debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ec52f-126">This definition would give the following root signature, noting:</span></span>

-   <span data-ttu-id="ec52f-127">El uso de parámetros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="ec52f-127">The use of default parameters.</span></span>
-   <span data-ttu-id="ec52f-128">b0 y (b0, space=1) no entren en conflicto</span><span class="sxs-lookup"><span data-stu-id="ec52f-128">b0 and (b0, space=1) do not conflict</span></span>
-   <span data-ttu-id="ec52f-129">u0 solo es visible para el sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="ec52f-129">u0 is only visible to the geometry shader</span></span>
-   <span data-ttu-id="ec52f-130">u4 y u5 tienen alias para el mismo descriptor en un montón</span><span class="sxs-lookup"><span data-stu-id="ec52f-130">u4 and u5 are aliased to the same descriptor in a heap</span></span>

![una firma raíz especificada mediante el lenguaje de sombreador de alto nivel](images/hlsl-root-signature.png)

### <a name="root-signature-version-11"></a><span data-ttu-id="ec52f-132">Versión 1.1 de la firma raíz</span><span class="sxs-lookup"><span data-stu-id="ec52f-132">Root Signature Version 1.1</span></span>

<span data-ttu-id="ec52f-133">[Root Signature Version 1.1 habilita](root-signature-version-1-1.md) las optimizaciones de controladores en los descriptores de firma raíz y los datos.</span><span class="sxs-lookup"><span data-stu-id="ec52f-133">[Root Signature Version 1.1](root-signature-version-1-1.md) enables driver optimizations on root signature descriptors and data.</span></span>

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

<span data-ttu-id="ec52f-134">El lenguaje de firma raíz HLSL se corresponde estrechamente con las API de firma raíz de C++ y tiene una capacidad expresiva equivalente.</span><span class="sxs-lookup"><span data-stu-id="ec52f-134">The HLSL root signature language closely corresponds to the C++ root signature APIs and has equivalent expressive power.</span></span> <span data-ttu-id="ec52f-135">La firma raíz se especifica como una secuencia de cláusulas, separadas por comas.</span><span class="sxs-lookup"><span data-stu-id="ec52f-135">The root signature is specified as a sequence of clauses, separated by comma.</span></span> <span data-ttu-id="ec52f-136">El orden de las cláusulas es importante, ya que el orden de análisis determina la posición de la ranura en la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="ec52f-136">The order of clauses is important, as the order of parsing determines the slot position in the root signature.</span></span> <span data-ttu-id="ec52f-137">Cada cláusula toma uno o varios parámetros con nombre.</span><span class="sxs-lookup"><span data-stu-id="ec52f-137">Each clause takes one or more named parameters.</span></span> <span data-ttu-id="ec52f-138">Sin embargo, el orden de los parámetros no es importante.</span><span class="sxs-lookup"><span data-stu-id="ec52f-138">The order of parameters is not important, however.</span></span>

## <a name="rootflags"></a><span data-ttu-id="ec52f-139">RootFlags</span><span class="sxs-lookup"><span data-stu-id="ec52f-139">RootFlags</span></span>

<span data-ttu-id="ec52f-140">La *cláusula RootFlags* opcional toma 0 (el valor predeterminado para indicar que no hay marcas) o uno o varios valores de marcas raíz predefinidos, conectados a través del operador OR ' \| '.</span><span class="sxs-lookup"><span data-stu-id="ec52f-140">The optional *RootFlags* clause takes either 0 (the default value to indicate no flags), or one or several of predefined root flags values, connected via the OR ‘\|’ operator.</span></span> <span data-ttu-id="ec52f-141">Los valores de marca raíz permitidos se definen mediante [**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span><span class="sxs-lookup"><span data-stu-id="ec52f-141">The allowed root flag values are defined by [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

<span data-ttu-id="ec52f-142">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ec52f-142">For example:</span></span>

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a><span data-ttu-id="ec52f-143">Constantes raíz</span><span class="sxs-lookup"><span data-stu-id="ec52f-143">Root Constants</span></span>

<span data-ttu-id="ec52f-144">La *cláusula RootConstants* especifica las constantes raíz en la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="ec52f-144">The *RootConstants* clause specifies root constants in the root signature.</span></span> <span data-ttu-id="ec52f-145">Dos parámetros obligatorios son: *num32BitConstants* y *bReg* (el registro correspondiente a *BaseShaderRegister* en las API de *C++)* del cbuffer .</span><span class="sxs-lookup"><span data-stu-id="ec52f-145">Two mandatory parameters are: *num32BitConstants* and *bReg* (the register corresponding to *BaseShaderRegister* in C++ APIs) of the *cbuffer*.</span></span> <span data-ttu-id="ec52f-146">Los parámetros space *(RegisterSpace* en las API de C++) y *visibility (ShaderVisibility* en C++) son opcionales y los valores predeterminados son:</span><span class="sxs-lookup"><span data-stu-id="ec52f-146">The space (*RegisterSpace* in C++ APIs) and visibility (*ShaderVisibility* in C++) parameters are optional, and the default values are:</span></span>

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

<span data-ttu-id="ec52f-147">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ec52f-147">For example:</span></span>

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a><span data-ttu-id="ec52f-148">Visibilidad</span><span class="sxs-lookup"><span data-stu-id="ec52f-148">Visibility</span></span>

<span data-ttu-id="ec52f-149">Visibility es un parámetro opcional que puede tener uno de los valores de [**D3D12 \_ SHADER \_ VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span><span class="sxs-lookup"><span data-stu-id="ec52f-149">Visibility is an optional parameter that can have one of the values from [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

<span data-ttu-id="ec52f-150">SHADER \_ VISIBILITY \_ ALL difunde los argumentos raíz a todos los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="ec52f-150">SHADER\_VISIBILITY\_ALL broadcasts the root arguments to all shaders.</span></span> <span data-ttu-id="ec52f-151">En algún hardware esto no tiene ningún costo, pero en otro hardware hay un costo por bifurcar los datos a todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ec52f-151">On some hardware this has no cost, but on other hardware there is a cost to fork the data to all the shader stages.</span></span> <span data-ttu-id="ec52f-152">Al establecer una de las opciones, como SHADER VISIBILITY VERTEX, se limita \_ el argumento raíz a una sola fase del \_ sombreador.</span><span class="sxs-lookup"><span data-stu-id="ec52f-152">Setting one of the options, such as SHADER\_VISIBILITY\_VERTEX, limits the root argument to a single shader stage.</span></span>

<span data-ttu-id="ec52f-153">Establecer argumentos raíz en fases de sombreador único permite usar el mismo nombre de enlace en distintas fases.</span><span class="sxs-lookup"><span data-stu-id="ec52f-153">Setting root arguments to single shader stages allows the same bind name to be used at different stages.</span></span> <span data-ttu-id="ec52f-154">Por ejemplo, un enlace SRV de `t0,SHADER_VISIBILITY_VERTEX` y un enlace SRV de sería `t0,SHADER_VISIBILITY_PIXEL` válido.</span><span class="sxs-lookup"><span data-stu-id="ec52f-154">For example, an SRV binding of `t0,SHADER_VISIBILITY_VERTEX` and SRV binding of `t0,SHADER_VISIBILITY_PIXEL` would be valid.</span></span> <span data-ttu-id="ec52f-155">Pero si la configuración de `t0,SHADER_VISIBILITY_ALL` visibilidad fuera para uno de los enlaces, la firma raíz no sería válida.</span><span class="sxs-lookup"><span data-stu-id="ec52f-155">But if the visibility setting was `t0,SHADER_VISIBILITY_ALL` for one of the bindings, the root signature would be invalid.</span></span>

## <a name="root-level-cbv"></a><span data-ttu-id="ec52f-156">CBV de nivel raíz</span><span class="sxs-lookup"><span data-stu-id="ec52f-156">Root-level CBV</span></span>

<span data-ttu-id="ec52f-157">La cláusula (vista de búfer constante) especifica una entrada reg de búfer constante de nivel `CBV` raíz b-register.</span><span class="sxs-lookup"><span data-stu-id="ec52f-157">The `CBV` (constant buffer view) clause specifies a root-level constant buffer b-register Reg entry.</span></span> <span data-ttu-id="ec52f-158">Tenga en cuenta que se trata de una entrada escalar; no es posible especificar un intervalo para el nivel raíz.</span><span class="sxs-lookup"><span data-stu-id="ec52f-158">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a><span data-ttu-id="ec52f-159">SRV de nivel raíz</span><span class="sxs-lookup"><span data-stu-id="ec52f-159">Root-level SRV</span></span>

<span data-ttu-id="ec52f-160">La `SRV` cláusula (vista de recursos del sombreador) especifica una entrada SRV t-register Reg de nivel raíz.</span><span class="sxs-lookup"><span data-stu-id="ec52f-160">The `SRV` (shader resource view) clause specifies a root-level SRV t-register Reg entry.</span></span> <span data-ttu-id="ec52f-161">Tenga en cuenta que se trata de una entrada escalar; no es posible especificar un intervalo para el nivel raíz.</span><span class="sxs-lookup"><span data-stu-id="ec52f-161">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a><span data-ttu-id="ec52f-162">UAV de nivel de raíz</span><span class="sxs-lookup"><span data-stu-id="ec52f-162">Root-level UAV</span></span>

<span data-ttu-id="ec52f-163">La `UAV` cláusula (vista de acceso desordenado) especifica una entrada UAV u-register Reg de nivel raíz.</span><span class="sxs-lookup"><span data-stu-id="ec52f-163">The `UAV` (unordered access view) clause specifies a root-level UAV u-register Reg entry.</span></span> <span data-ttu-id="ec52f-164">Tenga en cuenta que se trata de una entrada escalar; no es posible especificar un intervalo para el nivel raíz.</span><span class="sxs-lookup"><span data-stu-id="ec52f-164">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="ec52f-165">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ec52f-165">For example:</span></span>

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a><span data-ttu-id="ec52f-166">Tabla descriptora</span><span class="sxs-lookup"><span data-stu-id="ec52f-166">Descriptor Table</span></span>

<span data-ttu-id="ec52f-167">La `DescriptorTable` cláusula es en sí misma una lista de cláusulas de tabla de descriptores separadas por comas, así como un parámetro de visibilidad opcional.</span><span class="sxs-lookup"><span data-stu-id="ec52f-167">The `DescriptorTable` clause is itself a list of comma-separated descriptor table clauses, as well as an optional visibility parameter.</span></span> <span data-ttu-id="ec52f-168">Las *cláusulas DescriptorTable* incluyen CBV, SRV, UAV y Sampler.</span><span class="sxs-lookup"><span data-stu-id="ec52f-168">The *DescriptorTable* clauses include CBV, SRV, UAV, and Sampler.</span></span> <span data-ttu-id="ec52f-169">Tenga en cuenta que sus parámetros difieren de los de las cláusulas de nivel raíz.</span><span class="sxs-lookup"><span data-stu-id="ec52f-169">Note that their parameters differ from those of the root-level clauses.</span></span>

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

<span data-ttu-id="ec52f-170">La tabla descriptor `CBV` tiene la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="ec52f-170">The Descriptor Table `CBV` has the following syntax:</span></span>

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="ec52f-171">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ec52f-171">For example:</span></span>

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

<span data-ttu-id="ec52f-172">El parámetro obligatorio *bReg* especifica el reg inicial del intervalo de cbuffer.</span><span class="sxs-lookup"><span data-stu-id="ec52f-172">The mandatory parameter *bReg* specifies the start Reg of the cbuffer range.</span></span> <span data-ttu-id="ec52f-173">El *parámetro numDescriptors* especifica el número de descriptores en el intervalo de cbuffer contiguo; el valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="ec52f-173">The *numDescriptors* parameter specifies the number of descriptors in the contiguous cbuffer range; the default value being 1.</span></span> <span data-ttu-id="ec52f-174">La entrada declara un intervalo de cbuffer ` [Reg, Reg + numDescriptors - 1]` , cuando *numDescriptors* es un número.</span><span class="sxs-lookup"><span data-stu-id="ec52f-174">The entry declares a cbuffer range` [Reg, Reg + numDescriptors - 1]`, when *numDescriptors* is a number.</span></span> <span data-ttu-id="ec52f-175">Si *numDescriptors* es igual a "sin enlazar", el intervalo es , lo que significa que la aplicación debe asegurarse de que no hace referencia a un área fuera de `[Reg, UINT_MAX]` límites.</span><span class="sxs-lookup"><span data-stu-id="ec52f-175">If *numDescriptors* is equal to "unbounded", the range is `[Reg, UINT_MAX]`, which means the app must ensure it is not referencing an out-of-bounds area.</span></span> <span data-ttu-id="ec52f-176">El *campo* offset representa el parámetro *OffsetInDescriptorsFromTableStart* en las API de C++, es decir, el desplazamiento (en descriptores) desde el principio de la tabla.</span><span class="sxs-lookup"><span data-stu-id="ec52f-176">The *offset* field represents the *OffsetInDescriptorsFromTableStart* parameter in the C++ APIs, that is, the offset (in descriptors) from the start of the table.</span></span> <span data-ttu-id="ec52f-177">Si el desplazamiento se establece en DESCRIPTOR RANGE OFFSET APPEND (valor predeterminado), significa que \_ el intervalo está directamente después del intervalo \_ \_ anterior.</span><span class="sxs-lookup"><span data-stu-id="ec52f-177">If the offset is set to DESCRIPTOR\_RANGE\_OFFSET\_APPEND (the default), it means the range is directly after the previous range.</span></span> <span data-ttu-id="ec52f-178">Sin embargo, la especificación de desplazamientos específicos permite que los intervalos se superpongan entre sí, lo que permite el alias de registro.</span><span class="sxs-lookup"><span data-stu-id="ec52f-178">However, entering specific offsets does allow for ranges to overlap each other, allowing register aliasing.</span></span>

<span data-ttu-id="ec52f-179">La tabla descriptor `SRV` tiene la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="ec52f-179">The Descriptor Table `SRV` has the following syntax:</span></span>

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="ec52f-180">Esto es similar a la entrada de la tabla descriptor, salvo que el intervalo especificado es para las vistas de recursos `CBV` del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ec52f-180">This is similar to the descriptor table `CBV` entry, except the specified range is for shader resource views.</span></span>

<span data-ttu-id="ec52f-181">La tabla descriptor `UAV` tiene la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="ec52f-181">The Descriptor Table `UAV` has the following syntax:</span></span>

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="ec52f-182">Esto es similar a la entrada de la tabla descriptor, salvo que `CBV` el intervalo especificado es para las vistas de acceso no ordenado.</span><span class="sxs-lookup"><span data-stu-id="ec52f-182">This is similar to the descriptor table `CBV` entry, except the specified range is for unordered access views.</span></span>

<span data-ttu-id="ec52f-183">La tabla descriptor `Sampler` tiene la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="ec52f-183">The Descriptor Table `Sampler` has the following syntax:</span></span>

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

<span data-ttu-id="ec52f-184">Esto es similar a la entrada de la tabla descriptor, salvo que el intervalo especificado es para los `CBV` muestreadores de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ec52f-184">This is similar to the descriptor table `CBV` entry, except the specified range is for shader samplers.</span></span> <span data-ttu-id="ec52f-185">Tenga en cuenta que los muestreadores no se pueden mezclar con otros tipos de descriptores en la misma tabla de descriptores (ya que están en un montón de descriptores independiente).</span><span class="sxs-lookup"><span data-stu-id="ec52f-185">Note that Samplers can’t be mixed with other types of descriptors in the same descriptor table (since they are in a separate descriptor heap).</span></span>

## <a name="static-sampler"></a><span data-ttu-id="ec52f-186">Sampler estático</span><span class="sxs-lookup"><span data-stu-id="ec52f-186">Static Sampler</span></span>

<span data-ttu-id="ec52f-187">El sampler estático representa la estructura [**D3D12 \_ STATIC \_ SAMPLER \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="ec52f-187">The static sampler represents the [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span> <span data-ttu-id="ec52f-188">El parámetro obligatorio para *StaticSampler* es un objeto escalar, sampler s-register Reg. Otros parámetros son opcionales con los valores predeterminados que se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="ec52f-188">The mandatory parameter for *StaticSampler* is a scalar, sampler s-register Reg. Other parameters are optional with default values shown below.</span></span> <span data-ttu-id="ec52f-189">La mayoría de los campos aceptan un conjunto de enumeraciones predefinidas.</span><span class="sxs-lookup"><span data-stu-id="ec52f-189">Most fields accept a set of predefined enums.</span></span>

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

<span data-ttu-id="ec52f-190">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ec52f-190">For example:</span></span>

``` syntax
StaticSampler(s4, filter=FILTER_MIN_MAG_MIP_LINEAR)
```

<span data-ttu-id="ec52f-191">Las opciones de parámetro son muy similares a las llamadas API de C++, excepto *borderColor*, que está restringido a una enumeración en HLSL.</span><span class="sxs-lookup"><span data-stu-id="ec52f-191">The parameter options are very similar to the C++ API calls, except for *borderColor*, which is restricted to an enum in HLSL.</span></span>

<span data-ttu-id="ec52f-192">El campo de filtro puede ser uno de [**D3D12 \_ FILTER.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)</span><span class="sxs-lookup"><span data-stu-id="ec52f-192">The filter field can be one of [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).</span></span>

<span data-ttu-id="ec52f-193">Los campos de dirección pueden ser de [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).</span><span class="sxs-lookup"><span data-stu-id="ec52f-193">The address fields can each be one of [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).</span></span>

<span data-ttu-id="ec52f-194">La función de comparación puede ser una de las funciones [**\_ \_ FUNC COMPARISON de D3D12.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)</span><span class="sxs-lookup"><span data-stu-id="ec52f-194">The comparison function can be one of [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).</span></span>

<span data-ttu-id="ec52f-195">El campo de color del borde puede ser uno de [**D3D12 \_ STATIC \_ BORDER \_ COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).</span><span class="sxs-lookup"><span data-stu-id="ec52f-195">The border color field can be one of [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).</span></span>

<span data-ttu-id="ec52f-196">La visibilidad puede ser una de [**las VISIBILIDAD DEL \_ SOMBREADOR \_ de D3D12.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)</span><span class="sxs-lookup"><span data-stu-id="ec52f-196">Visibility can be one of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

## <a name="compiling-an-hlsl-root-signature"></a><span data-ttu-id="ec52f-197">Compilación de una firma raíz HLSL</span><span class="sxs-lookup"><span data-stu-id="ec52f-197">Compiling an HLSL root signature</span></span>

<span data-ttu-id="ec52f-198">Hay dos mecanismos para compilar una firma raíz HLSL.</span><span class="sxs-lookup"><span data-stu-id="ec52f-198">There are two mechanisms to compile an HLSL root signature.</span></span> <span data-ttu-id="ec52f-199">En primer lugar, es posible adjuntar una cadena de firma raíz a un sombreador determinado mediante el atributo *RootSignature* (en el ejemplo siguiente, mediante el punto de entrada **MyRS1):**</span><span class="sxs-lookup"><span data-stu-id="ec52f-199">First, it is possible to attach a root signature string to a particular shader via the *RootSignature* attribute (in the following example, using the **MyRS1** entry point):</span></span>

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

<span data-ttu-id="ec52f-200">El compilador creará y comprobará el blob de firma raíz del sombreador e insertará junto con el código de bytes del sombreador en el blob del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ec52f-200">The compiler will create and verify the root signature blob for the shader and embed it alongside the shader byte code into the shader blob.</span></span> <span data-ttu-id="ec52f-201">El compilador admite la sintaxis de firma raíz para el modelo de sombreador 5.0 y superior.</span><span class="sxs-lookup"><span data-stu-id="ec52f-201">The compiler supports root signature syntax for shader model 5.0 and higher.</span></span> <span data-ttu-id="ec52f-202">Si una firma raíz está incrustada en un sombreador del modelo de sombreador 5.0 y ese sombreador se envía al runtime D3D11, en lugar de D3D12, D3D11 omitirá silenciosamente la parte de la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="ec52f-202">If a root signature is embedded in a shader model 5.0 shader and that shader is sent to the D3D11 runtime, as opposed to D3D12, the root signature portion will get silently ignored by D3D11.</span></span>

<span data-ttu-id="ec52f-203">El otro mecanismo es crear un blob de firma raíz independiente, quizás para reutilizarlo con un gran conjunto de sombreadores, lo que ahorra espacio.</span><span class="sxs-lookup"><span data-stu-id="ec52f-203">The other mechanism is to create a standalone root signature blob, perhaps to reuse it with a large set of shaders, saving space.</span></span> <span data-ttu-id="ec52f-204">[Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC) admite modelos de sombreador **rootsig \_ 1 \_ 0** y **rootsig \_ 1 \_ 1.**</span><span class="sxs-lookup"><span data-stu-id="ec52f-204">The [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC) supports both **rootsig\_1\_0** and **rootsig\_1\_1** shader models.</span></span> <span data-ttu-id="ec52f-205">El nombre de la cadena de definición se especifica mediante el argumento /E habitual.</span><span class="sxs-lookup"><span data-stu-id="ec52f-205">The name of the define string is specified via the usual /E argument.</span></span> <span data-ttu-id="ec52f-206">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ec52f-206">For example:</span></span>

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

<span data-ttu-id="ec52f-207">Tenga en cuenta que la definición de la cadena de firma raíz también se puede pasar en la línea de comandos, por ejemplo, /D MyRS1="...".</span><span class="sxs-lookup"><span data-stu-id="ec52f-207">Note that the root signature string define can also be passed on the command line, e.g, /D MyRS1=”…”.</span></span>

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a><span data-ttu-id="ec52f-208">Manipulación de firmas raíz con el compilador fxc</span><span class="sxs-lookup"><span data-stu-id="ec52f-208">Manipulating root signatures with the FXC compiler</span></span>

<span data-ttu-id="ec52f-209">El compilador FXC crea código de bytes del sombreador a partir de archivos de código fuente HLSL.</span><span class="sxs-lookup"><span data-stu-id="ec52f-209">The FXC compiler creates shader byte-code from HLSL source files.</span></span> <span data-ttu-id="ec52f-210">Hay una gran cantidad de parámetros opcionales para este compilador; consulte [la herramienta Effect-Compiler](/windows/desktop/direct3dtools/fxc).</span><span class="sxs-lookup"><span data-stu-id="ec52f-210">There are a lot of optional parameters for this compiler, refer to the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc).</span></span>

<span data-ttu-id="ec52f-211">Para administrar firmas raíz de HLSL, en la tabla siguiente se proporcionan algunos ejemplos de uso de FXC.</span><span class="sxs-lookup"><span data-stu-id="ec52f-211">For managing HLSL authored root signatures, the following table gives some examples of using FXC.</span></span>



| <span data-ttu-id="ec52f-212">Línea</span><span class="sxs-lookup"><span data-stu-id="ec52f-212">Line</span></span> | <span data-ttu-id="ec52f-213">Línea de comandos</span><span class="sxs-lookup"><span data-stu-id="ec52f-213">Command line</span></span>                                                                 | <span data-ttu-id="ec52f-214">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec52f-214">Description</span></span>                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec52f-215">1</span><span class="sxs-lookup"><span data-stu-id="ec52f-215">1</span></span>    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | <span data-ttu-id="ec52f-216">Compila un sombreador para el destino del sombreador de píxeles 5.1; el origen del sombreador está en el archivo shaderWithRootSig.hlsl, que incluye una firma raíz.</span><span class="sxs-lookup"><span data-stu-id="ec52f-216">Compiles a shader for the pixel shader 5.1 target, the shader source is in the shaderWithRootSig.hlsl file, which includes a root signature.</span></span> <span data-ttu-id="ec52f-217">El sombreador y la firma raíz se compilan como blobs independientes en el archivo binario rs1.fxo.</span><span class="sxs-lookup"><span data-stu-id="ec52f-217">The shader and root signature are compiled as separate blobs in the rs1.fxo binary file.</span></span>    |
| <span data-ttu-id="ec52f-218">2</span><span class="sxs-lookup"><span data-stu-id="ec52f-218">2</span></span>    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | <span data-ttu-id="ec52f-219">Extrae la firma raíz del archivo creado por la línea 1, por lo que el archivo rs1.rs.fxo contiene solo una firma raíz.</span><span class="sxs-lookup"><span data-stu-id="ec52f-219">Extracts the root signature from the file created by line 1, so the rs1.rs.fxo file contains just a root signature.</span></span>                                                                                                                      |
| <span data-ttu-id="ec52f-220">3</span><span class="sxs-lookup"><span data-stu-id="ec52f-220">3</span></span>    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | <span data-ttu-id="ec52f-221">Quita la firma raíz del archivo creado por la línea 1, por lo que el archivo rs1.striped.fxo contiene un sombreador sin firma raíz.</span><span class="sxs-lookup"><span data-stu-id="ec52f-221">Removes the root signature from the file created by line 1, so the rs1.stripped.fxo file contains a shader with no root signature.</span></span>                                                                                                       |
| <span data-ttu-id="ec52f-222">4</span><span class="sxs-lookup"><span data-stu-id="ec52f-222">4</span></span>    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | <span data-ttu-id="ec52f-223">Combina un sombreador y una firma raíz que están en archivos independientes en un archivo binario que contiene ambos blobs.</span><span class="sxs-lookup"><span data-stu-id="ec52f-223">Combines a shader and root signature that are in separate files into a binary file containing both blobs.</span></span> <span data-ttu-id="ec52f-224">En este ejemplo, rs1.new.fx0 sería idéntico a rs1.fx0 en la línea 1.</span><span class="sxs-lookup"><span data-stu-id="ec52f-224">In this example rs1.new.fx0 would be identical to rs1.fx0 in line 1.</span></span>                                                           |
| <span data-ttu-id="ec52f-225">5</span><span class="sxs-lookup"><span data-stu-id="ec52f-225">5</span></span>    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | <span data-ttu-id="ec52f-226">Crea un archivo binario de firma raíz independiente a partir de un origen que puede contener algo más que una firma raíz.</span><span class="sxs-lookup"><span data-stu-id="ec52f-226">Creates a stand-alone root signature binary file from a source that may contain more than just a root signature.</span></span> <span data-ttu-id="ec52f-227">Observe el destino rootsig 1 0 y que RS1 es el nombre de la cadena de macro de firma raíz (definir) en el \_ \_ archivo \# HLSL.</span><span class="sxs-lookup"><span data-stu-id="ec52f-227">Note the rootsig\_1\_0 target, and that RS1 is the name of the root signature (\#define) macro string in the HLSL file.</span></span> |



 

<span data-ttu-id="ec52f-228">La funcionalidad disponible a través de FXC también está disponible mediante programación mediante la [**función D3DCompile.**](/windows/desktop/direct3dhlsl/d3dcompile)</span><span class="sxs-lookup"><span data-stu-id="ec52f-228">The functionality available through FXC is also available programmatically using the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) function.</span></span> <span data-ttu-id="ec52f-229">Esta llamada compila un sombreador con una firma raíz o una firma raíz independiente (estableciendo el destino rootsig \_ \_ 1 0).</span><span class="sxs-lookup"><span data-stu-id="ec52f-229">This call compiles a shader with a root signature, or stand-alone root signature (setting the rootsig\_1\_0 target).</span></span> <span data-ttu-id="ec52f-230">[**D3DGetBlobPart y**](/windows/desktop/direct3dhlsl/d3dgetblobpart) [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) pueden extraer y adjuntar firmas raíz a un blob existente.</span><span class="sxs-lookup"><span data-stu-id="ec52f-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) and [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) can extract and attach root signatures to an existing blob.</span></span>  <span data-ttu-id="ec52f-231">D3D \_ BLOB ROOT SIGNATURE se usa para especificar el tipo de elemento de blob de firma \_ \_ raíz.</span><span class="sxs-lookup"><span data-stu-id="ec52f-231">D3D\_BLOB\_ROOT\_SIGNATURE is used to specify the root signature blob part type.</span></span> <span data-ttu-id="ec52f-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) quita la firma raíz (mediante la marca D3DCOMPILER \_ STRIP \_ ROOT \_ SIGNATURE) del blob.</span><span class="sxs-lookup"><span data-stu-id="ec52f-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) removes the root signature (using the D3DCOMPILER\_STRIP\_ROOT\_SIGNATURE flag) from the blob.</span></span>

## <a name="notes"></a><span data-ttu-id="ec52f-233">Notas</span><span class="sxs-lookup"><span data-stu-id="ec52f-233">Notes</span></span>

> [!Note]  
> <span data-ttu-id="ec52f-234">Mientras que se recomienda encarecidamente la compilación sin conexión de sombreadores, si los sombreadores tienen que compilarse en tiempo de ejecución, consulte los comentarios de [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).</span><span class="sxs-lookup"><span data-stu-id="ec52f-234">Whereas the offline compilation of shaders is strongly recommended, if shaders have to be compiled at runtime, refer to the remarks for [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).</span></span>

 

> [!Note]  
> <span data-ttu-id="ec52f-235">No es necesario cambiar los recursos HLSL existentes para controlar las firmas raíz que se usarán con ellos.</span><span class="sxs-lookup"><span data-stu-id="ec52f-235">Existing HLSL assets do not need to be changed to handle root signatures to be used with them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ec52f-236">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ec52f-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec52f-237">Indexado dinámico mediante HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="ec52f-237">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[<span data-ttu-id="ec52f-238">Características del modelo de sombreador HLSL 5.1 para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="ec52f-238">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="ec52f-239">Enlace de recursos</span><span class="sxs-lookup"><span data-stu-id="ec52f-239">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="ec52f-240">Enlace de recursos en HLSL</span><span class="sxs-lookup"><span data-stu-id="ec52f-240">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="ec52f-241">Firmas raíz</span><span class="sxs-lookup"><span data-stu-id="ec52f-241">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="ec52f-242">Modelo de sombreador 5.1</span><span class="sxs-lookup"><span data-stu-id="ec52f-242">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="ec52f-243">Valor de la referencia de galería de símbolos especificado por el sombreador</span><span class="sxs-lookup"><span data-stu-id="ec52f-243">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
</dt> <dt>

[<span data-ttu-id="ec52f-244">Cargas de la vista de acceso sin ordenar con tipo</span><span class="sxs-lookup"><span data-stu-id="ec52f-244">Typed Unordered Access View Loads</span></span>](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 

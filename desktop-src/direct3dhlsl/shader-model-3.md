---
title: Shader Model 3 (referencia de HLSL)
description: Los sombreadores de vértices y los sombreadores de píxeles se simplifican considerablemente de las versiones anteriores del sombreador.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3517266ace77b9235604770d9b42d10cd80e2d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420897"
---
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="106ae-103">Shader Model 3 (referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="106ae-103">Shader model 3 (HLSL reference)</span></span>

<span data-ttu-id="106ae-104">Los sombreadores de vértices y los sombreadores de píxeles se simplifican considerablemente de las versiones anteriores del sombreador.</span><span class="sxs-lookup"><span data-stu-id="106ae-104">Vertex shaders and pixel shaders are simplified considerably from earlier shader versions.</span></span> <span data-ttu-id="106ae-105">Si está implementando sombreadores en hardware, no puede usar vs \_ 3 \_ 0 o PS \_ 3 \_ 0 con ninguna otra versión del sombreador, y no puede usar ninguno de los tipos de sombreador con la canalización de función fija.</span><span class="sxs-lookup"><span data-stu-id="106ae-105">If you are implementing shaders in hardware, you may not use vs\_3\_0 or ps\_3\_0 with any other shader versions, and you may not use either shader type with the fixed function pipeline.</span></span> <span data-ttu-id="106ae-106">Estos cambios permiten simplificar los controladores y el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="106ae-106">These changes make it possible to simplify drivers and the runtime.</span></span> <span data-ttu-id="106ae-107">La única excepción es que los sombreadores de solo software vs \_ 3 \_ 0 se pueden usar con cualquier versión de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="106ae-107">The only exception is that software-only vs\_3\_0 shaders may be used with any pixel shader version.</span></span> <span data-ttu-id="106ae-108">Además, si usa un sombreador de solo software vs \_ 3 \_ 0 con una versión de sombreador de píxeles anterior, el sombreador de vértices solo puede utilizar la semántica de salida que sea compatible con los códigos de formato de vértice flexible (FVF).</span><span class="sxs-lookup"><span data-stu-id="106ae-108">In addition, if you are using a software-only vs\_3\_0 shader with a previous pixel shader version, the vertex shader can only use output semantics that are compatible with flexible vertex format (FVF) codes.</span></span>

<span data-ttu-id="106ae-109">La semántica que se usa en las salidas del sombreador de vértices se debe usar en entradas del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="106ae-109">The semantics used on vertex shader outputs must be used on pixel shader inputs.</span></span> <span data-ttu-id="106ae-110">La semántica se usa para asignar las salidas del sombreador de vértices a las entradas del sombreador de píxeles, similar a la forma en que se asigna la declaración de vértices a los registros de entrada del sombreador de vértices y los modelos de sombreador anteriores.</span><span class="sxs-lookup"><span data-stu-id="106ae-110">The semantics are used to map the vertex shader outputs to the pixel shader inputs, similar to the way the vertex declaration is mapped to the vertex shader input registers and previous shader models.</span></span> <span data-ttu-id="106ae-111">Consulte semántica de coincidencia en los sombreadores de vs 3,0 y PS 3,0.</span><span class="sxs-lookup"><span data-stu-id="106ae-111">See Match Semantics on vs 3.0 and ps 3.0 Shaders.</span></span>

<span data-ttu-id="106ae-112">Se han agregado Estados de representación del modo de ajuste adicionales para cubrir la posibilidad de coordenadas de textura adicionales en este nuevo esquema.</span><span class="sxs-lookup"><span data-stu-id="106ae-112">Additional wrap mode render states have been added to cover the possibility of additional texture coordinates in this new scheme.</span></span> <span data-ttu-id="106ae-113">Los atributos con D3DDECLUSAGE \_ TEXCOORD y el índice de uso de 0 a 15 se interpolan en el modo de ajuste cuando se establece el [**\_ ajuste \* de D3DRS**](/windows/desktop/direct3d9/d3drenderstatetype) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="106ae-113">Attributes with D3DDECLUSAGE\_TEXCOORD and usage index from 0 to 15 are interpolated in wrap mode when the corresponding [**D3DRS\_WRAP\***](/windows/desktop/direct3d9/d3drenderstatetype) is set.</span></span>

-   [<span data-ttu-id="106ae-114">Características del modelo de sombreador de vértice 3</span><span class="sxs-lookup"><span data-stu-id="106ae-114">Vertex Shader Model 3 Features</span></span>](#vertex-shader-model-3-features)
-   [<span data-ttu-id="106ae-115">Características del modelo de sombreador de píxeles 3</span><span class="sxs-lookup"><span data-stu-id="106ae-115">Pixel Shader Model 3 Features</span></span>](#pixel-shader-model-3-features)
-   [<span data-ttu-id="106ae-116">Coincidencia de la semántica en \_ los \_ sombreadores de vs 3 0 y PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="106ae-116">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>](/windows)
-   [<span data-ttu-id="106ae-117">Cambios en el modo de niebla, profundidad y sombreado</span><span class="sxs-lookup"><span data-stu-id="106ae-117">Fog, Depth, and Shading Mode Changes</span></span>](#fog-depth-and-shading-mode-changes)
-   [<span data-ttu-id="106ae-118">Conversiones de punto flotante y entero</span><span class="sxs-lookup"><span data-stu-id="106ae-118">Floating Point and Integer Conversions</span></span>](#floating-point-and-integer-conversions)
-   [<span data-ttu-id="106ae-119">Especificar una precisión completa o parcial</span><span class="sxs-lookup"><span data-stu-id="106ae-119">Specifying Full or Partial Precision</span></span>](#specifying-full-or-partial-precision)
-   [<span data-ttu-id="106ae-120">Sombreadores de píxeles y vértices de software</span><span class="sxs-lookup"><span data-stu-id="106ae-120">Software Vertex and Pixel Shaders</span></span>](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a><span data-ttu-id="106ae-121">Características del modelo de sombreador de vértice 3</span><span class="sxs-lookup"><span data-stu-id="106ae-121">Vertex Shader Model 3 Features</span></span>

<span data-ttu-id="106ae-122">Los tipos de registro de salida del sombreador de vértices se han contraído en doce registros (consulte [registros de salida](dx9-graphics-reference-asm-vs-registers-output.md)).</span><span class="sxs-lookup"><span data-stu-id="106ae-122">The vertex shader output register types have been collapsed into twelve registers (see [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)).</span></span> <span data-ttu-id="106ae-123">Cada registro que se usa debe declararse mediante la instrucción [DCL](dcl-usage---ps.md) y una semántica (por ejemplo, DCL \_ color0 O0. xyzw).</span><span class="sxs-lookup"><span data-stu-id="106ae-123">Each register that is used needs to be declared using the [dcl](dcl-usage---ps.md) instruction and a semantic (for example, dcl\_color0 o0.xyzw).</span></span>

<span data-ttu-id="106ae-124">El \_ modelo de sombreador de vértices 3 0 (vs \_ 3 \_ 0) amplía las características de vs \_ 2 \_ 0 con indexación de registros más eficaz, un conjunto de registros de salida simplificados, la capacidad de muestrear una textura en un sombreador de vértices y la capacidad de controlar la velocidad a la que se inicializan las entradas del sombreador.</span><span class="sxs-lookup"><span data-stu-id="106ae-124">The 3\_0 vertex shader model (vs\_3\_0) expands on the features of vs\_2\_0 with more powerful register indexing, a set of simplified output registers, the ability to sample a texture in a vertex shader, and the ability to control the rate at which shader inputs are initialized.</span></span>

### <a name="index-any-register"></a><span data-ttu-id="106ae-125">Indexar cualquier registro</span><span class="sxs-lookup"><span data-stu-id="106ae-125">Index Any Register</span></span>

<span data-ttu-id="106ae-126">Todos los registros (registros de [entrada](dx9-graphics-reference-asm-vs-registers-input.md) y registro de [salida](dx9-graphics-reference-asm-vs-registers-output.md)) se pueden indexar mediante [el registro de contadores de bucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (solo los registros de constantes se pueden indizar en versiones anteriores).</span><span class="sxs-lookup"><span data-stu-id="106ae-126">All registers( [Input Register](dx9-graphics-reference-asm-vs-registers-input.md) and [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)) can be indexed using [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (only constant registers could be indexed in earlier versions.)</span></span>

<span data-ttu-id="106ae-127">Debe declarar los registros de entrada y salida antes de indizarlos.</span><span class="sxs-lookup"><span data-stu-id="106ae-127">You must declare input and output registers before indexing them.</span></span> <span data-ttu-id="106ae-128">Sin embargo, no puede indexar ningún registro de salida que se haya declarado con una posición o una semántica de tamaño de punto.</span><span class="sxs-lookup"><span data-stu-id="106ae-128">However, you may not index any output register that has been declared with a position or point size semantic.</span></span> <span data-ttu-id="106ae-129">De hecho, si se usa la indexación, la semántica de posición y psize debe declararse en los registros O0 y O1, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="106ae-129">In fact, if indexing is used the position and psize semantics have to be declared in the o0 and o1 registers respectively.</span></span>

<span data-ttu-id="106ae-130">Solo se permite indexar un intervalo continuo de registros; es decir, no se puede indexar entre los registros que no se han declarado.</span><span class="sxs-lookup"><span data-stu-id="106ae-130">You are only allowed to index a continuous range of registers; that is, you cannot index across registers that have not been declared.</span></span> <span data-ttu-id="106ae-131">Aunque esta restricción puede ser inadecuada, permite que se lleve a cabo la optimización del hardware.</span><span class="sxs-lookup"><span data-stu-id="106ae-131">While this restriction may be inconvenient, it permits hardware optimization to take place.</span></span> <span data-ttu-id="106ae-132">Si se intenta indexar en registros no contiguos, se producirán resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="106ae-132">Attempting to index across non-contiguous registers will produce undefined results.</span></span> <span data-ttu-id="106ae-133">La validación del sombreador no aplica esta restricción.</span><span class="sxs-lookup"><span data-stu-id="106ae-133">Shader validation does not enforce this restriction.</span></span>

### <a name="simplify-output-registers"></a><span data-ttu-id="106ae-134">Simplificar registros de salida</span><span class="sxs-lookup"><span data-stu-id="106ae-134">Simplify Output Registers</span></span>

<span data-ttu-id="106ae-135">Todos los distintos tipos de registros de salida se han contraído en doce registros de salida: 1 para la posición, 2 para el color, 8 para la textura y 1 para la niebla o el tamaño del punto.</span><span class="sxs-lookup"><span data-stu-id="106ae-135">All the various types of output registers have been collapsed into twelve output registers: 1 for position, 2 for color, 8 for texture, and 1 for fog or point size.</span></span> <span data-ttu-id="106ae-136">Estos registros interpolarán los datos que contengan para el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="106ae-136">These registers will interpolate any data they contain for the pixel shader.</span></span> <span data-ttu-id="106ae-137">Las declaraciones de registro de salida son obligatorias y las semánticas se asignan a cada registro.</span><span class="sxs-lookup"><span data-stu-id="106ae-137">Output register declarations are required and semantics are assigned to each register.</span></span>

<span data-ttu-id="106ae-138">Los registros se pueden dividir de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="106ae-138">The registers can be broken down as follows:</span></span>

-   <span data-ttu-id="106ae-139">Al menos un registro debe declararse como un registro de posición de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="106ae-139">At least one register must be declared as a four-component position register.</span></span> <span data-ttu-id="106ae-140">Este es el único registro del sombreador de vértices necesario.</span><span class="sxs-lookup"><span data-stu-id="106ae-140">This is the only vertex shader register that is required.</span></span>
-   <span data-ttu-id="106ae-141">Los diez primeros registros utilizados por un sombreador pueden usar hasta cuatro componentes (xyzw) como máximo.</span><span class="sxs-lookup"><span data-stu-id="106ae-141">The first ten registers consumed by a shader may use up to four components (xyzw) maximum.</span></span>
-   <span data-ttu-id="106ae-142">El último (o duodécimo) registro solo puede contener un valor escalar (por ejemplo, un tamaño de punto).</span><span class="sxs-lookup"><span data-stu-id="106ae-142">The last (or twelfth) register may only contain a scalar (such as point size).</span></span>

<span data-ttu-id="106ae-143">Para obtener una lista de los registros, consulte [registros-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="106ae-143">For a listing of the registers, see [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>

### <a name="texture-sample-in-a-vertex-shader"></a><span data-ttu-id="106ae-144">Ejemplo de textura en un sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="106ae-144">Texture Sample in a Vertex Shader</span></span>

<span data-ttu-id="106ae-145">Vertex Shader 3 \_ 0 admite la búsqueda de texturas en el sombreador de vértices mediante [texldl-vs](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="106ae-145">Vertex shader 3\_0 supports texture lookup in the vertex shader using [texldl - vs](texldl---vs.md).</span></span>

## <a name="pixel-shader-model-3-features"></a><span data-ttu-id="106ae-146">Características del modelo de sombreador de píxeles 3</span><span class="sxs-lookup"><span data-stu-id="106ae-146">Pixel Shader Model 3 Features</span></span>

<span data-ttu-id="106ae-147">Los registros de color y textura del sombreador de píxeles se han contraído en diez registros de entrada (consulte [tipos de registro de entrada](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span><span class="sxs-lookup"><span data-stu-id="106ae-147">The pixel shader color and texture registers have been collapsed into ten input registers (see [Input Register Types](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span></span> <span data-ttu-id="106ae-148">El registro facial es un registro escalar de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="106ae-148">The Face Register is a floating point scalar register.</span></span> <span data-ttu-id="106ae-149">Solo el signo de este registro es válido.</span><span class="sxs-lookup"><span data-stu-id="106ae-149">Only the sign of this register is valid.</span></span> <span data-ttu-id="106ae-150">Si el signo es negativo, el primitivo es una parte posterior.</span><span class="sxs-lookup"><span data-stu-id="106ae-150">If the sign is negative the primitive is a back face.</span></span> <span data-ttu-id="106ae-151">Se puede usar dentro de un sombreador de píxeles para lograr la iluminación de dos caras, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="106ae-151">This can be used inside a pixel shader to achieve two-sided lighting, for instance.</span></span> <span data-ttu-id="106ae-152">El registro de posición hace referencia a los píxeles actuales (x, y).</span><span class="sxs-lookup"><span data-stu-id="106ae-152">The Position Register references the current (x,y) pixels.</span></span>

<span data-ttu-id="106ae-153">Los registros de constantes del sombreador se pueden establecer mediante:</span><span class="sxs-lookup"><span data-stu-id="106ae-153">The shader constant registers can be set using:</span></span>

-   [<span data-ttu-id="106ae-154">**SetPixelShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="106ae-154">**SetPixelShaderConstantB**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [<span data-ttu-id="106ae-155">**SetPixelShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="106ae-155">**SetPixelShaderConstantI**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [<span data-ttu-id="106ae-156">**SetPixelShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="106ae-156">**SetPixelShaderConstantF**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a><span data-ttu-id="106ae-157">Coincidencia de la semántica en \_ los \_ sombreadores de vs 3 0 y PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="106ae-157">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>

<span data-ttu-id="106ae-158">Existen algunas restricciones en el uso semántico con vs \_ 3 \_ 0 y PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="106ae-158">There are some restrictions on semantic usage with vs\_3\_0 and ps\_3\_0.</span></span> <span data-ttu-id="106ae-159">En general, debe tener cuidado al usar una semántica para una entrada de sombreador que coincida con una semántica usada en una salida de sombreador.</span><span class="sxs-lookup"><span data-stu-id="106ae-159">In general, you need to be careful when using a semantic for a shader input that matches a semantic used on a shader output.</span></span>

<span data-ttu-id="106ae-160">Por ejemplo, este sombreador de píxeles empaqueta varios nombres en un registro:</span><span class="sxs-lookup"><span data-stu-id="106ae-160">For instance, this pixel shader packs multiple names into one register:</span></span>


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



<span data-ttu-id="106ae-161">Cada registro tiene una semántica diferente.</span><span class="sxs-lookup"><span data-stu-id="106ae-161">Each register has a different semantic.</span></span> <span data-ttu-id="106ae-162">Tenga en cuenta que también puede denominar v0. x y v0. YZ con una semántica diferente (varias) debido al uso de la máscara de escritura.</span><span class="sxs-lookup"><span data-stu-id="106ae-162">Notice that you can also name v0.x and v0.yz with different (multiple) semantics because of the use of the write mask.</span></span>

<span data-ttu-id="106ae-163">Dado el sombreador de píxeles, el siguiente \_ sombreador de vs 3 \_ 0 no puede emparejarse con él:</span><span class="sxs-lookup"><span data-stu-id="106ae-163">Given the pixel shader, the following vs\_3\_0 shader cannot be paired with it:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



<span data-ttu-id="106ae-164">Estos dos sombreadores entran en conflicto con el uso de la semántica de [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) y **D3DDECLUSAGE \_ TEXCOORD1** .</span><span class="sxs-lookup"><span data-stu-id="106ae-164">These two shaders conflict with their use of the [**D3DDECLUSAGE\_TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) And **D3DDECLUSAGE\_TEXCOORD1** semantics.</span></span>

<span data-ttu-id="106ae-165">Vuelva a escribir el sombreador de vértices como este para evitar la colisión semántica:</span><span class="sxs-lookup"><span data-stu-id="106ae-165">Rewrite the vertex shader like this to avoid the semantic collision:</span></span>


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



<span data-ttu-id="106ae-166">Del mismo modo, no se puede usar un nombre semántico declarado en registros de entrada diferentes en el sombreador de píxeles (V0 y V1 en el sombreador de píxeles) en un registro de salida único en este sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="106ae-166">Similarly, a semantic name declared on different input registers in the pixel shader (v0 and v1 in the pixel shader) cannot be used in a single output register in this vertex shader.</span></span> <span data-ttu-id="106ae-167">Por ejemplo, este sombreador de vértices no se puede emparejar con el sombreador de píxeles porque D3DDECLUSAGE \_ TEXCOORD1 se usa para los registros de entrada del sombreador de píxeles (V0, V1) y el registro de salida del sombreador de vértices O3.</span><span class="sxs-lookup"><span data-stu-id="106ae-167">For instance, this vertex shader cannot be paired with the pixel shader because D3DDECLUSAGE\_TEXCOORD1 is used for both pixel shader input registers (v0, v1) and the vertex shader output register o3.</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



<span data-ttu-id="106ae-168">Por otro lado, este sombreador de vértices no se puede emparejar con el sombreador de píxeles porque la máscara de salida de un parámetro con una semántica determinada no proporciona los datos que el sombreador de píxeles solicita:</span><span class="sxs-lookup"><span data-stu-id="106ae-168">On the other hand, this vertex shader cannot be paired with the pixel shader because the output mask for a parameter with a given semantic does not provide the data that is requested by the pixel shader:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



<span data-ttu-id="106ae-169">Este sombreador de vértices no proporciona una salida con uno de los nombres semánticos solicitados por el sombreador de píxeles, por lo que el emparejamiento del sombreador no es válido:</span><span class="sxs-lookup"><span data-stu-id="106ae-169">This vertex shader does not provide an output with one of the semantic names requested by the pixel shader, so the shader pairing is invalid:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord3 o9 
// The pixel shader wants texcoord2, with a w component, 
// but it isn't output by this vertex shader at all! 
... 
```



## <a name="fog-depth-and-shading-mode-changes"></a><span data-ttu-id="106ae-170">Cambios en el modo de niebla, profundidad y sombreado</span><span class="sxs-lookup"><span data-stu-id="106ae-170">Fog, Depth, and Shading Mode Changes</span></span>

<span data-ttu-id="106ae-171">Cuando \_ se establece D3DRS SHADEMODE para el sombreado plano durante la rasterización de recorte y triángulos, los atributos con \_ color D3DDECLUSAGE se interpolan como sombreados planos.</span><span class="sxs-lookup"><span data-stu-id="106ae-171">When D3DRS\_SHADEMODE is set for flat shading during clipping and triangle rasterization, attributes with D3DDECLUSAGE\_COLOR are interpolated as flat shaded.</span></span> <span data-ttu-id="106ae-172">Si los componentes de un registro se declaran con una semántica de color, pero otros componentes del mismo registro tienen una semántica diferente, la interpolación de sombreado plano (lineal y plana) no se definirá en los componentes de que se registran sin una semántica de color.</span><span class="sxs-lookup"><span data-stu-id="106ae-172">If any components of a register are declared with a color semantic but other components of the same register are given different semantics, flat shading interpolation (linear vs. flat) will be undefined on the components in that register without a color semantic.</span></span>

<span data-ttu-id="106ae-173">Si se desea la representación de niebla, \_ los \_ sombreadores de vs 3 0 y PS \_ 3 \_ 0 deben implementar la niebla.</span><span class="sxs-lookup"><span data-stu-id="106ae-173">If fog rendering is desired, vs\_3\_0 and ps\_3\_0 shaders must implement fog.</span></span> <span data-ttu-id="106ae-174">No se realizan cálculos de niebla fuera de los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="106ae-174">No fog calculations are done outside of the shaders.</span></span> <span data-ttu-id="106ae-175">No hay ningún registro de niebla en vs \_ 3 \_ 0, y la niebla adicional D3DDECLUSAGE \_ (para el factor de mezcla de niebla calculada por vértice) y la profundidad de D3DDECLUSAGE \_ (para pasar un valor de profundidad al sombreador de píxeles para calcular el factor de mezcla de niebla) se han agregado.</span><span class="sxs-lookup"><span data-stu-id="106ae-175">There is no fog register in vs\_3\_0, and additional semantics D3DDECLUSAGE\_FOG (for fog blend factor computed per vertex) and D3DDECLUSAGE\_DEPTH (for passing in a depth value to the pixel shader to compute the fog blend factor) have been added.</span></span>

<span data-ttu-id="106ae-176">El estado de fase de textura D3DTSS \_ TEXCOORDINDEX se omite cuando se usa el sombreador de píxeles 3,0.</span><span class="sxs-lookup"><span data-stu-id="106ae-176">Texture stage state D3DTSS\_TEXCOORDINDEX is ignored when using pixel shader 3.0.</span></span>

<span data-ttu-id="106ae-177">Se han agregado los siguientes valores para dar cabida a estos cambios:</span><span class="sxs-lookup"><span data-stu-id="106ae-177">The following values have been added to accommodate these changes:</span></span>


```
// Fog and Depth usages
D3DDECLUSAGE_FOG 
D3DDECLUSAGE_DEPTH 

// Additional wrap states for vs_3_0 attributes with D3DDECLUSAGE_TEXCOORD 
D3DRS_WRAP8 
D3DRS_WRAP9 
D3DRS_WRAP10 
D3DRS_WRAP11 
D3DRS_WRAP12 
D3DRS_WRAP13 
D3DRS_WRAP14 
D3DRS_WRAP15
```



## <a name="floating-point-and-integer-conversions"></a><span data-ttu-id="106ae-178">Conversiones de punto flotante y entero</span><span class="sxs-lookup"><span data-stu-id="106ae-178">Floating Point and Integer Conversions</span></span>

<span data-ttu-id="106ae-179">Los cálculos matemáticos de punto flotante se producen en diferentes precisión y rangos (16 bits, 24 bits y 32 bits) en diferentes partes de la canalización.</span><span class="sxs-lookup"><span data-stu-id="106ae-179">Floating point math happens at different precision and ranges (16-bit, 24-bit, and 32-bit) in different parts of the pipeline.</span></span> <span data-ttu-id="106ae-180">Un valor mayor que el intervalo dinámico de la canalización que entra en esa canalización (por ejemplo, un mapa de textura flotante de 32 bits se muestrea en una canalización Float de 24 bits en PS \_ 2 \_ 0) crea un resultado no definido.</span><span class="sxs-lookup"><span data-stu-id="106ae-180">A value greater than the dynamic range of the pipeline that enters that pipeline (for example, a 32-bit float texture map is sampled into a 24-bit float pipeline in ps\_2\_0) creates an undefined result.</span></span> <span data-ttu-id="106ae-181">En el caso del comportamiento predecible, debe fijar este valor en el máximo del intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="106ae-181">For predictable behavior, you should clamp such a value to the dynamic range maximum.</span></span>

<span data-ttu-id="106ae-182">La conversión de un valor de punto flotante a un entero se produce en varios lugares, como:</span><span class="sxs-lookup"><span data-stu-id="106ae-182">Conversion from a floating point value to an integer happens in several places such as:</span></span>

-   <span data-ttu-id="106ae-183">Al encontrar una instrucción [mova-vs](mova---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="106ae-183">When encountering a [mova - vs](mova---vs.md) instruction.</span></span>
-   <span data-ttu-id="106ae-184">Durante el direccionamiento de textura.</span><span class="sxs-lookup"><span data-stu-id="106ae-184">During texture addressing.</span></span>
-   <span data-ttu-id="106ae-185">Al escribir en un destino de representación de punto no flotante.</span><span class="sxs-lookup"><span data-stu-id="106ae-185">When writing out to a non-floating point render target.</span></span>

## <a name="specifying-full-or-partial-precision"></a><span data-ttu-id="106ae-186">Especificar una precisión completa o parcial</span><span class="sxs-lookup"><span data-stu-id="106ae-186">Specifying Full or Partial Precision</span></span>

<span data-ttu-id="106ae-187">Tanto el PS \_ 3 \_ como el PS \_ 2 \_ x proporcionan compatibilidad con dos niveles de precisión:</span><span class="sxs-lookup"><span data-stu-id="106ae-187">Both ps\_3\_0 and ps\_2\_x provide support for two levels of precision:</span></span>



|          |          |                   |                      |
|----------|----------|-------------------|----------------------|
| <span data-ttu-id="106ae-188">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="106ae-188">ps\_3\_0</span></span> | <span data-ttu-id="106ae-189">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="106ae-189">ps\_2\_0</span></span> | <span data-ttu-id="106ae-190">Precisión</span><span class="sxs-lookup"><span data-stu-id="106ae-190">Precision</span></span>         | <span data-ttu-id="106ae-191">Value</span><span class="sxs-lookup"><span data-stu-id="106ae-191">Value</span></span>                |
| <span data-ttu-id="106ae-192">x</span><span class="sxs-lookup"><span data-stu-id="106ae-192">x</span></span>        |          | <span data-ttu-id="106ae-193">Completo</span><span class="sxs-lookup"><span data-stu-id="106ae-193">Full</span></span>              | <span data-ttu-id="106ae-194">fp32 o superior</span><span class="sxs-lookup"><span data-stu-id="106ae-194">fp32 or higher</span></span>       |
| <span data-ttu-id="106ae-195">x</span><span class="sxs-lookup"><span data-stu-id="106ae-195">x</span></span>        |          | <span data-ttu-id="106ae-196">Precisión parcial</span><span class="sxs-lookup"><span data-stu-id="106ae-196">Partial precision</span></span> | <span data-ttu-id="106ae-197">FP16 = s10e5</span><span class="sxs-lookup"><span data-stu-id="106ae-197">fp16=s10e5</span></span>           |
| <span data-ttu-id="106ae-198">x</span><span class="sxs-lookup"><span data-stu-id="106ae-198">x</span></span>        | <span data-ttu-id="106ae-199">x</span><span class="sxs-lookup"><span data-stu-id="106ae-199">x</span></span>        | <span data-ttu-id="106ae-200">Completo</span><span class="sxs-lookup"><span data-stu-id="106ae-200">Full</span></span>              | <span data-ttu-id="106ae-201">fp24 = s16e7 o superior</span><span class="sxs-lookup"><span data-stu-id="106ae-201">fp24=s16e7 or higher</span></span> |
| <span data-ttu-id="106ae-202">x</span><span class="sxs-lookup"><span data-stu-id="106ae-202">x</span></span>        | <span data-ttu-id="106ae-203">x</span><span class="sxs-lookup"><span data-stu-id="106ae-203">x</span></span>        | <span data-ttu-id="106ae-204">Precisión parcial</span><span class="sxs-lookup"><span data-stu-id="106ae-204">Partial precision</span></span> | <span data-ttu-id="106ae-205">FP16 = s10e5</span><span class="sxs-lookup"><span data-stu-id="106ae-205">fp16=s10e5</span></span>           |



 

<span data-ttu-id="106ae-206">PS \_ 3 \_ 0 admite más precisión que PS \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="106ae-206">ps\_3\_0 supports more precision than ps\_2\_0 does.</span></span> <span data-ttu-id="106ae-207">De forma predeterminada, todas las operaciones se producen en el nivel de precisión completa.</span><span class="sxs-lookup"><span data-stu-id="106ae-207">By default, all operations occur at the full precision level.</span></span>

<span data-ttu-id="106ae-208">La precisión parcial (vea [modificadores de registro del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers.md)) se solicita agregando el \_ modificador PP al código del sombreador (siempre que la implementación subyacente lo admita).</span><span class="sxs-lookup"><span data-stu-id="106ae-208">Partial precision (see [Pixel Shader Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md)) is requested by adding the \_pp modifier to shader code (provided that the underlying implementation supports it).</span></span> <span data-ttu-id="106ae-209">Las implementaciones siempre son gratuitas para omitir el modificador y realizar las operaciones afectadas con precisión completa.</span><span class="sxs-lookup"><span data-stu-id="106ae-209">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="106ae-210">El \_ modificador PP puede producirse en dos contextos:</span><span class="sxs-lookup"><span data-stu-id="106ae-210">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="106ae-211">En una declaración de coordenadas de textura para pasar coordenadas de textura de precisión parcial al sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="106ae-211">On a texture coordinate declaration to pass partial-precision texture coordinates to the pixel shader.</span></span> <span data-ttu-id="106ae-212">Esto se podría usar cuando las coordenadas de textura retransmiten los datos de color al sombreador de píxeles, que puede ser más rápido con una precisión parcial que con precisión completa en algunas implementaciones.</span><span class="sxs-lookup"><span data-stu-id="106ae-212">This could be used when texture coordinates relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span>
-   <span data-ttu-id="106ae-213">En cualquier instrucción para solicitar el uso de precisión parcial, incluidas las instrucciones de carga de textura.</span><span class="sxs-lookup"><span data-stu-id="106ae-213">On any instruction to request the use of partial precision, including texture load instructions.</span></span> <span data-ttu-id="106ae-214">Esto indica que la implementación puede ejecutar la instrucción con precisión parcial y almacenar un resultado de precisión parcial.</span><span class="sxs-lookup"><span data-stu-id="106ae-214">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial-precision result.</span></span> <span data-ttu-id="106ae-215">En ausencia de un modificador explícito, la instrucción se debe realizar a plena precisión (independientemente de la precisión de los operandos de entrada).</span><span class="sxs-lookup"><span data-stu-id="106ae-215">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the precision of the input operands).</span></span>

<span data-ttu-id="106ae-216">Una aplicación podría elegir deliberadamente la precisión para el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="106ae-216">An application might deliberately choose to trade off precision for performance.</span></span> <span data-ttu-id="106ae-217">Hay varios tipos de datos de entrada de sombreador que son candidatos naturales para el procesamiento de precisión parcial:</span><span class="sxs-lookup"><span data-stu-id="106ae-217">There are several kinds of shader input data which are natural candidates for partial precision processing:</span></span>

-   <span data-ttu-id="106ae-218">Los iteradores de color están bien representados por valores de precisión parcial.</span><span class="sxs-lookup"><span data-stu-id="106ae-218">Color iterators are well represented by partial-precision values.</span></span>
-   <span data-ttu-id="106ae-219">Los valores de las texturas de la mayoría de los formatos se pueden representar con precisión mediante valores de precisión parcial (los valores muestreados desde 32 bits, las texturas de formato de punto flotante son una excepción obvia).</span><span class="sxs-lookup"><span data-stu-id="106ae-219">Texture values from most formats can be accurately represented by partial-precision values (values sampled from 32-bit, floating-point format textures are an obvious exception).</span></span>
-   <span data-ttu-id="106ae-220">Las constantes se pueden representar mediante una representación de precisión parcial, según corresponda al sombreador.</span><span class="sxs-lookup"><span data-stu-id="106ae-220">Constants may be represented by partial-precision representation as appropriate to the shader.</span></span>

<span data-ttu-id="106ae-221">En todos estos casos, el desarrollador puede elegir especificar la precisión parcial para procesar los datos, sabiendo que no se pierde la precisión de los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="106ae-221">In all these cases the developer may choose to specify partial precision to process the data, knowing that no input data precision is lost.</span></span> <span data-ttu-id="106ae-222">En algunos casos, es posible que un sombreador requiera que los pasos internos de un cálculo se realicen con precisión completa, incluso cuando los valores de entrada y salida finales no tengan más de una precisión parcial.</span><span class="sxs-lookup"><span data-stu-id="106ae-222">In some cases, a shader may require that the internal steps of a calculation be performed at full precision even when input and final output values do not have more than partial precision.</span></span>

## <a name="software-vertex-and-pixel-shaders"></a><span data-ttu-id="106ae-223">Sombreadores de píxeles y vértices de software</span><span class="sxs-lookup"><span data-stu-id="106ae-223">Software Vertex and Pixel Shaders</span></span>

<span data-ttu-id="106ae-224">Las implementaciones de software (tiempo de ejecución y referencia para los sombreadores de vértices y referencia para los sombreadores de píxeles) de los sombreadores de la versión 2 \_ 0 y versiones posteriores tienen una validación relajada.</span><span class="sxs-lookup"><span data-stu-id="106ae-224">Software implementations (run-time and reference for vertex shaders and reference for pixel shaders) of version 2\_0 shaders and above have some validation relaxed.</span></span> <span data-ttu-id="106ae-225">Esto resulta útil para la depuración y la generación de prototipos.</span><span class="sxs-lookup"><span data-stu-id="106ae-225">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="106ae-226">La aplicación indica al tiempo de ejecución o ensamblador que necesita parte de la validación relajada mediante la \_ marca SW en el ensamblador (por ejemplo, vs \_ 2 \_ SW).</span><span class="sxs-lookup"><span data-stu-id="106ae-226">The application indicates to the runtime/assembler that it needs some of the validation relaxed using the \_sw flag in the assembler (for example, vs\_2\_sw).</span></span> <span data-ttu-id="106ae-227">Un sombreador de software no funcionará con el hardware.</span><span class="sxs-lookup"><span data-stu-id="106ae-227">A software shader will not work with hardware.</span></span>

<span data-ttu-id="106ae-228">vs \_ 2 \_ SW es una flexibilización de los límites máximos de vs \_ 2 \_ x; de forma similar, PS \_ 2 \_ SW es una flexibilización de los límites máximos de PS \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="106ae-228">vs\_2\_sw is a relaxation to the maximum caps of vs\_2\_x; similarly, ps\_2\_sw is a relaxation to the maximum caps of ps\_2\_x.</span></span> <span data-ttu-id="106ae-229">En concreto, se relajan las validaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="106ae-229">Specifically, the following validations are relaxed:</span></span>



|                                            |                                      |                                                                                                                                   |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="106ae-230">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="106ae-230">Shader Model</span></span>                               | <span data-ttu-id="106ae-231">Resource</span><span class="sxs-lookup"><span data-stu-id="106ae-231">Resource</span></span>                             | <span data-ttu-id="106ae-232">Límite</span><span class="sxs-lookup"><span data-stu-id="106ae-232">Limit</span></span>                                                                                                                             |
| <span data-ttu-id="106ae-233">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="106ae-233">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="106ae-234">Recuentos de instrucciones</span><span class="sxs-lookup"><span data-stu-id="106ae-234">Instruction Counts</span></span>                   | <span data-ttu-id="106ae-235">Sin límite</span><span class="sxs-lookup"><span data-stu-id="106ae-235">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="106ae-236">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="106ae-236">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="106ae-237">Registros de constantes Float</span><span class="sxs-lookup"><span data-stu-id="106ae-237">Float Constant Registers</span></span>             | <span data-ttu-id="106ae-238">8192</span><span class="sxs-lookup"><span data-stu-id="106ae-238">8192</span></span>                                                                                                                              |
| <span data-ttu-id="106ae-239">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="106ae-239">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="106ae-240">Registros de constantes de tipo entero</span><span class="sxs-lookup"><span data-stu-id="106ae-240">Integer Constant Registers</span></span>           | <span data-ttu-id="106ae-241">2048</span><span class="sxs-lookup"><span data-stu-id="106ae-241">2048</span></span>                                                                                                                              |
| <span data-ttu-id="106ae-242">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="106ae-242">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="106ae-243">Registros de constantes booleanas</span><span class="sxs-lookup"><span data-stu-id="106ae-243">Boolean Constant Registers</span></span>           | <span data-ttu-id="106ae-244">2048</span><span class="sxs-lookup"><span data-stu-id="106ae-244">2048</span></span>                                                                                                                              |
| <span data-ttu-id="106ae-245">PS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="106ae-245">ps\_2\_sw</span></span>                                  | <span data-ttu-id="106ae-246">Dependiente: profundidad de lectura</span><span class="sxs-lookup"><span data-stu-id="106ae-246">Dependent-read depth</span></span>                 | <span data-ttu-id="106ae-247">Sin límite</span><span class="sxs-lookup"><span data-stu-id="106ae-247">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="106ae-248">vs \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="106ae-248">vs\_2\_sw</span></span>                                  | <span data-ttu-id="106ae-249">instrucciones y etiquetas de control de flujo</span><span class="sxs-lookup"><span data-stu-id="106ae-249">flow control instructions and labels</span></span> | <span data-ttu-id="106ae-250">Sin límite</span><span class="sxs-lookup"><span data-stu-id="106ae-250">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="106ae-251">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="106ae-251">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="106ae-252">Inicio de bucle/pasos/recuentos</span><span class="sxs-lookup"><span data-stu-id="106ae-252">Loop start/step/counts</span></span>               | <span data-ttu-id="106ae-253">El tamaño de paso de iteración y de inicio de la iteración para las instrucciones REP y Loop son enteros de 32 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="106ae-253">Iteration start and iteration step size for rep and loop instructions are 32-bit signed integers.</span></span> <span data-ttu-id="106ae-254">Count puede ser hasta MAX \_ int/64.</span><span class="sxs-lookup"><span data-stu-id="106ae-254">Count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="106ae-255">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="106ae-255">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="106ae-256">Límites de Puerto</span><span class="sxs-lookup"><span data-stu-id="106ae-256">Port limits</span></span>                          | <span data-ttu-id="106ae-257">Los límites de puerto para todos los archivos de registro son relajados.</span><span class="sxs-lookup"><span data-stu-id="106ae-257">Port limits for all register files are relaxed.</span></span>                                                                                   |
| <span data-ttu-id="106ae-258">vs \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="106ae-258">vs\_3\_sw</span></span>                                  | <span data-ttu-id="106ae-259">Número de interpoladores</span><span class="sxs-lookup"><span data-stu-id="106ae-259">Number of interpolators</span></span>              | <span data-ttu-id="106ae-260">16 registros de salida en vs \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="106ae-260">16 output registers in vs\_3\_sw.</span></span>                                                                                                 |
| <span data-ttu-id="106ae-261">PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="106ae-261">ps\_3\_sw</span></span>                                  | <span data-ttu-id="106ae-262">Número de interpoladores</span><span class="sxs-lookup"><span data-stu-id="106ae-262">Number of interpolators</span></span>              | <span data-ttu-id="106ae-263">14 (16-2) registros de entrada para el \_ SW PS 3 \_ .</span><span class="sxs-lookup"><span data-stu-id="106ae-263">14(16-2) input registers for ps\_3\_sw.</span></span>                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="106ae-264">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="106ae-264">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="106ae-265">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="106ae-265">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
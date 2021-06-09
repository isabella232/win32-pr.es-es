---
title: Modelo de sombreador 3 (referencia hlsl)
description: Los sombreadores de vértices y los sombreadores de píxeles se simplifican considerablemente a partir de versiones anteriores del sombreador.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d87c791694e91de135052b4172e3bd5f55577d7
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827104"
---
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="35434-103">Modelo de sombreador 3 (referencia hlsl)</span><span class="sxs-lookup"><span data-stu-id="35434-103">Shader model 3 (HLSL reference)</span></span>

<span data-ttu-id="35434-104">Los sombreadores de vértices y los sombreadores de píxeles se simplifican considerablemente a partir de versiones anteriores del sombreador.</span><span class="sxs-lookup"><span data-stu-id="35434-104">Vertex shaders and pixel shaders are simplified considerably from earlier shader versions.</span></span> <span data-ttu-id="35434-105">Si va a implementar sombreadores en hardware, es posible que no use vs \_ 3 0 o \_ ps \_ 3 0 con ninguna otra versión del sombreador, y no puede usar ningún tipo de sombreador con la canalización de función \_ fija.</span><span class="sxs-lookup"><span data-stu-id="35434-105">If you are implementing shaders in hardware, you may not use vs\_3\_0 or ps\_3\_0 with any other shader versions, and you may not use either shader type with the fixed function pipeline.</span></span> <span data-ttu-id="35434-106">Estos cambios hacen posible simplificar los controladores y el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="35434-106">These changes make it possible to simplify drivers and the runtime.</span></span> <span data-ttu-id="35434-107">La única excepción es que los sombreadores de solo software frente a 3 0 se pueden \_ usar con cualquier versión del \_ sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="35434-107">The only exception is that software-only vs\_3\_0 shaders may be used with any pixel shader version.</span></span> <span data-ttu-id="35434-108">Además, si usa un sombreador solo de software frente a 3 0 con una versión anterior del sombreador de píxeles, el sombreador de vértices solo puede usar semántica de salida compatible con códigos de formato de vértice \_ \_ flexible (FVF).</span><span class="sxs-lookup"><span data-stu-id="35434-108">In addition, if you are using a software-only vs\_3\_0 shader with a previous pixel shader version, the vertex shader can only use output semantics that are compatible with flexible vertex format (FVF) codes.</span></span>

<span data-ttu-id="35434-109">La semántica usada en las salidas del sombreador de vértices debe usarse en las entradas del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="35434-109">The semantics used on vertex shader outputs must be used on pixel shader inputs.</span></span> <span data-ttu-id="35434-110">La semántica se usa para asignar las salidas del sombreador de vértices a las entradas del sombreador de píxeles, de forma similar a la forma en que la declaración de vértice se asigna a los registros de entrada del sombreador de vértices y a los modelos de sombreador anteriores.</span><span class="sxs-lookup"><span data-stu-id="35434-110">The semantics are used to map the vertex shader outputs to the pixel shader inputs, similar to the way the vertex declaration is mapped to the vertex shader input registers and previous shader models.</span></span> <span data-ttu-id="35434-111">Consulte Match Semantics on vs 3.0 and ps 3.0 Shaders (Semántica de coincidencias en los sombreadores de vs 3.0 y ps 3.0).</span><span class="sxs-lookup"><span data-stu-id="35434-111">See Match Semantics on vs 3.0 and ps 3.0 Shaders.</span></span>

<span data-ttu-id="35434-112">Se han agregado estados de representación de modo de encapsulado adicionales para cubrir la posibilidad de coordenadas de textura adicionales en este nuevo esquema.</span><span class="sxs-lookup"><span data-stu-id="35434-112">Additional wrap mode render states have been added to cover the possibility of additional texture coordinates in this new scheme.</span></span> <span data-ttu-id="35434-113">Los atributos con D3DDECLUSAGE TEXCOORD y el índice de uso de 0 a 15 se interpolan en modo de encapsulado cuando se establece el wrap \_ [**\_ \* D3DRS**](/windows/desktop/direct3d9/d3drenderstatetype) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="35434-113">Attributes with D3DDECLUSAGE\_TEXCOORD and usage index from 0 to 15 are interpolated in wrap mode when the corresponding [**D3DRS\_WRAP\***](/windows/desktop/direct3d9/d3drenderstatetype) is set.</span></span>

-   [<span data-ttu-id="35434-114">Características del modelo 3 del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="35434-114">Vertex Shader Model 3 Features</span></span>](#vertex-shader-model-3-features)
-   [<span data-ttu-id="35434-115">Características del modelo 3 del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="35434-115">Pixel Shader Model 3 Features</span></span>](#pixel-shader-model-3-features)
-   [<span data-ttu-id="35434-116">Semántica de coincidencias en \_ sombreadores frente a 3 \_ 0 y ps \_ \_ 3 0</span><span class="sxs-lookup"><span data-stu-id="35434-116">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>](/windows)
-   [<span data-ttu-id="35434-117">Cambios en el modo de sombreado, profundidad y profundidad</span><span class="sxs-lookup"><span data-stu-id="35434-117">Fog, Depth, and Shading Mode Changes</span></span>](#fog-depth-and-shading-mode-changes)
-   [<span data-ttu-id="35434-118">Conversiones de punto flotante y entero</span><span class="sxs-lookup"><span data-stu-id="35434-118">Floating Point and Integer Conversions</span></span>](#floating-point-and-integer-conversions)
-   [<span data-ttu-id="35434-119">Especificar precisión completa o parcial</span><span class="sxs-lookup"><span data-stu-id="35434-119">Specifying Full or Partial Precision</span></span>](#specifying-full-or-partial-precision)
-   [<span data-ttu-id="35434-120">Sombreadores de vértices y píxeles de software</span><span class="sxs-lookup"><span data-stu-id="35434-120">Software Vertex and Pixel Shaders</span></span>](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a><span data-ttu-id="35434-121">Características del modelo 3 del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="35434-121">Vertex Shader Model 3 Features</span></span>

<span data-ttu-id="35434-122">Los tipos de registro de salida del sombreador de vértices se han contraído en doce registros (vea [Registros de salida).](dx9-graphics-reference-asm-vs-registers-output.md)</span><span class="sxs-lookup"><span data-stu-id="35434-122">The vertex shader output register types have been collapsed into twelve registers (see [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)).</span></span> <span data-ttu-id="35434-123">Cada registro que se usa debe declararse mediante la instrucción [dcl](dcl-usage---ps.md) y una semántica (por ejemplo, dcl \_ color0 o0.xyzw).</span><span class="sxs-lookup"><span data-stu-id="35434-123">Each register that is used needs to be declared using the [dcl](dcl-usage---ps.md) instruction and a semantic (for example, dcl\_color0 o0.xyzw).</span></span>

<span data-ttu-id="35434-124">El modelo de sombreador de \_ vértices 3 0 (frente a 3 0) se expande en las características de frente a 2 0 con una indexación de registros más eficaz, un conjunto de registros de salida simplificados, la capacidad de muestrear una textura en un sombreador de vértices y la capacidad de controlar la velocidad a la que se inicializan las entradas del \_ \_ \_ \_ sombreador.</span><span class="sxs-lookup"><span data-stu-id="35434-124">The 3\_0 vertex shader model (vs\_3\_0) expands on the features of vs\_2\_0 with more powerful register indexing, a set of simplified output registers, the ability to sample a texture in a vertex shader, and the ability to control the rate at which shader inputs are initialized.</span></span>

### <a name="index-any-register"></a><span data-ttu-id="35434-125">Indexar cualquier registro</span><span class="sxs-lookup"><span data-stu-id="35434-125">Index Any Register</span></span>

<span data-ttu-id="35434-126">Todos los registros [(registros de](dx9-graphics-reference-asm-vs-registers-input.md) entrada y de [salida)](dx9-graphics-reference-asm-vs-registers-output.md)se pueden indexar mediante el registro de contadores de [bucles](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (solo los registros constantes se podían indexar en versiones anteriores).</span><span class="sxs-lookup"><span data-stu-id="35434-126">All registers( [Input Register](dx9-graphics-reference-asm-vs-registers-input.md) and [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)) can be indexed using [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (only constant registers could be indexed in earlier versions.)</span></span>

<span data-ttu-id="35434-127">Debe declarar los registros de entrada y salida antes de indexarlos.</span><span class="sxs-lookup"><span data-stu-id="35434-127">You must declare input and output registers before indexing them.</span></span> <span data-ttu-id="35434-128">Sin embargo, no puede indexar ningún registro de salida que se haya declarado con una semántica de tamaño de punto o posición.</span><span class="sxs-lookup"><span data-stu-id="35434-128">However, you may not index any output register that has been declared with a position or point size semantic.</span></span> <span data-ttu-id="35434-129">De hecho, si se usa la indexación, la semántica de la posición y el tamaño psize deben declararse en los registros o0 y o1 respectivamente.</span><span class="sxs-lookup"><span data-stu-id="35434-129">In fact, if indexing is used the position and psize semantics have to be declared in the o0 and o1 registers respectively.</span></span>

<span data-ttu-id="35434-130">Solo puede indexar un intervalo continuo de registros. es decir, no se puede indexar entre registros que no se han declarado.</span><span class="sxs-lookup"><span data-stu-id="35434-130">You are only allowed to index a continuous range of registers; that is, you cannot index across registers that have not been declared.</span></span> <span data-ttu-id="35434-131">Aunque esta restricción puede ser inconveniente, permite que se lleve a cabo la optimización del hardware.</span><span class="sxs-lookup"><span data-stu-id="35434-131">While this restriction may be inconvenient, it permits hardware optimization to take place.</span></span> <span data-ttu-id="35434-132">Si se intenta indexar entre registros no contiguos, se producirán resultados no definidos.</span><span class="sxs-lookup"><span data-stu-id="35434-132">Attempting to index across non-contiguous registers will produce undefined results.</span></span> <span data-ttu-id="35434-133">La validación del sombreador no aplica esta restricción.</span><span class="sxs-lookup"><span data-stu-id="35434-133">Shader validation does not enforce this restriction.</span></span>

### <a name="simplify-output-registers"></a><span data-ttu-id="35434-134">Simplificación de los registros de salida</span><span class="sxs-lookup"><span data-stu-id="35434-134">Simplify Output Registers</span></span>

<span data-ttu-id="35434-135">Todos los distintos tipos de registros de salida se han contraído en doce registros de salida: 1 para la posición, 2 para el color, 8 para la textura y 1 para el tamaño de punto o de color.</span><span class="sxs-lookup"><span data-stu-id="35434-135">All the various types of output registers have been collapsed into twelve output registers: 1 for position, 2 for color, 8 for texture, and 1 for fog or point size.</span></span> <span data-ttu-id="35434-136">Estos registros interpolarán los datos que contengan para el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="35434-136">These registers will interpolate any data they contain for the pixel shader.</span></span> <span data-ttu-id="35434-137">Las declaraciones de registro de salida son necesarias y la semántica se asigna a cada registro.</span><span class="sxs-lookup"><span data-stu-id="35434-137">Output register declarations are required and semantics are assigned to each register.</span></span>

<span data-ttu-id="35434-138">Los registros se pueden desglosar de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="35434-138">The registers can be broken down as follows:</span></span>

-   <span data-ttu-id="35434-139">Al menos un registro debe declararse como un registro de posición de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="35434-139">At least one register must be declared as a four-component position register.</span></span> <span data-ttu-id="35434-140">Este es el único registro de sombreador de vértices necesario.</span><span class="sxs-lookup"><span data-stu-id="35434-140">This is the only vertex shader register that is required.</span></span>
-   <span data-ttu-id="35434-141">Los diez primeros registros consumidos por un sombreador pueden usar hasta cuatro componentes (xyzw) como máximo.</span><span class="sxs-lookup"><span data-stu-id="35434-141">The first ten registers consumed by a shader may use up to four components (xyzw) maximum.</span></span>
-   <span data-ttu-id="35434-142">El último registro (o duodécimo) solo puede contener un valor escalar (como el tamaño de punto).</span><span class="sxs-lookup"><span data-stu-id="35434-142">The last (or twelfth) register may only contain a scalar (such as point size).</span></span>

<span data-ttu-id="35434-143">Para obtener una lista de los registros, vea [Registros- frente \_ a \_ 3 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="35434-143">For a listing of the registers, see [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>

### <a name="texture-sample-in-a-vertex-shader"></a><span data-ttu-id="35434-144">Muestra de textura en un sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="35434-144">Texture Sample in a Vertex Shader</span></span>

<span data-ttu-id="35434-145">El sombreador de \_ vértices 3 0 admite la búsqueda de textura en el sombreador de vértices [mediante texldl- frente a](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="35434-145">Vertex shader 3\_0 supports texture lookup in the vertex shader using [texldl - vs](texldl---vs.md).</span></span>

## <a name="pixel-shader-model-3-features"></a><span data-ttu-id="35434-146">Características del modelo 3 del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="35434-146">Pixel Shader Model 3 Features</span></span>

<span data-ttu-id="35434-147">El color del sombreador de píxeles y los registros de textura se han contraído en diez registros de entrada (vea [Input Register Types](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span><span class="sxs-lookup"><span data-stu-id="35434-147">The pixel shader color and texture registers have been collapsed into ten input registers (see [Input Register Types](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span></span> <span data-ttu-id="35434-148">Face Register es un registro escalar de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="35434-148">The Face Register is a floating point scalar register.</span></span> <span data-ttu-id="35434-149">Solo el signo de este registro es válido.</span><span class="sxs-lookup"><span data-stu-id="35434-149">Only the sign of this register is valid.</span></span> <span data-ttu-id="35434-150">Si el signo es negativo, la primitiva es una cara posterior.</span><span class="sxs-lookup"><span data-stu-id="35434-150">If the sign is negative the primitive is a back face.</span></span> <span data-ttu-id="35434-151">Esto se puede usar dentro de un sombreador de píxeles para lograr una iluminación de dos lados, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="35434-151">This can be used inside a pixel shader to achieve two-sided lighting, for instance.</span></span> <span data-ttu-id="35434-152">El registro de posición hace referencia a los píxeles actuales (x,y).</span><span class="sxs-lookup"><span data-stu-id="35434-152">The Position Register references the current (x,y) pixels.</span></span>

<span data-ttu-id="35434-153">Los registros constantes del sombreador se pueden establecer mediante:</span><span class="sxs-lookup"><span data-stu-id="35434-153">The shader constant registers can be set using:</span></span>

-   [<span data-ttu-id="35434-154">**SetPixelShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="35434-154">**SetPixelShaderConstantB**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [<span data-ttu-id="35434-155">**SetPixelShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="35434-155">**SetPixelShaderConstantI**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [<span data-ttu-id="35434-156">**SetPixelShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="35434-156">**SetPixelShaderConstantF**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a><span data-ttu-id="35434-157">Semántica de coincidencias en \_ sombreadores frente a 3 \_ 0 y ps \_ \_ 3 0</span><span class="sxs-lookup"><span data-stu-id="35434-157">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>

<span data-ttu-id="35434-158">Hay algunas restricciones en el uso semántico con frente \_ a 3 \_ 0 y ps \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="35434-158">There are some restrictions on semantic usage with vs\_3\_0 and ps\_3\_0.</span></span> <span data-ttu-id="35434-159">En general, debe tener cuidado al usar una semántica para una entrada de sombreador que coincida con una semántica usada en una salida del sombreador.</span><span class="sxs-lookup"><span data-stu-id="35434-159">In general, you need to be careful when using a semantic for a shader input that matches a semantic used on a shader output.</span></span>

<span data-ttu-id="35434-160">Por ejemplo, este sombreador de píxeles empaqueta varios nombres en un solo registro:</span><span class="sxs-lookup"><span data-stu-id="35434-160">For instance, this pixel shader packs multiple names into one register:</span></span>


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



<span data-ttu-id="35434-161">Cada registro tiene una semántica diferente.</span><span class="sxs-lookup"><span data-stu-id="35434-161">Each register has a different semantic.</span></span> <span data-ttu-id="35434-162">Tenga en cuenta que también puede nombrar v0.x y v0.yz con una semántica diferente (múltiple) debido al uso de la máscara de escritura.</span><span class="sxs-lookup"><span data-stu-id="35434-162">Notice that you can also name v0.x and v0.yz with different (multiple) semantics because of the use of the write mask.</span></span>

<span data-ttu-id="35434-163">Dado el sombreador de píxeles, el siguiente sombreador frente \_ a 3 0 no se puede \_ emparejar con él:</span><span class="sxs-lookup"><span data-stu-id="35434-163">Given the pixel shader, the following vs\_3\_0 shader cannot be paired with it:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



<span data-ttu-id="35434-164">Estos dos sombreadores están en conflicto con su uso de la semántica [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) y **D3DDECLUSAGE \_ TEXCOORD1.**</span><span class="sxs-lookup"><span data-stu-id="35434-164">These two shaders conflict with their use of the [**D3DDECLUSAGE\_TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) And **D3DDECLUSAGE\_TEXCOORD1** semantics.</span></span>

<span data-ttu-id="35434-165">Vuelva a escribir el sombreador de vértices de esta forma para evitar la colisión semántica:</span><span class="sxs-lookup"><span data-stu-id="35434-165">Rewrite the vertex shader like this to avoid the semantic collision:</span></span>


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



<span data-ttu-id="35434-166">Del mismo modo, un nombre semántico declarado en distintos registros de entrada en el sombreador de píxeles (v0 y v1 en el sombreador de píxeles) no se puede usar en un único registro de salida en este sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="35434-166">Similarly, a semantic name declared on different input registers in the pixel shader (v0 and v1 in the pixel shader) cannot be used in a single output register in this vertex shader.</span></span> <span data-ttu-id="35434-167">Por ejemplo, este sombreador de vértices no se puede emparejar con el sombreador de píxeles porque D3DDECLUSAGE TEXCOORD1 se usa para los registros de entrada del sombreador de píxeles (v0, v1) y el registro de salida del sombreador de \_ vértices o3.</span><span class="sxs-lookup"><span data-stu-id="35434-167">For instance, this vertex shader cannot be paired with the pixel shader because D3DDECLUSAGE\_TEXCOORD1 is used for both pixel shader input registers (v0, v1) and the vertex shader output register o3.</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



<span data-ttu-id="35434-168">Por otro lado, este sombreador de vértices no se puede emparejar con el sombreador de píxeles porque la máscara de salida de un parámetro con una semántica determinada no proporciona los datos solicitados por el sombreador de píxeles:</span><span class="sxs-lookup"><span data-stu-id="35434-168">On the other hand, this vertex shader cannot be paired with the pixel shader because the output mask for a parameter with a given semantic does not provide the data that is requested by the pixel shader:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



<span data-ttu-id="35434-169">Este sombreador de vértices no proporciona una salida con uno de los nombres semánticos solicitados por el sombreador de píxeles, por lo que el emparejamiento del sombreador no es válido:</span><span class="sxs-lookup"><span data-stu-id="35434-169">This vertex shader does not provide an output with one of the semantic names requested by the pixel shader, so the shader pairing is invalid:</span></span>


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



## <a name="fog-depth-and-shading-mode-changes"></a><span data-ttu-id="35434-170">Cambios en el modo de sombreado, profundidad y profundidad</span><span class="sxs-lookup"><span data-stu-id="35434-170">Fog, Depth, and Shading Mode Changes</span></span>

<span data-ttu-id="35434-171">Cuando D3DRS SHADEMODE se establece para sombreado plano durante el recorte y la rasterización de triángulos, los atributos con \_ color D3DDECLUSAGE se interpolan como \_ sombreado plano.</span><span class="sxs-lookup"><span data-stu-id="35434-171">When D3DRS\_SHADEMODE is set for flat shading during clipping and triangle rasterization, attributes with D3DDECLUSAGE\_COLOR are interpolated as flat shaded.</span></span> <span data-ttu-id="35434-172">Si algún componente de un registro se declara con una semántica de color pero a otros componentes del mismo registro se les da una semántica diferente, la interpolación de sombreado plano (lineal frente a plana) no se definirá en los componentes de ese registro sin una semántica de color.</span><span class="sxs-lookup"><span data-stu-id="35434-172">If any components of a register are declared with a color semantic but other components of the same register are given different semantics, flat shading interpolation (linear vs. flat) will be undefined on the components in that register without a color semantic.</span></span>

<span data-ttu-id="35434-173">Si se desea la representación en forma de nube, frente a \_ 3 \_ 0 y ps \_ 3 \_ 0, los sombreadores deben implementar el sombreador.</span><span class="sxs-lookup"><span data-stu-id="35434-173">If fog rendering is desired, vs\_3\_0 and ps\_3\_0 shaders must implement fog.</span></span> <span data-ttu-id="35434-174">No se realizan cálculos de cálculo fuera de los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="35434-174">No fog calculations are done outside of the shaders.</span></span> <span data-ttu-id="35434-175">No hay ningún registro en comparación con 3 0, y se han agregado semánticas adicionales D3DDECLUSAGE PHP (para el factor de fusión calculado por vértice) y \_ \_ \_ D3DDECLUSAGE \_ DEPTH (para pasar un valor de profundidad al sombreador de píxeles para calcular el factor de mezcla de mezcla).</span><span class="sxs-lookup"><span data-stu-id="35434-175">There is no fog register in vs\_3\_0, and additional semantics D3DDECLUSAGE\_FOG (for fog blend factor computed per vertex) and D3DDECLUSAGE\_DEPTH (for passing in a depth value to the pixel shader to compute the fog blend factor) have been added.</span></span>

<span data-ttu-id="35434-176">El estado de la fase de textura D3DTSS TEXCOORDINDEX se omite cuando se usa el \_ sombreador de píxeles 3.0.</span><span class="sxs-lookup"><span data-stu-id="35434-176">Texture stage state D3DTSS\_TEXCOORDINDEX is ignored when using pixel shader 3.0.</span></span>

<span data-ttu-id="35434-177">Se han agregado los siguientes valores para dar cabida a estos cambios:</span><span class="sxs-lookup"><span data-stu-id="35434-177">The following values have been added to accommodate these changes:</span></span>


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



## <a name="floating-point-and-integer-conversions"></a><span data-ttu-id="35434-178">Conversiones de punto flotante y entero</span><span class="sxs-lookup"><span data-stu-id="35434-178">Floating Point and Integer Conversions</span></span>

<span data-ttu-id="35434-179">Las matemáticas de punto flotante se produce con diferentes precisións e intervalos (16 bits, 24 bits y 32 bits) en diferentes partes de la canalización.</span><span class="sxs-lookup"><span data-stu-id="35434-179">Floating point math happens at different precision and ranges (16-bit, 24-bit, and 32-bit) in different parts of the pipeline.</span></span> <span data-ttu-id="35434-180">Un valor mayor que el intervalo dinámico de la canalización que entra en esa canalización (por ejemplo, un mapa de textura float de 32 bits se muestrea en una canalización float de 24 bits en ps 2 0) crea un resultado \_ indefinido. \_</span><span class="sxs-lookup"><span data-stu-id="35434-180">A value greater than the dynamic range of the pipeline that enters that pipeline (for example, a 32-bit float texture map is sampled into a 24-bit float pipeline in ps\_2\_0) creates an undefined result.</span></span> <span data-ttu-id="35434-181">Para un comportamiento predecible, debe fijar este valor al máximo del intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="35434-181">For predictable behavior, you should clamp such a value to the dynamic range maximum.</span></span>

<span data-ttu-id="35434-182">La conversión de un valor de punto flotante a un entero se produce en varios lugares, como:</span><span class="sxs-lookup"><span data-stu-id="35434-182">Conversion from a floating point value to an integer happens in several places such as:</span></span>

-   <span data-ttu-id="35434-183">Al encontrar una [mova : vs](mova---vs.md) instrucción.</span><span class="sxs-lookup"><span data-stu-id="35434-183">When encountering a [mova - vs](mova---vs.md) instruction.</span></span>
-   <span data-ttu-id="35434-184">Durante el direccionamiento de textura.</span><span class="sxs-lookup"><span data-stu-id="35434-184">During texture addressing.</span></span>
-   <span data-ttu-id="35434-185">Al escribir en un destino de representación de punto no flotante.</span><span class="sxs-lookup"><span data-stu-id="35434-185">When writing out to a non-floating point render target.</span></span>

## <a name="specifying-full-or-partial-precision"></a><span data-ttu-id="35434-186">Especificar precisión completa o parcial</span><span class="sxs-lookup"><span data-stu-id="35434-186">Specifying Full or Partial Precision</span></span>

<span data-ttu-id="35434-187">Tanto ps \_ 3 \_ 0 como ps \_ 2 \_ x proporcionan compatibilidad con dos niveles de precisión:</span><span class="sxs-lookup"><span data-stu-id="35434-187">Both ps\_3\_0 and ps\_2\_x provide support for two levels of precision:</span></span>



| <span data-ttu-id="35434-188">ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="35434-188">ps\_3\_0</span></span> | <span data-ttu-id="35434-189">ps \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="35434-189">ps\_2\_0</span></span> | <span data-ttu-id="35434-190">Precision</span><span class="sxs-lookup"><span data-stu-id="35434-190">Precision</span></span>         | <span data-ttu-id="35434-191">Valor</span><span class="sxs-lookup"><span data-stu-id="35434-191">Value</span></span>                |
|----------|----------|-------------------|----------------------|
| <span data-ttu-id="35434-192">x</span><span class="sxs-lookup"><span data-stu-id="35434-192">x</span></span>        |          | <span data-ttu-id="35434-193">Completo</span><span class="sxs-lookup"><span data-stu-id="35434-193">Full</span></span>              | <span data-ttu-id="35434-194">fp32 o superior</span><span class="sxs-lookup"><span data-stu-id="35434-194">fp32 or higher</span></span>       |
| <span data-ttu-id="35434-195">x</span><span class="sxs-lookup"><span data-stu-id="35434-195">x</span></span>        |          | <span data-ttu-id="35434-196">Precisión parcial</span><span class="sxs-lookup"><span data-stu-id="35434-196">Partial precision</span></span> | <span data-ttu-id="35434-197">fp16=s10e5</span><span class="sxs-lookup"><span data-stu-id="35434-197">fp16=s10e5</span></span>           |
| <span data-ttu-id="35434-198">x</span><span class="sxs-lookup"><span data-stu-id="35434-198">x</span></span>        | <span data-ttu-id="35434-199">x</span><span class="sxs-lookup"><span data-stu-id="35434-199">x</span></span>        | <span data-ttu-id="35434-200">Completo</span><span class="sxs-lookup"><span data-stu-id="35434-200">Full</span></span>              | <span data-ttu-id="35434-201">fp24=s16e7 o superior</span><span class="sxs-lookup"><span data-stu-id="35434-201">fp24=s16e7 or higher</span></span> |
| <span data-ttu-id="35434-202">x</span><span class="sxs-lookup"><span data-stu-id="35434-202">x</span></span>        | <span data-ttu-id="35434-203">x</span><span class="sxs-lookup"><span data-stu-id="35434-203">x</span></span>        | <span data-ttu-id="35434-204">Precisión parcial</span><span class="sxs-lookup"><span data-stu-id="35434-204">Partial precision</span></span> | <span data-ttu-id="35434-205">fp16=s10e5</span><span class="sxs-lookup"><span data-stu-id="35434-205">fp16=s10e5</span></span>           |



 

<span data-ttu-id="35434-206">ps \_ 3 \_ 0 admite más precisión que ps \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="35434-206">ps\_3\_0 supports more precision than ps\_2\_0 does.</span></span> <span data-ttu-id="35434-207">De forma predeterminada, todas las operaciones se producen en el nivel de precisión completa.</span><span class="sxs-lookup"><span data-stu-id="35434-207">By default, all operations occur at the full precision level.</span></span>

<span data-ttu-id="35434-208">La precisión parcial (consulte [Modificadores de](dx9-graphics-reference-asm-ps-registers-modifiers.md)registro del sombreador de píxeles) se solicita agregando el modificador pp al código del sombreador (siempre que la \_ implementación subyacente lo admita).</span><span class="sxs-lookup"><span data-stu-id="35434-208">Partial precision (see [Pixel Shader Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md)) is requested by adding the \_pp modifier to shader code (provided that the underlying implementation supports it).</span></span> <span data-ttu-id="35434-209">Las implementaciones siempre son libres de omitir el modificador y realizar las operaciones afectadas con precisión completa.</span><span class="sxs-lookup"><span data-stu-id="35434-209">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="35434-210">El \_ modificador pp puede producirse en dos contextos:</span><span class="sxs-lookup"><span data-stu-id="35434-210">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="35434-211">En una declaración de coordenada de textura para pasar coordenadas de textura de precisión parcial al sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="35434-211">On a texture coordinate declaration to pass partial-precision texture coordinates to the pixel shader.</span></span> <span data-ttu-id="35434-212">Esto se puede usar cuando la textura coordina los datos de color de retransmisión al sombreador de píxeles, que puede ser más rápido con precisión parcial que con precisión completa en algunas implementaciones.</span><span class="sxs-lookup"><span data-stu-id="35434-212">This could be used when texture coordinates relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span>
-   <span data-ttu-id="35434-213">En cualquier instrucción para solicitar el uso de precisión parcial, incluidas las instrucciones de carga de textura.</span><span class="sxs-lookup"><span data-stu-id="35434-213">On any instruction to request the use of partial precision, including texture load instructions.</span></span> <span data-ttu-id="35434-214">Esto indica que la implementación puede ejecutar la instrucción con precisión parcial y almacenar un resultado de precisión parcial.</span><span class="sxs-lookup"><span data-stu-id="35434-214">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial-precision result.</span></span> <span data-ttu-id="35434-215">En ausencia de un modificador explícito, la instrucción debe realizarse con precisión completa (independientemente de la precisión de los operandos de entrada).</span><span class="sxs-lookup"><span data-stu-id="35434-215">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the precision of the input operands).</span></span>

<span data-ttu-id="35434-216">Una aplicación podría elegir deliberadamente cambiar la precisión por el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="35434-216">An application might deliberately choose to trade off precision for performance.</span></span> <span data-ttu-id="35434-217">Hay varios tipos de datos de entrada de sombreador que son candidatos naturales para el procesamiento de precisión parcial:</span><span class="sxs-lookup"><span data-stu-id="35434-217">There are several kinds of shader input data which are natural candidates for partial precision processing:</span></span>

-   <span data-ttu-id="35434-218">Los iteradores de color están bien representados por valores de precisión parcial.</span><span class="sxs-lookup"><span data-stu-id="35434-218">Color iterators are well represented by partial-precision values.</span></span>
-   <span data-ttu-id="35434-219">Los valores de textura de la mayoría de los formatos se pueden representar con precisión mediante valores de precisión parcial (los valores muestreados de texturas de formato de punto flotante de 32 bits son una excepción obvia).</span><span class="sxs-lookup"><span data-stu-id="35434-219">Texture values from most formats can be accurately represented by partial-precision values (values sampled from 32-bit, floating-point format textures are an obvious exception).</span></span>
-   <span data-ttu-id="35434-220">Las constantes se pueden representar mediante una representación de precisión parcial según corresponda para el sombreador.</span><span class="sxs-lookup"><span data-stu-id="35434-220">Constants may be represented by partial-precision representation as appropriate to the shader.</span></span>

<span data-ttu-id="35434-221">En todos estos casos, el desarrollador puede optar por especificar una precisión parcial para procesar los datos, sabiendo que no se pierde ninguna precisión de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="35434-221">In all these cases the developer may choose to specify partial precision to process the data, knowing that no input data precision is lost.</span></span> <span data-ttu-id="35434-222">En algunos casos, un sombreador puede requerir que los pasos internos de un cálculo se realicen con precisión completa, incluso cuando los valores de entrada y salida final no tienen más de precisión parcial.</span><span class="sxs-lookup"><span data-stu-id="35434-222">In some cases, a shader may require that the internal steps of a calculation be performed at full precision even when input and final output values do not have more than partial precision.</span></span>

## <a name="software-vertex-and-pixel-shaders"></a><span data-ttu-id="35434-223">Sombreadores de vértices y píxeles de software</span><span class="sxs-lookup"><span data-stu-id="35434-223">Software Vertex and Pixel Shaders</span></span>

<span data-ttu-id="35434-224">Las implementaciones de software (tiempo de ejecución y referencia para sombreadores de vértices y referencia para sombreadores de píxeles) de los sombreadores de la versión 2 0 y posteriores tienen cierta validación \_ relajada.</span><span class="sxs-lookup"><span data-stu-id="35434-224">Software implementations (run-time and reference for vertex shaders and reference for pixel shaders) of version 2\_0 shaders and above have some validation relaxed.</span></span> <span data-ttu-id="35434-225">Esto es útil para fines de depuración y creación de prototipos.</span><span class="sxs-lookup"><span data-stu-id="35434-225">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="35434-226">La aplicación indica al runtime o ensamblador que necesita parte de la validación relajada mediante la marca sw en el \_ ensamblador (por ejemplo, frente a \_ 2 \_ sw).</span><span class="sxs-lookup"><span data-stu-id="35434-226">The application indicates to the runtime/assembler that it needs some of the validation relaxed using the \_sw flag in the assembler (for example, vs\_2\_sw).</span></span> <span data-ttu-id="35434-227">Un sombreador de software no funcionará con hardware.</span><span class="sxs-lookup"><span data-stu-id="35434-227">A software shader will not work with hardware.</span></span>

<span data-ttu-id="35434-228">vs 2 sw es una relajación a los límites máximos de frente a 2 x; de forma similar, ps 2 sw es una relajación hasta los \_ \_ límites máximos de ps \_ \_ \_ \_ \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="35434-228">vs\_2\_sw is a relaxation to the maximum caps of vs\_2\_x; similarly, ps\_2\_sw is a relaxation to the maximum caps of ps\_2\_x.</span></span> <span data-ttu-id="35434-229">En concreto, las validaciones siguientes son relajadas:</span><span class="sxs-lookup"><span data-stu-id="35434-229">Specifically, the following validations are relaxed:</span></span>



| <span data-ttu-id="35434-230">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="35434-230">Shader model</span></span>                                           |  <span data-ttu-id="35434-231">Recurso</span><span class="sxs-lookup"><span data-stu-id="35434-231">Resource</span></span>                                    |  <span data-ttu-id="35434-232">Límite</span><span class="sxs-lookup"><span data-stu-id="35434-232">Limit</span></span>                                                                                                                                  |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35434-233">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="35434-233">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="35434-234">Recuentos de instrucciones</span><span class="sxs-lookup"><span data-stu-id="35434-234">Instruction Counts</span></span>                   | <span data-ttu-id="35434-235">Sin límite</span><span class="sxs-lookup"><span data-stu-id="35434-235">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="35434-236">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="35434-236">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="35434-237">Registros de constantes float</span><span class="sxs-lookup"><span data-stu-id="35434-237">Float Constant Registers</span></span>             | <span data-ttu-id="35434-238">8192</span><span class="sxs-lookup"><span data-stu-id="35434-238">8192</span></span>                                                                                                                              |
| <span data-ttu-id="35434-239">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="35434-239">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="35434-240">Registros constantes enteros</span><span class="sxs-lookup"><span data-stu-id="35434-240">Integer Constant Registers</span></span>           | <span data-ttu-id="35434-241">2048</span><span class="sxs-lookup"><span data-stu-id="35434-241">2048</span></span>                                                                                                                              |
| <span data-ttu-id="35434-242">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="35434-242">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="35434-243">Registros de constantes booleanos</span><span class="sxs-lookup"><span data-stu-id="35434-243">Boolean Constant Registers</span></span>           | <span data-ttu-id="35434-244">2048</span><span class="sxs-lookup"><span data-stu-id="35434-244">2048</span></span>                                                                                                                              |
| <span data-ttu-id="35434-245">ps \_ 2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="35434-245">ps\_2\_sw</span></span>                                  | <span data-ttu-id="35434-246">Profundidad de lectura dependiente</span><span class="sxs-lookup"><span data-stu-id="35434-246">Dependent-read depth</span></span>                 | <span data-ttu-id="35434-247">Sin límite</span><span class="sxs-lookup"><span data-stu-id="35434-247">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="35434-248">vs \_ 2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="35434-248">vs\_2\_sw</span></span>                                  | <span data-ttu-id="35434-249">etiquetas y instrucciones de control de flujo</span><span class="sxs-lookup"><span data-stu-id="35434-249">flow control instructions and labels</span></span> | <span data-ttu-id="35434-250">Sin límite</span><span class="sxs-lookup"><span data-stu-id="35434-250">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="35434-251">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="35434-251">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="35434-252">Inicio,paso/recuentos de bucles</span><span class="sxs-lookup"><span data-stu-id="35434-252">Loop start/step/counts</span></span>               | <span data-ttu-id="35434-253">El tamaño del paso de inicio e iteración de iteración para las instrucciones de repetición y bucle son enteros de 32 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="35434-253">Iteration start and iteration step size for rep and loop instructions are 32-bit signed integers.</span></span> <span data-ttu-id="35434-254">El recuento puede ser de hasta MAX \_ INT/64.</span><span class="sxs-lookup"><span data-stu-id="35434-254">Count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="35434-255">vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="35434-255">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="35434-256">Límites de puerto</span><span class="sxs-lookup"><span data-stu-id="35434-256">Port limits</span></span>                          | <span data-ttu-id="35434-257">Los límites de puerto para todos los archivos de registro son relajadas.</span><span class="sxs-lookup"><span data-stu-id="35434-257">Port limits for all register files are relaxed.</span></span>                                                                                   |
| <span data-ttu-id="35434-258">vs \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="35434-258">vs\_3\_sw</span></span>                                  | <span data-ttu-id="35434-259">Número de interpoladores</span><span class="sxs-lookup"><span data-stu-id="35434-259">Number of interpolators</span></span>              | <span data-ttu-id="35434-260">16 registros de salida en vs \_ 3 \_ sw.</span><span class="sxs-lookup"><span data-stu-id="35434-260">16 output registers in vs\_3\_sw.</span></span>                                                                                                 |
| <span data-ttu-id="35434-261">ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="35434-261">ps\_3\_sw</span></span>                                  | <span data-ttu-id="35434-262">Número de interpoladores</span><span class="sxs-lookup"><span data-stu-id="35434-262">Number of interpolators</span></span>              | <span data-ttu-id="35434-263">14 (16-2) registros de entrada para ps \_ 3 \_ sw.</span><span class="sxs-lookup"><span data-stu-id="35434-263">14(16-2) input registers for ps\_3\_sw.</span></span>                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="35434-264">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="35434-264">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35434-265">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35434-265">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 

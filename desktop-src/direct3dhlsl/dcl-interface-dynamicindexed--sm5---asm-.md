---
title: dcl_interface_dynamicindexed (SM5-ASM)
description: Declare punteros de tabla de función (interfaces). | dcl_interface_dynamicindexed (SM5-ASM)
ms.assetid: 5C77EBB6-7AEC-4471-AA6E-0F6D3E215156
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78bb0152b44f7e29b9e76221db13da0c465a434
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998213"
---
# <a name="dcl_interface_dynamicindexed-sm5---asm"></a><span data-ttu-id="589ed-104">\_interfaz DCL \_ dynamicindexed (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="589ed-104">dcl\_interface\_dynamicindexed (sm5 - asm)</span></span>

<span data-ttu-id="589ed-105">Declare punteros de tabla de función (interfaces).</span><span class="sxs-lookup"><span data-stu-id="589ed-105">Declare function table pointers (interfaces).</span></span>



| <span data-ttu-id="589ed-106">DCL \_ interface \_ dynamicindexed FP \# \[ tamaño \] \[ numCallSites \] = {ft \# , ft \# ,...}</span><span class="sxs-lookup"><span data-stu-id="589ed-106">dcl\_interface\_dynamicindexed fp\#\[arraySize\]\[numCallSites\] = {ft\#, ft\#, ...}</span></span> |
|--------------------------------------------------------------------------------------|



 



| <span data-ttu-id="589ed-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="589ed-107">Item</span></span>                                                          | <span data-ttu-id="589ed-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="589ed-108">Description</span></span>                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="589ed-109"><span id="fp_"></span><span id="FP_"></span>*FP\#*</span><span class="sxs-lookup"><span data-stu-id="589ed-109"><span id="fp_"></span><span id="FP_"></span>*fp\#*</span></span><br/> | <span data-ttu-id="589ed-110">\[en \] los punteros de la tabla de función.</span><span class="sxs-lookup"><span data-stu-id="589ed-110">\[in\] The function table pointers.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="589ed-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="589ed-111">Remarks</span></span>

<span data-ttu-id="589ed-112">Cada interfaz debe estar enlazada desde la API antes de que se pueda usar el sombreador.</span><span class="sxs-lookup"><span data-stu-id="589ed-112">Each interface needs to be bound from the API before the shader is usable.</span></span> <span data-ttu-id="589ed-113">El enlace proporciona una referencia a una de las tablas de funciones para que se puedan rellenar las ranuras de método.</span><span class="sxs-lookup"><span data-stu-id="589ed-113">Binding gives a reference to one of the function tables so that the method slots can be filled in.</span></span> <span data-ttu-id="589ed-114">El compilador no generará punteros para objetos sin referencia.</span><span class="sxs-lookup"><span data-stu-id="589ed-114">The compiler will not generate pointers for unreferenced objects.</span></span>

<span data-ttu-id="589ed-115">Un puntero de tabla de función tiene un conjunto completo de ranuras de método para evitar el nivel de direccionamiento indirecto adicional que requeriría una representación de puntero a puntero a vtable de C++.</span><span class="sxs-lookup"><span data-stu-id="589ed-115">A function table pointer has a full set of method slots to avoid the extra level of indirection that a C++ pointer-to- pointer-to-vtable representation would require.</span></span> <span data-ttu-id="589ed-116">Esto también requeriría que estos punteros sean 5-tuplas.</span><span class="sxs-lookup"><span data-stu-id="589ed-116">That would also require that this pointers be 5-tuples.</span></span> <span data-ttu-id="589ed-117">En el modelo de inserción virtual de HLSL, siempre se sabe qué variable global/entrada se usa para una llamada, de modo que podamos configurar tablas por objeto raíz.</span><span class="sxs-lookup"><span data-stu-id="589ed-117">In the HLSL virtual inlining model it's always known what global variable/input is used for a call so we can set up tables per root object.</span></span>

<span data-ttu-id="589ed-118">Las declaraciones de puntero de función indican qué tablas de función son válidas para su uso con ellas.</span><span class="sxs-lookup"><span data-stu-id="589ed-118">Function pointer declarations indicate which function tables are legal to use with them.</span></span> <span data-ttu-id="589ed-119">Esto también permite la derivación de información de correlación de métodos.</span><span class="sxs-lookup"><span data-stu-id="589ed-119">This also allows derivation of method correlation information.</span></span>

<span data-ttu-id="589ed-120">La primera \[ \] de una declaración de interfaz es el tamaño de la matriz.</span><span class="sxs-lookup"><span data-stu-id="589ed-120">The first \[\] of an interface declaration is the array size.</span></span> <span data-ttu-id="589ed-121">Si se utiliza la indexación dinámica, la declaración indicará que, como se muestra.</span><span class="sxs-lookup"><span data-stu-id="589ed-121">If dynamic indexing is used the declaration will indicate that as shown.</span></span> <span data-ttu-id="589ed-122">Una matriz de punteros de interfaz se puede indizar de forma estática; no es necesario que las matrices de punteros de interfaz signifiquen una indexación dinámica.</span><span class="sxs-lookup"><span data-stu-id="589ed-122">An array of interface pointers can be indexed statically also, it is not required that arrays of interface pointers mean dynamic indexing.</span></span>

<span data-ttu-id="589ed-123">La numeración de punteros de interfaz comienza en 0 para la primera declaración y, posteriormente, tiene en cuenta el tamaño de la matriz, por lo que el primer puntero después de una matriz de cuatro entradas FP0 \[ 4 \] \[ 1 \] sería FP4 \[ \] \[ \] .</span><span class="sxs-lookup"><span data-stu-id="589ed-123">Numbering of interface pointers starts at 0 for the first declaration and subsequently takes array size into account, so the first pointer after a four entry array fp0\[4\]\[1\] would be fp4\[\]\[\].</span></span>

<span data-ttu-id="589ed-124">La segunda \[ \] de una declaración de interfaz es el número de sitios de llamada, que debe coincidir con el número de cuerpos de cada tabla a la que se hace referencia en la declaración.</span><span class="sxs-lookup"><span data-stu-id="589ed-124">The second \[\] of an interface declaration is the number of call sites, which must match the number of bodies in each table referenced in the declaration.</span></span>

<span data-ttu-id="589ed-125">No hay límites en el número de opciones de la tabla de funciones (ft \# ) que se pueden enumerar en una declaración de interfaz.</span><span class="sxs-lookup"><span data-stu-id="589ed-125">There are no bounds to how many function table (ft\#) choices can be listed in an interface declaration.</span></span>

<span data-ttu-id="589ed-126">Una tabla de función determinada (ft \# ) puede aparecer más de una vez en una o varias declaraciones de interfaz.</span><span class="sxs-lookup"><span data-stu-id="589ed-126">A given function table (ft\#) can appear more than once in one or more interface declarations.</span></span>

### <a name="restrictions"></a><span data-ttu-id="589ed-127">Restricciones</span><span class="sxs-lookup"><span data-stu-id="589ed-127">Restrictions</span></span>

-   <span data-ttu-id="589ed-128">El número de sitios de objetos en un sombreador, que es la suma de todas las declaraciones *FP \#* de sus \[ \] declaraciones tamaño, no debe ser superior a 253.</span><span class="sxs-lookup"><span data-stu-id="589ed-128">The number of object sites in a shader, which is the sum across all *fp\#* declarations of their \[arraySize\] declarations, must be no more than 253.</span></span> <span data-ttu-id="589ed-129">Este número corresponde **a cuántos punteros** pueden estar presentes.</span><span class="sxs-lookup"><span data-stu-id="589ed-129">This number corresponds to how many **this** pointers can be present.</span></span> <span data-ttu-id="589ed-130">El tiempo de ejecución aplica este límite de 253 para mantener un límite en el tamaño de DDI para comunicar estos datos de puntero.</span><span class="sxs-lookup"><span data-stu-id="589ed-130">The runtime enforces this 253 limit to keep a bound on the size of the DDI for communicating this pointer data.</span></span>
-   <span data-ttu-id="589ed-131">El número de sitios de llamada en un sombreador, que es la suma de todas las instrucciones fcall del número de posibles destinos de rama, no debe ser superior a 4096.</span><span class="sxs-lookup"><span data-stu-id="589ed-131">The number of call sites in a shader, which is the sum across all fcall statements of the number of potential branch targets, must be no more than 4096.</span></span>

    <span data-ttu-id="589ed-132">Por ejemplo, un [fcall](fcall--sm5---asm-.md) que utiliza un índice estático para la primera *dimensión \[ \] \[ \] FP* cuenta como uno:</span><span class="sxs-lookup"><span data-stu-id="589ed-132">For example, an [fcall](fcall--sm5---asm-.md) that uses a static index for the first *fp\[\]\[\]* dimension counts as one:</span></span>

    `                       fcall fp0[0][0]         // +1`

    <span data-ttu-id="589ed-133">Un **fcall** que utiliza un índice dinámico cuenta como el número de elementos de la matriz (primero \[ \] de **la \_ interfaz DCL**):</span><span class="sxs-lookup"><span data-stu-id="589ed-133">An **fcall** that uses a dynamic index counts as the number of elements in the array (first \[\] of **dcl\_interface**):</span></span>

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    <span data-ttu-id="589ed-134">Este límite ayuda a algunas implementaciones a ajustar fácilmente las tablas de las selecciones de cuerpo de función en el almacenamiento de tipo búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="589ed-134">This limit helps some implementations easily fit tables of function body selections in constant buffer-like storage.</span></span>

<span data-ttu-id="589ed-135">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="589ed-135">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="589ed-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="589ed-136">Vertex</span></span> | <span data-ttu-id="589ed-137">Casco</span><span class="sxs-lookup"><span data-stu-id="589ed-137">Hull</span></span> | <span data-ttu-id="589ed-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="589ed-138">Domain</span></span> | <span data-ttu-id="589ed-139">Geometría</span><span class="sxs-lookup"><span data-stu-id="589ed-139">Geometry</span></span> | <span data-ttu-id="589ed-140">Píxel</span><span class="sxs-lookup"><span data-stu-id="589ed-140">Pixel</span></span> | <span data-ttu-id="589ed-141">Compute</span><span class="sxs-lookup"><span data-stu-id="589ed-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="589ed-142">X</span><span class="sxs-lookup"><span data-stu-id="589ed-142">X</span></span>      | <span data-ttu-id="589ed-143">X</span><span class="sxs-lookup"><span data-stu-id="589ed-143">X</span></span>    | <span data-ttu-id="589ed-144">X</span><span class="sxs-lookup"><span data-stu-id="589ed-144">X</span></span>      | <span data-ttu-id="589ed-145">X</span><span class="sxs-lookup"><span data-stu-id="589ed-145">X</span></span>        | <span data-ttu-id="589ed-146">X</span><span class="sxs-lookup"><span data-stu-id="589ed-146">X</span></span>     | <span data-ttu-id="589ed-147">X</span><span class="sxs-lookup"><span data-stu-id="589ed-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="589ed-148">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="589ed-148">Minimum Shader Model</span></span>

<span data-ttu-id="589ed-149">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="589ed-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="589ed-150">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="589ed-150">Shader Model</span></span>                                              | <span data-ttu-id="589ed-151">Compatible</span><span class="sxs-lookup"><span data-stu-id="589ed-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="589ed-152">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="589ed-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="589ed-153">sí</span><span class="sxs-lookup"><span data-stu-id="589ed-153">yes</span></span>       |
| [<span data-ttu-id="589ed-154">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="589ed-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="589ed-155">no</span><span class="sxs-lookup"><span data-stu-id="589ed-155">no</span></span>        |
| [<span data-ttu-id="589ed-156">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="589ed-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="589ed-157">no</span><span class="sxs-lookup"><span data-stu-id="589ed-157">no</span></span>        |
| [<span data-ttu-id="589ed-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="589ed-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="589ed-159">no</span><span class="sxs-lookup"><span data-stu-id="589ed-159">no</span></span>        |
| [<span data-ttu-id="589ed-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="589ed-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="589ed-161">no</span><span class="sxs-lookup"><span data-stu-id="589ed-161">no</span></span>        |
| [<span data-ttu-id="589ed-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="589ed-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="589ed-163">no</span><span class="sxs-lookup"><span data-stu-id="589ed-163">no</span></span>        |



 

<span data-ttu-id="589ed-164">CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción para UAV y SRV.</span><span class="sxs-lookup"><span data-stu-id="589ed-164">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

## <a name="related-topics"></a><span data-ttu-id="589ed-165">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="589ed-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="589ed-166">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="589ed-166">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 






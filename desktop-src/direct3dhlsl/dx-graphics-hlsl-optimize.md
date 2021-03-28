---
title: Optimizar los sombreadores HLSL
description: En esta sección se describen las estrategias de uso general que puede usar para optimizar los sombreadores. Puede aplicar estas estrategias a los sombreadores que se escriben en cualquier lenguaje, en cualquier plataforma.
ms.assetid: 014b9cb3-a489-48d7-8174-b97de168bf3a
keywords:
- lenguaje de sombreador de alto nivel
- HLSL, rendimiento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06d3bb806e98e489020aa1755ef2a6c952459d86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076110"
---
# <a name="optimizing-hlsl-shaders"></a><span data-ttu-id="d8e96-106">Optimizar los sombreadores HLSL</span><span class="sxs-lookup"><span data-stu-id="d8e96-106">Optimizing HLSL Shaders</span></span>

<span data-ttu-id="d8e96-107">En esta sección se describen las estrategias de uso general que puede usar para optimizar los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="d8e96-107">This section describes general-purpose strategies that you can use to optimize your shaders.</span></span> <span data-ttu-id="d8e96-108">Puede aplicar estas estrategias a los sombreadores que se escriben en cualquier lenguaje, en cualquier plataforma.</span><span class="sxs-lookup"><span data-stu-id="d8e96-108">You can apply these strategies to shaders that are written in any language, on any platform.</span></span>

-   [<span data-ttu-id="d8e96-109">Saber dónde realizar los cálculos del sombreador</span><span class="sxs-lookup"><span data-stu-id="d8e96-109">Know Where To Perform Shader Calculations</span></span>](#know-where-to-perform-shader-calculations)
-   [<span data-ttu-id="d8e96-110">Omitir instrucciones innecesarias</span><span class="sxs-lookup"><span data-stu-id="d8e96-110">Skip Unnecessary Instructions</span></span>](#skip-unnecessary-instructions)
-   [<span data-ttu-id="d8e96-111">Variables del paquete y Interpolants</span><span class="sxs-lookup"><span data-stu-id="d8e96-111">Pack Variables and Interpolants</span></span>](#pack-variables-and-interpolants)
-   [<span data-ttu-id="d8e96-112">Reducir la complejidad del sombreador</span><span class="sxs-lookup"><span data-stu-id="d8e96-112">Reduce Shader Complexity</span></span>](#reduce-shader-complexity)
-   [<span data-ttu-id="d8e96-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d8e96-113">Related Topics</span></span>](#related-topics)
-   [<span data-ttu-id="d8e96-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d8e96-114">Related topics</span></span>](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a><span data-ttu-id="d8e96-115">Saber dónde realizar los cálculos del sombreador</span><span class="sxs-lookup"><span data-stu-id="d8e96-115">Know Where To Perform Shader Calculations</span></span>

<span data-ttu-id="d8e96-116">Los sombreadores de vértices realizan operaciones que incluyen la captura de vértices y la transformación de la matriz de datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="d8e96-116">Vertex shaders perform operations that include fetching vertices and performing matrix transformation of vertex data.</span></span> <span data-ttu-id="d8e96-117">Normalmente, los sombreadores de vértices se ejecutan una vez por vértice.</span><span class="sxs-lookup"><span data-stu-id="d8e96-117">Typically, vertex shaders are executed once per vertex.</span></span>

<span data-ttu-id="d8e96-118">Los sombreadores de píxeles realizan operaciones que incluyen la captura de datos de textura y la realización de cálculos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="d8e96-118">Pixel Shaders perform operations that include fetching texture data and performing lighting calculations.</span></span> <span data-ttu-id="d8e96-119">Normalmente, los sombreadores de píxeles se ejecutan una vez por píxel para un elemento de geometría determinado.</span><span class="sxs-lookup"><span data-stu-id="d8e96-119">Typically, pixel shaders are executed once per pixel for a given piece of geometry.</span></span>

<span data-ttu-id="d8e96-120">Normalmente, los píxeles superan los vértices de una escena, por lo que los sombreadores de píxeles se ejecutan con más frecuencia que los sombreadores de vértices.</span><span class="sxs-lookup"><span data-stu-id="d8e96-120">Typically, pixels outnumber vertices in a scene, so pixel shaders execute more often than vertex shaders.</span></span>

<span data-ttu-id="d8e96-121">Al diseñar algoritmos de sombreador, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d8e96-121">When you design shader algorithms, keep the following in mind:</span></span>

-   <span data-ttu-id="d8e96-122">Realice cálculos en el sombreador de vértices si es posible.</span><span class="sxs-lookup"><span data-stu-id="d8e96-122">Perform calculations on the vertex shader if possible.</span></span> <span data-ttu-id="d8e96-123">Un cálculo que se realiza en un sombreador de píxeles es mucho más caro que un cálculo que se realiza en un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="d8e96-123">A calculation that is performed on a pixel shader is much more expensive than a calculation that is performed on a vertex shader.</span></span>
-   <span data-ttu-id="d8e96-124">Considere la posibilidad de usar cálculos por vértices para mejorar el rendimiento en situaciones como mallas densas.</span><span class="sxs-lookup"><span data-stu-id="d8e96-124">Consider using per-vertex calculations to improve performance in situations such as dense meshes.</span></span> <span data-ttu-id="d8e96-125">En el caso de las mallas densas, los cálculos por vértices pueden producir resultados que no se pueden distinguir visualmente de los resultados generados con cálculos por píxel.</span><span class="sxs-lookup"><span data-stu-id="d8e96-125">For dense meshes, per-vertex calculations may produce results that are visually indistinguishable from results produced with per-pixel calculations.</span></span>

## <a name="skip-unnecessary-instructions"></a><span data-ttu-id="d8e96-126">Omitir instrucciones innecesarias</span><span class="sxs-lookup"><span data-stu-id="d8e96-126">Skip Unnecessary Instructions</span></span>

<span data-ttu-id="d8e96-127">En HLSL, la bifurcación dinámica proporciona la capacidad de limitar el número de instrucciones que se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="d8e96-127">In HLSL, dynamic branching provides the ability to limit the number of instructions that are executed.</span></span> <span data-ttu-id="d8e96-128">Por lo tanto, la bifurcación dinámica puede ayudar a acelerar el tiempo de ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d8e96-128">Therefore, dynamic branching can help speed up shader execution time.</span></span> <span data-ttu-id="d8e96-129">Si no se muestran geometría o píxeles, use la bifurcación dinámica para salir del sombreador o para limitar las instrucciones.</span><span class="sxs-lookup"><span data-stu-id="d8e96-129">If geometry or pixels are not displayed, use dynamic branching to exit the shader or to limit instructions.</span></span> <span data-ttu-id="d8e96-130">Por ejemplo, si un píxel no está iluminado, no hay ningún punto en ejecutar el algoritmo de iluminación.</span><span class="sxs-lookup"><span data-stu-id="d8e96-130">For example, if a pixel is not lit, there is no point in executing the lighting algorithm.</span></span>

<span data-ttu-id="d8e96-131">En la tabla siguiente se muestran algunos casos en los que puede probar condiciones en el sombreador y usar la bifurcación dinámica para omitir las instrucciones innecesarias.</span><span class="sxs-lookup"><span data-stu-id="d8e96-131">The following table lists some cases where you can test conditions in your shader and use dynamic branching to skip unnecessary instructions.</span></span> <span data-ttu-id="d8e96-132">La tabla no es completa.</span><span class="sxs-lookup"><span data-stu-id="d8e96-132">The table not comprehensive.</span></span> <span data-ttu-id="d8e96-133">En su lugar, se pretende ofrecer ideas para optimizar el código.</span><span class="sxs-lookup"><span data-stu-id="d8e96-133">Rather, it is intended to give you ideas for optimizing your code.</span></span>



| <span data-ttu-id="d8e96-134">Condición para comprobar</span><span class="sxs-lookup"><span data-stu-id="d8e96-134">Condition to Check</span></span>                                    | <span data-ttu-id="d8e96-135">Respuesta en el sombreador</span><span class="sxs-lookup"><span data-stu-id="d8e96-135">Response in the Shader</span></span>       |
|-------------------------------------------------------|------------------------------|
| <span data-ttu-id="d8e96-136">La comprobación alfa determina que no se verá un píxel.</span><span class="sxs-lookup"><span data-stu-id="d8e96-136">Alpha check determines that a pixel will not be seen.</span></span> | <span data-ttu-id="d8e96-137">Omita el resto del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d8e96-137">Skip the rest of the shader.</span></span> |
| <span data-ttu-id="d8e96-138">El píxel o la geometría están totalmente nebulizados.</span><span class="sxs-lookup"><span data-stu-id="d8e96-138">The pixel or geometry is fully fogged.</span></span>                | <span data-ttu-id="d8e96-139">Omita el resto del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d8e96-139">Skip the rest of the shader.</span></span> |
| <span data-ttu-id="d8e96-140">Los pesos de la máscara son cero.</span><span class="sxs-lookup"><span data-stu-id="d8e96-140">Skin weights are zero.</span></span>                                | <span data-ttu-id="d8e96-141">Omita los huesos.</span><span class="sxs-lookup"><span data-stu-id="d8e96-141">Skip bones.</span></span>                  |
| <span data-ttu-id="d8e96-142">La atenuación de luz es cero.</span><span class="sxs-lookup"><span data-stu-id="d8e96-142">Light attenuation is zero.</span></span>                            | <span data-ttu-id="d8e96-143">Omitir iluminación.</span><span class="sxs-lookup"><span data-stu-id="d8e96-143">Skip lighting.</span></span>               |
| <span data-ttu-id="d8e96-144">Término Lambertian no positivo.</span><span class="sxs-lookup"><span data-stu-id="d8e96-144">Non-positive Lambertian term.</span></span>                         | <span data-ttu-id="d8e96-145">Omitir iluminación.</span><span class="sxs-lookup"><span data-stu-id="d8e96-145">Skip lighting.</span></span>               |



 

## <a name="pack-variables-and-interpolants"></a><span data-ttu-id="d8e96-146">Variables del paquete y Interpolants</span><span class="sxs-lookup"><span data-stu-id="d8e96-146">Pack Variables and Interpolants</span></span>

<span data-ttu-id="d8e96-147">Tenga en cuentan el espacio necesario para los datos del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d8e96-147">Be mindful of the space required for shader data.</span></span> <span data-ttu-id="d8e96-148">Empaquete toda la información en una variable o interpolant como sea posible.</span><span class="sxs-lookup"><span data-stu-id="d8e96-148">Pack as much information into a variable or interpolant as possible.</span></span> <span data-ttu-id="d8e96-149">A veces, la información de dos variables se puede empaquetar en el espacio de memoria de una sola variable.</span><span class="sxs-lookup"><span data-stu-id="d8e96-149">Sometimes, the information from two variables can be packed into the memory space of a single variable.</span></span>

## <a name="reduce-shader-complexity"></a><span data-ttu-id="d8e96-150">Reducir la complejidad del sombreador</span><span class="sxs-lookup"><span data-stu-id="d8e96-150">Reduce Shader Complexity</span></span>

<span data-ttu-id="d8e96-151">Mantenga los sombreadores pequeños y sencillos.</span><span class="sxs-lookup"><span data-stu-id="d8e96-151">Keep your shaders small and simple.</span></span> <span data-ttu-id="d8e96-152">En general, los sombreadores con menos instrucciones se ejecutan más rápidamente que los sombreadores con más instrucciones.</span><span class="sxs-lookup"><span data-stu-id="d8e96-152">In general, shaders with fewer instructions execute more quickly than shaders with more instructions.</span></span> <span data-ttu-id="d8e96-153">También es más fácil depurar y optimizar los sombreadores más pequeños y menos complejos.</span><span class="sxs-lookup"><span data-stu-id="d8e96-153">It is also easier to debug and optimize smaller, less complex shaders.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8e96-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d8e96-154">Related Topics</span></span>

[<span data-ttu-id="d8e96-155">Guía de programación para HLSL</span><span class="sxs-lookup"><span data-stu-id="d8e96-155">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="d8e96-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d8e96-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8e96-157">Guía de programación para HLSL</span><span class="sxs-lookup"><span data-stu-id="d8e96-157">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 





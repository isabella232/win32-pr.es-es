---
title: Tendencia de profundidad
description: Los polígonos que se coplanan en el espacio 3D pueden crearse como si no fueran coplanares agregando un sesgo z (o una diferencia de profundidad) a cada uno de ellos.
ms.assetid: ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6f9a3850b03e033a90b358d0c6ffd1ceef830f
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797350"
---
# <a name="depth-bias"></a><span data-ttu-id="6f948-103">Tendencia de profundidad</span><span class="sxs-lookup"><span data-stu-id="6f948-103">Depth Bias</span></span>

<span data-ttu-id="6f948-104">Los polígonos que se coplanan en el espacio 3D pueden crearse como si no fueran coplanares agregando un sesgo z (o una diferencia de profundidad) a cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="6f948-104">Polygons that are coplanar in 3D space can be made to appear as if they are not coplanar by adding a z-bias (or depth bias) to each one.</span></span>

<span data-ttu-id="6f948-105">Se trata de una técnica que se usa normalmente para asegurarse de que las sombras de una escena se muestran correctamente.</span><span class="sxs-lookup"><span data-stu-id="6f948-105">This is a technique commonly used to ensure that shadows in a scene are displayed properly.</span></span> <span data-ttu-id="6f948-106">Por ejemplo, una sombra en un muro probablemente tendrá el mismo valor de profundidad que la pared.</span><span class="sxs-lookup"><span data-stu-id="6f948-106">For instance, a shadow on a wall will likely have the same depth value as the wall.</span></span> <span data-ttu-id="6f948-107">Si una aplicación representa una pared primero y después una sombra, puede que la sombra no sea visible o que los artefactos de profundidad estén visibles.</span><span class="sxs-lookup"><span data-stu-id="6f948-107">If an application renders a wall first and then a shadow, the shadow might not be visible, or depth artifacts might be visible.</span></span>


<span data-ttu-id="6f948-108">Una aplicación puede ayudar a garantizar que los polígonos coplanares se representen correctamente agregando la diferencia (del miembro **DepthBias** de [**D3D11 \_ rasterizador \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) a los valores z que el sistema utiliza al representar los conjuntos de polígonos coplanares.</span><span class="sxs-lookup"><span data-stu-id="6f948-108">An application can help ensure that coplanar polygons are rendered properly by adding the bias (from the **DepthBias** member of [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) to the z-values that the system uses when rendering the sets of coplanar polygons.</span></span> <span data-ttu-id="6f948-109">Los polígonos con un valor z más grande se dibujarán delante de los polígonos con un valor z más pequeño.</span><span class="sxs-lookup"><span data-stu-id="6f948-109">Polygons with a larger z value will be drawn in front of polygons with a smaller z value.</span></span>

<span data-ttu-id="6f948-110">Hay dos opciones para calcular la diferencia de profundidad.</span><span class="sxs-lookup"><span data-stu-id="6f948-110">There are two options for calculating depth bias.</span></span>

1.  <span data-ttu-id="6f948-111">Si el búfer de profundidad actualmente enlazado a la fase de combinación de resultados tiene un formato **UNORM** o no hay ningún búfer de profundidad enlazado, el valor de Bias se calcula como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="6f948-111">If the depth buffer currently bound to the output-merger stage has a **UNORM** format or no depth buffer is bound, the bias value is calculated like this:</span></span>
    ```
    Bias = (float)DepthBias * r + SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    <span data-ttu-id="6f948-112">donde *r* es el valor representable mínimo > 0 en el formato de búfer de profundidad convertido en **float32**.</span><span class="sxs-lookup"><span data-stu-id="6f948-112">where *r* is the minimum representable value > 0 in the depth-buffer format converted to **float32**.</span></span> <span data-ttu-id="6f948-113">Los valores **DepthBias** y **SlopeScaledDepthBias** son miembros de la estructura de [**\_ rasterizador D3D11 \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) .</span><span class="sxs-lookup"><span data-stu-id="6f948-113">The **DepthBias** and **SlopeScaledDepthBias** values are [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) structure members.</span></span> <span data-ttu-id="6f948-114">El valor de **MaxDepthSlope** es el máximo de las pendientes horizontal y vertical del valor de profundidad en el píxel.</span><span class="sxs-lookup"><span data-stu-id="6f948-114">The **MaxDepthSlope** value is the maximum of the horizontal and vertical slopes of the depth value at the pixel.</span></span>
2.  <span data-ttu-id="6f948-115">Si un búfer de profundidad de punto flotante se enlaza a la fase de combinación de salida, el valor de la diferencia se calcula como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="6f948-115">If a floating-point depth buffer is bound to the output-merger stage the bias value is calculated like this:</span></span>
    ```
    Bias = (float)DepthBias * 2**(exponent(max z in primitive) - r) +
                SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    <span data-ttu-id="6f948-116">donde *r* es el número de bits de mantisa en la representación de punto flotante (sin incluir el bit oculto); por ejemplo, 23 para **float32**.</span><span class="sxs-lookup"><span data-stu-id="6f948-116">where *r* is the number of mantissa bits in the floating point representation (excluding the hidden bit); for example, 23 for **float32**.</span></span>

<span data-ttu-id="6f948-117">Después, el valor de la diferencia se fija de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6f948-117">The bias value is then clamped like this:</span></span>


```
if(DepthBiasClamp > 0)
    Bias = min(DepthBiasClamp, Bias)
else if(DepthBiasClamp < 0)
    Bias = max(DepthBiasClamp, Bias)
```



<span data-ttu-id="6f948-118">A continuación, el valor de diferencia se usa para calcular la profundidad del píxel.</span><span class="sxs-lookup"><span data-stu-id="6f948-118">The bias value is then used to calculate the pixel depth.</span></span>


```
if ( (DepthBias != 0) || (SlopeScaledDepthBias != 0) )
    z = z + Bias
```



<span data-ttu-id="6f948-119">Las operaciones de diferencia de profundidad se producen en los vértices después del recorte, por lo tanto, la diferencia de profundidad no tiene ningún efecto en el recorte geométrico.</span><span class="sxs-lookup"><span data-stu-id="6f948-119">Depth-bias operations occur on vertices after clipping, therefore, depth-bias has no effect on geometric clipping.</span></span> <span data-ttu-id="6f948-120">El valor de Bias es constante para un primitivo determinado y se agrega al valor z para cada vértice antes de la configuración del interpolador.</span><span class="sxs-lookup"><span data-stu-id="6f948-120">The bias value is constant for a given primitive and is added to the z value for each vertex before interpolator setup.</span></span> <span data-ttu-id="6f948-121">Cuando se usan [los niveles de características](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 y posteriores, todos los cálculos de sesgo se realizan mediante aritmética de punto flotante de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6f948-121">When you use [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 10.0 and higher, all bias calculations are performed using 32-bit floating-point arithmetic.</span></span> <span data-ttu-id="6f948-122">La diferencia no se aplica a los primitivos de punto o de línea, excepto en el caso de las líneas dibujadas en el modo de alambre.</span><span class="sxs-lookup"><span data-stu-id="6f948-122">Bias is not applied to any point or line primitives, except for lines drawn in wireframe mode.</span></span>

<span data-ttu-id="6f948-123">Uno de los artefactos con sombras basadas en el búfer de sombra es Shadow acne, o una sombra en sí misma debido a pequeñas diferencias entre el cálculo de profundidad en un sombreador y la profundidad de la misma superficie en el búfer de la sombra.</span><span class="sxs-lookup"><span data-stu-id="6f948-123">One of the artifacts with shadow buffer based shadows is shadow acne, or a surface shadowing itself due to minor differences between the depth computation in a shader, and the depth of the same surface in the shadow buffer.</span></span> <span data-ttu-id="6f948-124">Una manera de solucionar esto es usar **DepthBias** y **SlopeScaledDepthBias** al representar un búfer de sombra.</span><span class="sxs-lookup"><span data-stu-id="6f948-124">One way to alleviate this is to use **DepthBias** and **SlopeScaledDepthBias** when rendering a shadow buffer.</span></span> <span data-ttu-id="6f948-125">La idea es que las superficies se inserten lo suficiente al representar un búfer de sombra, de modo que el resultado de la comparación (entre el búfer de la sombra z y el sombreador z) sea coherente en toda la superficie y evitar la sombra automática local.</span><span class="sxs-lookup"><span data-stu-id="6f948-125">The idea is to push surfaces out enough while rendering a shadow buffer so that the comparison result (between the shadow buffer z and the shader z) is consistent across the surface, and avoid local self-shadowing.</span></span>

<span data-ttu-id="6f948-126">Sin embargo, el uso de **DepthBias** y **SlopeScaledDepthBias** puede introducir nuevos problemas de representación cuando un polígono visto en un ángulo muy nítido hace que la ecuación de diferencia genere un valor z muy grande.</span><span class="sxs-lookup"><span data-stu-id="6f948-126">However, using **DepthBias** and **SlopeScaledDepthBias** can introduce new rendering problems when a polygon viewed at an extremely sharp angle causes the bias equation to generate a very large z value.</span></span> <span data-ttu-id="6f948-127">Esto, de hecho, empuja el polígono muy lejos de la superficie original en la instantánea.</span><span class="sxs-lookup"><span data-stu-id="6f948-127">This in effect pushes the polygon extremely far away from the original surface in the shadow map.</span></span> <span data-ttu-id="6f948-128">Una manera de ayudar a mitigar este problema concreto es usar **DepthBiasClamp**, que proporciona un límite superior (positivo o negativo) en la magnitud de la diferencia de z calculada.</span><span class="sxs-lookup"><span data-stu-id="6f948-128">One way to help alleviate this particular problem is to use **DepthBiasClamp**, which provides an upper bound (positive or negative) on the magnitude of the z bias calculated.</span></span>

> [!Note]  
> <span data-ttu-id="6f948-129">No se admiten [los niveles de características](overviews-direct3d-11-devices-downlevel-intro.md) 9,1, 9,2, 9,3, **DepthBiasClamp** .</span><span class="sxs-lookup"><span data-stu-id="6f948-129">For [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 9.1, 9.2, 9.3, **DepthBiasClamp** is not supported.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6f948-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6f948-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f948-131">Fase de combinación de salida</span><span class="sxs-lookup"><span data-stu-id="6f948-131">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> </dl>

 

 





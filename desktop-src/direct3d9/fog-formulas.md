---
description: Las aplicaciones de C++ pueden controlar cómo afecta la niebla al color de los objetos en una escena cambiando la forma en que Microsoft Direct3D calcula los efectos de niebla a través de la distancia.
ms.assetid: b7148ae8-45c7-4dbe-8295-0335c7fdeff0
title: Fórmulas de niebla (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75150a00d491f1e3fc1ea1444209449c1c2a825d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906545"
---
# <a name="fog-formulas-direct3d-9"></a><span data-ttu-id="6d1fd-103">Fórmulas de niebla (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6d1fd-103">Fog Formulas (Direct3D 9)</span></span>

<span data-ttu-id="6d1fd-104">Las aplicaciones de C++ pueden controlar cómo afecta la niebla al color de los objetos en una escena cambiando la forma en que Microsoft Direct3D calcula los efectos de niebla a través de la distancia.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-104">C++ applications can control how fog affects the color of objects in a scene by changing how Microsoft Direct3D computes fog effects over distance.</span></span> <span data-ttu-id="6d1fd-105">El tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) contiene miembros que identifican las tres fórmulas de niebla.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-105">The [**D3DFOGMODE**](./d3dfogmode.md) enumerated type contains members that identify the three fog formulas.</span></span> <span data-ttu-id="6d1fd-106">Todas las fórmulas calculan un factor de niebla como una función de distancia, dados los parámetros que establece la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-106">All formulas calculate a fog factor as a function of distance, given parameters that your application sets.</span></span>

## <a name="linear-fog"></a><span data-ttu-id="6d1fd-107">Niebla lineal</span><span class="sxs-lookup"><span data-stu-id="6d1fd-107">Linear Fog</span></span>

<span data-ttu-id="6d1fd-108">Se establece con la ecuación lineal de D3DFOG siguiente \_ .</span><span class="sxs-lookup"><span data-stu-id="6d1fd-108">This is set with the following D3DFOG\_LINEAR equation.</span></span>

![ecuación de niebla lineal de Direct3D](images/fogliner.png)

<span data-ttu-id="6d1fd-110">where</span><span class="sxs-lookup"><span data-stu-id="6d1fd-110">where</span></span>

-   <span data-ttu-id="6d1fd-111">Start es la distancia a la que comienzan los efectos de niebla.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-111">start is the distance at which fog effects begin.</span></span>
-   <span data-ttu-id="6d1fd-112">end es la distancia a la que los efectos de niebla ya no aumentan.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-112">end is the distance at which fog effects no longer increase.</span></span>
-   <span data-ttu-id="6d1fd-113">d representa la profundidad o la distancia desde el punto de vista.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-113">d represents depth, or the distance from the viewpoint.</span></span> <span data-ttu-id="6d1fd-114">En el caso de la niebla basada en intervalo, el valor de d es la distancia entre la posición de la cámara y un vértice.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-114">For range based fog, the value for d is the distance between the camera position and a vertex.</span></span> <span data-ttu-id="6d1fd-115">En el caso de una niebla no basada en intervalos, el valor de d es el valor absoluto de la coordenada Z del espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-115">For non-range based fog, the value for d is the absolute value of the Z-coordinate in camera space.</span></span>

## <a name="exponential-fog"></a><span data-ttu-id="6d1fd-116">Niebla exponencial</span><span class="sxs-lookup"><span data-stu-id="6d1fd-116">Exponential Fog</span></span>

<span data-ttu-id="6d1fd-117">Las fórmulas lineal y exponencial se admiten tanto para la niebla de píxeles como para la niebla de vértice.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-117">Linear and exponential formulas are supported for both pixel fog and vertex fog.</span></span>

<span data-ttu-id="6d1fd-118">Se establece con la siguiente ecuación D3DFOG \_ exp.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-118">This is set with the following D3DFOG\_EXP equation.</span></span>

![ecuación de la niebla exponencial de Direct3D](images/fogexp.png)

<span data-ttu-id="6d1fd-120">where</span><span class="sxs-lookup"><span data-stu-id="6d1fd-120">where</span></span>

-   <span data-ttu-id="6d1fd-121">e es la base de los logaritmos naturales (aproximadamente 2,71828).</span><span class="sxs-lookup"><span data-stu-id="6d1fd-121">e is the base of natural logarithms (approximately 2.71828).</span></span>
-   <span data-ttu-id="6d1fd-122">la densidad es una densidad de niebla arbitraria que puede oscilar entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-122">density is an arbitrary fog density that can range from 0.0 to 1.0.</span></span>
-   <span data-ttu-id="6d1fd-123">d representa la profundidad, o la distancia desde el punto de vista, como se indicó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-123">d represents depth, or the distance from the viewpoint, as stated earlier.</span></span>

<span data-ttu-id="6d1fd-124">Se establece con la siguiente ecuación de \_ EXP2 de D3DFOG.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-124">This is set with the following D3DFOG\_EXP2 equation.</span></span>

![ecuación de la niebla de Direct3D exponencial 2](images/fogexp2.png)

<span data-ttu-id="6d1fd-126">where</span><span class="sxs-lookup"><span data-stu-id="6d1fd-126">where</span></span>

-   <span data-ttu-id="6d1fd-127">e es la base de los logaritmos naturales tal y como se indicó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-127">e is the base of natural logarithms as stated above.</span></span>
-   <span data-ttu-id="6d1fd-128">la densidad es una densidad de niebla arbitraria que puede oscilar entre 0,0 y 1,0, tal y como se indicó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-128">density is an arbitrary fog density that can range from 0.0 to 1.0 as stated above.</span></span>
-   <span data-ttu-id="6d1fd-129">d representa la profundidad, o la distancia desde el punto de vista, como se indicó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-129">d represents depth, or the distance from the viewpoint, as stated above.</span></span>

> [!Note]  
> <span data-ttu-id="6d1fd-130">El sistema almacena el factor de niebla en el componente alfa del color especular de un vértice.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-130">The system stores the fog factor in the alpha component of the specular color for a vertex.</span></span> <span data-ttu-id="6d1fd-131">Si la aplicación realiza su propia transformación e iluminación, puede insertar valores de factor de niebla manualmente para que los aplique el sistema durante la representación.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-131">If your application performs its own transformation and lighting, you can insert fog factor values manually, to be applied by the system during rendering.</span></span>

 

<span data-ttu-id="6d1fd-132">En el gráfico siguiente se muestran estas fórmulas con valores comunes como en los parámetros de la fórmula.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-132">The following graph shows these formulas, using common values as in the formula parameters.</span></span>

![gráfico de las fórmulas de niebla a través de la distancia y la cantidad de color](images/foggraph.png)

<span data-ttu-id="6d1fd-134">D3DFOG \_ linear es 1,0 en Start y 0,0 al final.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-134">D3DFOG\_LINEAR is 1.0 at start and 0.0 at end.</span></span> <span data-ttu-id="6d1fd-135">No se mide en relación con los planos near o FAR.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-135">It is not measured relative to the near or far planes.</span></span>

<span data-ttu-id="6d1fd-136">Cuando Direct3D calcula los efectos de niebla, utiliza el factor de niebla de una de las ecuaciones anteriores en la siguiente ecuación de fusión.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-136">When Direct3D calculates fog effects, it uses the fog factor from one of the preceding equations in the following blending equation.</span></span>

![ecuación de efectos de niebla para Direct3D](images/fogcalc.png)

<span data-ttu-id="6d1fd-138">Esta fórmula escala eficazmente el color del polígono actual C mediante el factor de niebla f, y agrega el producto al color de niebla C, escalado por el inverso bit a bit del factor de niebla.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-138">This formula effectively scales the color of the current polygon C by the fog factor f, and adds the product to the fog color C, scaled by the bitwise inverse of the fog factor.</span></span> <span data-ttu-id="6d1fd-139">El valor de color resultante es una mezcla del color de niebla y el color original, como un factor de distancia.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-139">The resulting color value is a blend of the fog color and the original color, as a factor of distance.</span></span> <span data-ttu-id="6d1fd-140">La fórmula se aplica a todos los dispositivos compatibles con Microsoft DirectX 7,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-140">The formula applies to all devices supported in Microsoft DirectX 7.0 and later.</span></span> <span data-ttu-id="6d1fd-141">En el caso del dispositivo de rampa heredado, el factor de niebla escala los componentes de color difuso y especular, fijados en el intervalo de 0,0 y 1,0, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-141">For the legacy ramp device, the fog factor scales the diffuse and specular color components, clamped to the range of 0.0 and 1.0, inclusive.</span></span> <span data-ttu-id="6d1fd-142">Normalmente, el factor de niebla comienza en 1,0 para el plano próximo y se reduce a 0,0 en el plano lejano.</span><span class="sxs-lookup"><span data-stu-id="6d1fd-142">The fog factor typically starts at 1.0 for the near plane and decreases to 0.0 at the far plane.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d1fd-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6d1fd-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d1fd-144">Tipos de niebla</span><span class="sxs-lookup"><span data-stu-id="6d1fd-144">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 

---
description: La iluminación en el mundo real contiene un intervalo dinámico muy alto (HDR) de valores de luminancia.
ms.assetid: 537700e2-802d-4fd1-b026-142d6f4f0559
title: Iluminación de HDR (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f397ccef2b1fa315e64861453b13f0f6fddfe77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274607"
---
# <a name="hdr-lighting-direct3d-9"></a><span data-ttu-id="f1897-103">Iluminación de HDR (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f1897-103">HDR Lighting (Direct3D 9)</span></span>

<span data-ttu-id="f1897-104">La iluminación en el mundo real contiene un intervalo dinámico muy alto (HDR) de valores de luminancia.</span><span class="sxs-lookup"><span data-stu-id="f1897-104">Lighting in the real world contains a very high dynamic range (HDR) of luminance values.</span></span> <span data-ttu-id="f1897-105">El mundo real tiene aproximadamente 10 pedidos de intervalo dinámico (DR) para los valores de luminancia distribuidos en el espectro de oscuridad al brillo.</span><span class="sxs-lookup"><span data-stu-id="f1897-105">The real world has about 10 orders of dynamic range (DR) for luminance values spread across the spectrum of darkness to brightness.</span></span> <span data-ttu-id="f1897-106">Por otro lado, una pantalla de equipo tiene una gama de pantalla muy limitada (o un intervalo de valores de luminancia): aproximadamente dos pedidos de intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="f1897-106">On the other hand, a computer screen has a very limited display gamut (or range of luminance values): approximately two orders of dynamic range.</span></span> <span data-ttu-id="f1897-107">El reto de producir imágenes representadas de HDR es asignar los valores de HDR del mundo real en la gama limitada de la pantalla de un equipo.</span><span class="sxs-lookup"><span data-stu-id="f1897-107">The challenge to producing HDR rendered images is to map the real world HDR values into the limited gamut of a computer screen.</span></span>

<span data-ttu-id="f1897-108">La asignación de tono es la técnica que usa DirectX para asignar información de HDR a un intervalo más limitado.</span><span class="sxs-lookup"><span data-stu-id="f1897-108">Tone mapping is the technique used by DirectX for mapping HDR information into a more limited range.</span></span> <span data-ttu-id="f1897-109">La asignación de tono aplicada a la representación en CGI puede mejorar drásticamente la cantidad de detalles de iluminación representada, lo que permite ver los detalles en las áreas más oscuras y proporcionar un contraste en las áreas que son tan brillantes, que aparecen grabadas.</span><span class="sxs-lookup"><span data-stu-id="f1897-109">Tone mapping applied to CGI rendering can dramatically improve the amount of lighting detail rendered, allowing details in the darkest areas to be seen, and providing contrast in areas that are so bright, they appear burned.</span></span> <span data-ttu-id="f1897-110">Las escenas resultantes se representan con detalles de iluminación mucho más visibles.</span><span class="sxs-lookup"><span data-stu-id="f1897-110">The resulting scenes render with far more visible lighting detail.</span></span>

<span data-ttu-id="f1897-111">El [ejemplo HDRLighting](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) es un ejemplo de SDK que muestra la iluminación HDR.</span><span class="sxs-lookup"><span data-stu-id="f1897-111">[HDRLighting Sample](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) is a SDK sample that demonstrates HDR lighting.</span></span>

## <a name="tone-mapping"></a><span data-ttu-id="f1897-112">Asignación de tono</span><span class="sxs-lookup"><span data-stu-id="f1897-112">Tone Mapping</span></span>

<span data-ttu-id="f1897-113">Normalmente, la asignación de tono simula los fenómenos ópticos que no pueden ser causados por la recuperación ante desastres del monitor.</span><span class="sxs-lookup"><span data-stu-id="f1897-113">Tone mapping generally simulates optical phenomena that cannot be caused by the DR of the monitor.</span></span> <span data-ttu-id="f1897-114">Ejemplos de esto son los destellos o la floración (que son principalmente propiedades de lentes), el turno azul que ocurre en el ojo humano en condiciones de poca luz y otras adaptaciones que son el resultado de la bioquímica del ojo.</span><span class="sxs-lookup"><span data-stu-id="f1897-114">Examples of this are flares or blooming (which are mostly properties of lenses), the blue shift that happens in the human eye in low light conditions, and other adaptations that are a result of the biochemistry of the eye.</span></span> <span data-ttu-id="f1897-115">Si la recuperación ante desastres de la pantalla era lo suficientemente grande, la asignación de tono no sería tan necesaria, salvo para proporcionar efectos artísticos o algunas de las propiedades de una lente de la cámara o un dispositivo acoplado a carga (CCD).</span><span class="sxs-lookup"><span data-stu-id="f1897-115">If the DR of the display were large enough, tone mapping would not be as neccessary, except for providing artistic effects or some of the properties of a camera lens or a charge coupled device (CCD).</span></span>

<span data-ttu-id="f1897-116">La asignación de tono divide el intervalo de valores de luminancia de una escena en un conjunto de zonas.</span><span class="sxs-lookup"><span data-stu-id="f1897-116">Tone mapping divides the range of luminance values in a scene into a set of zones.</span></span> <span data-ttu-id="f1897-117">Cada zona abarca un intervalo de valores de luminancia.</span><span class="sxs-lookup"><span data-stu-id="f1897-117">Each zone encompasses a range of luminance values.</span></span>

<span data-ttu-id="f1897-118">HDR usa los siguientes términos:</span><span class="sxs-lookup"><span data-stu-id="f1897-118">HDR uses the following terms:</span></span>

-   <span data-ttu-id="f1897-119">Zona-intervalo de valores de luminancia</span><span class="sxs-lookup"><span data-stu-id="f1897-119">Zone - range of luminance values</span></span>
-   <span data-ttu-id="f1897-120">Región de brillo central gris de la escena</span><span class="sxs-lookup"><span data-stu-id="f1897-120">Middle gray - middle brightness region of the scene</span></span>
-   <span data-ttu-id="f1897-121">Intervalo dinámico: relación entre la luminancia de la escena más alta y la luminancia de la escena más baja</span><span class="sxs-lookup"><span data-stu-id="f1897-121">Dynamic range - ratio of the highest scene luminance to the lowest scene luminance</span></span>
-   <span data-ttu-id="f1897-122">Medición clave-subjetiva de la iluminación de la escena: varía de una luz a una moderada</span><span class="sxs-lookup"><span data-stu-id="f1897-122">Key - subjective measurement of scene lighting: this varies from light to moderate to dark</span></span>

<span data-ttu-id="f1897-123">Para calcular la luminancia a partir de los valores RGB, use lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f1897-123">To calculate luminance from RGB values, use this:</span></span>


```
L = 0.27R + 0.67G + 0.06B;
```



<span data-ttu-id="f1897-124">La luminancia media del registro es una aproximación útil para la clave de una escena.</span><span class="sxs-lookup"><span data-stu-id="f1897-124">The log-average luminance is a useful approximation for the key of a scene.</span></span> <span data-ttu-id="f1897-125">Una ecuación general tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="f1897-125">A general equation looks like this:</span></span>

<span data-ttu-id="f1897-126">L<sub>w</sub> = exp \[ 1/N (registro de suma \[ (delta + L<sub>w</sub>(x, y)) \] ) \]</span><span class="sxs-lookup"><span data-stu-id="f1897-126">L<sub>w</sub> = exp\[ 1 / N( sum\[ log( delta + L<sub>w</sub>( x, y ) ) \] ) \]</span></span>

<span data-ttu-id="f1897-127">Donde:</span><span class="sxs-lookup"><span data-stu-id="f1897-127">Where:</span></span>

-   <span data-ttu-id="f1897-128">L<sub>registro-promedio de luminancia</sub></span><span class="sxs-lookup"><span data-stu-id="f1897-128">L<sub>w</sub> - log-average luminance</span></span>
-   <span data-ttu-id="f1897-129">N: número de píxeles de la imagen</span><span class="sxs-lookup"><span data-stu-id="f1897-129">N - number of pixels in the image</span></span>
-   <span data-ttu-id="f1897-130">Delta: un pequeño factor para evitar problemas con los píxeles negros</span><span class="sxs-lookup"><span data-stu-id="f1897-130">delta - a small factor to avoid problems with black pixels</span></span>
-   <span data-ttu-id="f1897-131">L<sub>w</sub>(x, y): la luminancia del espacio mundial del píxel (x, y)</span><span class="sxs-lookup"><span data-stu-id="f1897-131">L<sub>w</sub>( x, y ) - the world space luminance for pixel ( x, y )</span></span>

<span data-ttu-id="f1897-132">Para asignarlo a un valor de gris medio, este es un operador de escala de luminancia:</span><span class="sxs-lookup"><span data-stu-id="f1897-132">To map this to a middle-gray value, here is a luminance scaling operator:</span></span>

<span data-ttu-id="f1897-133">L (x, y) = a \* l<sub>w</sub>(x, y)/L<sub>w</sub></span><span class="sxs-lookup"><span data-stu-id="f1897-133">L( x, y ) = a \* L<sub>w</sub>( x, y ) / L<sub>w</sub></span></span>

<span data-ttu-id="f1897-134">Donde:</span><span class="sxs-lookup"><span data-stu-id="f1897-134">Where:</span></span>

-   <span data-ttu-id="f1897-135">L (x, y): luminancia escalada para píxel (x, y)</span><span class="sxs-lookup"><span data-stu-id="f1897-135">L( x, y ) - scaled luminance for pixel ( x, y )</span></span>
-   <span data-ttu-id="f1897-136">un valor de clave-Image después de aplicar el ajuste de escala</span><span class="sxs-lookup"><span data-stu-id="f1897-136">a - image key value after applying the scaling</span></span>

<span data-ttu-id="f1897-137">Y, por último, aquí se muestra un operador de asignación de tono simple para comprimir el luminances alto:</span><span class="sxs-lookup"><span data-stu-id="f1897-137">And finally, here is a simple tone mapping operator for compressing the high luminances:</span></span>

<span data-ttu-id="f1897-138">L<sub>d</sub>(x, y) = L (x, y)/(1 + L (x, y))</span><span class="sxs-lookup"><span data-stu-id="f1897-138">L<sub>d</sub>( x, y ) = L( x, y ) / ( 1 + L( x, y ) )</span></span>

<span data-ttu-id="f1897-139">Donde:</span><span class="sxs-lookup"><span data-stu-id="f1897-139">Where:</span></span>

-   <span data-ttu-id="f1897-140">L<sub>d</sub>(x, y): luminancia comprimida y escalada para el píxel (x, y)</span><span class="sxs-lookup"><span data-stu-id="f1897-140">L<sub>d</sub>( x, y ) - compressed and scaled luminance for pixel ( x, y )</span></span>
-   <span data-ttu-id="f1897-141">un valor de clave-Image después de aplicar el ajuste de escala</span><span class="sxs-lookup"><span data-stu-id="f1897-141">a - image key value after applying the scaling</span></span>

<span data-ttu-id="f1897-142">Este operador escala luminances alto en 1/L y luminances inferior en 1.</span><span class="sxs-lookup"><span data-stu-id="f1897-142">This operator scales high luminances by 1/L and low luminances by 1.</span></span> <span data-ttu-id="f1897-143">Para obtener más información, consulte el siguiente documento.</span><span class="sxs-lookup"><span data-stu-id="f1897-143">For more details, see the following paper.</span></span>

<span data-ttu-id="f1897-144">Reinhard, Erik, Mike, Peter Shirley y James Ferwerda.</span><span class="sxs-lookup"><span data-stu-id="f1897-144">Reinhard, Erik, Mike Stark, Peter Shirley, and James Ferwerda.</span></span> <span data-ttu-id="f1897-145">["Reproducción de tonos fotográficos para imágenes digitales"](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf).</span><span class="sxs-lookup"><span data-stu-id="f1897-145">["Photographic Tone Reproduction for Digital Images"](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf).</span></span> <span data-ttu-id="f1897-146">Transacciones ACM en gráficos (TOG), procedimientos de la campaña 29 de la Conferencia sobre gráficos de equipos y técnicas interactivas (SIGGRAPH), PP. 267-276.</span><span class="sxs-lookup"><span data-stu-id="f1897-146">ACM Transactions on Graphics (TOG), Proceedings of the 29th Annual Conference on Computer Graphics and Interactive Techniques (SIGGRAPH), pp. 267-276.</span></span> <span data-ttu-id="f1897-147">Nueva York, NY: ACM Press, 2002.</span><span class="sxs-lookup"><span data-stu-id="f1897-147">New York, NY: ACM Press, 2002.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1897-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f1897-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1897-149">Temas avanzados</span><span class="sxs-lookup"><span data-stu-id="f1897-149">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 




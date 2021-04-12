---
description: Las texturas siempre se dirigen linealmente desde (0,0, 0,0) en la esquina superior izquierda a (1,0, 1,0) en la esquina inferior derecha, tal como se muestra en la siguiente ilustración.
ms.assetid: 16fb04b9-4476-4dbe-a24f-51c0813a7917
title: Filtrado de textura bilineal (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51213e5187c775963de2fa740847d55084c5be2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423455"
---
# <a name="bilinear-texture-filtering-direct3d-9"></a><span data-ttu-id="99226-103">Filtrado de textura bilineal (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="99226-103">Bilinear Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="99226-104">Las texturas siempre se dirigen linealmente desde (0,0, 0,0) en la esquina superior izquierda a (1,0, 1,0) en la esquina inferior derecha, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="99226-104">Textures are always linearly addressed from (0.0, 0.0) at the top-left corner to (1.0, 1.0) at the bottom-right corner, as shown in the following illustration.</span></span>

![Ilustración de textura 4x4 con bloques sólidos de color](images/bilinear-fig7a.png)

<span data-ttu-id="99226-106">Normalmente, las texturas se representan como si estuviesen compuestas de bloques sólidos de color, pero es realmente más correcto pensar en las texturas de la misma manera que debería pensar en la presentación de trama: cada textura se define en el centro exacto de una celda de la cuadrícula, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="99226-106">Textures are usually represented as if they were composed of solid blocks of color, but it's actually more correct to think of textures the same way you should think of the raster display: Each texel is defined at the exact center of a grid cell, as shown in the following illustration.</span></span>

![Ilustración de textura 4x4 con textura definidos en el centro de las celdas de la cuadrícula](images/bilinear-fig7b.png)

<span data-ttu-id="99226-108">Si pide al muestrario de texturas el color de esta textura en coordenadas UV (0,375, 0,375), obtendrá rojo sólido (255, 0,0).</span><span class="sxs-lookup"><span data-stu-id="99226-108">If you ask the texture sampler for this texture's color at UV coordinates (0.375, 0.375) you'll get solid red (255, 0, 0).</span></span> <span data-ttu-id="99226-109">Esto resulta perfecto porque el centro exacto de la celda textura roja está en UV (0,375, 0,375).</span><span class="sxs-lookup"><span data-stu-id="99226-109">That makes perfect sense because the exact center of the red texel cell is at UV (0.375, 0.375).</span></span> <span data-ttu-id="99226-110">¿Qué ocurre si pide al muestreador el color de la textura en UV (0,25, 0,25)?</span><span class="sxs-lookup"><span data-stu-id="99226-110">What if you ask the sampler for the texture's color at UV (0.25, 0.25)?</span></span> <span data-ttu-id="99226-111">Eso no es tan fácil, porque el punto en UV (0,25, 0,25) se encuentra en la esquina exacta de 4 textura.</span><span class="sxs-lookup"><span data-stu-id="99226-111">That's not quite as easy, because the point at UV (0.25, 0.25) lies at the exact corner of 4 texels.</span></span>

<span data-ttu-id="99226-112">El esquema más sencillo es simplemente hacer que la muestra devuelva el color del textura más cercano; Esto se conoce como filtrado de puntos (vea el [muestreo de punto más cercano (Direct3D 9)](nearest-point-sampling.md)) y normalmente no es deseable debido a resultados granulares o bloqueados.</span><span class="sxs-lookup"><span data-stu-id="99226-112">The simplest scheme is simply to have the sampler return the color of the closest texel; this is called Point filtering (see [Nearest-Point Sampling (Direct3D 9)](nearest-point-sampling.md)), and is usually undesirable due to grainy or blocky results.</span></span> <span data-ttu-id="99226-113">Muestreo de puntos nuestra textura en UV (0,25, 0,25) muestra otro problema sutil con filtrado de punto más cercano: hay cuatro textura equidistantes desde el punto de muestreo, por lo que no hay una sola textura más cercana.</span><span class="sxs-lookup"><span data-stu-id="99226-113">Point-sampling our texture at UV (0.25, 0.25) shows another subtle problem with nearest-point filtering: there are four texels equidistant from the sampling point, so there's no single nearest texel.</span></span> <span data-ttu-id="99226-114">Una de esas cuatro textura se elegirá como el color devuelto, pero la selección depende de cómo se redondee la coordenada, lo que puede producir artefactos de desgarro (vea el artículo de muestreo de Nearest-Point en el SDK).</span><span class="sxs-lookup"><span data-stu-id="99226-114">One of those four texels will be chosen as the returned color, but the selection depends on how the coordinate is rounded, which may introduce tearing artifacts (see the Nearest-Point Sampling article in the SDK).</span></span>

<span data-ttu-id="99226-115">Un esquema de filtrado ligeramente más preciso y más común consiste en calcular el promedio ponderado de 4 textura más cercano al punto de muestreo; Esto se denomina filtrado bilineal y el costo computacional adicional suele ser insignificante, ya que esta rutina se implementa en el hardware de gráficos moderno.</span><span class="sxs-lookup"><span data-stu-id="99226-115">A slightly more accurate and more common filtering scheme is to calculate the weighted average of the 4 texels closest to the sampling point; this is called Bilinear filtering, and the extra computational cost is usually negligible because this routine is implemented in modern graphics hardware.</span></span> <span data-ttu-id="99226-116">Estos son los colores que obtenemos en algunos puntos de ejemplo diferentes mediante el filtrado bilineal:</span><span class="sxs-lookup"><span data-stu-id="99226-116">Here are the colors we get at a few different sample points using bilinear filtering:</span></span>


```
UV: (0.5, 0.5)
```



<span data-ttu-id="99226-117">Este punto se encuentra en el borde exacto entre el textura rojo, verde, azul y blanco.</span><span class="sxs-lookup"><span data-stu-id="99226-117">This point is at the exact border between red, green, blue, and white texels.</span></span> <span data-ttu-id="99226-118">El color que devuelve el muestreador es gris:</span><span class="sxs-lookup"><span data-stu-id="99226-118">The color the sampler returns is gray:</span></span>


```
  0.25 * (255, 0, 0)
  0.25 * (0, 255, 0) 
  0.25 * (0, 0, 255) 
## + 0.25 * (255, 255, 255) 
------------------------
= (128, 128, 128)
```




```
UV: (0.5, 0.375)
```



<span data-ttu-id="99226-119">Este punto está en el punto medio del borde entre el textura rojo y el verde.</span><span class="sxs-lookup"><span data-stu-id="99226-119">This point is at the midpoint of the border between red and green texels.</span></span> <span data-ttu-id="99226-120">El color que devuelve la muestra es amarillo-gris (tenga en cuenta que las contribuciones del textura azul y blanco se escalan a 0):</span><span class="sxs-lookup"><span data-stu-id="99226-120">The color the sampler returns is yellow-gray (note that the contributions of the blue and white texels are scaled to 0):</span></span>


```
  0.5 * (255, 0, 0)
  0.5 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (128, 128, 0)
```




```
UV: (0.375, 0.375)
```



<span data-ttu-id="99226-121">Se trata de la dirección del textura rojo, que es el color devuelto (el resto de textura en el cálculo de filtrado se pondera en 0):</span><span class="sxs-lookup"><span data-stu-id="99226-121">This is the address of the red texel, which is the returned color (all other texels in the filtering calculation are weighted to 0):</span></span>


```
  1.0 * (255, 0, 0)
  0.0 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (255, 0, 0)
```



<span data-ttu-id="99226-122">Compare estos cálculos con la siguiente ilustración, que muestra lo que sucede si se realiza el cálculo de filtrado bilineal en cada dirección de textura a través de la textura 4x4.</span><span class="sxs-lookup"><span data-stu-id="99226-122">Compare these calculations against the following illustration, which shows what happens if the bilinear filtering calculation is performed at every texture address across the 4x4 texture.</span></span>

![Ilustración de textura 4x4 con filtrado bilineal realizado en cada dirección de textura](images/bilinear-fig7c.jpg)

## <a name="related-topics"></a><span data-ttu-id="99226-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="99226-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99226-125">Filtrado de textura</span><span class="sxs-lookup"><span data-stu-id="99226-125">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 




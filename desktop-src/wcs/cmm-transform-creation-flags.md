---
title: Indicadores de creación de transformación de CMM
description: CMMs usar marcas de creación de transformación como sugerencias para crear una transformación de color. Depende de la CMM determinar el mejor modo de usar estas marcas.
ms.assetid: f3942929-272c-4f08-98ac-a4d14d2f6ac4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852ef5c080c361bfffb6915d808787d46e63ba5c
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/02/2021
ms.locfileid: "105721163"
---
# <a name="cmm-transform-creation-flags"></a><span data-ttu-id="cec68-104">Indicadores de creación de transformación de CMM</span><span class="sxs-lookup"><span data-stu-id="cec68-104">CMM Transform Creation Flags</span></span>

<span data-ttu-id="cec68-105">CMMs usar marcas de creación de transformación como sugerencias para crear una transformación de color.</span><span class="sxs-lookup"><span data-stu-id="cec68-105">CMMs use transform creation flags as hints for how to create a color transform.</span></span> <span data-ttu-id="cec68-106">Depende de la CMM determinar el mejor modo de usar estas marcas.</span><span class="sxs-lookup"><span data-stu-id="cec68-106">It is up to the CMM to determine how best to use these flags.</span></span>

<span data-ttu-id="cec68-107">Todas las funciones que utilizan estas marcas pasan o reciben valores de marca a través de un parámetro denominado *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="cec68-107">All of the functions that use these flags pass or receive flag values through a parameter called *dwFlags*.</span></span> <span data-ttu-id="cec68-108">La **palabra** de orden superior de *dwFlags* debe establecerse en un valor de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="cec68-108">The high-order **WORD** of *dwFlags* should be set to a value from the following table.</span></span>



| <span data-ttu-id="cec68-109">Constante</span><span class="sxs-lookup"><span data-stu-id="cec68-109">Constant</span></span>                    | <span data-ttu-id="cec68-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cec68-110">Description</span></span>                                                                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cec68-111">HABILITAR la comprobación de la \_ gama \_</span><span class="sxs-lookup"><span data-stu-id="cec68-111">ENABLE\_GAMUT\_CHECKING</span></span>     | <span data-ttu-id="cec68-112">Use esta transformación para la comprobación de la gama.</span><span class="sxs-lookup"><span data-stu-id="cec68-112">Use this transform for gamut checking.</span></span>                                                                                                       |
| <span data-ttu-id="cec68-113">USAR \_ \_ colorimétrico relativo</span><span class="sxs-lookup"><span data-stu-id="cec68-113">USE\_RELATIVE\_COLORIMETRIC</span></span> | <span data-ttu-id="cec68-114">No conserve el punto blanco.</span><span class="sxs-lookup"><span data-stu-id="cec68-114">Do not preserve the white point.</span></span> <span data-ttu-id="cec68-115">Si la gama de salida no admite un color determinado, use el color compatible más cercano.</span><span class="sxs-lookup"><span data-stu-id="cec68-115">If the output gamut does not support a given color, use the nearest supported color.</span></span> <span data-ttu-id="cec68-116">Consulte representación de los intentos.</span><span class="sxs-lookup"><span data-stu-id="cec68-116">See Rendering Intents.</span></span> |
| <span data-ttu-id="cec68-117">\_traducción rápida</span><span class="sxs-lookup"><span data-stu-id="cec68-117">FAST\_TRANSLATE</span></span>             | <span data-ttu-id="cec68-118">Solo buscar color.</span><span class="sxs-lookup"><span data-stu-id="cec68-118">Look up color only.</span></span> <span data-ttu-id="cec68-119">No interpole el color.</span><span class="sxs-lookup"><span data-stu-id="cec68-119">Do not interpolate the color.</span></span>                                                                                            |
| <span data-ttu-id="cec68-120">PRESERVEBLACK</span><span class="sxs-lookup"><span data-stu-id="cec68-120">PRESERVEBLACK</span></span>               | <span data-ttu-id="cec68-121">Inserta la generación de negro adecuada GMMP como el último GMMP de la secuencia de transformación.</span><span class="sxs-lookup"><span data-stu-id="cec68-121">Inserts the appropriate black generation GMMP as the last GMMP in the transform sequence</span></span>                                                     |
| <span data-ttu-id="cec68-122">WCS \_ siempre</span><span class="sxs-lookup"><span data-stu-id="cec68-122">WCS\_ALWAYS</span></span>                 | <span data-ttu-id="cec68-123">Use la ruta de acceso del código WCS incluso para las transformaciones ICC.</span><span class="sxs-lookup"><span data-stu-id="cec68-123">Use the WCS code path even for ICC transforms.</span></span>                                                                                               |
| <span data-ttu-id="cec68-124">\_transformación secuencial</span><span class="sxs-lookup"><span data-stu-id="cec68-124">SEQUENTIAL\_TRANSFORM</span></span>       | <span data-ttu-id="cec68-125">Marca de creación de transformación para crear una transformación de color secuencial (no optimizado).</span><span class="sxs-lookup"><span data-stu-id="cec68-125">Transform creation flag for creating a sequential (non-optimized) color transform.</span></span>                                                           |



 

<span data-ttu-id="cec68-126">La **palabra** de orden inferior puede tener uno de los siguientes valores constantes.</span><span class="sxs-lookup"><span data-stu-id="cec68-126">The low-order **WORD** can have one of the following constant values.</span></span>



| <span data-ttu-id="cec68-127">Constante</span><span class="sxs-lookup"><span data-stu-id="cec68-127">Constant</span></span>     | <span data-ttu-id="cec68-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="cec68-128">Description</span></span>                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cec68-129">modo de prueba \_</span><span class="sxs-lookup"><span data-stu-id="cec68-129">PROOF\_MODE</span></span>  | <span data-ttu-id="cec68-130">La transformación se usará para obtener una vista previa de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cec68-130">Transform will be used to preview the image.</span></span> <span data-ttu-id="cec68-131">Calidad de imagen baja.</span><span class="sxs-lookup"><span data-stu-id="cec68-131">Low image quality.</span></span>                                    |
| <span data-ttu-id="cec68-132">\_modo normal</span><span class="sxs-lookup"><span data-stu-id="cec68-132">NORMAL\_MODE</span></span> | <span data-ttu-id="cec68-133">La transformación se usará para la presentación de imágenes normal.</span><span class="sxs-lookup"><span data-stu-id="cec68-133">Transform will be used for normal image display.</span></span> <span data-ttu-id="cec68-134">Calidad media de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cec68-134">Average image quality.</span></span>                            |
| <span data-ttu-id="cec68-135">MEJOR \_ modo</span><span class="sxs-lookup"><span data-stu-id="cec68-135">BEST\_MODE</span></span>   | <span data-ttu-id="cec68-136">La transformación se usará para mostrar la imagen de mayor calidad posible en el dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="cec68-136">Transform will be used for the display of the highest-quality image possible on the target device.</span></span> |



 

<span data-ttu-id="cec68-137">Al pasar del \_ modo de prueba al \_ modo mejor, la calidad de salida suele mejorar y transformar la disminución de velocidad.</span><span class="sxs-lookup"><span data-stu-id="cec68-137">Moving from PROOF\_MODE to BEST\_MODE, output quality generally improves and transform speed declines.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cec68-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cec68-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cec68-139">Conceptos básicos de la administración del color</span><span class="sxs-lookup"><span data-stu-id="cec68-139">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="cec68-140">Constantes de ICM</span><span class="sxs-lookup"><span data-stu-id="cec68-140">ICM Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 





---
description: Las marcas siguientes se usan para especificar los canales de una textura en los que se va a operar.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c83fd0b3e12d6b5bccb13f9c5fab5e078587dbd4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342870"
---
# <a name="d3dx_filter"></a><span data-ttu-id="01f7b-103">FILTRO \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="01f7b-103">D3DX\_FILTER</span></span>

<span data-ttu-id="01f7b-104">Las marcas siguientes se usan para especificar los canales de una textura en los que se va a operar.</span><span class="sxs-lookup"><span data-stu-id="01f7b-104">The following flags are used to specify which channels in a texture to operate on.</span></span>



| <span data-ttu-id="01f7b-105">\#Definir</span><span class="sxs-lookup"><span data-stu-id="01f7b-105">\#define</span></span>                | <span data-ttu-id="01f7b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="01f7b-106">Description</span></span>                                                                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01f7b-107">D3DX \_ FILTER \_ NONE</span><span class="sxs-lookup"><span data-stu-id="01f7b-107">D3DX\_FILTER\_NONE</span></span>      | <span data-ttu-id="01f7b-108">No se realizará ningún escalado ni filtrado.</span><span class="sxs-lookup"><span data-stu-id="01f7b-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="01f7b-109">Se supone que los píxeles fuera de los límites de la imagen de origen son de color negro transparente.</span><span class="sxs-lookup"><span data-stu-id="01f7b-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>                                                                                 |
| <span data-ttu-id="01f7b-110">PUNTO DE FILTRO \_ \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="01f7b-110">D3DX\_FILTER\_POINT</span></span>     | <span data-ttu-id="01f7b-111">Cada píxel de destino se calcula mediante el muestreo del píxel más cercano de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="01f7b-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>                                                                                                                     |
| <span data-ttu-id="01f7b-112">D3DX \_ FILTER \_ LINEAR</span><span class="sxs-lookup"><span data-stu-id="01f7b-112">D3DX\_FILTER\_LINEAR</span></span>    | <span data-ttu-id="01f7b-113">Cada píxel de destino se calcula mediante el muestreo de los cuatro píxeles más cercanos de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="01f7b-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="01f7b-114">Este filtro funciona mejor cuando la escala en ambos ejes es menor que dos.</span><span class="sxs-lookup"><span data-stu-id="01f7b-114">This filter works best when the scale on both axes is less than two.</span></span>                                          |
| <span data-ttu-id="01f7b-115">TRIÁNGULO DE FILTRO \_ \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="01f7b-115">D3DX\_FILTER\_TRIANGLE</span></span>  | <span data-ttu-id="01f7b-116">Cada píxel de la imagen de origen contribuye igualmente a la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="01f7b-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="01f7b-117">Este es el más lento de los filtros.</span><span class="sxs-lookup"><span data-stu-id="01f7b-117">This is the slowest of the filters.</span></span>                                                                                           |
| <span data-ttu-id="01f7b-118">CUADRO DE FILTRO \_ \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="01f7b-118">D3DX\_FILTER\_BOX</span></span>       | <span data-ttu-id="01f7b-119">Cada píxel se calcula calcula calculando un promedio de un cuadro de 2 x 2 (x2) de píxeles a partir de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="01f7b-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="01f7b-120">Este filtro solo funciona cuando las dimensiones del destino son la mitad de las del origen, como es el caso de los mapas mip.</span><span class="sxs-lookup"><span data-stu-id="01f7b-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span> |
| <span data-ttu-id="01f7b-121">REFLEJO DEL FILTRO D3DX \_ \_ \_ U</span><span class="sxs-lookup"><span data-stu-id="01f7b-121">D3DX\_FILTER\_MIRROR\_U</span></span> | <span data-ttu-id="01f7b-122">Los píxeles del borde de la textura en el eje U deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="01f7b-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="01f7b-123">D3DX \_ FILTER \_ MIRROR \_ V</span><span class="sxs-lookup"><span data-stu-id="01f7b-123">D3DX\_FILTER\_MIRROR\_V</span></span> | <span data-ttu-id="01f7b-124">Los píxeles del borde de la textura en el eje v deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="01f7b-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="01f7b-125">D3DX \_ FILTER \_ MIRROR \_ W</span><span class="sxs-lookup"><span data-stu-id="01f7b-125">D3DX\_FILTER\_MIRROR\_W</span></span> | <span data-ttu-id="01f7b-126">Los píxeles del borde de la textura en el eje w deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="01f7b-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="01f7b-127">REFLEJO DEL FILTRO D3DX \_ \_</span><span class="sxs-lookup"><span data-stu-id="01f7b-127">D3DX\_FILTER\_MIRROR</span></span>    | <span data-ttu-id="01f7b-128">Especificar esta marca es lo mismo que especificar las marcas D3DX \_ FILTER \_ MIRROR \_ U, D3DX FILTER MIRROR V y \_ \_ \_ D3DX \_ FILTER MIRROR \_ \_ W.</span><span class="sxs-lookup"><span data-stu-id="01f7b-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>                                                                     |
| <span data-ttu-id="01f7b-129">D3DX \_ FILTER \_ DITHER</span><span class="sxs-lookup"><span data-stu-id="01f7b-129">D3DX\_FILTER\_DITHER</span></span>    | <span data-ttu-id="01f7b-130">La imagen resultante debe estar entrelazada mediante un algoritmo de dither ordenado de 4x4.</span><span class="sxs-lookup"><span data-stu-id="01f7b-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span>                                                                                                                                  |
| <span data-ttu-id="01f7b-131">FILTRO D3DX \_ \_ SRGB \_ IN</span><span class="sxs-lookup"><span data-stu-id="01f7b-131">D3DX\_FILTER\_SRGB\_IN</span></span>  | <span data-ttu-id="01f7b-132">Los datos de entrada están en el espacio de colores sRGB (gamma 2.2).</span><span class="sxs-lookup"><span data-stu-id="01f7b-132">Input data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                              |
| <span data-ttu-id="01f7b-133">D3DX \_ FILTER \_ SRGB \_ OUT</span><span class="sxs-lookup"><span data-stu-id="01f7b-133">D3DX\_FILTER\_SRGB\_OUT</span></span> | <span data-ttu-id="01f7b-134">Los datos de salida están en el espacio de colores sRGB (gamma 2.2).</span><span class="sxs-lookup"><span data-stu-id="01f7b-134">The output data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                         |
| <span data-ttu-id="01f7b-135">D3DX \_ FILTER \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="01f7b-135">D3DX\_FILTER\_SRGB</span></span>      | <span data-ttu-id="01f7b-136">Igual que especificar D3DX \_ FILTER \_ SRGB \_ IN \| D3DX \_ FILTER \_ SRGB \_ OUT.</span><span class="sxs-lookup"><span data-stu-id="01f7b-136">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span>                                                                                                                                       |



 

<span data-ttu-id="01f7b-137">Cada filtro válido debe contener exactamente una de las marcas siguientes: D3DX \_ FILTER \_ NONE, D3DX \_ FILTER \_ POINT, D3DX \_ FILTER \_ LINEAR, D3DX FILTER TRIANGLE o \_ \_ D3DX \_ FILTER \_ BOX.</span><span class="sxs-lookup"><span data-stu-id="01f7b-137">Each valid filter must contain exactly one of the following flags: D3DX\_FILTER\_NONE, D3DX\_FILTER\_POINT, D3DX\_FILTER\_LINEAR, D3DX\_FILTER\_TRIANGLE, or D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="01f7b-138">Además, puede usar el operador OR para especificar cero o más de las siguientes marcas opcionales con un filtro válido: D3DX \_ FILTER \_ MIRROR \_ U, D3DX \_ FILTER MIRROR \_ \_ V, D3DX \_ FILTER MIRROR \_ \_ W, D3DX \_ FILTER MIRROR \_ W, D3DX \_ FILTER \_ DITHER, D3DX \_ FILTER \_ SRGB \_ IN, D3DX FILTER SRGB OUT o \_ \_ \_ D3DX \_ FILTER \_ SRGB.</span><span class="sxs-lookup"><span data-stu-id="01f7b-138">In addition, you can use the OR operator to specify zero or more of the following optional flags with a valid filter: D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, D3DX\_FILTER\_MIRROR\_W, D3DX\_FILTER\_MIRROR, D3DX\_FILTER\_DITHER, D3DX\_FILTER\_SRGB\_IN, D3DX\_FILTER\_SRGB\_OUT or D3DX\_FILTER\_SRGB.</span></span>

<span data-ttu-id="01f7b-139">Especificar D3DX DEFAULT para este parámetro suele ser equivalente a especificar \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.</span><span class="sxs-lookup"><span data-stu-id="01f7b-139">Specifying D3DX\_DEFAULT for this parameter is usually the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="01f7b-140">Sin embargo, D3DX \_ DEFAULT puede tener significados diferentes, dependiendo del método que use el filtro.</span><span class="sxs-lookup"><span data-stu-id="01f7b-140">However, D3DX\_DEFAULT can have different meanings, depending on which method uses the filter.</span></span> <span data-ttu-id="01f7b-141">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="01f7b-141">For example:</span></span>

-   <span data-ttu-id="01f7b-142">Al usar [**D3DXCreateTextureFromFileEx,**](d3dxcreatetexturefromfileex.md)D3DX DEFAULT se asigna a \_ D3DX \_ FILTER TRIANGLE \_ \| D3DX \_ FILTER \_ DITHER.</span><span class="sxs-lookup"><span data-stu-id="01f7b-142">When using [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>
-   <span data-ttu-id="01f7b-143">Cuando se [**usa D3DXFilterTexture,**](d3dxfiltertexture.md)D3DX DEFAULT se asigna a D3DX FILTER BOX si el tamaño de textura es una potencia de dos \_ y \_ \_ D3DX \_ FILTER BOX \_ \| D3DX \_ FILTER DITHER \_ en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="01f7b-143">When using [**D3DXFilterTexture**](d3dxfiltertexture.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

<span data-ttu-id="01f7b-144">Haga referencia a cada método para buscar información sobre cómo se asigna el \_ filtro D3DX DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="01f7b-144">Reference each method to check for information about how D3DX\_DEFAULT filter is mapped.</span></span>

## <a name="constant-information"></a><span data-ttu-id="01f7b-145">Información constante</span><span class="sxs-lookup"><span data-stu-id="01f7b-145">Constant Information</span></span>



| <span data-ttu-id="01f7b-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="01f7b-146">Requirement</span></span>                         | <span data-ttu-id="01f7b-147">Value</span><span class="sxs-lookup"><span data-stu-id="01f7b-147">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="01f7b-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01f7b-148">Header</span></span>                   | <span data-ttu-id="01f7b-149">d3dx9tex.h</span><span class="sxs-lookup"><span data-stu-id="01f7b-149">d3dx9tex.h</span></span> |
| <span data-ttu-id="01f7b-150">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="01f7b-150">Minimum operating system</span></span> | <span data-ttu-id="01f7b-151">Windows 98</span><span class="sxs-lookup"><span data-stu-id="01f7b-151">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="01f7b-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01f7b-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01f7b-153">Constantes D3DX</span><span class="sxs-lookup"><span data-stu-id="01f7b-153">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 




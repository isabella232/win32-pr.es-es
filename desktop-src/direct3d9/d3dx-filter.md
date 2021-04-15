---
description: Las marcas siguientes se usan para especificar en qué canales de una textura se va a operar.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 128525de2e403c11239c300372b79bd8ee8c1277
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494734"
---
# <a name="d3dx_filter"></a><span data-ttu-id="e77e4-103">Filtro de D3DX \_</span><span class="sxs-lookup"><span data-stu-id="e77e4-103">D3DX\_FILTER</span></span>

<span data-ttu-id="e77e4-104">Las marcas siguientes se usan para especificar en qué canales de una textura se va a operar.</span><span class="sxs-lookup"><span data-stu-id="e77e4-104">The following flags are used to specify which channels in a texture to operate on.</span></span>



|                         |                                                                                                                                                                                                             |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e77e4-105">\#define</span><span class="sxs-lookup"><span data-stu-id="e77e4-105">\#define</span></span>                | <span data-ttu-id="e77e4-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="e77e4-106">Description</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="e77e4-107">D3DX \_ Filter \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="e77e4-107">D3DX\_FILTER\_NONE</span></span>      | <span data-ttu-id="e77e4-108">No se llevará a cabo ningún ajuste de escala o filtro.</span><span class="sxs-lookup"><span data-stu-id="e77e4-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="e77e4-109">Se supone que los píxeles que están fuera de los límites de la imagen de origen son negros transparentes.</span><span class="sxs-lookup"><span data-stu-id="e77e4-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>                                                                                 |
| <span data-ttu-id="e77e4-110">\_Punto de filtro de D3DX \_</span><span class="sxs-lookup"><span data-stu-id="e77e4-110">D3DX\_FILTER\_POINT</span></span>     | <span data-ttu-id="e77e4-111">Cada píxel de destino se calcula mediante el muestreo del píxel más cercano de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="e77e4-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>                                                                                                                     |
| <span data-ttu-id="e77e4-112">\_Filtro \_ lineal de D3DX</span><span class="sxs-lookup"><span data-stu-id="e77e4-112">D3DX\_FILTER\_LINEAR</span></span>    | <span data-ttu-id="e77e4-113">Cada píxel de destino se calcula mediante el muestreo de los cuatro píxeles más cercanos de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="e77e4-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="e77e4-114">Este filtro funciona mejor cuando la escala en ambos ejes es menor que dos.</span><span class="sxs-lookup"><span data-stu-id="e77e4-114">This filter works best when the scale on both axes is less than two.</span></span>                                          |
| <span data-ttu-id="e77e4-115">\_Triángulo de filtro de D3DX \_</span><span class="sxs-lookup"><span data-stu-id="e77e4-115">D3DX\_FILTER\_TRIANGLE</span></span>  | <span data-ttu-id="e77e4-116">Cada píxel de la imagen de origen contribuye igualmente a la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="e77e4-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="e77e4-117">Este es el más lento de los filtros.</span><span class="sxs-lookup"><span data-stu-id="e77e4-117">This is the slowest of the filters.</span></span>                                                                                           |
| <span data-ttu-id="e77e4-118">\_Cuadro de filtro de D3DX \_</span><span class="sxs-lookup"><span data-stu-id="e77e4-118">D3DX\_FILTER\_BOX</span></span>       | <span data-ttu-id="e77e4-119">Cada píxel se calcula calculando el promedio de un cuadro 2x2 (x2) de píxeles de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="e77e4-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="e77e4-120">Este filtro solo funciona cuando las dimensiones del destino son la mitad de las del origen, como sucede con los mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="e77e4-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span> |
| <span data-ttu-id="e77e4-121">Reflejo de filtro de D3DX \_ \_ \_ U</span><span class="sxs-lookup"><span data-stu-id="e77e4-121">D3DX\_FILTER\_MIRROR\_U</span></span> | <span data-ttu-id="e77e4-122">Los píxeles que están fuera del borde de la textura en el eje u deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="e77e4-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="e77e4-123">Espejo del filtro de D3DX \_ \_ \_ V</span><span class="sxs-lookup"><span data-stu-id="e77e4-123">D3DX\_FILTER\_MIRROR\_V</span></span> | <span data-ttu-id="e77e4-124">Los píxeles que están fuera del borde de la textura en el eje v deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="e77e4-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="e77e4-125">Reflejo del filtro de D3DX \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="e77e4-125">D3DX\_FILTER\_MIRROR\_W</span></span> | <span data-ttu-id="e77e4-126">Los píxeles que están fuera del borde de la textura en el eje w deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="e77e4-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="e77e4-127">\_Reflejo del filtro de D3DX \_</span><span class="sxs-lookup"><span data-stu-id="e77e4-127">D3DX\_FILTER\_MIRROR</span></span>    | <span data-ttu-id="e77e4-128">La especificación de esta marca es la misma que la especificación de las marcas de la imagen reflejada del filtro de D3DX U, de la versión reflejada del filtro de d3dx \_ \_ \_ \_ \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e77e4-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>                                                                     |
| <span data-ttu-id="e77e4-129">\_Interpolación de filtros de D3DX \_</span><span class="sxs-lookup"><span data-stu-id="e77e4-129">D3DX\_FILTER\_DITHER</span></span>    | <span data-ttu-id="e77e4-130">La imagen resultante debe ser interpolada mediante un algoritmo de tramado ordenado de 4x4.</span><span class="sxs-lookup"><span data-stu-id="e77e4-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span>                                                                                                                                  |
| <span data-ttu-id="e77e4-131">El \_ filtro \_ de D3DX está \_ en sRGB</span><span class="sxs-lookup"><span data-stu-id="e77e4-131">D3DX\_FILTER\_SRGB\_IN</span></span>  | <span data-ttu-id="e77e4-132">Los datos de entrada están en el espacio de colores sRGB (gamma 2,2).</span><span class="sxs-lookup"><span data-stu-id="e77e4-132">Input data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                              |
| <span data-ttu-id="e77e4-133">Filtro de D3DX de \_ \_ \_ salida sRGB</span><span class="sxs-lookup"><span data-stu-id="e77e4-133">D3DX\_FILTER\_SRGB\_OUT</span></span> | <span data-ttu-id="e77e4-134">Los datos de salida están en el espacio de colores sRGB (gamma 2,2).</span><span class="sxs-lookup"><span data-stu-id="e77e4-134">The output data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                         |
| <span data-ttu-id="e77e4-135">Filtro de D3DX \_ \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="e77e4-135">D3DX\_FILTER\_SRGB</span></span>      | <span data-ttu-id="e77e4-136">Igual que al especificar el \_ filtro de d3dx \_ sRGB \_ en el \| filtro de d3dx \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e77e4-136">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span>                                                                                                                                       |



 

<span data-ttu-id="e77e4-137">Cada filtro válido debe contener exactamente una de las marcas siguientes: el \_ filtro \_ de d3dx no, el \_ \_ punto de filtro de d3dx, el filtro de d3dx \_ \_ lineal, el triángulo de filtro de d3dx \_ o el \_ cuadro de filtro de d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e77e4-137">Each valid filter must contain exactly one of the following flags: D3DX\_FILTER\_NONE, D3DX\_FILTER\_POINT, D3DX\_FILTER\_LINEAR, D3DX\_FILTER\_TRIANGLE, or D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="e77e4-138">Además, puede usar el operador OR para especificar cero o más de las siguientes marcas opcionales con un filtro válido: el filtro de D3DX de la versión u, el reflejado del filtro de d3dx, el filtro de d3dx, el filtro de d3dx y el filtro de d3dx \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e77e4-138">In addition, you can use the OR operator to specify zero or more of the following optional flags with a valid filter: D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, D3DX\_FILTER\_MIRROR\_W, D3DX\_FILTER\_MIRROR, D3DX\_FILTER\_DITHER, D3DX\_FILTER\_SRGB\_IN, D3DX\_FILTER\_SRGB\_OUT or D3DX\_FILTER\_SRGB.</span></span>

<span data-ttu-id="e77e4-139">Especificar \_ el valor predeterminado de d3dx para este parámetro suele ser el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e77e4-139">Specifying D3DX\_DEFAULT for this parameter is usually the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="e77e4-140">Sin embargo, \_ el valor predeterminado de D3DX puede tener distintos significados, en función del método que use el filtro.</span><span class="sxs-lookup"><span data-stu-id="e77e4-140">However, D3DX\_DEFAULT can have different meanings, depending on which method uses the filter.</span></span> <span data-ttu-id="e77e4-141">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e77e4-141">For example:</span></span>

-   <span data-ttu-id="e77e4-142">Cuando se usa [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), el \_ valor predeterminado de d3dx se asigna al filtro de d3dx Triangle del filtro de d3dx \_ \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e77e4-142">When using [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>
-   <span data-ttu-id="e77e4-143">Cuando se usa [**D3DXFilterTexture**](d3dxfiltertexture.md), \_ el valor predeterminado de d3dx se asigna al cuadro de filtro de d3dx \_ \_ si el tamaño de la textura es una potencia de dos, y el filtro de d3dx del \_ cuadro de filtro de \_ \| d3dx \_ \_ en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e77e4-143">When using [**D3DXFilterTexture**](d3dxfiltertexture.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

<span data-ttu-id="e77e4-144">Haga referencia a cada método para comprobar la información sobre cómo \_ se asigna el filtro predeterminado de D3DX.</span><span class="sxs-lookup"><span data-stu-id="e77e4-144">Reference each method to check for information about how D3DX\_DEFAULT filter is mapped.</span></span>

## <a name="constant-information"></a><span data-ttu-id="e77e4-145">Información constante</span><span class="sxs-lookup"><span data-stu-id="e77e4-145">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="e77e4-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e77e4-146">Header</span></span>                   | <span data-ttu-id="e77e4-147">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="e77e4-147">d3dx9tex.h</span></span> |
| <span data-ttu-id="e77e4-148">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="e77e4-148">Minimum operating system</span></span> | <span data-ttu-id="e77e4-149">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e77e4-149">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e77e4-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e77e4-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e77e4-151">Constantes de D3DX</span><span class="sxs-lookup"><span data-stu-id="e77e4-151">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 




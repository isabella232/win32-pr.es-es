---
title: Trasladar llamadas de color
description: En la tabla siguiente se enumeran las funciones de color de GL de IRIS y sus funciones de OpenGL equivalentes.
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- Puerto de GL de IRIS, color
- portabilidad de IRIS GL, color
- trasladar a OpenGL desde IRIS GL, color
- Exportación de OpenGL desde IRIS GL, color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856b9f9d0a62b866ac1c9981d9fbb716cf243341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773999"
---
# <a name="porting-color-calls"></a><span data-ttu-id="c930a-107">Trasladar llamadas de color</span><span class="sxs-lookup"><span data-stu-id="c930a-107">Porting Color Calls</span></span>

<span data-ttu-id="c930a-108">En la tabla siguiente se enumeran las funciones de color de GL de IRIS y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="c930a-108">The following table lists IRIS GL color functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="c930a-109">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="c930a-109">IRIS GL function</span></span>                  | <span data-ttu-id="c930a-110">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="c930a-110">OpenGL function</span></span>                                                                                                                               | <span data-ttu-id="c930a-111">Significado</span><span class="sxs-lookup"><span data-stu-id="c930a-111">Meaning</span></span>                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c930a-112">**c**</span><span class="sxs-lookup"><span data-stu-id="c930a-112">**c**</span></span>                             | [<span data-ttu-id="c930a-113">glColor</span><span class="sxs-lookup"><span data-stu-id="c930a-113">glColor</span></span>](glcolor-functions.md)                                                                                                              | <span data-ttu-id="c930a-114">Establece el color RGB.</span><span class="sxs-lookup"><span data-stu-id="c930a-114">Sets RGB color.</span></span>                                      |
| <span data-ttu-id="c930a-115">**color**</span><span class="sxs-lookup"><span data-stu-id="c930a-115">**color**</span></span>                         | [<span data-ttu-id="c930a-116">glIndex</span><span class="sxs-lookup"><span data-stu-id="c930a-116">glIndex</span></span>](glindex-functions.md)                                                                                                              | <span data-ttu-id="c930a-117">Establece el índice de color.</span><span class="sxs-lookup"><span data-stu-id="c930a-117">Sets the color index.</span></span>                                |
| <span data-ttu-id="c930a-118">**GetColor**</span><span class="sxs-lookup"><span data-stu-id="c930a-118">**getcolor**</span></span>                      | <span data-ttu-id="c930a-119">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ índice actual de contabilidad \_ )</span><span class="sxs-lookup"><span data-stu-id="c930a-119">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_CURRENT\_INDEX )</span></span>                                               | <span data-ttu-id="c930a-120">Devuelve el índice de color actual.</span><span class="sxs-lookup"><span data-stu-id="c930a-120">Returns the current color index.</span></span>                     |
| <span data-ttu-id="c930a-121">**getmcolor**</span><span class="sxs-lookup"><span data-stu-id="c930a-121">**getmcolor**</span></span>                     |                                                                                                                                               | <span data-ttu-id="c930a-122">Obtiene una copia de los valores RGB para una entrada de mapa de color.</span><span class="sxs-lookup"><span data-stu-id="c930a-122">Gets a copy of the RGB values for a color map entry.</span></span> |
| <span data-ttu-id="c930a-123">**gRGBcolor**</span><span class="sxs-lookup"><span data-stu-id="c930a-123">**gRGBcolor**</span></span>                     | <span data-ttu-id="c930a-124">**glGet**( \_ color actual de GL \_ )</span><span class="sxs-lookup"><span data-stu-id="c930a-124">**glGet**( GL\_CURRENT\_COLOR )</span></span>                                                                                                               | <span data-ttu-id="c930a-125">Obtiene los valores de color RGB actuales.</span><span class="sxs-lookup"><span data-stu-id="c930a-125">Gets the current RGB color values.</span></span>                   |
| <span data-ttu-id="c930a-126">**mapcolor**</span><span class="sxs-lookup"><span data-stu-id="c930a-126">**mapcolor**</span></span>                      |                                                                                                                                               |                                                      |
| <span data-ttu-id="c930a-127">**RGBcolor**</span><span class="sxs-lookup"><span data-stu-id="c930a-127">**RGBcolor**</span></span>                      | <span data-ttu-id="c930a-128">**glColor**</span><span class="sxs-lookup"><span data-stu-id="c930a-128">**glColor**</span></span>                                                                                                                                   | <span data-ttu-id="c930a-129">Establece el color RGB.</span><span class="sxs-lookup"><span data-stu-id="c930a-129">Sets RGB color.</span></span>                                      |
| <span data-ttu-id="c930a-130">**writemask**</span><span class="sxs-lookup"><span data-stu-id="c930a-130">**writemask**</span></span>                     | [<span data-ttu-id="c930a-131">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="c930a-131">**glIndexMask**</span></span>](glindexmask.md)                                                                                                            | <span data-ttu-id="c930a-132">Establece la máscara de color del modo de índice de color.</span><span class="sxs-lookup"><span data-stu-id="c930a-132">Sets the color-index mode color mask.</span></span>                |
| <span data-ttu-id="c930a-133">**wmpackRGBwritemask**</span><span class="sxs-lookup"><span data-stu-id="c930a-133">**wmpackRGBwritemask**</span></span><br/> | [<span data-ttu-id="c930a-134">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="c930a-134">**glColorMask**</span></span>](glcolormask.md)                                                                                                            | <span data-ttu-id="c930a-135">Establece la máscara del modo de color RGB.</span><span class="sxs-lookup"><span data-stu-id="c930a-135">Sets the RGB color mode mask.</span></span>                        |
| <span data-ttu-id="c930a-136">**getwritemask**</span><span class="sxs-lookup"><span data-stu-id="c930a-136">**getwritemask**</span></span>                  | <span data-ttu-id="c930a-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL \_ color \_ WRITEMASK)**glGet**(GL \_ index \_ WRITEMASK)</span><span class="sxs-lookup"><span data-stu-id="c930a-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_COLOR\_WRITEMASK )**glGet**( GL\_INDEX\_WRITEMASK )</span></span><br/> | <span data-ttu-id="c930a-138">Obtiene la máscara de color.</span><span class="sxs-lookup"><span data-stu-id="c930a-138">Gets the color mask.</span></span>                                 |
| <span data-ttu-id="c930a-139">**gRGBmask**</span><span class="sxs-lookup"><span data-stu-id="c930a-139">**gRGBmask**</span></span>                      | <span data-ttu-id="c930a-140">**glGet**(GL \_ color \_ WRITEMASK)</span><span class="sxs-lookup"><span data-stu-id="c930a-140">**glGet**( GL\_COLOR\_WRITEMASK )</span></span>                                                                                                             | <span data-ttu-id="c930a-141">Obtiene la máscara de color.</span><span class="sxs-lookup"><span data-stu-id="c930a-141">Gets the color mask.</span></span>                                 |
| <span data-ttu-id="c930a-142">**zwritemask**</span><span class="sxs-lookup"><span data-stu-id="c930a-142">**zwritemask**</span></span>                    | [<span data-ttu-id="c930a-143">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="c930a-143">**glDepthMask**</span></span>](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> <span data-ttu-id="c930a-144">Tenga cuidado al sustituir **zwritemask** por [**glDepthMask**](gldepthmask.md); **glDepthMask** toma un argumento booleano, mientras que **zwritemask** toma un campo de bits.</span><span class="sxs-lookup"><span data-stu-id="c930a-144">Be careful when replacing **zwritemask** with [**glDepthMask**](gldepthmask.md); **glDepthMask** takes a Boolean argument, whereas **zwritemask** takes a bit field.</span></span>

 

<span data-ttu-id="c930a-145">Si desea usar varias asignaciones de color, debe usar las funciones de mapa de colores de Windows adecuadas.</span><span class="sxs-lookup"><span data-stu-id="c930a-145">If you want to use multiple color maps, you need to use the appropriate Windows color map functions.</span></span> <span data-ttu-id="c930a-146">Por lo tanto, **Multimap**, **onemap**, **getcmmode**, **setmap** y **GetMap** no tienen equivalentes de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="c930a-146">Therefore, **multimap**, **onemap**, **getcmmode**, **setmap**, and **getmap** have no OpenGL equivalents.</span></span>

 

 






---
description: Los volúmenes de sombra se usan para dibujar sombras con el búfer de estarcido.
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: Two-Sided Galería de símbolos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b238c4b778b9894029764032e76b60c476a891a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714772"
---
# <a name="two-sided-stencil-direct3d-9"></a><span data-ttu-id="9185c-103">Two-Sided Galería de símbolos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9185c-103">Two-Sided Stencil (Direct3D 9)</span></span>

<span data-ttu-id="9185c-104">Los volúmenes de sombra se usan para dibujar sombras con el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="9185c-104">Shadow Volumes are used for drawing shadows with the stencil buffer.</span></span> <span data-ttu-id="9185c-105">La aplicación calcula los volúmenes de sombra convertidos por geometría occluding, mediante el cálculo de los bordes de la silueta y la extrusión de la luz en un conjunto de volúmenes 3D.</span><span class="sxs-lookup"><span data-stu-id="9185c-105">The application computes the shadow volumes cast by occluding geometry, by computing the silhouette edges and extruding them away from the light into a set of 3D volumes.</span></span> <span data-ttu-id="9185c-106">A continuación, estos volúmenes se representan dos veces en el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="9185c-106">These volumes are then rendered twice into the stencil buffer.</span></span>

<span data-ttu-id="9185c-107">La primera representación dibuja polígonos hacia delante e incrementa los valores del búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="9185c-107">The first render draws forward-facing polygons, and increments the stencil-buffer values.</span></span> <span data-ttu-id="9185c-108">La segunda representación dibuja los polígonos hacia delante del volumen de instantáneas y disminuye los valores de búfer de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="9185c-108">The second render draws the back-facing polygons of the shadow volume, and decrements the stencil buffer values.</span></span> <span data-ttu-id="9185c-109">Normalmente, todos los valores incrementados y disminuidos se cancelan entre sí. Sin embargo, la escena ya se representó con geometría normal, lo que provoca que algunos píxeles no superen la prueba de búfer z mientras se representa el volumen de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="9185c-109">Normally, all incremented and decremented values cancel each other out. However, the scene was already rendered with normal geometry causing some pixels to fail the z-buffer test as the shadow volume is rendered.</span></span> <span data-ttu-id="9185c-110">Los valores que quedan en el búfer de estarcido se corresponden con los píxeles que están en la sombra.</span><span class="sxs-lookup"><span data-stu-id="9185c-110">Values left in the stencil buffer correspond to pixels that are in the shadow.</span></span> <span data-ttu-id="9185c-111">El resto del contenido del búfer de la galería de símbolos se usa como máscara, para que la combinación de alfa sea una gran cantidad de color negro que abarque a la escena.</span><span class="sxs-lookup"><span data-stu-id="9185c-111">These remaining stencil-buffer contents are used as a mask, to alpha-blend a large, all-encompassing black quad into the scene.</span></span> <span data-ttu-id="9185c-112">Con el búfer de estarcido que actúa como máscara, el resultado es oscurecer los píxeles que se encuentran en las sombras.</span><span class="sxs-lookup"><span data-stu-id="9185c-112">With the stencil buffer acting as a mask, the result is to darken pixels that are in the shadows.</span></span>

<span data-ttu-id="9185c-113">Esto significa que la geometría de la sombra se dibuja dos veces por origen de la luz, por lo que se pone presión sobre el rendimiento de los vértices de la GPU.</span><span class="sxs-lookup"><span data-stu-id="9185c-113">This means that the shadow geometry is drawn twice per light source, hence putting pressure on the vertex throughput of the GPU.</span></span> <span data-ttu-id="9185c-114">La característica de galería de símbolos de dos caras se ha diseñado para mitigar esta situación.</span><span class="sxs-lookup"><span data-stu-id="9185c-114">The two-sided stencil feature has been designed to mitigate this situation.</span></span> <span data-ttu-id="9185c-115">En este enfoque, hay dos conjuntos de estado de la galería de símbolos (denominados a continuación), uno para cada uno de los triángulos orientados delante y otro para los triángulos de cara a la inversa.</span><span class="sxs-lookup"><span data-stu-id="9185c-115">In this approach, there are two sets of stencil state (named below), one set each for the front-facing triangles and the other for the back-facing triangles.</span></span> <span data-ttu-id="9185c-116">De este modo, solo se dibuja un único paso por volumen de instantánea, por luz.</span><span class="sxs-lookup"><span data-stu-id="9185c-116">This way, only a single pass is drawn per shadow volume, per light.</span></span>

<span data-ttu-id="9185c-117">Los cambios de la API se restringen a un nuevo conjunto de Estados de representación.</span><span class="sxs-lookup"><span data-stu-id="9185c-117">The API changes are restricted to a new set of render states.</span></span> <span data-ttu-id="9185c-118">El nuevo estado de representación D3DRS \_ dos \_ \_ StencilMODE se puede establecer en **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="9185c-118">The new render state D3DRS\_Two\_Sided\_StencilMODE can be set to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="9185c-119">Es **false** de forma predeterminada, lo que significa que es el comportamiento actual (DirectX 8).</span><span class="sxs-lookup"><span data-stu-id="9185c-119">It is **FALSE** by default, meaning current (DirectX 8) behavior.</span></span> <span data-ttu-id="9185c-120">Cuando se establece en **true** (solo funcionará si \_ se establece D3DSTENCILCAPS TWOSIDED), los siguientes Estados de representación solo se aplicarán a los triángulos orientados hacia delante (en el sentido de las agujas del reloj).</span><span class="sxs-lookup"><span data-stu-id="9185c-120">When this is set to **TRUE** (it will work only if D3DSTENCILCAPS\_TWOSIDED is set), the following render states will apply only to the front-facing (clockwise) triangles.</span></span>



| <span data-ttu-id="9185c-121">Estado de representación</span><span class="sxs-lookup"><span data-stu-id="9185c-121">Render state</span></span>        | <span data-ttu-id="9185c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="9185c-122">Description</span></span>                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9185c-123">D3DRS \_ STENCILFAIL</span><span class="sxs-lookup"><span data-stu-id="9185c-123">D3DRS\_STENCILFAIL</span></span>  | <span data-ttu-id="9185c-124">D3DSTENCILOP si se produce un error en la prueba de estarcido.</span><span class="sxs-lookup"><span data-stu-id="9185c-124">D3DSTENCILOP to do if stencil test fails.</span></span>                                                |
| <span data-ttu-id="9185c-125">D3DRS \_ STENCILZFAIL</span><span class="sxs-lookup"><span data-stu-id="9185c-125">D3DRS\_STENCILZFAIL</span></span> | <span data-ttu-id="9185c-126">D3DSTENCILOP si se supera la prueba de estarcido y se produce un error en la prueba z.</span><span class="sxs-lookup"><span data-stu-id="9185c-126">D3DSTENCILOP to do if stencil test passes and z-test fails.</span></span>                              |
| <span data-ttu-id="9185c-127">D3DRS \_ STENCILPASS</span><span class="sxs-lookup"><span data-stu-id="9185c-127">D3DRS\_STENCILPASS</span></span>  | <span data-ttu-id="9185c-128">D3DSTENCILOP si se superan las pruebas de estarcido y z.</span><span class="sxs-lookup"><span data-stu-id="9185c-128">D3DSTENCILOP to do if both stencil and z-tests pass.</span></span>                                     |
| <span data-ttu-id="9185c-129">D3DRS \_ STENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="9185c-129">D3DRS\_STENCILFUNC</span></span>  | <span data-ttu-id="9185c-130">D3DCMPFUNC FN.</span><span class="sxs-lookup"><span data-stu-id="9185c-130">D3DCMPFUNC fn.</span></span> <span data-ttu-id="9185c-131">La prueba de estarcido se supera si (((Ref & Mask) stencilfn (Galería de símbolos & máscara)) es true.</span><span class="sxs-lookup"><span data-stu-id="9185c-131">Stencil Test passes if ((ref & mask) stencilfn (stencil & mask)) is true.</span></span> |



 

<span data-ttu-id="9185c-132">Un nuevo conjunto de Estados de representación se aplica a los triángulos hacia delante (en sentido contrario a las agujas del reloj).</span><span class="sxs-lookup"><span data-stu-id="9185c-132">A new set of render states apply to the back-facing (counterclockwise) triangles.</span></span>



| <span data-ttu-id="9185c-133">Estado de representación</span><span class="sxs-lookup"><span data-stu-id="9185c-133">Render state</span></span>             | <span data-ttu-id="9185c-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="9185c-134">Description</span></span>                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9185c-135">D3DRS \_ CCW \_ STENCILFAIL</span><span class="sxs-lookup"><span data-stu-id="9185c-135">D3DRS\_CCW\_STENCILFAIL</span></span>  | <span data-ttu-id="9185c-136">D3DSTENCILOP si se produce un error en la prueba de estarcido.</span><span class="sxs-lookup"><span data-stu-id="9185c-136">D3DSTENCILOP to do if stencil test fails.</span></span>                                                      |
| <span data-ttu-id="9185c-137">D3DRS \_ CCW \_ STENCILZFAIL</span><span class="sxs-lookup"><span data-stu-id="9185c-137">D3DRS\_CCW\_STENCILZFAIL</span></span> | <span data-ttu-id="9185c-138">D3DSTENCILOP si se supera la prueba de estarcido y se produce un error en la prueba z.</span><span class="sxs-lookup"><span data-stu-id="9185c-138">D3DSTENCILOP to do if stencil test passes and z-test fails.</span></span>                                    |
| <span data-ttu-id="9185c-139">D3DRS \_ CCW \_ STENCILPASS</span><span class="sxs-lookup"><span data-stu-id="9185c-139">D3DRS\_CCW\_STENCILPASS</span></span>  | <span data-ttu-id="9185c-140">D3DSTENCILOP si se superan las pruebas de estarcido y z.</span><span class="sxs-lookup"><span data-stu-id="9185c-140">D3DSTENCILOP to do if both stencil and z-tests pass.</span></span>                                           |
| <span data-ttu-id="9185c-141">D3DRS \_ CCW \_ STENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="9185c-141">D3DRS\_CCW\_STENCILFUNC</span></span>  | <span data-ttu-id="9185c-142">Función D3DCMPFUNC.</span><span class="sxs-lookup"><span data-stu-id="9185c-142">D3DCMPFUNC function.</span></span> <span data-ttu-id="9185c-143">La prueba de estarcido se supera si (((Ref & Mask) stencilfn (Galería de símbolos & máscara)) es true.</span><span class="sxs-lookup"><span data-stu-id="9185c-143">Stencil test passes if ((ref & mask) stencilfn (stencil & mask)) is true.</span></span> |



 

<span data-ttu-id="9185c-144">Los Estados de representación de estarcido restantes siempre se aplican a los triángulos en el sentido de las agujas del reloj y en el sentido contrario</span><span class="sxs-lookup"><span data-stu-id="9185c-144">The remaining stencil render states always apply to both clockwise and counterclockwise triangles.</span></span>

<span data-ttu-id="9185c-145">D3DRS \_ dos \_ \_ StencilMODE se omiten para las líneas y los sprites de punto, lo que significa que el comportamiento no se ha modificado desde DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="9185c-145">D3DRS\_Two\_Sided\_StencilMODE is ignored for lines and point sprites, which means that the behavior is unchanged from DirectX 8.</span></span> <span data-ttu-id="9185c-146">\_ \_ Se omiten los Estados de representación de la galería de símbolos CCW de D3DRS \* .</span><span class="sxs-lookup"><span data-stu-id="9185c-146">The D3DRS\_CCW\_STENCIL\* render states are ignored.</span></span>

<span data-ttu-id="9185c-147">Un nuevo bit Cap indica si el dispositivo admite esta característica.</span><span class="sxs-lookup"><span data-stu-id="9185c-147">A new cap bit indicates if the device supports this feature.</span></span> <span data-ttu-id="9185c-148">Se espera que los controladores que no admiten esta característica omitan estos nuevos Estados de representación.</span><span class="sxs-lookup"><span data-stu-id="9185c-148">Drivers that do not support this feature are expected to ignore these new render states.</span></span> <span data-ttu-id="9185c-149">Todos los demás bits de los extremos de la galería de símbolos se aplican a ambos modos de almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="9185c-149">All other stencil cap bits apply to both modes of stencil buffering.</span></span> <span data-ttu-id="9185c-150">Dado que dos \_ \_ galerías de símbolos están a la vez la capacidad de dibujar con D3DCULLMODE \_ None establecido, el controlador debe establecer el límite correspondiente si es compatible con este nuevo modo de estarcido.</span><span class="sxs-lookup"><span data-stu-id="9185c-150">Because Two\_Sided\_Stencil implies the ability to draw with D3DCULLMODE\_NONE set, the corresponding cap must be set by the driver if it supports this new stencil mode.</span></span> <span data-ttu-id="9185c-151">Los laboratorios de calidad de hardware (WHQL) de Microsoft Windows deberían aplicar esto.</span><span class="sxs-lookup"><span data-stu-id="9185c-151">Microsoft Windows Hardware Quality Labs (WHQL) should enforce this.</span></span>

<span data-ttu-id="9185c-152">Nuevos Estados de representación:</span><span class="sxs-lookup"><span data-stu-id="9185c-152">New render states:</span></span>


```
D3DRS_Two_Sided_StencilMODE // BOOL (default is FALSE)
D3DRS_CCW_STENCILFAIL     // Same default as D3DRS_STENCILFAIL
D3DRS_CCW_STENCILZFAIL    // Same default as D3DRS_STENCILZFAIL
D3DRS_CCW_STENCILPASS     // Same default as D3DRS_STENCILPASS
D3DRS_CCW_STENCILFUNC     // Same default as D3DRS_STENCILFUNC
```



<span data-ttu-id="9185c-153">Nuevo Cap:</span><span class="sxs-lookup"><span data-stu-id="9185c-153">New cap:</span></span>


```
D3DSTENCILCAPS_TWOSIDED // a flag on D3DCAPS9.StencilCaps
```



## <a name="related-topics"></a><span data-ttu-id="9185c-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9185c-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9185c-155">Técnicas de búfer de estarcido</span><span class="sxs-lookup"><span data-stu-id="9185c-155">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> <dt>

[<span data-ttu-id="9185c-156">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="9185c-156">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 

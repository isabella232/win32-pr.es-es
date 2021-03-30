---
title: Efecto de la matriz de colores
description: Utilice el efecto de la matriz de colores para modificar los valores RGBA de un mapa de bits.
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- efecto de la matriz de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1078b1858bc68396546e1036c717e01acb1069c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079248"
---
# <a name="color-matrix-effect"></a><span data-ttu-id="6c5fa-104">Efecto de la matriz de colores</span><span class="sxs-lookup"><span data-stu-id="6c5fa-104">Color matrix effect</span></span>

<span data-ttu-id="6c5fa-105">Utilice el efecto de la matriz de colores para modificar los valores RGBA de un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-105">Use the color matrix effect to alter the RGBA values of a bitmap.</span></span>

<span data-ttu-id="6c5fa-106">Puede usar este efecto para:</span><span class="sxs-lookup"><span data-stu-id="6c5fa-106">You can use this effect to:</span></span>

-   <span data-ttu-id="6c5fa-107">Quitar un canal de color de una imagen.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-107">Remove a color channel from an image.</span></span>
-   <span data-ttu-id="6c5fa-108">Reduzca el color de una imagen.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-108">Reduce the color in an image.</span></span>
-   <span data-ttu-id="6c5fa-109">Intercambie los canales de color.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-109">Swap color channels.</span></span>
-   <span data-ttu-id="6c5fa-110">Combinar canales de color.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-110">Combine color channels.</span></span>

<span data-ttu-id="6c5fa-111">Muchos efectos integrados son especializaciones de la matriz de colores que están optimizadas para el uso previsto de los efectos.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-111">Many built-in effects are specializations of color matrix that are optimized for the intended use of the effects.</span></span> <span data-ttu-id="6c5fa-112">Entre los ejemplos se incluyen [saturación](saturation.md), [matiz, rotación](hue-rotate.md), [sepia](sepia-effect.md)y [temperatura y matiz](temperature-and-tint-effect.md).</span><span class="sxs-lookup"><span data-stu-id="6c5fa-112">Examples include [saturation](saturation.md), [hue rotate](hue-rotate.md), [sepia](sepia-effect.md), and [temperature and tint](temperature-and-tint-effect.md).</span></span>

<span data-ttu-id="6c5fa-113">El CLSID para este efecto es CLSID \_ D2D1ColorMatrix.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-113">The CLSID for this effect is CLSID\_D2D1ColorMatrix.</span></span>

-   [<span data-ttu-id="6c5fa-114">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="6c5fa-114">Example image</span></span>](#example-image)
-   [<span data-ttu-id="6c5fa-115">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="6c5fa-115">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="6c5fa-116">Modos alfa</span><span class="sxs-lookup"><span data-stu-id="6c5fa-116">Alpha modes</span></span>](#alpha-modes)
-   [<span data-ttu-id="6c5fa-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c5fa-117">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6c5fa-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6c5fa-118">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="6c5fa-119">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="6c5fa-119">Example image</span></span>

<span data-ttu-id="6c5fa-120">En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de la matriz de colores que intercambia los canales rojo y azul.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-120">The example here shows the input and output images of the color matrix effect that swaps the red and blue channels.</span></span>



| <span data-ttu-id="6c5fa-121">Antes</span><span class="sxs-lookup"><span data-stu-id="6c5fa-121">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)   |
| <span data-ttu-id="6c5fa-123">Después</span><span class="sxs-lookup"><span data-stu-id="6c5fa-123">After</span></span>                                                        |
| ![la imagen después de la transformación.](images/15-colormatrix.png) |



 


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect);

colorMatrixEffect->SetInput(0, bitmap);
D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="6c5fa-125">Este efecto multiplica los valores RGBA de la imagen por una matriz de columnas principales de 5x4, como se muestra en esta ecuación.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-125">This effect multiplies the RGBA values of the image by a 5x4, column major matrix as shown in this equation.</span></span>

![una definición de matriz de ejemplo.](images/color-matrix-formula.png)

<span data-ttu-id="6c5fa-127">Este efecto funciona en imágenes alfa directas y premultiplicadas.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-127">This effect works on straight and premultiplied alpha images.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="6c5fa-128">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="6c5fa-128">Effect properties</span></span>



| <span data-ttu-id="6c5fa-129">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="6c5fa-129">Display name and index enumeration</span></span>                                       | <span data-ttu-id="6c5fa-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c5fa-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5fa-131">ColorMatrix</span><span class="sxs-lookup"><span data-stu-id="6c5fa-131">ColorMatrix</span></span><br/> <span data-ttu-id="6c5fa-132">\_Matriz de colores D2D1 COLORMATRIX \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="6c5fa-132">D2D1\_COLORMATRIX\_PROP\_COLOR\_MATRIX</span></span><br/> | <span data-ttu-id="6c5fa-133">Matriz 5x4 de valores float.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-133">A 5x4 matrix of float values.</span></span> <span data-ttu-id="6c5fa-134">Los elementos de la matriz no están enlazados y no tienen unidades.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-134">The elements in the matrix are not bounded and are unitless.</span></span><br/> <span data-ttu-id="6c5fa-135">El valor predeterminado es la matriz de identidad.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-135">The default is the identity matrix.</span></span><br/> <span data-ttu-id="6c5fa-136">El tipo es D2D1 \_ Matrix \_ 5x4 \_ F.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-136">The type is D2D1\_MATRIX\_5X4\_F.</span></span><br/> <span data-ttu-id="6c5fa-137">El valor predeterminado es Matrix5x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="6c5fa-137">The default value is Matrix5x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0).</span></span> <br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="6c5fa-138">AlphaMode</span><span class="sxs-lookup"><span data-stu-id="6c5fa-138">AlphaMode</span></span><br/> <span data-ttu-id="6c5fa-139">\_ \_ Modo alfa de prop D2D1 COLORMATRIX \_ \_</span><span class="sxs-lookup"><span data-stu-id="6c5fa-139">D2D1\_COLORMATRIX\_PROP\_ALPHA\_MODE</span></span><br/>     | <span data-ttu-id="6c5fa-140">Modo alfa de la salida.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-140">The alpha mode of the output.</span></span> <span data-ttu-id="6c5fa-141">Vea [modos alfa](#alpha-modes) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-141">See [Alpha modes](#alpha-modes) for more info.</span></span> <br/> <span data-ttu-id="6c5fa-142">El tipo es D2D1 \_ COLORMATRIX \_ alpha \_ .</span><span class="sxs-lookup"><span data-stu-id="6c5fa-142">The type is D2D1\_COLORMATRIX\_ALPHA\_MODE.</span></span><br/> <span data-ttu-id="6c5fa-143">El valor predeterminado es el \_ \_ modo alfa D2D1 COLORMATRIX \_ \_ premultiplicado.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-143">The default value is D2D1\_COLORMATRIX\_ALPHA\_MODE\_PREMULTIPLIED.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6c5fa-144">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="6c5fa-144">ClampOutput</span></span><br/> <span data-ttu-id="6c5fa-145">Salida de la abrazadera de prop de D2D1 \_ COLORMATRIX \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6c5fa-145">D2D1\_COLORMATRIX\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="6c5fa-146">Si el efecto fija los valores de color entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto del gráfico.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-146">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="6c5fa-147">El efecto fija los valores antes de que premultiplique el alfa.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-147">The effect clamps the values before it premultiplies the alpha .</span></span><br/> <span data-ttu-id="6c5fa-148">Si establece este valor en TRUE, el efecto fijará los valores.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-148">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="6c5fa-149">Si se establece en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no son de precisión lo suficientemente alta.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-149">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> <span data-ttu-id="6c5fa-150">El tipo es BOOL.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-150">The type is BOOL.</span></span><br/> <span data-ttu-id="6c5fa-151">El valor predeterminado es FALSE.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-151">The default value is FALSE.</span></span><br/> |



 

## <a name="alpha-modes"></a><span data-ttu-id="6c5fa-152">Modos alfa</span><span class="sxs-lookup"><span data-stu-id="6c5fa-152">Alpha modes</span></span>



| <span data-ttu-id="6c5fa-153">Nombre</span><span class="sxs-lookup"><span data-stu-id="6c5fa-153">Name</span></span>                                          | <span data-ttu-id="6c5fa-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c5fa-154">Description</span></span>                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5fa-155">Premultiplicado por el \_ \_ modo alfa D2D1 COLORMATRIX \_ \_</span><span class="sxs-lookup"><span data-stu-id="6c5fa-155">D2D1\_COLORMATRIX\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="6c5fa-156">El efecto anula la multiplicación de la entrada, aplica la matriz de colores y premultiplica el resultado.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-156">The effect un-premultiplies the input, applies the color matrix, and premultiplies the output.</span></span><br/> |
| <span data-ttu-id="6c5fa-157">\_ \_ Modo alfa D2D1 \_ COLORMATRIX \_ recto</span><span class="sxs-lookup"><span data-stu-id="6c5fa-157">D2D1\_COLORMATRIX\_ALPHA\_MODE\_STRAIGHT</span></span>      | <span data-ttu-id="6c5fa-158">El efecto aplica la matriz de colores directamente a la entrada y no multiplica la salida.</span><span class="sxs-lookup"><span data-stu-id="6c5fa-158">The effect applies the color matrix directly to the input, and doesn't premultiply the output.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6c5fa-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c5fa-159">Requirements</span></span>



| <span data-ttu-id="6c5fa-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c5fa-160">Requirement</span></span> | <span data-ttu-id="6c5fa-161">Value</span><span class="sxs-lookup"><span data-stu-id="6c5fa-161">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5fa-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c5fa-162">Minimum supported client</span></span> | <span data-ttu-id="6c5fa-163">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="6c5fa-163">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6c5fa-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c5fa-164">Minimum supported server</span></span> | <span data-ttu-id="6c5fa-165">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="6c5fa-165">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6c5fa-166">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c5fa-166">Header</span></span>                   | <span data-ttu-id="6c5fa-167">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="6c5fa-167">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="6c5fa-168">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c5fa-168">Library</span></span>                  | <span data-ttu-id="6c5fa-169">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="6c5fa-169">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="6c5fa-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6c5fa-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c5fa-171">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="6c5fa-171">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


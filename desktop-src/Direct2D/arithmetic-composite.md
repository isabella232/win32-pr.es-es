---
title: Efecto compuesto aritmético
description: Use el efecto compuesto aritmético para combinar 2 imágenes usando una suma ponderada de píxeles de las imágenes de entrada.
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- efecto compuesto aritmético
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c235ecb024c6b9e7adbce31c9f0cd65bc36cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996862"
---
# <a name="arithmetic-composite-effect"></a><span data-ttu-id="4c35a-104">Efecto compuesto aritmético</span><span class="sxs-lookup"><span data-stu-id="4c35a-104">Arithmetic composite effect</span></span>

<span data-ttu-id="4c35a-105">Use el efecto compuesto aritmético para combinar 2 imágenes usando una suma ponderada de píxeles de las imágenes de entrada.</span><span class="sxs-lookup"><span data-stu-id="4c35a-105">Use the arithmetic composite effect to combine 2 images using a weighted sum of pixels from the input images.</span></span>

<span data-ttu-id="4c35a-106">El CLSID para este efecto es CLSID \_ D2D1ArithmeticComposite.</span><span class="sxs-lookup"><span data-stu-id="4c35a-106">The CLSID for this effect is CLSID\_D2D1ArithmeticComposite.</span></span>

-   [<span data-ttu-id="4c35a-107">Fórmula</span><span class="sxs-lookup"><span data-stu-id="4c35a-107">Formula</span></span>](#formula)
-   [<span data-ttu-id="4c35a-108">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c35a-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="4c35a-109">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="4c35a-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="4c35a-110">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="4c35a-110">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="4c35a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c35a-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="4c35a-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c35a-112">Related topics</span></span>](#related-topics)

## <a name="formula"></a><span data-ttu-id="4c35a-113">Fórmula</span><span class="sxs-lookup"><span data-stu-id="4c35a-113">Formula</span></span>

<span data-ttu-id="4c35a-114">La fórmula aquí se usa para calcular este efecto.</span><span class="sxs-lookup"><span data-stu-id="4c35a-114">The formula here is used to compute this effect.</span></span>

<span data-ttu-id="4c35a-115">Salida<sub>RGBA</sub> = origen de código C1 de \* destino<sub>RGBA</sub> \* + origen de C2<sub></sub> \* <sub>RGBA</sub> + C3 \* destino<sub>RGBA</sub> + C4</span><span class="sxs-lookup"><span data-stu-id="4c35a-115">Output<sub>rgba</sub> = C1 \* Source<sub>rgba</sub> \* Destination<sub>rgba</sub> + C2 \* Source<sub>rgba</sub> + C3 \* Destination<sub>rgba</sub> + C4</span></span>

<span data-ttu-id="4c35a-116">Donde C1, C2, C3, C4 son coeficientes que se establecen.</span><span class="sxs-lookup"><span data-stu-id="4c35a-116">Where C1, C2, C3, C4 are coefficients that you set.</span></span>

<span data-ttu-id="4c35a-117">Los coeficientes se asignan a los valores de un D2D1 \_ Vector \_ 4F (x, y, z, w):</span><span class="sxs-lookup"><span data-stu-id="4c35a-117">The coefficients map to the values in a D2D1\_VECTOR\_4F (x, y, z, w):</span></span>

-   <span data-ttu-id="4c35a-118">x = C1</span><span class="sxs-lookup"><span data-stu-id="4c35a-118">x = C1</span></span>
-   <span data-ttu-id="4c35a-119">y = C2</span><span class="sxs-lookup"><span data-stu-id="4c35a-119">y = C2</span></span>
-   <span data-ttu-id="4c35a-120">z = C3</span><span class="sxs-lookup"><span data-stu-id="4c35a-120">z = C3</span></span>
-   <span data-ttu-id="4c35a-121">w = C4</span><span class="sxs-lookup"><span data-stu-id="4c35a-121">w = C4</span></span>

## <a name="example-image"></a><span data-ttu-id="4c35a-122">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c35a-122">Example image</span></span>

<span data-ttu-id="4c35a-123">Un ejemplo sencillo es agregar los píxeles de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="4c35a-123">A simple example is to add the source and destination pixels.</span></span> <span data-ttu-id="4c35a-124">En el ejemplo, se componen dos rectángulos redondeados.</span><span class="sxs-lookup"><span data-stu-id="4c35a-124">In the example, 2 rounded rectangles are composited together.</span></span> <span data-ttu-id="4c35a-125">El rectángulo de origen es azul y el destino es rojo.</span><span class="sxs-lookup"><span data-stu-id="4c35a-125">The source rectangle is blue and the destination is red.</span></span>

<span data-ttu-id="4c35a-126">La imagen siguiente es la salida del efecto compuesto aritmético con los coeficientes de la ecuación establecida en los valores aquí.</span><span class="sxs-lookup"><span data-stu-id="4c35a-126">The image here is the output of the Arithmetic Composite effect with the coefficients of the equation set to the values here.</span></span>

-   <span data-ttu-id="4c35a-127">C1 = 0</span><span class="sxs-lookup"><span data-stu-id="4c35a-127">C1 = 0</span></span>
-   <span data-ttu-id="4c35a-128">C2 = 1</span><span class="sxs-lookup"><span data-stu-id="4c35a-128">C2 = 1</span></span>
-   <span data-ttu-id="4c35a-129">C3 = 1</span><span class="sxs-lookup"><span data-stu-id="4c35a-129">C3 = 1</span></span>
-   <span data-ttu-id="4c35a-130">C4 = 0</span><span class="sxs-lookup"><span data-stu-id="4c35a-130">C4 = 0</span></span>

![imagen de ejemplo que muestra dos rectángulos redondeados del mismo tamaño que se superponen con el efecto compuesto aritmético.](images/arithmetic-50-percent.png)

<span data-ttu-id="4c35a-132">El resultado es que se agregan los valores de píxel para el origen y el destino.</span><span class="sxs-lookup"><span data-stu-id="4c35a-132">The result is that the pixel values for the source and destination are added.</span></span> <span data-ttu-id="4c35a-133">Las regiones en las que los rectángulos no se superponen los valores RGBA son 0.</span><span class="sxs-lookup"><span data-stu-id="4c35a-133">The regions where the rectangles don't overlap the RGBA values are all 0.</span></span> <span data-ttu-id="4c35a-134">Donde los rectángulos se superponen el color es magenta porque los valores R y B están en el máximo.</span><span class="sxs-lookup"><span data-stu-id="4c35a-134">Where the rectangles overlap the color is magenta because the R and B values are both at maximum.</span></span>

<span data-ttu-id="4c35a-135">Esta es otra imagen de ejemplo con el código.</span><span class="sxs-lookup"><span data-stu-id="4c35a-135">Here's another example image with code.</span></span>



| <span data-ttu-id="4c35a-136">Antes de la imagen 1</span><span class="sxs-lookup"><span data-stu-id="4c35a-136">Before image 1</span></span>                                                             |
|----------------------------------------------------------------------------|
| ![primera imagen de origen antes del efecto.](images/default-before.jpg)    |
| <span data-ttu-id="4c35a-138">Antes de la imagen 2</span><span class="sxs-lookup"><span data-stu-id="4c35a-138">Before image 2</span></span>                                                             |
| ![segunda imagen anterior al efecto.](images/4-arthimetic-composite2.jpg) |
| <span data-ttu-id="4c35a-140">Después</span><span class="sxs-lookup"><span data-stu-id="4c35a-140">After</span></span>                                                                      |
| ![la imagen después de la transformación.](images/4-arithmeticcomposite.png)        |



 


```C++
ComPtr<ID2D1Effect> arithmeticCompositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &arithmeticCompositeEffect);

arithmeticCompositeEffect->SetInput(0, bitmap);
arithmeticCompositeEffect->SetInput(1, bitmapTwo);
arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, D2D1::Vector4F(0.0f, 0.5f, 0.5f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(arithmeticCompositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="4c35a-142">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="4c35a-142">Effect properties</span></span>



| <span data-ttu-id="4c35a-143">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="4c35a-143">Display name and index enumeration</span></span>                                               | <span data-ttu-id="4c35a-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c35a-144">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c35a-145">Coeficientes</span><span class="sxs-lookup"><span data-stu-id="4c35a-145">Coefficients</span></span><br/> <span data-ttu-id="4c35a-146">Coeficientes de D2D1 \_ ARITHMETICCOMPOSITE \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c35a-146">D2D1\_ARITHMETICCOMPOSITE\_PROP\_COEFFICIENTS</span></span><br/> | <span data-ttu-id="4c35a-147">Coeficientes para la ecuación que se usa para componer las dos imágenes de entrada.</span><span class="sxs-lookup"><span data-stu-id="4c35a-147">The coefficients for the equation used to composite the two input images.</span></span> <span data-ttu-id="4c35a-148">Los coeficientes son sin unidades y sin límite.</span><span class="sxs-lookup"><span data-stu-id="4c35a-148">The coefficients are unitless and unbounded.</span></span> <span data-ttu-id="4c35a-149">El tipo es D2D1 \_ Vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="4c35a-149">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="4c35a-150">El valor predeterminado es {1,0 f, 0.0 f, 0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="4c35a-150">Default value is {1.0f, 0.0f, 0.0f, 0.0f}.</span></span><br/>                                                                                                                                                                                                                                 |
| <span data-ttu-id="4c35a-151">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="4c35a-151">ClampOutput</span></span><br/> <span data-ttu-id="4c35a-152">Salida de la abrazadera de D2D1 \_ ARITHMETICCOMPOSITE \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4c35a-152">D2D1\_ARITHMETICCOMPOSITE\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="4c35a-153">El efecto fija los valores de color entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto del gráfico.</span><span class="sxs-lookup"><span data-stu-id="4c35a-153">The effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <br/> <span data-ttu-id="4c35a-154">Si establece este valor en TRUE, el efecto fijará los valores.</span><span class="sxs-lookup"><span data-stu-id="4c35a-154">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="4c35a-155">Si se establece en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no son de precisión lo suficientemente alta.</span><span class="sxs-lookup"><span data-stu-id="4c35a-155">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> <span data-ttu-id="4c35a-156">El tipo es BOOL.</span><span class="sxs-lookup"><span data-stu-id="4c35a-156">Type is BOOL.</span></span><br/> <span data-ttu-id="4c35a-157">El valor predeterminado es FALSE.</span><span class="sxs-lookup"><span data-stu-id="4c35a-157">Default value is FALSE.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="4c35a-158">Mapa de bits de salida</span><span class="sxs-lookup"><span data-stu-id="4c35a-158">Output bitmap</span></span>

<span data-ttu-id="4c35a-159">El mapa de bits de salida depende de los valores de coeficiente.</span><span class="sxs-lookup"><span data-stu-id="4c35a-159">The output bitmap depends on the coefficient values.</span></span> <span data-ttu-id="4c35a-160">Estos son los posibles tamaños de mapa de bits de salida.</span><span class="sxs-lookup"><span data-stu-id="4c35a-160">These are the possible output bitmap sizes.</span></span>

-   <span data-ttu-id="4c35a-161">Si C1 es el único coeficiente distinto de cero, el tamaño de salida es la intersección de los rectángulos de entrada.</span><span class="sxs-lookup"><span data-stu-id="4c35a-161">If C1 is the only non-zero coefficient, the output size is the intersection of the input rectangles.</span></span>
-   <span data-ttu-id="4c35a-162">Si C2 es el único coeficiente distinto de cero, el tamaño de salida es el tamaño del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="4c35a-162">If C2 is the only non-zero coefficient, the output size is the size of the Source rectangle.</span></span>
-   <span data-ttu-id="4c35a-163">Si C3 es el único coeficiente distinto de cero, el tamaño de salida es el tamaño del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="4c35a-163">If C3 is the only non-zero coefficient, the output size is the size of the Destination rectangle..</span></span>
-   <span data-ttu-id="4c35a-164">Si todos los coeficientes son cero, el tamaño de salida es un rectángulo vacío.</span><span class="sxs-lookup"><span data-stu-id="4c35a-164">If all coefficients are zero, the output size is an empty rectangle.</span></span>
-   <span data-ttu-id="4c35a-165">Para todos los demás valores de coeficiente, el tamaño de salida es la Unión de los rectángulos de entrada.</span><span class="sxs-lookup"><span data-stu-id="4c35a-165">For all other coefficient values, the output size is the union of the input rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c35a-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c35a-166">Requirements</span></span>



| <span data-ttu-id="4c35a-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c35a-167">Requirement</span></span> | <span data-ttu-id="4c35a-168">Value</span><span class="sxs-lookup"><span data-stu-id="4c35a-168">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c35a-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c35a-169">Minimum supported client</span></span> | <span data-ttu-id="4c35a-170">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="4c35a-170">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4c35a-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c35a-171">Minimum supported server</span></span> | <span data-ttu-id="4c35a-172">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="4c35a-172">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4c35a-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c35a-173">Header</span></span>                   | <span data-ttu-id="4c35a-174">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="4c35a-174">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="4c35a-175">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c35a-175">Library</span></span>                  | <span data-ttu-id="4c35a-176">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="4c35a-176">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="4c35a-177">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c35a-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c35a-178">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="4c35a-178">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


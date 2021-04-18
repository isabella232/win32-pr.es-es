---
title: Métodos de ID2D1Brush SetTransform (D2d1 \_ 1. h)
description: Establece la transformación que se aplica al pincel.
ms.assetid: 57afadc1-88c9-4a5b-a83f-63c4c69182a7
keywords:
- Métodos de SetTransform Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 89d0da76368fac2d2335cabda1f6d0a6130b499f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681163"
---
# <a name="id2d1brushsettransform-methods"></a><span data-ttu-id="ced8d-104">ID2D1Brush:: SetTransform (métodos)</span><span class="sxs-lookup"><span data-stu-id="ced8d-104">ID2D1Brush::SetTransform methods</span></span>

<span data-ttu-id="ced8d-105">Establece la transformación que se aplica al pincel.</span><span class="sxs-lookup"><span data-stu-id="ced8d-105">Sets the transformation applied to the brush.</span></span>

### <a name="overload-list"></a><span data-ttu-id="ced8d-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="ced8d-106">Overload list</span></span>



| <span data-ttu-id="ced8d-107">Método</span><span class="sxs-lookup"><span data-stu-id="ced8d-107">Method</span></span>                                                                                       | <span data-ttu-id="ced8d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ced8d-108">Description</span></span>                                              |
|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| <span data-ttu-id="ced8d-109">[**SetTransform (D2D1 \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="ced8d-109">[**SetTransform(D2D1\_MATRIX\_3X2\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))</span></span>  | <span data-ttu-id="ced8d-110">Establece la transformación que se aplica al pincel.</span><span class="sxs-lookup"><span data-stu-id="ced8d-110">Sets the transformation applied to the brush.</span></span><br/> |
| <span data-ttu-id="ced8d-111">[**SetTransform (D2D1 \_ Matrix \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f))</span><span class="sxs-lookup"><span data-stu-id="ced8d-111">[**SetTransform(D2D1\_MATRIX\_3X2\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f))</span></span> | <span data-ttu-id="ced8d-112">Establece la transformación que se aplica al pincel.</span><span class="sxs-lookup"><span data-stu-id="ced8d-112">Sets the transformation applied to the brush.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ced8d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ced8d-113">Remarks</span></span>

<span data-ttu-id="ced8d-114">Cuando se pinta con un pincel, pinta en el espacio de coordenadas del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="ced8d-114">When you paint with a brush, it paints in the coordinate space of the render target.</span></span> <span data-ttu-id="ced8d-115">Los pinceles no se colocan automáticamente para alinearse con el objeto que se está dibujando; de forma predeterminada, empiezan a pintar en el origen (0,0) del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="ced8d-115">Brushes do not automatically position themselves to align with the object being painted; by default, they begin painting at the origin (0, 0) of the render target.</span></span>

<span data-ttu-id="ced8d-116">Puede "desplace" el degradado definido por un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) a un área de destino estableciendo el punto inicial y el punto final.</span><span class="sxs-lookup"><span data-stu-id="ced8d-116">You can "move" the gradient defined by an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) to a target area by setting its start point and end point.</span></span> <span data-ttu-id="ced8d-117">Del mismo modo, puede trasladar el degradado definido por un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) cambiando su centro y radios.</span><span class="sxs-lookup"><span data-stu-id="ced8d-117">Likewise, you can move the gradient defined by an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) by changing its center and radii.</span></span>

<span data-ttu-id="ced8d-118">Para alinear el contenido de un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) con el área que se está dibujando, puede usar el método **SetTransform** para traducir el mapa de bits a la ubicación deseada.</span><span class="sxs-lookup"><span data-stu-id="ced8d-118">To align the content of an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to the area being painted, you can use the **SetTransform** method to translate the bitmap to the desired location.</span></span> <span data-ttu-id="ced8d-119">Esta transformación solo afecta al pincel; no afecta a ningún otro contenido dibujado por el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="ced8d-119">This transform only affects the brush; it does not affect any other content drawn by the render target.</span></span>

<span data-ttu-id="ced8d-120">En las ilustraciones siguientes se muestra el efecto de usar un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para rellenar un rectángulo ubicado en (100, 100).</span><span class="sxs-lookup"><span data-stu-id="ced8d-120">The following illustrations show the effect of using an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to fill a rectangle located at (100, 100).</span></span> <span data-ttu-id="ced8d-121">En la ilustración de la ilustración izquierda se muestra el resultado de llenar el rectángulo sin transformar el pincel: el mapa de bits se dibuja en el origen del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="ced8d-121">The illustration on the left illustration shows the result of filling the rectangle without transforming the brush: the bitmap is drawn at the render target's origin.</span></span> <span data-ttu-id="ced8d-122">Como resultado, solo aparece una parte del mapa de bits en el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="ced8d-122">As a result, only a portion of the bitmap appears in the rectangle.</span></span>

<span data-ttu-id="ced8d-123">En la ilustración de la derecha se muestra el resultado de transformar el [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para que su contenido se desplace 50 píxeles hacia la derecha y 50 píxeles hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="ced8d-123">The illustration on the right shows the result of transforming the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) so that its content is shifted 50 pixels to the right and 50 pixels down.</span></span> <span data-ttu-id="ced8d-124">El mapa de bits ahora rellena el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="ced8d-124">The bitmap now fills the rectangle.</span></span>

![Ilustración de dos cuadrados, uno pintado con un mapa de bits sin un pincel transformado y otro pintado con un pincel transformado](images/brushes-ovw-transform.png)

## <a name="examples"></a><span data-ttu-id="ced8d-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ced8d-126">Examples</span></span>

<span data-ttu-id="ced8d-127">En los siguientes ejemplos de código se muestra cómo crear la transformación que se muestra en el diagrama de la derecha de la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="ced8d-127">The following code examples show how to create the transformation shown in the right diagram in the preceding illustration.</span></span> <span data-ttu-id="ced8d-128">En primer lugar, aplique una traducción al [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moviendo el pincel 50 píxeles a lo largo del eje x y 50 píxeles hacia abajo a lo largo del eje y.</span><span class="sxs-lookup"><span data-stu-id="ced8d-128">First apply a translation to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moving the brush 50 pixels right along the x-axis and 50 pixels down along the y-axis.</span></span> <span data-ttu-id="ced8d-129">A continuación, use **ID2D1BitmapBrush** para rellenar el rectángulo que tiene la esquina superior izquierda en (100, 100) y la esquina inferior derecha en (200, 200).</span><span class="sxs-lookup"><span data-stu-id="ced8d-129">Then use the **ID2D1BitmapBrush** to fill the rectangle that has the upper-left corner at (100, 100) and the lower-right corner at (200, 200).</span></span>


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &amp;m_pBitmap
        );
   
}
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &amp;m_pBitmapBrush
        );
}
```




```C++
D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);



 // Demonstrate the effect of transforming a bitmap brush.
 m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

 // To see the content of the rcTransformedBrushRect, comment
 // out this statement.
 m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

 m_pRenderTarget-&gt;DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```





## <a name="requirements"></a><span data-ttu-id="ced8d-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ced8d-130">Requirements</span></span>



| <span data-ttu-id="ced8d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ced8d-131">Requirement</span></span> | <span data-ttu-id="ced8d-132">Value</span><span class="sxs-lookup"><span data-stu-id="ced8d-132">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ced8d-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ced8d-133">Header</span></span><br/>  | <dl> <span data-ttu-id="ced8d-134"><dt>D2d1 \_ 1. h (incluir D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ced8d-134"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="ced8d-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ced8d-135">Library</span></span><br/> | <dl> <span data-ttu-id="ced8d-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ced8d-136"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ced8d-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ced8d-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="ced8d-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ced8d-138"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="ced8d-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="ced8d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ced8d-140">Información general sobre los pinceles</span><span class="sxs-lookup"><span data-stu-id="ced8d-140">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> <dt>

[<span data-ttu-id="ced8d-141">**ID2D1Brush**</span><span class="sxs-lookup"><span data-stu-id="ced8d-141">**ID2D1Brush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)
</dt> </dl>

<span data-ttu-id="ced8d-142">�</span><span class="sxs-lookup"><span data-stu-id="ced8d-142">�</span></span>

<span data-ttu-id="ced8d-143">�</span><span class="sxs-lookup"><span data-stu-id="ced8d-143">�</span></span>

---
title: Error de vaciado de D1110
ms.assetid: 44f122b0-08e3-4f63-a575-0f3619144823
description: Error en una llamada de vaciado de un destino de representación
keywords:
- Error de vaciado de D1110 Direct2D
topic_type:
- apiref
api_name:
- D1110 Flush Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 721fb27e8cfd5e83f94b93079ee66e4a1c35992d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549930"
---
# <a name="d1110-flush-failure"></a><span data-ttu-id="28f95-104">D1110: Error de vaciado</span><span class="sxs-lookup"><span data-stu-id="28f95-104">D1110: Flush Failure</span></span>

<span data-ttu-id="28f95-105">Una llamada de vaciado por un recurso de destino de \[ *representación con error.* \]</span><span class="sxs-lookup"><span data-stu-id="28f95-105">A Flush call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="28f95-106">Etiquetas \[ *tag1*, *tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="28f95-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="28f95-107">Marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="28f95-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="28f95-108"><span id="resource"></span><span id="RESOURCE"></span>*Recursos*</span><span class="sxs-lookup"><span data-stu-id="28f95-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="28f95-109">Dirección del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="28f95-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="28f95-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span><span class="sxs-lookup"><span data-stu-id="28f95-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="28f95-111">Primer valor de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="28f95-111">The first tag value.</span></span> <span data-ttu-id="28f95-112">Consulte [**SetTags para**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) obtener más información.</span><span class="sxs-lookup"><span data-stu-id="28f95-112">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="28f95-113"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span><span class="sxs-lookup"><span data-stu-id="28f95-113"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="28f95-114">Segundo valor de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="28f95-114">The second tag value.</span></span> <span data-ttu-id="28f95-115">Consulte [**SetTags para**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) obtener más información.</span><span class="sxs-lookup"><span data-stu-id="28f95-115">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="28f95-116">Nivel de error</span><span class="sxs-lookup"><span data-stu-id="28f95-116">Error Level</span></span> | <span data-ttu-id="28f95-117">Advertencia</span><span class="sxs-lookup"><span data-stu-id="28f95-117">Warning</span></span> |



 

## <a name="examples"></a><span data-ttu-id="28f95-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="28f95-118">Examples</span></span>

<span data-ttu-id="28f95-119">**Ejemplo 1:** El código siguiente muestra que una llamada a draw está en un estado no válido.</span><span class="sxs-lookup"><span data-stu-id="28f95-119">**Example 1:** The following code shows that a draw call is in an invalid state.</span></span> <span data-ttu-id="28f95-120">Para evitar el mensaje de advertencia, use [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) para establecer D2D1 \_ ANTIALIAS MODE ANTIALIASED antes de una \_ llamada a \_ [**FillOpacityMask.**](id2d1rendertarget-fillopacitymask.md)</span><span class="sxs-lookup"><span data-stu-id="28f95-120">To avoid the warning message, use [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set D2D1\_ANTIALIAS\_MODE\_ANTIALIASED before a [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) call.</span></span>


```C++
       
        if(SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateBitmap(
                D2D1::SizeU(1,1),
                NULL,
                0,
                D2D1::BitmapProperties(D2D1::PixelFormat(
                    DXGI_FORMAT_A8_UNORM, 
                    D2D1_ALPHA_MODE_PREMULTIPLIED
                    )),
                &m_pBitmap
                );                    
        }


        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );

        hr = m_pRenderTarget->Flush();

        hr = m_pRenderTarget->EndDraw();
```





<span data-ttu-id="28f95-121">En este ejemplo se genera el siguiente mensaje de depuración:</span><span class="sxs-lookup"><span data-stu-id="28f95-121">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

<span data-ttu-id="28f95-122">**Ejemplo 2:** El código siguiente muestra que se llama [**a Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) después de la llamada [**a EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)</span><span class="sxs-lookup"><span data-stu-id="28f95-122">**Example 2:** The following code shows that the [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called after the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call.</span></span>


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



<span data-ttu-id="28f95-123">En este ejemplo se genera el siguiente mensaje de depuración:</span><span class="sxs-lookup"><span data-stu-id="28f95-123">This example produces the following debug message:</span></span>

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a><span data-ttu-id="28f95-124">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="28f95-124">Possible Causes</span></span>

<span data-ttu-id="28f95-125">La [**llamada Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) puede producir un error por uno de estos dos motivos.</span><span class="sxs-lookup"><span data-stu-id="28f95-125">The [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call can fail for one of two reasons.</span></span> <span data-ttu-id="28f95-126">Puede producirse un error porque se llamó al método fuera de la llamada [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)EndDraw o puede producirse un error porque se produjo un error en una de las operaciones de destino de representación que se han procesado desde la última llamada Flush o / [](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) **EndDraw.** </span><span class="sxs-lookup"><span data-stu-id="28f95-126">It may fail because the method was called outside of the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)/[**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call, or it may fail because there was an error produced by one of the render target operations that have been processed since the last **Flush** call or **EndDraw** call.</span></span> <span data-ttu-id="28f95-127">Para corregir el problema, la aplicación debe determinar la causa del error y realizar la acción adecuada.</span><span class="sxs-lookup"><span data-stu-id="28f95-127">To fix the issue, the application should determine the cause of the error and take the appropriate action.</span></span>

## <a name="fixes"></a><span data-ttu-id="28f95-128">Correcciones</span><span class="sxs-lookup"><span data-stu-id="28f95-128">Fixes</span></span>

<span data-ttu-id="28f95-129">Hay muchas razones por las que una [**llamada de vaciado**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) podría producir un error.</span><span class="sxs-lookup"><span data-stu-id="28f95-129">There are many reasons that a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call might fail.</span></span> <span data-ttu-id="28f95-130">La aplicación debe determinar la causa del error y realizar la acción adecuada.</span><span class="sxs-lookup"><span data-stu-id="28f95-130">The application should determine the cause of the error and take the appropriate action.</span></span>

 

 
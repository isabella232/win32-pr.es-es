---
title: Error de vaciado de D1110
ms.assetid: 44f122b0-08e3-4f63-a575-0f3619144823
description: Error en una llamada de vaciado por un destino de representación
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
ms.openlocfilehash: 4821ba291f3adc8d22d1d1298a88c74b47dc648b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421384"
---
# <a name="d1110-flush-failure"></a><span data-ttu-id="4d567-104">D1110: error de vaciado</span><span class="sxs-lookup"><span data-stu-id="4d567-104">D1110: Flush Failure</span></span>

<span data-ttu-id="4d567-105">Error en una llamada de vaciado de un recurso de destino de representación \[  \] .</span><span class="sxs-lookup"><span data-stu-id="4d567-105">A Flush call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="4d567-106">Tags \[ *TAG1*, *etiqueta2* \] .</span><span class="sxs-lookup"><span data-stu-id="4d567-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="4d567-107">Marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="4d567-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="4d567-108"><span id="resource"></span><span id="RESOURCE"></span>*recurso*</span><span class="sxs-lookup"><span data-stu-id="4d567-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="4d567-109">Dirección del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="4d567-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="4d567-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span><span class="sxs-lookup"><span data-stu-id="4d567-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="4d567-111">Primer valor de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="4d567-111">The first tag value.</span></span> <span data-ttu-id="4d567-112">Vea [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4d567-112">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="4d567-113"><span id="tag2"></span><span id="TAG2"></span>*etiqueta2*</span><span class="sxs-lookup"><span data-stu-id="4d567-113"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="4d567-114">El segundo valor de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="4d567-114">The second tag value.</span></span> <span data-ttu-id="4d567-115">Vea [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4d567-115">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="4d567-116">Nivel de error</span><span class="sxs-lookup"><span data-stu-id="4d567-116">Error Level</span></span> | <span data-ttu-id="4d567-117">Advertencia</span><span class="sxs-lookup"><span data-stu-id="4d567-117">Warning</span></span> |



 

## <a name="examples"></a><span data-ttu-id="4d567-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4d567-118">Examples</span></span>

<span data-ttu-id="4d567-119">**Ejemplo 1:** En el código siguiente se muestra que una llamada a Draw está en un estado no válido.</span><span class="sxs-lookup"><span data-stu-id="4d567-119">**Example 1:** The following code shows that a draw call is in an invalid state.</span></span> <span data-ttu-id="4d567-120">Para evitar el mensaje de advertencia, use [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) para establecer el modo antialias de D2D1 \_ \_ \_ antes de una llamada a [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) .</span><span class="sxs-lookup"><span data-stu-id="4d567-120">To avoid the warning message, use [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set D2D1\_ANTIALIAS\_MODE\_ANTIALIASED before a [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) call.</span></span>


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





<span data-ttu-id="4d567-121">Este ejemplo genera el siguiente mensaje de depuración:</span><span class="sxs-lookup"><span data-stu-id="4d567-121">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

<span data-ttu-id="4d567-122">**Ejemplo 2:** En el código siguiente se muestra que se llama al [**vaciado**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) después de la llamada a [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="4d567-122">**Example 2:** The following code shows that the [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called after the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call.</span></span>


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



<span data-ttu-id="4d567-123">Este ejemplo genera el siguiente mensaje de depuración:</span><span class="sxs-lookup"><span data-stu-id="4d567-123">This example produces the following debug message:</span></span>

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a><span data-ttu-id="4d567-124">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="4d567-124">Possible Causes</span></span>

<span data-ttu-id="4d567-125">Se puede producir un error en la llamada de [**vaciado**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) por una de estas dos razones.</span><span class="sxs-lookup"><span data-stu-id="4d567-125">The [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call can fail for one of two reasons.</span></span> <span data-ttu-id="4d567-126">Puede producirse un error porque se llamó al método fuera de la llamada a [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) / [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o se puede producir un error porque se produjo un error producido por una de las operaciones de destino de representación procesadas desde la última llamada de **vaciado** o llamada a **EndDraw** .</span><span class="sxs-lookup"><span data-stu-id="4d567-126">It may fail because the method was called outside of the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)/[**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call, or it may fail because there was an error produced by one of the render target operations that have been processed since the last **Flush** call or **EndDraw** call.</span></span> <span data-ttu-id="4d567-127">Para solucionar el problema, la aplicación debe determinar la causa del error y realizar la acción apropiada.</span><span class="sxs-lookup"><span data-stu-id="4d567-127">To fix the issue, the application should determine the cause of the error and take the appropriate action.</span></span>

## <a name="fixes"></a><span data-ttu-id="4d567-128">Correcciones</span><span class="sxs-lookup"><span data-stu-id="4d567-128">Fixes</span></span>

<span data-ttu-id="4d567-129">Hay muchas razones por las que se puede producir un error en una llamada de [**vaciado**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="4d567-129">There are many reasons that a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call might fail.</span></span> <span data-ttu-id="4d567-130">La aplicación debe determinar la causa del error y realizar la acción apropiada.</span><span class="sxs-lookup"><span data-stu-id="4d567-130">The application should determine the cause of the error and take the appropriate action.</span></span>

 

 
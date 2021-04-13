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
# <a name="d1110-flush-failure"></a>D1110: error de vaciado

Error en una llamada de vaciado de un recurso de destino de representación \[  \] . Tags \[ *TAG1*, *etiqueta2* \] .

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*recurso*
</dt> <dd>

Dirección del destino de representación.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*tag1*
</dt> <dd>

Primer valor de etiqueta. Vea [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) para obtener más información.

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*etiqueta2*
</dt> <dd>

El segundo valor de etiqueta. Vea [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) para obtener más información.

</dd> </dl> 

|             |         |
|-------------|---------|
| Nivel de error | Advertencia |



 

## <a name="examples"></a>Ejemplos

**Ejemplo 1:** En el código siguiente se muestra que una llamada a Draw está en un estado no válido. Para evitar el mensaje de advertencia, use [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) para establecer el modo antialias de D2D1 \_ \_ \_ antes de una llamada a [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) .


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





Este ejemplo genera el siguiente mensaje de depuración:

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

**Ejemplo 2:** En el código siguiente se muestra que se llama al [**vaciado**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) después de la llamada a [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



Este ejemplo genera el siguiente mensaje de depuración:

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a>Causas posibles

Se puede producir un error en la llamada de [**vaciado**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) por una de estas dos razones. Puede producirse un error porque se llamó al método fuera de la llamada a [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) / [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o se puede producir un error porque se produjo un error producido por una de las operaciones de destino de representación procesadas desde la última llamada de **vaciado** o llamada a **EndDraw** . Para solucionar el problema, la aplicación debe determinar la causa del error y realizar la acción apropiada.

## <a name="fixes"></a>Correcciones

Hay muchas razones por las que se puede producir un error en una llamada de [**vaciado**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) . La aplicación debe determinar la causa del error y realizar la acción apropiada.

 

 
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
ms.openlocfilehash: 12d6a990d3d65c1a711825e6d45720f3df977ca78efb16c1d39bb9b2251c53b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758155"
---
# <a name="d1110-flush-failure"></a>D1110: Error de vaciado

Una llamada de vaciado por un recurso de destino de \[ *representación con error.* \] Etiquetas \[ *tag1*, *tag2* \] .

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Recursos*
</dt> <dd>

Dirección del destino de representación.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*tag1*
</dt> <dd>

Primer valor de etiqueta. Consulte [**SetTags para**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) obtener más información.

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*tag2*
</dt> <dd>

Segundo valor de etiqueta. Consulte [**SetTags para**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) obtener más información.

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Nivel de error | Advertencia |



 

## <a name="examples"></a>Ejemplos

**Ejemplo 1:** El código siguiente muestra que una llamada a draw está en un estado no válido. Para evitar el mensaje de advertencia, use [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) para establecer D2D1 \_ ANTIALIAS MODE ANTIALIASED antes de una \_ llamada a \_ [**FillOpacityMask.**](id2d1rendertarget-fillopacitymask.md)


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





En este ejemplo se genera el siguiente mensaje de depuración:

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

**Ejemplo 2:** El código siguiente muestra que se llama [**a Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) después de la llamada [**a EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



En este ejemplo se genera el siguiente mensaje de depuración:

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a>Causas posibles

La [**llamada flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) puede producir un error por uno de estos dos motivos. Puede producirse un error porque se llamó al método fuera de la llamada [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)EndDraw o puede producir un error porque se produjo un error en una de las operaciones de destino de representación que se han procesado desde la última llamada Flush o / [](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) **EndDraw.**  Para corregir el problema, la aplicación debe determinar la causa del error y realizar la acción adecuada.

## <a name="fixes"></a>Correcciones

Hay muchas razones por las que una [**llamada de**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) vaciado podría producir un error. La aplicación debe determinar la causa del error y realizar la acción adecuada.

 

 
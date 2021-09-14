---
title: Métodos ID2D1RenderTarget CreateCompatibleRenderTarget (D2d1.h)
description: Crea un nuevo destino de representación de mapa de bits para usarlo durante el dibujo fuera de pantalla intermedio que es compatible con el destino de representación actual.
ms.assetid: 4a799a7c-0d2f-460f-99f9-24c6cf7c4537
keywords:
- Métodos CreateCompatibleRenderTarget de Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 0f0de8478d2ab3ee2e7142bd0e197053dc58ac2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162846"
---
# <a name="id2d1rendertargetcreatecompatiblerendertarget-methods"></a>Métodos ID2D1RenderTarget::CreateCompatibleRenderTarget

Crea un nuevo destino de representación de mapa de bits para usarlo durante el dibujo fuera de pantalla intermedio que es compatible con el destino de representación actual.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateCompatibleRenderTarget(D2D1 \_ SIZE \_ F,D2D1 \_ SIZE \_ U,D2D1 \_ PIXEL \_ FORMAT,D2D1 \_ COMPATIBLE RENDER TARGET \_ \_ \_ OPTIONS,ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget))       | Crea un destino de representación de mapa de bits para usarlo durante el dibujo fuera de pantalla intermedio que es compatible con el destino de representación actual.<br/>                                                                                                             |
| [**CreateCompatibleRenderTarget(D2D1 \_ SIZE \_ F \* ,D2D1 \_ SIZE \_ \* U,D2D1 \_ PIXEL FORMAT \_ \* ,D2D1 \_ COMPATIBLE RENDER TARGET \_ \_ \_ OPTIONS,ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget)) | Crea un destino de representación de mapa de bits para usarlo durante el dibujo fuera de pantalla intermedio que es compatible con el destino de representación actual. <br/>                                                                                                            |
| [**CreateCompatibleRenderTarget(ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))                                                                                                 | Crea un nuevo destino de representación de mapa de bits para su uso durante el dibujo fuera de pantalla intermedio que es compatible con el destino de representación actual y tiene el mismo tamaño, PPP y formato de píxel (pero no el modo alfa) que el destino de representación actual. <br/>         |
| [**CreateCompatibleRenderTarget(D2D1 \_ SIZE \_ F,ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_id2d1bitmaprendertarget))                                                                                   | Crea un nuevo destino de representación de mapa de bits para su uso durante el dibujo fuera de pantalla intermedio que es compatible con el destino de representación actual y tiene el mismo formato de píxel (pero no el modo alfa) que el destino de representación actual. <br/>                        |
| [**CreateCompatibleRenderTarget(D2D1 \_ SIZE \_ F,D2D1 \_ SIZE \_ U,ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_id2d1bitmaprendertarget))                                                                     | Crea un destino de representación de mapa de bits para usarlo durante el dibujo intermedio fuera de la pantalla que es compatible con el destino de representación actual. El nuevo destino de representación de mapa de bits tiene el mismo formato de píxel (pero no el modo alfa) que el destino de representación actual. <br/> |
| [**CreateCompatibleRenderTarget(D2D1 \_ SIZE \_ F,D2D1 \_ SIZE \_ U,D2D1 \_ PIXEL \_ FORMAT,ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_id2d1bitmaprendertarget))                                                 | Crea un destino de representación de mapa de bits para usarlo durante el dibujo fuera de pantalla intermedio que es compatible con el destino de representación actual. <br/>                                                                                                            |



## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa el **método CreateCompatibleRenderTarget** para crear un [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) y se usa para dibujar un patrón de cuadrícula. El patrón de cuadrícula se usa como origen de [**id2D1BitmapBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)


```C++
HRESULT DemoApp::CreateGridPatternBrush(
    ID2D1RenderTarget *pRenderTarget,
    ID2D1BitmapBrush **ppBitmapBrush
    )
{
    // Create a compatible render target.
    ID2D1BitmapRenderTarget *pCompatibleRenderTarget = NULL;
    HRESULT hr = pRenderTarget->CreateCompatibleRenderTarget(
        D2D1::SizeF(10.0f, 10.0f),
        &amp;pCompatibleRenderTarget
        );
    if (SUCCEEDED(hr))
    {
        // Draw a pattern.
        ID2D1SolidColorBrush *pGridBrush = NULL;
        hr = pCompatibleRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
            &amp;pGridBrush
            );
        if (SUCCEEDED(hr))
        {
            pCompatibleRenderTarget->BeginDraw();
            pCompatibleRenderTarget->FillRectangle(D2D1::RectF(0.0f, 0.0f, 10.0f, 1.0f), pGridBrush);
            pCompatibleRenderTarget->FillRectangle(D2D1::RectF(0.0f, 0.1f, 1.0f, 10.0f), pGridBrush);
            pCompatibleRenderTarget->EndDraw();

            // Retrieve the bitmap from the render target.
            ID2D1Bitmap *pGridBitmap = NULL;
            hr = pCompatibleRenderTarget->GetBitmap(&amp;pGridBitmap);
            if (SUCCEEDED(hr))
            {
                // Choose the tiling mode for the bitmap brush.
                D2D1_BITMAP_BRUSH_PROPERTIES brushProperties =
                    D2D1::BitmapBrushProperties(D2D1_EXTEND_MODE_WRAP, D2D1_EXTEND_MODE_WRAP);

                // Create the bitmap brush.
                hr = m_pRenderTarget->CreateBitmapBrush(pGridBitmap, brushProperties, ppBitmapBrush);

                pGridBitmap->Release();
            }

            pGridBrush->Release();
        }

        pCompatibleRenderTarget->Release();
    }

    return hr;
}
```



En el ejemplo de código siguiente se usa el pincel para pintar un patrón.


```C++
// Paint a grid background.
m_pRenderTarget->FillRectangle(
    D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
    m_pGridPatternBitmapBrush
    );
```



En este ejemplo se ha omitido el código.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�

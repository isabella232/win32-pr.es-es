---
title: Métodos ID2D1RenderTarget FillRoundedRectangle (D2d1. h)
description: Pinta el interior del rectángulo redondeado especificado.
ms.assetid: 9c4765b0-858f-4a20-b044-0acf87a1f131
keywords:
- Métodos de FillRoundedRectangle Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 2abc39ed364de0653813aab14ee5777ccf3c4e08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660326"
---
# <a name="id2d1rendertargetfillroundedrectangle-methods"></a>ID2D1RenderTarget:: FillRoundedRectangle (métodos)

Pinta el interior del rectángulo redondeado especificado.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                          | Descripción                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [**FillRoundedRectangle (D2D1 \_ redondeado \_ rectangular&, ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillroundedrectangle(constd2d1_rounded_rect__id2d1brush))  | Pinta el interior del rectángulo redondeado especificado. <br/> |
| [**FillRoundedRectangle ( \_ rectángulo redondeado \_ D2D1 \* , ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillroundedrectangle(constd2d1_rounded_rect__id2d1brush)) | Pinta el interior del rectángulo redondeado especificado.<br/>  |



## <a name="remarks"></a>Observaciones

Este método no devuelve un código de error si se produce un error. Para determinar si una operación de dibujo (como **FillRoundedRectangle**) produjo un error, compruebe el resultado devuelto por los métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usan los métodos [**DrawRoundedRectangle**](id2d1rendertarget-drawroundedrectangle.md) y **FillRoundedRectangle** para esquematizar y rellenar un rectángulo redondeado. En este ejemplo se genera el resultado que se muestra en la ilustración siguiente.

![Ilustración de cuatro rectángulos redondeados con distintos estilos y rellenos de trazo](images/drawroundedrectangle-scr.png)


```C++
//  Called whenever the application needs to display the client
//  window.
HRESULT DrawAndFillRoundedRectangleExample::OnRender()
{
    HRESULT hr;

    // Create the render target and brushes if they
    // don't already exists.
    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        // Paint a grid background.
        m_pRenderTarget->FillRectangle(
            D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
            m_pGridPatternBitmapBrush
            );

        // Define a rounded rectangle.
        D2D1_ROUNDED_RECT roundedRect = D2D1::RoundedRect(
            D2D1::RectF(20.f, 20.f, 150.f, 100.f),
            10.f,
            10.f
            );

        // Draw the rectangle.
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f);

        // Apply a translation transform.
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(200.f, 0.f));

        // Draw the rounded rectangle again, this time with a dashed stroke.
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);

        // Apply another translation transform.
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(0.f, 150.f));

        // Draw, then fill the rounded rectangle.
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);
        m_pRenderTarget->FillRoundedRectangle(roundedRect, m_pSilverBrush);

        // Apply another translation transform.
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(200.f, 150.f));

        // Fill, then draw the rounded rectangle.
        m_pRenderTarget->FillRoundedRectangle(roundedRect, m_pSilverBrush);
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Cómo dibujar y rellenar una forma básica](how-to-draw-an-ellipse.md)
</dt> <dt>

[**D2D1::RoundedRect**](/windows/win32/api/d2d1/nf-d2d1-id2d1roundedrectanglegeometry-getroundedrect)
</dt> </dl>

�

�

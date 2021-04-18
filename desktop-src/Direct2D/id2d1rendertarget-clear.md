---
title: ID2D1RenderTarget borrar métodos
description: Borra el área de dibujo con el color especificado.
ms.assetid: 3bfec923-17fc-479a-a760-9baab2ff3a56
keywords:
- Borrar métodos Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 346e44e3ce0b59e40577d3207f45faafdc33b367
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660910"
---
# <a name="id2d1rendertargetclear-methods"></a>ID2D1RenderTarget:: CLEAR (métodos)

Borra el área de dibujo con el color especificado.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                 | Descripción                                                 |
|:-----------------------------------------------------------------------|:------------------------------------------------------------|
| [**Borrar (D2D1 de \_ color \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) | Borra el área de dibujo con el color especificado. <br/> |
| [**Clear (D2D1 de \_ color \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f_))  | Borra el área de dibujo con el color especificado. <br/> |



## <a name="remarks"></a>Observaciones

Direct2D interpreta *clearColor* como alfa recto (no multiplicado previamente). Si el modo alfa del destino de representación es el [**\_ \_ modo \_ alfa D2D1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), el canal alfa de *clearColor* se omite y se reemplaza con 1,0 f (totalmente opaco).

Si el destino de representación tiene un clip activo (especificado por [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))), el comando borrar solo se aplica al área dentro de la región de recorte.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa el método **Clear** para crear un fondo blanco antes de representar otro contenido.


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

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
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 


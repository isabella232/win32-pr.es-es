---
title: Métodos de ID2D1RenderTarget PushLayer (D2d1 \_ 1. h)
description: Agrega la capa especificada al destino de representación para que reciba todas las operaciones de dibujo posteriores hasta que se llame a PopLayer.
ms.assetid: 9336662c-e94e-40ba-adbe-066d704958bc
keywords:
- Métodos de PushLayer Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 6a5609192162ae0b0c0e2af8f1b84429d8710509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691044"
---
# <a name="id2d1rendertargetpushlayer-methods"></a>ID2D1RenderTarget::P ushLayer métodos)

Agrega la capa especificada al destino de representación para que reciba todas las operaciones de dibujo posteriores hasta que se llame a [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                            | Descripción                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PushLayer ( \_ \_ parámetros de nivel D2D1&, ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))  | Agrega la capa especificada al destino de representación para que reciba todas las operaciones de dibujo posteriores hasta que se llame a [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) . <br/> |
| [**PushLayer ( \_ \_ parámetros de nivel D2D1 \* , ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer)) | Agrega la capa especificada al destino de representación para que reciba todas las operaciones de dibujo posteriores hasta que se llame a [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) . <br/> |



## <a name="remarks"></a>Observaciones

El método [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) permite a un llamador comenzar a redirigir la representación a una capa. Todas las operaciones de representación son válidas en una capa. La ubicación de la capa se ve afectada por el conjunto de transformación universal en el destino de representación.

Cada **PushLayer** debe tener una llamada [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) coincidente. Si hay más llamadas a **PopLayer** que llamadas a **PushLayer** , el destino de representación se coloca en un estado de error. Si se llama a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) antes de que se extraigan todos los niveles pendientes, el destino de representación se coloca en un estado de error y se devuelve un error. El estado de error se puede borrar mediante una llamada a [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

Un recurso [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) determinado solo puede estar activo al mismo tiempo. En otras palabras, no puede llamar a un método [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) y después seguir inmediatamente con otro método **PushLayer** con el mismo recurso de capa. En su lugar, debe llamar al segundo método **PushLayer** con distintos recursos de capa.

Para obtener un ejemplo, consulte [Cómo recortar una región con capas](how-to-clip-with-layers.md).

Este método no devuelve un código de error si se produce un error. Para determinar si una operación de dibujo (como **PushLayer**) produjo un error, compruebe el resultado devuelto por los métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa una capa para recortar un mapa de bits a una máscara geométrica. Para obtener el ejemplo completo, consulte [Cómo recortar en una máscara geométrica](how-to-clip-with-layers.md).


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &amp;pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&amp;pLayer);

    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D2d1 \_ 1. h (incluir D2d1. h)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Información general sobre capas](direct2d-layers-overview.md)
</dt> </dl>

�

�

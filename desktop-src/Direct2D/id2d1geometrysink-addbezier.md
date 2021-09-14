---
title: Métodos ID2D1GeometrySink AddBezier (D2d1.h)
description: Crea una curva Bézier cúbica entre el punto actual y el punto de conexión especificado y la agrega al receptor de geometría.
ms.assetid: d1e228eb-dac6-485d-b3c9-69b2bd45e531
keywords:
- Métodos AddBezier de Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b470129350463920583c34bec5f886f60b16485e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162930"
---
# <a name="id2d1geometrysinkaddbezier-methods"></a>Métodos ID2D1GeometrySink::AddBezier

Crea una curva Bézier cúbica entre el punto actual y el punto de conexión especificado y la agrega al receptor de geometría.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                            | Descripción                                                                                    |
|:--------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**AddBezier(D2D1 \_ BEZIER \_ SEGMENT&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment_))  | Crea una curva Bézier cúbica entre el punto actual y el punto final especificado.<br/> |
| [**AddBezier(D2D1 \_ BEZIER \_ SEGMENT \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment)) | Crea una curva Bézier cúbica entre el punto actual y el punto de conexión especificado.<br/>  |



## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea [**un id2D1PathGeometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)se recupera un receptor y se usa para definir una forma de reloj de reloj. Para obtener el ejemplo completo, [vea Cómo dibujar y rellenar una forma compleja.](how-to-draw-and-fill-a-complex-shape.md)


```C++
ID2D1GeometrySink *pSink = NULL;



// Create a path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);

    if (SUCCEEDED(hr))
    {
        // Write to the path geometry using the geometry sink.
        hr = m_pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            pSink->BeginFigure(
                D2D1::Point2F(0, 0),
                D2D1_FIGURE_BEGIN_FILLED
                );

            pSink->AddLine(D2D1::Point2F(200, 0));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(150, 50),
                    D2D1::Point2F(150, 150),
                    D2D1::Point2F(200, 200))
                );

            pSink->AddLine(D2D1::Point2F(0, 200));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(50, 150),
                    D2D1::Point2F(50, 50),
                    D2D1::Point2F(0, 0))
                );

            pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

            hr = pSink->Close();
        }
        SafeRelease(&pSink);
    }
}
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)
</dt> </dl>

�

�

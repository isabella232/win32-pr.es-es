---
title: Métodos ID2D1Factory CreateTransformedGeometry (D2d1. h)
description: Transforma la geometría especificada y almacena el resultado como un objeto ID2D1TransformedGeometry.
ms.assetid: 71f26200-0f35-49d7-951d-2962768d16bc
keywords:
- Métodos de CreateTransformedGeometry Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5da3b548c3118209c915714e03fe9e4061c77e96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679197"
---
# <a name="id2d1factorycreatetransformedgeometry-methods"></a>ID2D1Factory:: CreateTransformedGeometry (métodos)

Transforma la geometría especificada y almacena el resultado como un objeto [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                                  | Descripción                                                                                                                                    |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateTransformedGeometry (ID2D1Geometry \* , D2D \_ Matrix \_ 3x2 \_ F \* , ID2D1TransformedGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) | Transforma la geometría especificada y almacena el resultado como un objeto [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) . <br/> |
| [**CreateTransformedGeometry (ID2D1Geometry \* , D2D \_ Matrix \_ 3x2 \_ F&, ID2D1TransformedGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))  | Transforma la geometría especificada y almacena el resultado como un objeto [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) . <br/> |



## <a name="remarks"></a>Observaciones

Al igual que otros recursos, una geometría transformada hereda el espacio de recursos y la Directiva de subprocesos del generador que lo creó. Este objeto es inmutable.

Al trazar una geometría transformada con el método [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) , el ancho del trazo no se ve afectado por la transformación que se aplica a la geometría. El ancho del trazo solo se ve afectado por la transformación del mundo.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea una [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))y, a continuación, se dibuja sin transformarla. Genera la salida que se muestra en la ilustración siguiente.

![Ilustración de un rectángulo](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```



En el ejemplo siguiente se usa el destino de representación para escalar la geometría en un factor de 3 y, a continuación, se dibuja. En la ilustración siguiente se muestra el resultado de dibujar el rectángulo sin la transformación y con la transformación; observa que el trazo es más grueso después de la transformación, aunque el grosor del trazo sea 1.

![Ilustración de un rectángulo más pequeño dentro de un rectángulo más grande con un trazo más grueso](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



En el ejemplo siguiente se usa el método **CreateTransformedGeometry** para escalar la geometría en un factor de 3 y, a continuación, se dibuja. Genera la salida que se muestra en la ilustración siguiente. Observe que, aunque el rectángulo es mayor, su trazo no ha aumentado.

![Ilustración de un rectángulo más pequeño dentro de un rectángulo más grande con el mismo trazo](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );


// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

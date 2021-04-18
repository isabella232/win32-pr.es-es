---
title: D2D1_MATRIX_3X2_F (D2d1. h)
description: Representa una matriz de 3 por 2.
ms.assetid: f05d7555-6482-4eea-950f-7b443892cc1f
keywords:
- D2D1_MATRIX_3X2_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb252e35508c48570c96f251205fc8a54755687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676659"
---
# <a name="d2d1_matrix_3x2_f"></a>D2D1 \_ Matrix \_ 3x2 \_ F

Representa una matriz de 3 por 2.


```C++
typedef D2D_MATRIX_3X2_F D2D1_MATRIX_3X2_F;
```



## <a name="remarks"></a>Observaciones

**D2D1 \_ MATRIX \_ 3x2** es un nombre nuevo para la estructura de la [**matriz de D2D \_ \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) . Para obtener una lista de los campos que proporciona la matriz, vea [**D2D \_ Matrix \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).

Para simplificar las operaciones de matriz comunes, Direct2D proporciona la clase [**D2D1:: Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) , que se deriva de la estructura 3x2 de la [**\_ matriz \_ D2D1**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) . La clase **Matrix3x2F** proporciona un conjunto de métodos auxiliares para realizar tareas comunes, como la creación de una matriz de traslación o sesgo.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa el método [**D2D1:: Matrix3x2F:: Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) para crear una matriz de rotación que gira un cuadrado en el sentido de las agujas del reloj 45 grados sobre el centro del cuadrado y pasa la matriz al método [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) del destino de representación (*m \_ pRenderTarget*).

En la ilustración siguiente se muestra el efecto de aplicar la transformación rotación anterior al cuadrado. El cuadrado original es un contorno punteado y el cuadrado girado es un contorno sólido.

![Ilustración de un cuadrado girado en el sentido de las agujas del reloj 45 grados sobre el centro del cuadrado original](images/rotate-ovw.png)


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



El código se ha omitido en este ejemplo. Para obtener más información sobre las transformaciones, vea [información general sobre transformaciones](direct2d-transforms-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D2D1::Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)
</dt> <dt>

[Información general sobre transformaciones](direct2d-transforms-overview.md)
</dt> <dt>

[Cómo girar un objeto](how-to-rotate.md)
</dt> <dt>

[Cómo escalar un objeto](how-to-scale.md)
</dt> <dt>

[Cómo sesgar un objeto](how-to-skew.md)
</dt> <dt>

[Cómo trasladar un objeto](how-to-translate.md)
</dt> <dt>

[**D2D \_ Matrix \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)
</dt> </dl>

 


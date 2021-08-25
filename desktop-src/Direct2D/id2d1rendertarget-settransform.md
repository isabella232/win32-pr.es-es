---
title: Métodos Id2D1RenderTarget SetTransform
description: Aplica la transformación especificada al destino de representación, reemplazando la transformación existente. Todas las operaciones de dibujo posteriores se producen en el espacio transformado.
ms.assetid: 04799366-6458-40ff-a2fb-5d227eab041d
keywords:
- Métodos SetTransform de Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: f23ffcd8d64df02b0be2287a33eff63a6a680200c0e051a15c77958dafd81438
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873965"
---
# <a name="id2d1rendertargetsettransform-methods"></a>Métodos ID2D1RenderTarget::SetTransform

Aplica la transformación especificada al destino de representación, reemplazando la transformación existente. Todas las operaciones de dibujo posteriores se producen en el espacio transformado.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                              | Descripción                                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetTransform(D2D1 \_ MATRIX \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))  | Aplica la transformación especificada al destino de representación, reemplazando la transformación existente. Todas las operaciones de dibujo posteriores se producen en el espacio transformado. <br/> |
| [**SetTransform(D2D1 \_ MATRIX \_ 3X2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f)) | Aplica la transformación especificada al destino de representación, reemplazando la transformación existente. Todas las operaciones de dibujo posteriores se producen en el espacio transformado.<br/>  |



## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **el método SetTransform** para aplicar una rotación al destino de representación. Para obtener el ejemplo completo, [vea How to Rotate an Object](how-to-rotate.md).


```C++
// Apply the rotation transform to the render target.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(
        45.0f,
        D2D1::Point2F(468.0f, 331.5f))
    );
```



Para obtener ejemplos adicionales que muestran cómo transformar un destino de representación, vea [How to Scale an Object](how-to-scale.md), How to Skew an [Object](how-to-skew.md)y How to Translate [an Object](how-to-translate.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Introducción a las transformaciones](direct2d-transforms-overview.md)
</dt> <dt>

[Cómo girar un objeto](how-to-rotate.md)
</dt> <dt>

[Cómo escalar un objeto](how-to-scale.md)
</dt> <dt>

[Cómo sesgar un objeto](how-to-skew.md)
</dt> <dt>

[Cómo traducir un objeto](how-to-translate.md)
</dt> <dt>

[Cómo aplicar varias transformaciones a un objeto](how-to-apply-multiple-transforms.md)
</dt> </dl>

 


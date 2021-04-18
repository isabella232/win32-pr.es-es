---
title: Métodos ID2D1RenderTarget SetTransform
description: Aplica la transformación especificada al destino de representación, reemplazando la transformación existente. Todas las operaciones de dibujo posteriores se producen en el espacio transformado.
ms.assetid: 04799366-6458-40ff-a2fb-5d227eab041d
keywords:
- Métodos de SetTransform Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 8310bf9e5c97beb3ea3cf3b2a9a513f606079a18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661375"
---
# <a name="id2d1rendertargetsettransform-methods"></a>ID2D1RenderTarget:: SetTransform (métodos)

Aplica la transformación especificada al destino de representación, reemplazando la transformación existente. Todas las operaciones de dibujo posteriores se producen en el espacio transformado.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                              | Descripción                                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetTransform (D2D1 \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))  | Aplica la transformación especificada al destino de representación, reemplazando la transformación existente. Todas las operaciones de dibujo posteriores se producen en el espacio transformado. <br/> |
| [**SetTransform (D2D1 \_ Matrix \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f)) | Aplica la transformación especificada al destino de representación, reemplazando la transformación existente. Todas las operaciones de dibujo posteriores se producen en el espacio transformado.<br/>  |



## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa el método **SetTransform** para aplicar un giro al destino de representación. Para obtener el ejemplo completo, consulte [cómo girar un objeto](how-to-rotate.md).


```C++
// Apply the rotation transform to the render target.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(
        45.0f,
        D2D1::Point2F(468.0f, 331.5f))
    );
```



Para obtener ejemplos adicionales que muestran cómo transformar un destino de representación, vea [Cómo escalar un objeto](how-to-scale.md), [Cómo sesgar un objeto](how-to-skew.md)y [Cómo trasladar un objeto](how-to-translate.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
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

[Cómo aplicar varias transformaciones a un objeto](how-to-apply-multiple-transforms.md)
</dt> </dl>

 


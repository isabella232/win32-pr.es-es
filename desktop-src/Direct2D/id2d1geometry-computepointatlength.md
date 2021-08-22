---
title: Métodos ID2D1Geometry ComputePointAtLength
description: Calcula el punto y el vector tangente a la distancia especificada a lo largo de \ 160;geometry.
ms.assetid: b76aa3db-2967-4baa-a449-f664b080fb74
keywords:
- Métodos de ComputePointAtLength Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 6665d5317b5359228f2e27803a8fee443ed8233e893cf7e8986e3af1c21a9373
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342835"
---
# <a name="id2d1geometrycomputepointatlength-methods"></a>Métodos ID2D1Geometry::ComputePointAtLength

Calcula el vector de punto y tangente a la distancia especificada a lo largo de la geometría.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                        | Descripción                                                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComputePointAtLength(FLOAT,D2D1 \_ MATRIX \_ 3X2 \_ F&,D2D1 \_ POINT \_ 2F \* , D2D1 \_ POINT \_ 2F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f__d2d1_point_2f_d2d1_point_2f))              | Calcula el punto y el vector tangente a la distancia especificada a lo largo de la geometría después de que la matriz especificada lo haya transformado y se haya aplanado con la tolerancia predeterminada.<br/>   |
| [**ComputePointAtLength(FLOAT,D2D1 \_ MATRIX \_ 3X2 \_ F , \* D2D1 \_ POINT \_ 2F \* , D2D1 \_ POINT \_ 2F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f_d2d1_point_2f_d2d1_point_2f))             | Calcula el punto y el vector tangente a la distancia especificada a lo largo de la geometría después de que la matriz especificada lo haya transformado y se haya aplanado con la tolerancia predeterminada.<br/>   |
| [**ComputePointAtLength(FLOAT,D2D1 \_ MATRIX \_ 3X2 \_ F&,FLOAT,D2D1 \_ POINT \_ 2F \* , D2D1 \_ POINT \_ 2F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink))  | Calcula el vector de punto y tangente a la distancia especificada a lo largo de la geometría después de que la matriz especificada lo haya transformado y aplanado con la tolerancia especificada.<br/> |
| [**ComputePointAtLength(FLOAT,D2D1 \_ MATRIX \_ 3X2 \_ F , \* FLOAT,D2D1 \_ POINT \_ 2F \* , D2D1 POINT \_ \_ 2F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f_float_d2d1_point_2f_d2d1_point_2f)) | Calcula el vector de punto y tangente a la distancia especificada a lo largo de la geometría después de que la matriz especificada lo haya transformado y aplanado con la tolerancia especificada.<br/> |



## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo usar **ComputePointAtLength** para calcular el vector de punto y tangente a la distancia especificada a lo largo de la geometría.


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;
```




```C++
// Ask the geometry to give us the point that corresponds with the
// length at the current time.
hr = m_pPathGeometry->ComputePointAtLength(
    length, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 


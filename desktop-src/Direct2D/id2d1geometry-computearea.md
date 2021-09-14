---
title: Métodos ComputeArea ID2D1Geometry
description: Calcula el área de la geometría.
ms.assetid: 655f11bc-7435-4d23-b4b1-3d7c2110aa48
keywords:
- Métodos ComputeArea Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: f6b79e8434a2174bcb05659f6656a46cc2d43cbb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162978"
---
# <a name="id2d1geometrycomputearea-methods"></a>Métodos ID2D1Geometry::ComputeArea

Calcula el área de la geometría.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                      | Descripción                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComputeArea(D2D1 \_ MATRIX \_ 3X2 \_ F&,FLOAT \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))              | Calcula el área de la geometría después de que se haya transformado por la matriz especificada y se haya aplanado con la tolerancia predeterminada.<br/>    |
| [**ComputeArea(D2D1 \_ MATRIX \_ 3X2 \_ F , FLOAT \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))             | Calcula el área de la geometría después de que se haya transformado por la matriz especificada y se haya aplanado mediante la tolerancia predeterminada.<br/> |
| [**ComputeArea(D2D1 \_ MATRIX \_ 3X2 \_ F&,FLOAT,FLOAT \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))  | Calcula el área de la geometría después de que se haya transformado por la matriz especificada y se haya aplanado con la tolerancia especificada.<br/>  |
| [**ComputeArea(D2D1 \_ MATRIX \_ 3X2 \_ F , \* FLOAT,FLOAT \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float)) | Calcula el área de la geometría después de que se haya transformado por la matriz especificada y se haya aplanado con la tolerancia especificada.<br/>  |



## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se **usa ComputeArea** para calcular el área de un círculo especificado (**m \_ pCircleGeometry1**).


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 


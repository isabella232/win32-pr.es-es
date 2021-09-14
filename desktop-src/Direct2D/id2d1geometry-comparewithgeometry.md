---
title: Métodos ID2D1Geometry CompareWithGeometry
description: Describe la intersección entre esta geometría y la geometría especificada.
ms.assetid: 75ddd674-b50b-4d34-b291-9e7e65828304
keywords:
- Métodos CompareWithGeometry de Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: eee64e51d4717a9fe0983be849c78f99602cac9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162986"
---
# <a name="id2d1geometrycomparewithgeometry-methods"></a>Métodos ID2D1Geometry::CompareWithGeometry

Describe la intersección entre esta geometría y la geometría especificada.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                            | Descripción                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CompareWithGeometry(ID2D1Geometry \* ,D2D1 \_ MATRIX \_ 3X2 \_ F&,D2D1 \_ GEOMETRY RELATION \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__d2d1_geometry_relation))              | Describe la intersección entre esta geometría y la geometría especificada. La comparación se realiza utilizando la tolerancia de aplanación predeterminada.<br/>      |
| [**CompareWithGeometry(ID2D1Geometry \* ,D2D1 \_ MATRIX \_ 3X2 \_ F , \* D2D1 \_ GEOMETRY RELATION \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_d2d1_geometry_relation))             | Describe la intersección entre esta geometría y la geometría especificada. La comparación se realiza utilizando la tolerancia de aplanación predeterminada.<br/>      |
| [**CompareWithGeometry(ID2D1Geometry \* ,D2D1 \_ MATRIX \_ 3X2 \_ F&,FLOAT,D2D1 GEOMETRY RELATION \_ \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__float_d2d1_geometry_relation))  | Describe la intersección entre esta geometría y la geometría especificada. La comparación se realiza utilizando la tolerancia de aplanación especificada.<br/>    |
| [**CompareWithGeometry(ID2D1Geometry \* ,D2D1 \_ MATRIX \_ 3X2 \_ F , \* FLOAT,D2D1 \_ GEOMETRY RELATION \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_float_d2d1_geometry_relation)) | Describe la intersección entre esta geometría y la geometría especificada. La comparación se realiza mediante la tolerancia de aplanación especificada.<br/> |



## <a name="remarks"></a>Observaciones

Al interpretar el  valor de relación devuelto, es importante recordar que el miembro [**D2D1 \_ GEOMETRY RELATION \_ IS \_ \_ CONTAINED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) del tipo de enumeración **D2D1 \_ GEOMETRY \_ RELATION** significa que esta geometría se encuentra dentro de *inputGeometry,* no que esta geometría contiene *inputGeometry.*

Para obtener más información sobre cómo interpretar otros valores devueltos posibles, vea [**D2D1 \_ GEOMETRY \_ RELATION**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 


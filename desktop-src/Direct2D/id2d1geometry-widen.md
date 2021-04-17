---
title: ID2D1Geometry (métodos)
description: Amplía la geometría por el trazo especificado y escribe el resultado en un ID2D1SimplifiedGeometrySink.
ms.assetid: c951ab85-7980-41e3-95c4-291d2fb046c8
keywords:
- Ampliar métodos Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 73a1ce3f90192f49a719a92d80f448694ce43235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660918"
---
# <a name="id2d1geometrywiden-methods"></a>ID2D1Geometry:: Wide (métodos)

Amplía la geometría por el trazo especificado y escribe el resultado en un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                          | Descripción                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Widening (FLOAT, ID2D1StrokeStyle \* , D2D1 \_ Matrix \_ 3x2 \_ F \* , ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))             | Amplía la geometría por el trazo especificado y escribe el resultado en un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) una vez transformada por la matriz especificada y plana con la tolerancia predeterminada.<br/>   |
| [**Widening (FLOAT, ID2D1StrokeStyle \* , D2D1 \_ Matrix \_ 3x2 \_ F&, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))              | Amplía la geometría por el trazo especificado y escribe el resultado en un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) una vez transformada por la matriz especificada y plana con la tolerancia predeterminada.<br/>   |
| [**Widening (FLOAT, ID2D1StrokeStyle \* , D2D1 \_ Matrix \_ 3x2 \_ F \* , Float, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink)) | Amplía la geometría por el trazo especificado y escribe el resultado en un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) una vez transformada por la matriz especificada y plana con la tolerancia especificada.<br/> |
| [**Wide (FLOAT, ID2D1StrokeStyle \* , D2D1 \_ Matrix \_ 3x2 \_ F&, Float, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))  | Amplía la geometría por el trazo especificado y escribe el resultado en un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) una vez transformada por la matriz especificada y plana con la tolerancia especificada.<br/> |



## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo usar **ensanchar** para ensanchar la geometría por el trazo especificado y, a continuación, escribir el resultado en un objeto [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) .


```C++
 ID2D1GeometrySink *pGeometrySink = NULL;
 hr = pPathGeometry->Open(&pGeometrySink);
 if (SUCCEEDED(hr))
 {
     hr = pGeometry->Widen(
             strokeWidth,
             pIStrokeStyle,
             pWorldTransform,
             pGeometrySink
             );

     if (SUCCEEDED(hr))
     {
         hr = pGeometrySink->Close();
         if (SUCCEEDED(hr))
         {
             ID2D1Mesh *pMesh = NULL;
             hr = m_pRT->CreateMesh(&pMesh);
             if (SUCCEEDED(hr))
             {
                 ID2D1TessellationSink *pSink = NULL;
                 hr = pMesh->Open(&pSink);
                 if (SUCCEEDED(hr))
                 {
                     hr = pPathGeometry->Tessellate(
                             NULL, // world transform (already handled in Widen)
                             pSink
                             );
                     if (SUCCEEDED(hr))
                     {
                         hr = pSink->Close();
                         if (SUCCEEDED(hr))
                         {
                             SafeReplace(&m_pStrokeMesh, pMesh);
                         }
                     }
                     pSink->Release();
                 }
                 pMesh->Release();
             }
         }
     }
     pGeometrySink->Release();
 }
 pPathGeometry->Release();
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 


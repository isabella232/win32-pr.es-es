---
title: Métodos ID2D1Geometry dividirlas
description: Crea un conjunto de triángulos hacia la derecha que cubren la geometría después de que se haya transformado mediante la matriz especificada y aplanada mediante la tolerancia especificada.
ms.assetid: 4e0af188-d14b-43c0-be11-16577f054b90
keywords:
- Métodos de dividirlas Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 060fc42dddd7642f021d073b8addbe089d031393
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680547"
---
# <a name="id2d1geometrytessellate-methods"></a>ID2D1Geometry:: dividirlas (métodos)

Crea un conjunto de triángulos hacia la derecha que cubren la geometría después de que se haya transformado mediante la matriz especificada y aplanada mediante la tolerancia especificada.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                    | Descripción                                                                                                                                                                          |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dividirlas (D2D1 \_ Matrix \_ 3x2 \_ F \* , ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f__id2d1tessellationsink))             | Crea un conjunto de triángulos hacia la derecha que cubren la geometría después de que se haya transformado utilizando la matriz especificada y se haya simplificado con la tolerancia predeterminada. <br/>   |
| [**Dividirlas (D2D1 \_ Matrix \_ 3X2 \_ F&, ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f_id2d1tessellationsink))              | Crea un conjunto de triángulos hacia la derecha que cubren la geometría después de que se haya transformado utilizando la matriz especificada y se haya simplificado con la tolerancia predeterminada. <br/>   |
| [**Dividirlas (D2D1 \_ Matrix \_ 3x2 \_ F \* , Float, ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f_float_id2d1tessellationsink)) | Crea un conjunto de triángulos hacia la derecha que cubren la geometría después de que se haya transformado mediante la matriz especificada y aplanada mediante la tolerancia especificada. <br/> |
| [**Dividirlas (D2D1 \_ Matrix \_ 3X2 \_ F&, Float, ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f__float_id2d1tessellationsink))  | Crea un conjunto de triángulos hacia la derecha que cubren la geometría después de que se haya transformado mediante la matriz especificada y aplanada mediante la tolerancia especificada.<br/>  |



## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo usar dividirlas para crear un conjunto de triángulos que cubren la geometría en sentido de las agujas del reloj.


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

 


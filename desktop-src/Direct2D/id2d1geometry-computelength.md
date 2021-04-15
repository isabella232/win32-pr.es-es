---
title: Métodos ID2D1Geometry ComputeLength
description: Calcula la longitud de la geometría como si se hubiera desscrito cada segmento en una línea.
ms.assetid: 4659d880-0aa3-485d-ac71-044d9ace6759
keywords:
- Métodos de ComputeLength Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: b49b1beb0525d95967ad903b0f0fb3c464edf4d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661378"
---
# <a name="id2d1geometrycomputelength-methods"></a>ID2D1Geometry:: ComputeLength (métodos)

Calcula la longitud de la geometría como si se hubiera desscrito cada segmento en una línea.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                          | Descripción                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**ComputeLength (D2D1 \_ Matrix \_ 3X2 \_ F&, Float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))              | Calcula la longitud de la geometría como si se hubiera desscrito cada segmento en una línea.<br/>  |
| [**ComputeLength (D2D1 \_ Matrix \_ 3x2 \_ F \* , Float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))             | Calcula la longitud de la geometría como si se hubiera desscrito cada segmento en una línea.<br/>  |
| [**ComputeLength (D2D1 \_ Matrix \_ 3X2 \_ F&, Float, Float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f__float_float))  | Calcula la longitud de la geometría como si se hubiera desscrito cada segmento en una línea.<br/>  |
| [**ComputeLength (D2D1 \_ Matrix \_ 3x2 \_ F \* , Float, Float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float)) | Calcula la longitud de la geometría como si se hubiera desscrito cada segmento en una línea. <br/> |



## <a name="examples"></a>Ejemplos

En el código siguiente se muestra cómo usar **ComputeLength** para calcular la longitud de una geometría de ruta de acceso especificada.


```C++
float length = 0;
hr = m_pPathGeometry->ComputeLength(
    NULL, //no transform
    &length
    );

if (SUCCEEDED(hr))
{
    m_Animation.SetStart(0);        //start at beginning of path
    m_Animation.SetEnd(length);     //length at end of path
    m_Animation.SetDuration(5.0f);  //seconds

    ZeroMemory(&m_DwmTimingInfo, sizeof(m_DwmTimingInfo));
    m_DwmTimingInfo.cbSize = sizeof(m_DwmTimingInfo);

    // Get the composition refresh rate. If the DWM isn't running,
    // get the refresh rate from GDI -- probably going to be 60Hz
    if (FAILED(DwmGetCompositionTimingInfo(NULL, &m_DwmTimingInfo)))
    {
        HDC hdc = GetDC(m_hwnd);
        m_DwmTimingInfo.rateCompose.uiDenominator = 1;
        m_DwmTimingInfo.rateCompose.uiNumerator = GetDeviceCaps(hdc, VREFRESH);
        ReleaseDC(m_hwnd, hdc);
    }

    ShowWindow(m_hwnd, SW_SHOWNORMAL);

    UpdateWindow(m_hwnd);
}
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

 


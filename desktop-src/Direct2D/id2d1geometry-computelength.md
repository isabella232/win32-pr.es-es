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
# <a name="id2d1geometrycomputelength-methods"></a><span data-ttu-id="3f84b-104">ID2D1Geometry:: ComputeLength (métodos)</span><span class="sxs-lookup"><span data-stu-id="3f84b-104">ID2D1Geometry::ComputeLength methods</span></span>

<span data-ttu-id="3f84b-105">Calcula la longitud de la geometría como si se hubiera desscrito cada segmento en una línea.</span><span class="sxs-lookup"><span data-stu-id="3f84b-105">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span>

### <a name="overload-list"></a><span data-ttu-id="3f84b-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="3f84b-106">Overload list</span></span>



| <span data-ttu-id="3f84b-107">Método</span><span class="sxs-lookup"><span data-stu-id="3f84b-107">Method</span></span>                                                                                                                          | <span data-ttu-id="3f84b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f84b-108">Description</span></span>                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f84b-109">[**ComputeLength (D2D1 \_ Matrix \_ 3X2 \_ F&, Float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="3f84b-109">[**ComputeLength(D2D1\_MATRIX\_3X2\_F&,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span></span>              | <span data-ttu-id="3f84b-110">Calcula la longitud de la geometría como si se hubiera desscrito cada segmento en una línea.</span><span class="sxs-lookup"><span data-stu-id="3f84b-110">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span><br/>  |
| <span data-ttu-id="3f84b-111">[**ComputeLength (D2D1 \_ Matrix \_ 3x2 \_ F \* , Float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="3f84b-111">[**ComputeLength(D2D1\_MATRIX\_3X2\_F\*,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span></span>             | <span data-ttu-id="3f84b-112">Calcula la longitud de la geometría como si se hubiera desscrito cada segmento en una línea.</span><span class="sxs-lookup"><span data-stu-id="3f84b-112">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span><br/>  |
| <span data-ttu-id="3f84b-113">[**ComputeLength (D2D1 \_ Matrix \_ 3X2 \_ F&, Float, Float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f__float_float))</span><span class="sxs-lookup"><span data-stu-id="3f84b-113">[**ComputeLength(D2D1\_MATRIX\_3X2\_F&,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f__float_float))</span></span>  | <span data-ttu-id="3f84b-114">Calcula la longitud de la geometría como si se hubiera desscrito cada segmento en una línea.</span><span class="sxs-lookup"><span data-stu-id="3f84b-114">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span><br/>  |
| <span data-ttu-id="3f84b-115">[**ComputeLength (D2D1 \_ Matrix \_ 3x2 \_ F \* , Float, Float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="3f84b-115">[**ComputeLength(D2D1\_MATRIX\_3X2\_F\*,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span></span> | <span data-ttu-id="3f84b-116">Calcula la longitud de la geometría como si se hubiera desscrito cada segmento en una línea.</span><span class="sxs-lookup"><span data-stu-id="3f84b-116">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="3f84b-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3f84b-117">Examples</span></span>

<span data-ttu-id="3f84b-118">En el código siguiente se muestra cómo usar **ComputeLength** para calcular la longitud de una geometría de ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="3f84b-118">The following code shows how to use **ComputeLength** to compute the length of a specified path geometry.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3f84b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f84b-119">Requirements</span></span>



| <span data-ttu-id="3f84b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f84b-120">Requirement</span></span> | <span data-ttu-id="3f84b-121">Value</span><span class="sxs-lookup"><span data-stu-id="3f84b-121">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3f84b-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f84b-122">Library</span></span><br/> | <dl> <span data-ttu-id="3f84b-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f84b-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="3f84b-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3f84b-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="3f84b-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f84b-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f84b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f84b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f84b-127">**ID2D1Geometry**</span><span class="sxs-lookup"><span data-stu-id="3f84b-127">**ID2D1Geometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 


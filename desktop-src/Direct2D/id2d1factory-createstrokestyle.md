---
title: Métodos ID2D1Factory CreateStrokeStyle
description: Crea un id2D1StrokeStyle que describe el límite inicial, el patrón de guion y otras características de un trazo.
ms.assetid: cc7bd68b-a6eb-4d05-b331-032ce80f375c
keywords:
- Métodos CreateStrokeStyle de Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 09a578cafe6795bbf742d9dac114365d6e850586
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163010"
---
# <a name="id2d1factorycreatestrokestyle-methods"></a>Métodos ID2D1Factory::CreateStrokeStyle

Crea un [**id2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) que describe el límite inicial, el patrón de guion y otras características de un trazo.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                  | Descripción                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateStrokeStyle(D2D1 \_ STROKE STYLE PROPERTIES \_ \_&, FLOAT , \* UINT, ID2D1StrokeStyle \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties__constfloat_uint32_id2d1strokestyle))  | Crea un [**id2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) que describe el límite inicial, el patrón de guion y otras características de un trazo.<br/> |
| [**CreateStrokeStyle(D2D1 \_ STROKE STYLE PROPERTIES , \_ \_ \* \* FLOAT, UINT, ID2D1StrokeStyle \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties_constfloat_uint32_id2d1strokestyle)) | Crea un [**id2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) que describe el límite inicial, el patrón de guion y otras características de un trazo.<br/> |



## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un trazo que usa un patrón de guion personalizado.


```C++
// Dash array for dashStyle D2D1_DASH_STYLE_CUSTOM
float dashes[] = {1.0f, 2.0f, 2.0f, 3.0f, 2.0f, 2.0f};

// Stroke Style with Dash Style -- Custom
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateStrokeStyle(
        D2D1::StrokeStyleProperties(
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_ROUND,
            D2D1_LINE_JOIN_MITER,
            10.0f,
            D2D1_DASH_STYLE_CUSTOM,
            0.0f),
        dashes,
        ARRAYSIZE(dashes),
        &m_pStrokeStyleCustomOffsetZero
        );
}
```



En el ejemplo siguiente se usa el estilo de trazo al dibujar una línea.


```C++
m_pRenderTarget->DrawLine(
    D2D1::Point2F(0, 310),
    D2D1::Point2F(200, 310),
    m_pCornflowerBlueBrush,
    10.0f,
    m_pStrokeStyleCustomOffsetZero
    );
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 


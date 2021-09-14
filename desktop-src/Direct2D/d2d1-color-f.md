---
title: D2D1_COLOR_F (D2DBaseTypes.h)
description: Describe los componentes rojo, verde, azul y alfa de un color. | D2D1_COLOR_F (D2DBaseTypes.h)
ms.assetid: 564d4f41-2da7-49ed-b85a-d1070d662b40
keywords:
- D2D1_COLOR_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f12c4c833d7f73946b2309673dff8f3dd11395
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163526"
---
# <a name="d2d1_color_f"></a>D2D1 \_ COLOR \_ F

Describe los componentes rojo, verde, azul y alfa de un color.


```C++
typedef D2D_COLOR_F D2D1_COLOR_F;
```



## <a name="remarks"></a>Observaciones

**D2D1 \_ COLOR \_ F** es una definición de tipo [**para D2D \_ COLOR \_ F,**](d2d-color-f.md)que a su vez es una definición de tipo [para D3DCOLORVALUE.](../direct3d9/d3dcolorvalue.md) Para obtener información sobre los miembros proporcionados por **D2D1 \_ COLOR \_ F**, vea [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).

La [**clase ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) proporciona un conjunto de colores predefinidos y funciones auxiliares para definir colores. Para obtener más información, vea la [**referencia de ColorF.**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa [**la clase ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) para especificar un color predefinido (negro) al crear un [**objeto ID2D1SolidColorBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```



En el ejemplo siguiente se usa [**la clase ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) para especificar un color con valores rojo, verde, azul y alfa.


```C++
ID2D1SolidColorBrush *pGridBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
    &pGridBrush
    );
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y Actualización de plataforma para aplicaciones de escritorio Windows Vista \[ \| aplicaciones para UWP\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y Actualización de plataforma para aplicaciones de escritorio de Windows Server 2008 aplicaciones \[ \| para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>D2DBaseTypes.h (incluir D2d1.h)</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)
</dt> <dt>

[**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)
</dt> </dl>

 


---
title: D2D1_COLOR_F (D2DBaseTypes. h)
description: Describe los componentes rojo, verde, azul y alfa de un color. | D2D1_COLOR_F (D2DBaseTypes. h)
ms.assetid: 564d4f41-2da7-49ed-b85a-d1070d662b40
keywords:
- D2D1_COLOR_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f12c4c833d7f73946b2309673dff8f3dd11395
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678701"
---
# <a name="d2d1_color_f"></a>\_Color \_ F de D2D1

Describe los componentes rojo, verde, azul y alfa de un color.


```C++
typedef D2D_COLOR_F D2D1_COLOR_F;
```



## <a name="remarks"></a>Observaciones

**D2D1 \_ El COLOR \_ f** es una definición de tipo para el [**\_ color \_ f de D2D**](d2d-color-f.md), que es una definición de tipo para [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md). Para obtener información sobre los miembros proporcionados por **D2D1 \_ color \_ F**, consulte [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).

La clase [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) proporciona un conjunto de colores predefinidos y funciones auxiliares para definir colores. Para obtener más información, consulte la referencia de [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa la clase [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) para especificar un color predefinido (negro) al crear un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```



En el ejemplo siguiente se usa la clase [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) para especificar un color con los valores rojo, verde, azul y alfa.


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
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>D2DBaseTypes. h (incluye D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)
</dt> <dt>

[**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)
</dt> </dl>

 


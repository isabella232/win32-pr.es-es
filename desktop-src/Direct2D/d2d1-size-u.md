---
title: D2D1_SIZE_U (D2DBaseTypes.h)
description: Almacena un par de enteros ordenados, normalmente el ancho y el alto de un rectángulo.
ms.assetid: e28da5ee-7d68-4ec5-b477-c6ead0c725e6
keywords:
- D2D1_SIZE_U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b60627021e55e088a35692dffb8292d5c57fcf0932de255c19f4380ee29e8a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967105"
---
# <a name="d2d1_size_u"></a>D2D1 \_ SIZE \_ U

Almacena un par de enteros ordenados, normalmente el ancho y el alto de un rectángulo.


```C++
typedef D2D_SIZE_U D2D1_SIZE_U;
```



## <a name="remarks"></a>Comentarios

Al igual que los puntos, los tamaños son otro concepto de gráficos importante. En Direct2D, los tamaños se representan mediante las estructuras **D2D1 \_ SIZE \_ U** [**o D2D1 \_ SIZE \_ F.**](d2d1-size-f.md) Ambos contienen un par ordenado de números. La **estructura D2D1 \_ SIZE \_ U** contiene un par ordenado de valores **UINT32** y la estructura **D2D1 \_ SIZE \_ F** contiene un par ordenado de **valores FLOAT.**

La **estructura D2D1 \_ SIZE \_ U** proporciona una manera cómoda de almacenar un par ordenado de números, como el ancho y el alto de un rectángulo.

**D2D1 \_ SIZE \_ U** es un nuevo nombre para un tipo ya definido **D2D \_ SIZE \_ U**. Puede usar la función **D2D1::SizeU** para crear una estructura **D2D1 \_ SIZE \_ U.** Un uso común de esta estructura es especificar el tamaño de píxel de una estructura DE PROPIEDADES DE [**\_ DESTINO DE \_ HWND RENDER \_ \_ de D2D1.**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) A continuación se proporciona un ejemplo del uso de esta estructura.


```C++
    if (!m_pRenderTarget)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top
            );

        // Create a Direct2D render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y Platform Update for Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y Actualización de plataforma para aplicaciones de escritorio de Windows Server 2008 aplicaciones \[ \| para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2DBaseTypes.h (incluir D2d1.h)</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D2D \_ SIZE \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u)
</dt> <dt>

[**D2D1 \_ SIZE \_ F**](d2d1-size-f.md)
</dt> <dt>

[**D2D1::HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties)
</dt> </dl>

 


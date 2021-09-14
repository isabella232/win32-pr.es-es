---
title: D2D1_SIZE_U (D2DBaseTypes.h)
description: Almacena un par de enteros ordenados, normalmente el ancho y el alto de un rectángulo.
ms.assetid: e28da5ee-7d68-4ec5-b477-c6ead0c725e6
keywords:
- D2D1_SIZE_U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b5c317a98169957402dd125c054b8f6e0bc69
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163482"
---
# <a name="d2d1_size_u"></a>D2D1 \_ SIZE \_ U

Almacena un par de enteros ordenados, normalmente el ancho y el alto de un rectángulo.


```C++
typedef D2D_SIZE_U D2D1_SIZE_U;
```



## <a name="remarks"></a>Observaciones

Al igual que los puntos, los tamaños son otro concepto de gráficos importante. En Direct2D, los tamaños se representan mediante las estructuras **D2D1 \_ SIZE \_ U** [**o D2D1 \_ SIZE \_ F.**](d2d1-size-f.md) Ambos contienen un par ordenado de números. La **estructura D2D1 \_ SIZE \_ U** contiene un par ordenado de valores **UINT32** y la estructura **D2D1 \_ SIZE \_ F** contiene un par ordenado de **valores FLOAT.**

La **estructura D2D1 \_ SIZE \_ U** proporciona una manera cómoda de almacenar un par ordenado de números, como el ancho y el alto de un rectángulo.

**D2D1 \_ SIZE \_ U** es un nuevo nombre para un tipo ya definido **D2D \_ SIZE \_ U**. Puede usar la función **D2D1::SizeU** para crear una estructura **D2D1 \_ SIZE \_ U.** Un uso común de esta estructura es especificar el tamaño de píxel de una estructura DE PROPIEDADES DE [**\_ DESTINO DE \_ HWND RENDER \_ \_ de D2D1.**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) A continuación se proporciona un ejemplo del uso de esta estructura .


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
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y Actualización de plataforma para aplicaciones de escritorio Windows Vista \[ \| aplicaciones para UWP\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y Actualización de plataforma para aplicaciones de escritorio de Windows Server 2008 aplicaciones \[ \| para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>D2DBaseTypes.h (incluir D2d1.h)</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**D2D \_ SIZE \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u)
</dt> <dt>

[**D2D1 \_ SIZE \_ F**](d2d1-size-f.md)
</dt> <dt>

[**D2D1::HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties)
</dt> </dl>

 


---
title: Efecto de recorte
description: Use el efecto de recorte para generar una región especificada de una imagen.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- efecto de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e342bdef882fbff89d4c67c3accfbff7287a2ad9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164170"
---
# <a name="crop-effect"></a>Efecto de recorte

Use el efecto de recorte para generar una región especificada de una imagen.

El CLSID para este efecto es CLSID \_ D2D1Crop.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                     |
|------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg) |
| Después                                                      |
| ![la imagen después de la transformación.](images/8-crop.png)       |



 


```C++
ComPtr<ID2D1Effect> cropEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Crop, &cropEffect);

cropEffect->SetInput(0, bitmap);
cropEffect->SetValue(D2D1_CROP_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(cropEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propiedades de efecto




| Enumeración de nombre para mostrar e índice | Tipo y valor predeterminado | Descripción | 
|------------------------------------|------------------------|-------------|
| Rect<br /> | D2D1_VECTOR_4F<br /> | Región que se va a recortar especificada como vector con el formato (izquierda, parte superior, ancho, alto).<br /> | 
| D2D1_CROP_PROP_RECT<br /> | {-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX}<br /> | Las unidades están en DIP. <br /><blockquote><p>[!Note]</p><p>El rect se truncará si se superpone a los límites perimetrales de la imagen de entrada.<br /></p></blockquote><br /> | 
| D2D1_CROP_PROP_BORDER_MODE<br /> | D2D1_BORDER_MODE <br /> D2D1_BORDER_MODE_SOFT <br /> | <ul><li>D2D1_BORDER_MODE_SOFT: si el rectángulo de recorte se encuentra en coordenadas de píxeles fraccionados, el efecto aplica suavizado de contorno, lo que da como resultado un borde suave.</li><li>D2D1_BORDER_MODE_HARD: si el rectángulo de recorte se encuentra en coordenadas de píxel fraccionamiento, el efecto se fija, lo que da como resultado un borde duro.</li></ul> | 




 

## <a name="output-bitmap"></a>Mapa de bits de salida

La salida de este efecto es el tamaño de la propiedad Rect. La longitud y el ancho son calc

Se usan las ecuaciones aquí: <dl> Longitud de salida en Pixels=(Rect.Right-Rect.Left) \* (PPP/96 del usuario)  
Alto de salida en píxeles=(Rect.Bottom-Rect.Top) \* (PPP/96 del usuario)  
</dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio Windows aplicaciones de la \| Tienda\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio Windows aplicaciones de la \| Tienda\] |
| Encabezado                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


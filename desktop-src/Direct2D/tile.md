---
title: Efecto de mosaico
description: Use el efecto de mosaico para repetir la región especificada de la imagen.
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- efecto de icono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0df10143a727fb8ce6585264b65b6db46d75c731070f2ea46ff8e7dffd59dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430504"
---
# <a name="tile-effect"></a>Efecto de mosaico

Use el efecto de mosaico para repetir la región especificada de la imagen.

El CLSID para este efecto es CLSID \_ D2D1Tile.

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                     |
|------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg) |
| Después                                                      |
| ![la imagen después de la transformación.](images/9-tile.png)       |



 


```C++
ComPtr<ID2D1Effect> tileEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Tile, &tileEffect);

tileEffect->SetInput(0, bitmap);

tileEffect->SetValue(D2D1_TILE_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tileEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                | Tipo y valor predeterminado                                              | Descripción                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Rect<br/> D2D1 \_ TILE \_ PROP \_ RECT<br/> | D2D1 \_ VECTOR \_ 4F<br/> {0.0f, 0.0f, 100.0f, 100.0f}<br/> | Región de la imagen que se va a mosaico. Esta propiedad es una D2D1 \_ VECTOR \_ 4F definida como: (izquierda, superior, derecha, inferior). Las unidades están en DIP.<br/> |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

Este efecto genera un mapa de bits de tamaño lógico infinito.

Puede crear un icono de una imagen y generar un tamaño determinado sin ningún efecto adicional estableciendo el tamaño al llamar a [**ID2D1DeviceContext::D rawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Header                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


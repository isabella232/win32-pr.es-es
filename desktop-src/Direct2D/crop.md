---
title: Efecto de recorte
description: Use el efecto de recorte para generar una región específica de una imagen.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- efecto de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ceaf4cf8b5922fe05e151c1639269f3169b57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905224"
---
# <a name="crop-effect"></a>Efecto de recorte

Use el efecto de recorte para generar una región específica de una imagen.

El CLSID para este efecto es CLSID \_ D2D1Crop.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                     |
|------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg) |
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



## <a name="effect-properties"></a>Propiedades del efecto



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Enumeración de índice y nombre para mostrar</th>
<th>Tipo y valor predeterminado</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Rect<br/></td>
<td>D2D1_VECTOR_4F<br/></td>
<td>Región que se va a recortar como vector en el formato (izquierda, superior, ancho y alto).<br/></td>
</tr>
<tr class="even">
<td>D2D1_CROP_PROP_RECT<br/></td>
<td>{-FLT_MAX,-FLT_MAX, FLT_MAX, FLT_MAX}<br/></td>
<td>Las unidades están en DIP. <br/>
<blockquote>
<p>[!Note]</p>
<p>El rectángulo se truncará si se superpone a los límites de borde de la imagen de entrada.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>D2D1_CROP_PROP_BORDER_MODE<br/></td>
<td>D2D1_BORDER_MODE <br/> D2D1_BORDER_MODE_SOFT <br/></td>
<td><ul>
<li>D2D1_BORDER_MODE_SOFT: Si el rectángulo de recorte cae en coordenadas de píxeles fraccionarios, el efecto aplica el suavizado de contorno, lo que da como resultado un borde flexible.</li>
<li>D2D1_BORDER_MODE_HARD: Si el rectángulo de recorte cae en coordenadas de píxeles fraccionarios, el efecto se fija, lo que da como resultado un borde duro.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="output-bitmap"></a>Mapa de bits de salida

La salida de este efecto es el tamaño de la propiedad Rect. La longitud y el ancho son Calc

ulated usar las ecuaciones aquí: <dl> Longitud de salida en píxeles = (rect. Right-Rect. Left) \* (PPP del usuario/96)  
Alto de salida en píxeles = (rect. Bottom-Rect.Top) \* (PPP del usuario/96)  
</dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Servidor mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Encabezado                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


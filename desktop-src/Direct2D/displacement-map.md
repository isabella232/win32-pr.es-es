---
title: Efecto de mapa de desplazamiento
description: Use el efecto de mapa de desplazamiento para desplazar los píxeles de la imagen de entrada por los valores de intensidad de una segunda imagen de entrada.
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- efecto de mapa de desplazamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ad2deb0c584ccc9c55faebd60f803d66efa42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149929"
---
# <a name="displacement-map-effect"></a>Efecto de mapa de desplazamiento

Use el efecto de mapa de desplazamiento para desplazar los píxeles de la imagen de entrada por los valores de intensidad de una segunda imagen de entrada.

El CLSID para este efecto es CLSID \_ D2D1DisplacementMap.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Canales de color](#color-channels)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                           |
|------------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)       |
| Después                                                            |
| ![la imagen después de la transformación.](images/19-displacementmap.png) |



 


```C++
ComPtr<ID2D1Effect> displacementMapEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DisplacementMap, &displacementMapEffect);

displacementMapEffect->SetInput(0, bitmap);
displacementMapEffect->SetValue(D2D1_DISPLACEMENTMAP_PROP_SCALE, 100.0f);

// The second input of the displacement effect determines how the input image is transformed.
// For this example, we will use a turbulence effect as the second input to randomly distort the image.
ComPtr<ID2D1Effect> turbulenceEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Turbulence, &turbulenceEffect);
displacementMapEffect->SetInputEffect(1, turbulenceEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(displacementMapEffect.Get());
m_d2dContext->EndDraw();
```



Las ubicaciones de los píxeles de la salida se determinan mediante esta fórmula:

C ' (x, y) = C (x + Scale \* (XChannelSelector (mapa de bits de desplazamiento (x, y))-0.5), y + Scale \* (YChannelSelector (mapa de bits de desplazamiento (x, y))-0,5))

Donde:<dl> *C (x, y)* es el píxel de salida en (x, y).  
*C (x, y)* es el píxel de entrada en (x, y).  
El *mapa de bits de desplazamiento (x, y)* es la intensidad de píxeles de desplazamiento en las coordenadas especificadas.  
*XChannelSelector* la intensidad del canal RGBA seleccionado del mapa de bits de desplazamiento que coloca la imagen de entrada en la dirección X.  
*YChannelSelector* la intensidad del canal RGBA seleccionado del mapa de bits de desplazamiento que desplace la imagen de entrada en la dirección Y.  
</dl>

El efecto remuestrea la imagen de entrada según la propiedad de escala y la intensidad de la imagen de desplazamiento. Usa la interpolación bilineal si se muestrea desde los píxeles de la imagen de entrada.

Este efecto funciona en imágenes alfa directas y premultiplicadas. El formato alfa de salida es el mismo que el formato de entrada.

## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                                   | Tipo y valor predeterminado                                                   | Descripción                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Escala<br/> D2D1 \_ DISPLACEMENTMAP \_ prop \_ Scale<br/>                       | FLOAT<br/> 0,0F<br/>                                         | Multiplica la intensidad del canal seleccionado de la imagen de desplazamiento. Cuanto más alto establezca esta propiedad, más el efecto desplazará los píxeles<br/>                       |
| XChannelSelect<br/> D2D1 \_ DISPLACEMENTMAP \_ prop \_ X \_ canal \_ Select<br/> | \_Selector de canal de D2D1 \_<br/> \_ \_ Selector de canal \_ de D2D1 A<br/> | El efecto extrae la intensidad de este canal de color y la usa para desplazar espacialmente la imagen en la dirección X. Vea [canales de color](#color-channels) para obtener más información.<br/> |
| YChannelSelect<br/> D2D1 \_ DISPLACEMENTMAP \_ prop \_ Y \_ canal \_ Select<br/> | \_Selector de canal de D2D1 \_<br/> \_ \_ Selector de canal \_ de D2D1 A<br/> | El efecto extrae la intensidad de este canal de color y la usa para desplazar espacialmente la imagen en la dirección Y. Vea [canales de color](#color-channels) para obtener más información.<br/> |



 

## <a name="color-channels"></a>Canales de color



| Enumeración                | Descripción                                                      |
|----------------------------|------------------------------------------------------------------|
| Selector de canal de D2D1 \_ \_ \_ R | El efecto extrae la salida de intensidad del canal rojo.   |
| Selector de canal de D2D1 \_ \_ \_ G | El efecto extrae la salida de intensidad del canal verde. |
| Selector de canal de D2D1 \_ \_ \_ B | El efecto extrae la salida de intensidad del canal azul.  |
| \_ \_ Selector de canal \_ de D2D1 A | El efecto extrae la salida de intensidad del canal alfa. |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

Puede determinar el tamaño máximo del mapa de bits de salida con estas ecuaciones:

¿Mapa de bits de salida? Píxeles = (tamaño del mapa de bits de entrada? ( DIP) + escala \* (PPP de usuario/96)

Mapa de bits<sub>y</sub> píxeles de salida = (tamaño del mapa de bits de entrada<sub>y</sub>(DIP) + escala) \* (PPP del usuario/96)

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

 


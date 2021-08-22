---
title: Efecto de mapa de desplazamiento
description: Use el efecto mapa de desplazamiento para desplazar los píxeles de la imagen de entrada por los valores de intensidad de una segunda imagen de entrada.
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- efecto de mapa de desplazamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73888d8168e411bf0f8daee1f2e04801353ee8358d27ba4d5cc9b1f71630a762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833024"
---
# <a name="displacement-map-effect"></a>Efecto de mapa de desplazamiento

Use el efecto mapa de desplazamiento para desplazar los píxeles de la imagen de entrada por los valores de intensidad de una segunda imagen de entrada.

El CLSID para este efecto es CLSID \_ D2D1DisplacementMap.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Canales de color](#color-channels)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                           |
|------------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg)       |
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

C' (x,y)=C(x+ scale \* (XChannelSelector(Bitmap Bitmap (x,y))-0.5),y+ scale \* (YChannelSelector(Bitmap (x,y))-0.5))

Donde:<dl> *C (x, y)* es el píxel de salida en (x, y).  
*C (x, y)* es el píxel de entrada en (x, y).  
*Mapa de bits de desplazamiento (x, y)* es la intensidad de píxeles de desplazamiento en las coordenadas especificadas.  
*XChannelSelecto la* intensidad del canal RGBA seleccionado del mapa de bits de desplazamiento que desplaza la imagen de entrada en la dirección X.  
*YChannelSelecto la* intensidad del canal RGBA seleccionado del mapa de bits de desplazamiento que desplaza la imagen de entrada en la dirección Y.  
</dl>

El efecto vuelve a muestrear la imagen de entrada según la propiedad de escala y la intensidad de la imagen de desplazamiento. Usa la interpolación bilineal si el muestreo de entre píxeles de la imagen de entrada.

Este efecto funciona en imágenes alfa rectas y premultiplicadas. El formato alfa de salida es el mismo que el formato de entrada.

## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                                   | Tipo y valor predeterminado                                                   | Descripción                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Escala<br/> ESCALA DE PROP DE MAPA DE DESPLAZAMIENTO D2D1 \_ \_ \_<br/>                       | FLOAT<br/> 0,0f<br/>                                         | Multiplica la intensidad del canal seleccionado a partir de la imagen de desplazamiento. Cuanto mayor sea el valor de esta propiedad, más desplazará el efecto a los píxeles.<br/>                       |
| XChannelSelect<br/> SELECCIÓN DE CANAL X DE PROP X DE LA PROPIEDAD DE MAPA DE DESPLAZAMIENTO \_ \_ \_ \_ D2D1 \_<br/> | SELECTOR DE CANALES D2D1 \_ \_<br/> SELECTOR DE CANAL D2D1 \_ \_ \_ A<br/> | El efecto extrae la intensidad de este canal de color y la usa para desplazar espacialmente la imagen en la dirección X. Consulte [Canales de color](#color-channels) para obtener más información.<br/> |
| YChannelSelect<br/> SELECCIÓN DEL CANAL DE \_ PROP Y DEL MAPA DE DESPLAZAMIENTO \_ \_ \_ D2D1 \_<br/> | SELECTOR DE CANALES D2D1 \_ \_<br/> SELECTOR DE CANAL D2D1 \_ \_ \_ A<br/> | El efecto extrae la intensidad de este canal de color y la usa para desplazar espacialmente la imagen en la dirección Y. Consulte [Canales de color](#color-channels) para obtener más información.<br/> |



 

## <a name="color-channels"></a>Canales de color



| Enumeración                | Descripción                                                      |
|----------------------------|------------------------------------------------------------------|
| SELECTOR DE CANALES D2D1 \_ \_ \_ R | El efecto extrae la salida de intensidad del canal rojo.   |
| SELECTOR DE CANAL D2D1 \_ \_ \_ G | El efecto extrae la salida de intensidad del canal verde. |
| SELECTOR DE CANALES D2D1 \_ \_ \_ B | El efecto extrae la salida de intensidad del canal azul.  |
| SELECTOR DE CANAL D2D1 \_ \_ \_ A | El efecto extrae la salida de intensidad del canal alfa. |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

Puede determinar el tamaño máximo del mapa de bits de salida con estas ecuaciones:

¿Mapa de bits de salida? Pixels=(Input Bitmap Size?( DIP)+Escala) \* (PPP de usuario/96)

Output Bitmap<sub>y</sub> Pixels=(Input Bitmap Size y (DIP) + Scale) (Tamaño de mapa de bits<sub>de entrada y</sub>(DIP) + Escala) \* (PPP/96 del usuario)

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

 


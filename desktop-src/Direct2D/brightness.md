---
title: Efecto de brillo
description: Use el efecto de brillo para controlar el brillo de la imagen.
ms.assetid: 5088D4D4-DFC8-45D3-B1C3-D576742D931C
keywords:
- efecto de brillo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88b67615948cbea74333605e900de194c0eeeb3d747d83af5eae8a750e6f135
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119215395"
---
# <a name="brightness-effect"></a>Efecto de brillo

Use el efecto de brillo para controlar el brillo de la imagen.

El CLSID para este efecto es CLSID \_ D2D1Brightness.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                      |
|-------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg)  |
| Después                                                       |
| ![la imagen después de la transformación.](images/34-brightness.png) |



 


```C++
ComPtr<ID2D1Effect> brightnessEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Brightness, &brightnessEffect);

brightnessEffect->SetValue(D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1::Vector2F(0.0f, 0.2f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(brightnessEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propiedades de efecto



| Nombre para mostrar de la propiedad                                                 | Tipo y valor predeterminado                              | Descripción                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WhitePoint<br/> PUNTO BLANCO DE PROP DE BRILLO D2D1 \_ \_ \_ \_<br/> | D2D1 \_ VECTOR \_ 2F<br/> {1.0f, 1.0f}<br/> | Parte superior de la curva de transferencia de brillo. El punto blanco ajusta la apariencia de las partes más brillantes de la imagen. Esta propiedad es para el valor x y el valor y, en ese orden. Cada uno de los valores de esta propiedad está entre 0 y 1, ambos inclusive. |
| BlackPoint<br/> PUNTO NEGRO DE PROP DE BRILLO D2D1 \_ \_ \_ \_<br/> | D2D1 \_ VECTOR \_ 2F<br/> {0.0f, 0.0f}<br/> | Parte inferior de la curva de transferencia de brillo. El punto negro ajusta la apariencia de las partes más oscuras de la imagen. Esta propiedad es para el valor x y el valor y, en ese orden. Cada uno de los valores de esta propiedad está entre 0 y 1, ambos inclusive.   |



 

Este efecto usa los puntos blanco y negro especificados para generar una función de transferencia que se usa para ajustar el mapa de bits. En la siguiente ecuación se describe la función de transferencia. Las intensidades de entrada se definen entre 0 y 1.

![algoritmo de brillo](images/brightness-formula1.png)

El algoritmo de efecto implementa una ecuación que crea la función de transferencia. Usamos esta función para ajustar los píxeles de la imagen. Los valores x e y del punto negro y el punto blanco son las coordenadas de dos dimensiones que están conectadas para formar la transformación. Cada parte de la ecuación de salida final:

1.  Convierte los datos de imagen del espacio lineal al espacio no lineal mediante esta ecuación:![función auxiliar 1](images/brightness-formula2.png)

2.  Ajusta la imagen según estos valores:
    -   *input es* los valores de intensidad de píxeles de la imagen de entrada de 0 a 1.

    -   *Pt. blanco (x, y)* la ubicación de la curva de transformación para intensidades de píxeles más brillantes.

    -   *Pt. negro (x, y)* es la ubicación de la curva de transformación para las intensidades de píxeles de dimmer.

3.  Convierte los datos de la imagen en un espacio lineal mediante esta ecuación: ![función auxiliar 2](images/brightness-formula3.png)

La ecuación de salida final y las partes del componente se muestran aquí.

![los cálculos completos para el ajuste de brillo](images/brightness-formula4.png)

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del mapa de bits de salida es el mismo que el tamaño del mapa de bits de entrada.

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

 


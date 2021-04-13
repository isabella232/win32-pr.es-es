---
title: Efecto de sombra
description: Use el efecto de sombra para generar una sombra a partir del canal alfa de una imagen.
ms.assetid: 53525584-10CF-46C2-9400-C4FB225D4693
keywords:
- efecto de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42fd8755078dd79f2b01b623b1839785beb3c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359680"
---
# <a name="shadow-effect"></a>Efecto de sombra

Use el efecto de sombra para generar una sombra a partir del canal alfa de una imagen. La sombra es más opaca para los valores alfa más altos y más transparente para los valores alfa más bajos. Puede establecer la cantidad de desenfoque y el color de la sombra.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Modos de optimización](#optimization-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

El CLSID para este efecto es CLSID \_ D2D1Shadow.

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestra la salida del efecto de sombra que se traslada hacia abajo y hacia la derecha con la imagen de origen compuesta en la ubicación original. El efecto de sombra solo produce la sombra.



| Antes                                                  |
|---------------------------------------------------------|
| ![imagen anterior al efecto.](images/8-crop.png)      |
| Después                                                   |
| ![la imagen después de la transformación.](images/25-shadow.png) |



 


```C++
ComPtr<ID2D1Effect> shadowEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect);

shadowEffect->SetInput(0, bitmap);

// Shadow is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, affineTransformEffect.Get());
compositeEffect->SetInput(2, bitmap);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BlurStandardDeviation<br/> \_ \_ \_ Desviación estándar de desenfoque de \_ la instantánea D2D1 \_<br/> | Cantidad de desenfoque que se va a aplicar al canal alfa de la imagen. Puede calcular el radio de desenfoque del kernel multiplicando la desviación estándar por 3. Las unidades de la desviación estándar y el radio de desenfoque son DIP.<br/> Esta propiedad es igual que la propiedad [desenfoque gausiano](gaussian-blur.md) desviación estándar. <br/> El tipo es FLOAT.<br/> El valor predeterminado es 3.0 f.<br/> |
| Color<br/> COLOR de la instantánea de D2D1 \_ \_ \_<br/>                                     | Color de la sombra paralela. Esta propiedad es un D2D1 \_ Vector \_ 4F definido como: (R, G, B, a). Debe especificar este color en alfa recto.<br/> El tipo es D2D1 \_ Vector \_ 4F.<br/> El valor predeterminado es {0.0 f, 0.0 f, 0.0 f, 1.0 f.<br/>                                                                                                                                                                     |
| Optimization<br/> Optimización de D2D1 \_ Shadow \_ prop \_<br/>                       | Nivel de optimización del rendimiento.<br/> El tipo es D2D1 \_ Shadow \_ Optimization.<br/> El valor predeterminado es D2D1 \_ Shadow \_ Optimization \_ .<br/>                                                                                                                                                                                                                                                   |



 

## <a name="optimization-modes"></a>Modos de optimización



| Nombre                                          | Descripción                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Velocidad de optimización de D2D1 \_ DIRECTIONALBLUR \_ \_    | Aplica las optimizaciones internas, como el escalado previo en radios relativamente pequeños. Utiliza el filtrado lineal.                                  |
| Optimización de D2D1 \_ DIRECTIONALBLUR \_ \_ equilibrada | Usa los mismos umbrales de optimización que el modo de velocidad, pero utiliza el filtrado trilineal.                                                    |
| Calidad de optimización de D2D1 \_ DIRECTIONALBLUR \_ \_  | Solo usa optimizaciones internas con radios de desenfoque grandes, donde es menos probable que las aproximaciones sean visibles. Utiliza el filtrado trilineal. |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del mapa de bits de salida es el tamaño de la salida de desenfoque. La cantidad de crecimiento del mapa de bits de salida en relación con el mapa de bits original se puede calcular mediante la siguiente ecuación:

Crecimiento del mapa de bits de salida (X e y) = BlurStandardDeviation (píxeles independientes del dispositivo (DIP)) \* 6 \* (PPP del usuario)/96

El resultado aumenta igualmente en todas las direcciones, por lo que, por ejemplo, si el tamaño aumenta en 10 píxeles en cada dirección, la esquina superior izquierda del mapa de bits se encuentra en (-5,-5) y la parte inferior derecha estará en (105, 105), tal y como se muestra en el diagrama aquí.

![diagrama de crecimiento del tamaño de salida de efecto de sombra.](images/drop-shadow-output-growth.png)

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

 


---
title: Efecto de desenfoque gaussiano
description: Use el efecto de desenfoque gaussiano para crear un desenfoque basado en la función gaussiana en toda la imagen de entrada.
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- Desenfoque gaussiano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbe8b309a498315e389be45d382eca3ee1b98ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163265"
---
# <a name="gaussian-blur-effect"></a>Efecto de desenfoque gaussiano

Use el efecto de desenfoque gaussiano para crear un desenfoque basado en la función gaussiana en toda la imagen de entrada.

Puede usar este efecto para crear sombras y sombras paralelas y usar [el](composite.md) efecto compuesto para aplicar el resultado a la imagen original. Es útil en el procesamiento de fotos para filtros como resaltados y sombras. Puede usar la salida de este efecto para la entrada [](diffuse-lighting.md) en efectos de iluminación, como los efectos De iluminación [especular](specular-lighting.md) o Iluminación difusa, porque el canal alfa también está desenfocado y los efectos de iluminación usan el canal alfa para determinar la geometría de la superficie como un mapa de altura.

Este efecto lo usa el efecto de [sombra](drop-shadow.md) integrado.

El CLSID para este efecto es CLSID \_ D2D1GaussianBlur.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Modos de optimización](#optimization-modes)
-   [Modos de borde](#border-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                       |
|--------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg)   |
| Después                                                        |
| ![la imagen después de la transformación.](images/1-gaussianblur.png) |



 


```C++
ComPtr<ID2D1Effect> gaussianBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect);

gaussianBlurEffect->SetInput(0, bitmap);
gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 3.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gaussianBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                                    | Descripción                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation<br/> D2D1 \_ GAUSSIANBLUR \_ PROP \_ STANDARD \_ DEVIATION<br/> | Cantidad de desenfoque que se va a aplicar a la imagen. Puede calcular el radio de desenfoque del kernel multiplicando la desviación estándar por 3. Las unidades de la desviación estándar y el radio de desenfoque son DIP. Un valor de cero DIP deshabilita este efecto por completo. El tipo es FLOAT.<br/> El valor predeterminado es 3,0f.<br/> |
| Optimization<br/> OPTIMIZACIÓN DE PROPIEDADES DE D2D1 \_ GAUSSIANBLUR \_ \_<br/>             | Modo de optimización. Consulte [Modos de optimización](#optimization-modes) para obtener más información. El tipo es D2D1 \_ GAUSSIANBLUR \_ OPTIMIZATION.<br/> El valor predeterminado es D2D1 \_ GAUSSIANBLUR \_ OPTIMIZATION \_ BALANCED.<br/>                                                                                                            |
| BorderMode<br/> D2D1 \_ MODO DE BORDE DE PROP DE GAUSSIANBLUR \_ \_ \_<br/>               | Modo que se usa para calcular el borde de la imagen, de forma flexible o dura. Consulte [Modos de borde](#border-modes) para obtener más información. <br/> El tipo es D2D1 \_ GAUSSIANBLUR \_ BORDER \_ MODE.<br/> El valor predeterminado es D2D1 \_ BORDER \_ MODE \_ SOFT.<br/>                                                                                   |



 

## <a name="optimization-modes"></a>Modos de optimización



| Nombre                                          | Descripción                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| VELOCIDAD DE OPTIMIZACIÓN \_ DIRECCIONAL DE D2D1BLUR \_ \_    | Aplica optimizaciones internas, como el escalado previo en radios relativamente pequeños. Usa el filtrado lineal.                                  |
| D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION \_ BALANCED | Usa los mismos umbrales de optimización que el modo de velocidad, pero usa el filtrado trilineal.                                                    |
| D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION \_ QUALITY  | Solo usa optimizaciones internas con radii de desenfoque grandes, donde es menos probable que las aproximaciones sean visibles. Usa el filtrado trilineal. |



 

## <a name="border-modes"></a>Modos de borde



| Nombre                     | Descripción                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODO DE BORDE D2D1 \_ \_ \_ SOFT | El efecto aplica un panel a la imagen con píxeles de color negro transparente a medida que aplica el kernel de desenfoque, lo que da lugar a un borde suave. <br/>                                                                                             |
| D2D1 \_ BORDER \_ MODE \_ HARD | El efecto fija la salida al tamaño de la imagen de entrada. Cuando el efecto aplica el kernel de desenfoque, extiende la imagen de entrada con una transformación de borde de tipo reflejo para muestras fuera de los límites de entrada.<br/> |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

La salida de este efecto puede ser mayor que el mapa de bits de entrada en función del radio de desenfoque y el modo de borde. Si el modo de borde se establece en D2D1 BORDER MODE SOFT, el tamaño del mapa de bits de salida aumenta por el tamaño del kernel de desenfoque, representado \_ \_ en \_ píxeles. Esta tabla proporciona una ecuación que puede usar para calcular el mapa de bits de salida.

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

Por lo tanto, si el tamaño de la imagen aumenta en 10 píxeles en cada dirección, la esquina superior izquierda de la imagen se ubicará en (-5, -5), mientras que la parte inferior derecha estará en (105, 105).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Encabezado                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


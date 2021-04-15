---
title: Efecto Desenfoque gaussiano
description: Use el efecto Desenfoque gaussiano para crear un desenfoque basado en la función gaussiano en toda la imagen de entrada.
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- Desenfoque gaussiano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbe8b309a498315e389be45d382eca3ee1b98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104560581"
---
# <a name="gaussian-blur-effect"></a>Efecto Desenfoque gaussiano

Use el efecto Desenfoque gaussiano para crear un desenfoque basado en la función gaussiano en toda la imagen de entrada.

Puede usar este efecto para crear iluminaciones y sombras paralelas y usar el efecto [compuesto](composite.md) para aplicar el resultado a la imagen original. Resulta útil en el procesamiento fotográfico para filtros como resaltados y sombras. Puede usar la salida de este efecto para la entrada en efectos de iluminación, como la [iluminación especular](specular-lighting.md) o los efectos de [luz difusa](diffuse-lighting.md) , ya que el canal alfa está borroso, y los efectos de iluminación usan el canal alfa para determinar la geometría de la superficie como un mapa de alto.

Este efecto lo usa el efecto de [sombra](drop-shadow.md) integrado.

El CLSID para este efecto es CLSID \_ D2D1GaussianBlur.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Modos de optimización](#optimization-modes)
-   [Modos de borde](#border-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                       |
|--------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)   |
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



## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                                    | Descripción                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation<br/> \_ \_ \_ Desviación estándar de la D2D1 GAUSSIANBLUR \_<br/> | Cantidad de desenfoque que se va a aplicar a la imagen. Puede calcular el radio de desenfoque del kernel multiplicando la desviación estándar por 3. Las unidades de la desviación estándar y el radio de desenfoque son DIP. Un valor de cero DIP deshabilita este efecto por completo. El tipo es FLOAT.<br/> El valor predeterminado es 3.0 f.<br/> |
| Optimization<br/> Optimización de D2D1 \_ GAUSSIANBLUR \_ \_<br/>             | Modo de optimización. Vea [modos de optimización](#optimization-modes) para obtener más información. El tipo es D2D1 \_ GAUSSIANBLUR \_ Optimization.<br/> El valor predeterminado es D2D1 \_ GAUSSIANBLUR \_ optimizado de optimización \_ .<br/>                                                                                                            |
| BorderMode<br/> D2D1 \_ GAUSSIANBLUR \_ \_ modo de borde \_ de la Prop<br/>               | El modo que se usa para calcular el borde de la imagen, es decir, es flexible o difícil. Vea [modos de borde](#border-modes) para obtener más información. <br/> El tipo es D2D1 \_ GAUSSIANBLUR \_ Border \_ mode.<br/> El valor predeterminado es D2D1 \_ Border \_ Mode \_ .<br/>                                                                                   |



 

## <a name="optimization-modes"></a>Modos de optimización



| Nombre                                          | Descripción                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Velocidad de optimización de D2D1 \_ DIRECTIONALBLUR \_ \_    | Aplica las optimizaciones internas, como el escalado previo en radios relativamente pequeños. Utiliza el filtrado lineal.                                  |
| Optimización de D2D1 \_ DIRECTIONALBLUR \_ \_ equilibrada | Usa los mismos umbrales de optimización que el modo de velocidad, pero utiliza el filtrado trilineal.                                                    |
| Calidad de optimización de D2D1 \_ DIRECTIONALBLUR \_ \_  | Solo usa optimizaciones internas con radios de desenfoque grandes, donde es menos probable que las aproximaciones sean visibles. Utiliza el filtrado trilineal. |



 

## <a name="border-modes"></a>Modos de borde



| Nombre                     | Descripción                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ modo de borde \_ \_ flexible | El efecto rellena la imagen con píxeles negros transparentes cuando aplica el kernel de desenfoque, lo que da lugar a un borde flexible. <br/>                                                                                             |
| D2D1 \_ del \_ modo de borde \_ | El efecto fija la salida al tamaño de la imagen de entrada. Cuando el efecto aplica el kernel de desenfoque, extiende la imagen de entrada con una transformación de borde de tipo de reflejo para las muestras fuera de los límites de entrada.<br/> |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

La salida de este efecto puede ser mayor que el mapa de bits de entrada basado en el radio de desenfoque y el modo de borde. Si el modo de borde se establece en el \_ modo de borde D2D1 \_ \_ , aumenta el tamaño del mapa de bits de salida en función del tamaño del kernel de desenfoque, representado en píxeles. En esta tabla se proporciona una ecuación que se puede usar para calcular el mapa de bits de salida.

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

Por lo tanto, si el tamaño de la imagen aumenta en 10 píxeles en cada dirección, la esquina superior izquierda de la imagen se ubicará en (-5,-5), mientras que la parte inferior derecha estará en (105, 105).

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

 


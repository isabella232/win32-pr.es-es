---
title: Efecto de iluminación difusa distante
description: Use el efecto de iluminación difusa lejana para crear una imagen que parece ser una superficie no reflectante con donde la fuente de luz parece estar procedente de una distancia larga (como el sol o las luces sobrecargadas) y la luz se dispersa en todas las direcciones.
ms.assetid: 981FD58B-0565-4D0E-957C-3ED81BA8A6EB
keywords:
- efecto de iluminación difusa lejana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f1860f196685c3d7dc0dcc30ae575cee70bc1eb0fcc29e8da7709c1174ee411
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260414"
---
# <a name="distant-diffuse-lighting-effect"></a>Efecto de iluminación difusa distante

Use el efecto de iluminación difusa lejana para crear una imagen que parece ser una superficie no reflectante con donde la fuente de luz parece estar procedente de una distancia larga (como el sol o las luces sobrecargadas) y la luz se dispersa en todas las direcciones. Este efecto usa el canal alfa como mapa de altura y enciende la imagen con una fuente de luz lejana.

El color del mapa de bits de salida es el resultado del color claro, la posición de la luz y la geometría de la superficie de la imagen. La salida del canal alfa para cada píxel con iluminación difusa siempre es 1,0.

El CLSID para este efecto es CLSID \_ D2D1DistantDiffuse.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Modos de escalado](#scale-modes)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de iluminación difusa lejana.

![Ejemplo de efecto captura de pantalla las imágenes de entrada y salida del efecto de iluminación difusa lejana.](images/distant-diffuse-example.png)

## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Acimut<br/> D2D1 \_ DISTANTDIFFUSE \_ PROP \_ AZIMUTH<br/>                       | Ángulo de dirección de la fuente de luz en el plano XY con respecto al eje X en la dirección del reloj del contador. Las unidades están en grados y deben estar entre 0 y 360 grados.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 0,0f.<br/>                                                                                                                                                                                                                                                            |
| Elevation<br/> ELEVACIÓN DE PROP DE D2D1 \_ DISTANTDIFFUSE \_ \_<br/>                   | Ángulo de dirección de la fuente de luz en el plano YZ con respecto al eje Y en la dirección del reloj del contador. Las unidades están en grados y deben estar entre 0 y 360 grados. <br/> El tipo es FLOAT.<br/> El valor predeterminado es 0,0f.<br/>                                                                                                                                                                                                                                                           |
| DiffuseConstant<br/> D2D1 \_ DISTANTDIFFUSE \_ PROP \_ DIFUSO \_ CONSTANTE<br/>     | Proporción de reflexión difusa con la cantidad de luz entrante. Esta propiedad debe estar entre 0 y 10 000 y no tiene unidad. <br/> El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                                                      |
| SurfaceScale<br/> D2D1 \_ DISTANTDIFFUSE \_ PROP \_ SURFACE \_ SCALE<br/>           | Factor de escala en la dirección Z. La escala de superficie no tiene unidad y debe estar entre 0 y 10 000.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                                                                           |
| Color<br/> COLOR DE PROP D2D1 \_ DISTANTDIFFUSE \_ \_<br/>                           | Color de la luz entrante. Esta propiedad se expone como D2D1 \_ VECTOR \_ 3F (R, G,<sub></sub>B) y<sub></sub>se usa para calcular L<sub>R</sub>, L G , L B . <br/> El tipo es D2D1 \_ VECTOR \_ 3F.<br/> El valor predeterminado es {1.0f, 1.0f, 1.0f}.<br/>                                                                                                                                                                                                                                                         |
| KernelUnitLength<br/> LONGITUD DE UNIDAD DE KERNEL DE PROP DE D2D1 \_ DISTANTDIFFUSE \_ \_ \_ \_<br/> | Tamaño de un elemento en el kernel de Sobel que se usa para generar la superficie normal en la dirección X e Y. Esta propiedad se asigna a los valores dx y dy en el degradado Sobel. Esta propiedad es D2D1 VECTOR 2F (longitud de unidad de kernel X, longitud de unidad de kernel Y) y se define en (píxeles independientes del dispositivo \_ \_ (DIP)/unidad de kernel). El efecto usa la interpolación bilineal para escalar el mapa de bits para que coincida con el tamaño de los elementos del kernel. <br/> El tipo es D2D1 \_ VECTOR \_ 2F.<br/> El valor predeterminado es {1.0f, 1.0f}.<br/> |
| Scalemode<br/> D2D1 \_ DISTANTDIFFUSE \_ PROP \_ SCALE \_ MODE<br/>                 | Modo de interpolación que usa el efecto para escalar la imagen a la longitud de unidad de kernel correspondiente. Hay seis modos de escala que varían en calidad y velocidad.<br/> El tipo es D2D1 \_ DISTANTDIFFUSE \_ SCALE \_ MODE.<br/> El valor predeterminado es D2D1 \_ DISTANTDIFFUSE \_ SCALE \_ MODE \_ LINEAR.<br/>                                                                                                                                                                                                                 |



 

## <a name="scale-modes"></a>Modos de escalado



| Enumeración                                              | Descripción                                                                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ DISTANTDIFFUSE \_ SCALE \_ MODE \_ NEAREST \_ NEIGHBOR     | Muestrea el punto único más cercano y lo usa. Este modo usa menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| D2D1 \_ DISTANTDIFFUSE \_ SCALE \_ MODE \_ LINEAR                | Usa una muestra de cuatro puntos e interpolación lineal. Este modo genera una imagen de mayor calidad que el vecino más próximo.                                                                                   |
| D2D1 \_ DISTANTDIFFUSE \_ SCALE \_ MODE \_ CUBIC                 | Usa un kernel cúbica de 16 muestras para la interpolación. Este modo usa el mayor tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ DISTANTDIFFUSE \_ SCALE \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 muestras lineales dentro de un solo píxel para un suavizado de alias de borde bueno. Este modo es bueno para reducir verticalmente en pequeñas cantidades en imágenes con pocos píxeles.                                              |
| D2D1 \_ DISTANTDIFFUSE \_ SCALE \_ MODE \_ ANISOTROPIC           | Usa el filtrado anisotropico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ DISTANTDIFFUSE \_ SCALE \_ MODE \_ HIGH \_ QUALITY \_ CUBIC  | Usa un kernel cúbica de alta calidad de tamaño variable para realizar una escala previa a la baja de la imagen si la escala hacia abajo está implicada en la matriz de transformación. A continuación, usa el modo de interpolación cúbica para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el valor predeterminado del efecto es D2D1 \_ DISTANTDIFFUSE \_ SCALE \_ MODE \_ LINEAR.

 
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

 


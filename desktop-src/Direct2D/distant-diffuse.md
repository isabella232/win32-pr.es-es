---
title: Efecto de iluminación difusa distante
description: Use el efecto de luz distanl-difusa para crear una imagen que parezca una superficie no reflectante con la que parezca que la fuente de luz proviene de una larga distancia (como el sol o las luces de sobrecarga) y que la luz está dispersa en todas las direcciones.
ms.assetid: 981FD58B-0565-4D0E-957C-3ED81BA8A6EB
keywords:
- efecto de luz difusa distanl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30d8e7f918c0b1a55e25c18c83e3eff51b75233
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078848"
---
# <a name="distant-diffuse-lighting-effect"></a>Efecto de iluminación difusa distante

Use el efecto de luz distanl-difusa para crear una imagen que parezca una superficie no reflectante con la que parezca que la fuente de luz proviene de una larga distancia (como el sol o las luces de sobrecarga) y que la luz está dispersa en todas las direcciones. Este efecto usa el canal alfa como mapa de alto y enciende la imagen con una fuente de luz distanl.

El color del mapa de bits de salida es el resultado del color claro, la posición de la luz y la geometría de la superficie de la imagen. La salida del canal alfa para cada píxel con iluminación difusa siempre es 1,0.

El CLSID para este efecto es CLSID \_ D2D1DistantDiffuse.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Modos de escala](#scale-modes)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de iluminación de difusión distanl.

![ejemplo de efecto captura de pantalla de las imágenes de entrada y salida del efecto de iluminación difusa distanl.](images/distant-diffuse-example.png)

## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azimuth<br/> D2D1 \_ DISTANTDIFFUSE \_ prop \_ Azimuth<br/>                       | Ángulo de dirección de la fuente de luz en el plano XY en relación con el eje X en la dirección del reloj de contador. Las unidades están en grados y deben estar entre 0 y 360 grados.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 0.0 f.<br/>                                                                                                                                                                                                                                                            |
| Elevation<br/> Elevación de D2D1 \_ DISTANTDIFFUSE \_ \_<br/>                   | El ángulo de dirección de la fuente de luz en el plano YZ con respecto al eje Y en la dirección del reloj de contador. Las unidades están en grados y deben estar entre 0 y 360 grados. <br/> El tipo es FLOAT.<br/> El valor predeterminado es 0.0 f.<br/>                                                                                                                                                                                                                                                           |
| DiffuseConstant<br/> D2D1 \_ DISTANTDIFFUSE \_ prop ( \_ \_ constante difusa)<br/>     | La proporción de reflexión difusa con respecto a la cantidad de luz entrante. Esta propiedad debe estar comprendida entre 0 y 10.000 y no es una unidad. <br/> El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                      |
| SurfaceScale<br/> \_Escala de \_ superficie de prop \_ \_ de D2D1 DISTANTDIFFUSE<br/>           | Factor de escala en la dirección Z. La escala de superficie es sin unidades y debe estar comprendida entre 0 y 10.000.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                           |
| Color<br/> D2D1 \_ DISTANTDIFFUSE \_ prop \_ color<br/>                           | Color de la luz entrante. Esta propiedad se expone como vector D2D1 \_ \_ 3F (R, G, B) y se usa para calcular l<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. <br/> El tipo es D2D1 \_ Vector \_ 3F.<br/> El valor predeterminado es {1.0 f, 1.0 f, 1.0 f.<br/>                                                                                                                                                                                                                                                         |
| KernelUnitLength<br/> Longitud de la \_ unidad de kernel de prop D2D1 DISTANTDIFFUSE \_ \_ \_ \_<br/> | Tamaño de un elemento en el kernel de Sobel que se usa para generar la superficie normal en la dirección X e y. Esta propiedad se asigna a los valores DX y DY en el degradado Sobel. Esta propiedad es un \_ Vector D2D1 \_ 2F (longitud de unidad de kernel X, longitud de unidad de kernel y) y se define en (unidad/kernel de píxeles independientes del dispositivo (DIP)). El efecto utiliza la interpolación bilineal para escalar el mapa de bits para que coincida con el tamaño de los elementos de kernel. <br/> El tipo es D2D1 \_ Vector \_ 2F.<br/> El valor predeterminado es {1.0 f, 1.0 f}.<br/> |
| ModoDeLaEscala<br/> \_Modo de \_ \_ escalado de propiedades \_ de D2D1 DISTANTDIFFUSE<br/>                 | El modo de interpolación que el efecto usa para escalar la imagen a la longitud de unidad de kernel correspondiente. Hay seis modos de escala que abarcan la calidad y la velocidad.<br/> El tipo es D2D1 \_ DISTANTDIFFUSE \_ Scale \_ mode.<br/> El valor predeterminado es D2D1 \_ DISTANTDIFFUSE en \_ modo de escala \_ \_ lineal.<br/>                                                                                                                                                                                                                 |



 

## <a name="scale-modes"></a>Modos de escala



| Enumeración                                              | Descripción                                                                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ el \_ modo de escalado DISTANTDIFFUSE \_ \_ más cercano \_     | Muestrea el punto único más cercano y lo usa. Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| \_Modo de \_ escala \_ \_ lineal de D2D1 DISTANTDIFFUSE                | Utiliza un ejemplo de cuatro puntos y una interpolación lineal. Este modo genera una imagen de mayor calidad que el vecino más cercano.                                                                                   |
| D2D1 \_ \_ modo de escala DISTANTDIFFUSE \_ \_ cúbico                 | Usa un kernel cúbico de ejemplo 16 para la interpolación. Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ DISTANTDIFFUSE en \_ modo de escala lineal de \_ \_ varios \_ ejemplos \_ | Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado. Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.                                              |
| \_Modo de \_ escala D2D1 DISTANTDIFFUSE \_ \_           | Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ DISTANTDIFFUSE, \_ modo de escalado de \_ \_ alta \_ calidad \_ cúbico  | Usa un kernel cúbico de alta calidad de tamaño variable para realizar una downscale previa de la imagen si downscaling está implicado en la matriz de transformación. A continuación, usa el modo de interpolación cúbico para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el efecto tiene como valor predeterminado D2D1 \_ DISTANTDIFFUSE \_ modo de escala \_ \_ lineal.

 
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

 


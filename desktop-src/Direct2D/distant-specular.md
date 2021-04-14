---
title: Efecto de iluminación especular distante
description: Use el efecto de luz especular distante para crear una imagen que parezca una superficie reflectante en la que parezca que la fuente de luz proviene de una larga distancia (como el sol o las luces de sobrecarga).
ms.assetid: 74D71A2D-8D1D-4FDE-898A-2D2F5A8D5D31
keywords:
- iluminación especular Distant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fa21553e36839f854b4567b2aa2a3805406380
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422542"
---
# <a name="distant-specular-lighting-effect"></a>Efecto de iluminación especular distante

Use el efecto de luz especular distante para crear una imagen que parezca una superficie reflectante en la que parezca que la fuente de luz proviene de una larga distancia (como el sol o las luces de sobrecarga). Este efecto usa el canal alfa como mapa de alto y enciende la imagen con una fuente de luz distanl.

El color del mapa de bits de salida es el resultado del color claro, la posición de la luz y la geometría de la superficie. La salida del canal alfa para cada píxel con iluminación especular es el máximo de las salidas de canal rojo, verde y azul para ese píxel.

El CLSID para este efecto es CLSID \_ D2D1DistantSpecular.

-   [Imagen de ejemplo](#example-image)
-   [Fuente de luz distanl](#distant-light-source)
-   [Propiedades del efecto](#effect-properties)
-   [Modos de escala](#scale-modes)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de iluminación especular distante.

![captura de pantalla de ejemplo de efecto que muestra las imágenes de entrada y salida del efecto de luz especular distanl. ](images/distant-spec-example.png)

El mapa de bits de salida final se puede calcular mediante las siguientes ecuaciones.

![cálculo de mapa de bits de salida](images/distant-spec-formula1.png)

where <dl> k? = constante de iluminación especular.  
![símbolo normal de superficie. ](images/point-spec-mathchar-n.png) = Vector de unidad normal de superficie.  
![símbolo de vector medio. ](images/point-spec-mathchar-h.png) = Vector de unidad "medio" entre el vector de unidad ocular y el vector de unidad de luz.  
C<sub>r</sub>, c<sub>g</sub>, c<sub>b</sub> = el color claro en los componentes RGB.  
</dl>

## <a name="distant-light-source"></a>Fuente de luz distanl

La imagen siguiente muestra un ejemplo de la dirección de la luz desde una fuente de luz distanl.

![fuente de luz distanl](images/distant-spec-lightsource.png)

El efecto usa los parámetros Azimuth y elevation para calcular el vector de luz ![Vector l.](images/distant-spec-mathchar-l.png) usar las ecuaciones siguientes:

![cálculo del vector claro](images/distant-spec-formula2.png)

donde Light?, Light<sub>y</sub>y Light<sub>z</sub> son los valores de posición de la luz de entrada.

## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azimuth<br/> D2D1 \_ DISTANTSPECULAR \_ prop \_ Azimuth<br/>                       | Ángulo de dirección de la fuente de luz en el plano XY en relación con el eje X en la dirección del reloj de contador. Las unidades están en grados y deben estar entre 0 y 360 grados.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 0.0 f.<br/>                                                                                                                                                                              |
| Elevation<br/> Elevación de D2D1 \_ DISTANTSPECULAR \_ \_<br/>                   | El ángulo de dirección de la fuente de luz en el plano YZ con respecto al eje Y en la dirección del reloj de contador. Las unidades están en grados y deben estar entre 0 y 360 grados. <br/> El tipo es FLOAT.<br/> El valor predeterminado es 0.0 f.<br/>                                                                                                                                                                             |
| SpecularExponent<br/> \_ \_ \_ Exponente especular de D2D1 DISTANTSPECULAR \_<br/>   | Exponente para el término especular de la ecuación de iluminación Phong. Un valor mayor corresponde a una superficie más reflectante. El valor es una unidad y debe estar entre 1,0 y 128. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                          |
| SpecularConstant<br/> D2D1 \_ DISTANTSPECULAR \_ prop \_ ( \_ constante especular)<br/>   | La proporción de reflexión especular con respecto a la luz entrante. El valor es una unidad y debe estar entre 0 y 10.000. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                             |
| SurfaceScale<br/> \_Escala de \_ superficie de prop \_ \_ de D2D1 DISTANTSPECULAR<br/>           | Factor de escala en la dirección Z. El valor es una unidad y debe estar entre 0 y 10.000. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                |
| Color<br/> D2D1 \_ DISTANTSPECULAR \_ prop \_ color<br/>                           | Color de la luz entrante. Esta propiedad se expone como vector D2D1 \_ \_ 3F (R, G, B) y se usa para calcular l<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. El tipo es D2D1 \_ Vector \_ 3F.<br/> El valor predeterminado es {1.0 f, 1.0 f, 1.0 f.<br/>                                                                                                                                                                                       |
| KernelUnitLength<br/> Longitud de la \_ unidad de kernel de prop D2D1 DISTANTSPECULAR \_ \_ \_ \_<br/> | Tamaño de un elemento en el kernel de Sobel que se usa para generar la superficie normal en la dirección X e y. Esta propiedad es un \_ Vector D2D1 \_ 2F (longitud de unidad de kernel X, longitud de unidad de kernel y) y se define en (unidad/kernel de píxeles independientes del dispositivo (DIP)). El efecto utiliza la interpolación bilineal para escalar el mapa de bits para que coincida con el tamaño de los elementos de kernel. El tipo es D2D1 \_ Vector \_ 2F.<br/> El valor predeterminado es {1.0 f, 1.0 f}.<br/> |
| ModoDeLaEscala<br/> \_Modo de \_ \_ escalado de propiedades \_ de D2D1 DISTANTSPECULAR<br/>                 | El modo de interpolación que el efecto usa para escalar la imagen a la longitud de unidad de kernel correspondiente. Hay seis modos de escala que abarcan la calidad y la velocidad.<br/> El tipo es D2D1 \_ DISTANTSPECULAR \_ Scale \_ mode.<br/> El valor predeterminado es D2D1 \_ DISTANTSPECULAR en \_ modo de escala \_ \_ lineal.<br/>                                                                                                                                 |



 

## <a name="scale-modes"></a>Modos de escala



| Enumeración                                               | Descripción                                                                                                                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ el \_ modo de escalado DISTANTSPECULAR \_ \_ más cercano \_     | Muestrea el punto único más cercano y lo usa. Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| \_Modo de \_ escala \_ \_ lineal de D2D1 DISTANTSPECULAR                | Utiliza un ejemplo de cuatro puntos y una interpolación lineal. Este modo genera una imagen de mayor calidad que el vecino más cercano.                                                                                   |
| D2D1 \_ \_ modo de escala DISTANTSPECULAR \_ \_ cúbico                 | Usa un kernel cúbico de ejemplo 16 para la interpolación. Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ DISTANTSPECULAR en \_ modo de escala lineal de \_ \_ varios \_ ejemplos \_ | Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado. Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.                                              |
| \_Modo de \_ escala D2D1 DISTANTSPECULAR \_ \_           | Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ DISTANTSPECULAR, \_ modo de escalado de \_ \_ alta \_ calidad \_ cúbico  | Usa un kernel cúbico de alta calidad de tamaño variable para realizar una downscale previa de la imagen si downscaling está implicado en la matriz de transformación. A continuación, usa el modo de interpolación cúbico para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el efecto tiene como valor predeterminado D2D1 \_ DISTANTSPECULAR \_ modo de escala \_ \_ lineal.

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

 


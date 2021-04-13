---
title: Efecto de iluminación difusa puntual
description: Use el efecto de iluminación de difusión puntual para crear una imagen que parezca una superficie no reflectante con la que la fuente de luz está limitada a un cono dirigido de luz y la luz está dispersa en todas las direcciones.
ms.assetid: 9048D664-28DB-4DB6-9B95-3A61A1EDF5EC
keywords:
- efecto de iluminación difusa puntual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d085e43f161275cbe46d5b8eeb03f0ad13ff5f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104568664"
---
# <a name="spot-diffuse-lighting-effect"></a>Efecto de iluminación difusa puntual

Use el efecto de iluminación de difusión puntual para crear una imagen que parezca una superficie no reflectante con la que la fuente de luz está limitada a un cono dirigido de luz y la luz está dispersa en todas las direcciones. Este efecto usa el canal alfa como mapa de alto y enciende la imagen con una fuente de luz puntual.

El color del mapa de bits de salida es el resultado del color claro, la posición de la luz y la geometría de la superficie. La salida del canal alfa para cada píxel con iluminación difusa siempre es 1,0.

El CLSID para este efecto es CLSID \_ D2D1SpotDiffuse.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Modos de escala](#scale-modes)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de luz difusor puntual.

![captura de pantalla de ejemplo de efecto que muestra ](images/spot-diffuse-example.png)

El efecto calcula los valores finales de píxeles de salida que se calculan mediante estas ecuaciones:

![cálculo de mapa de bits de salida](images/spot-diffuse-formula.png)

Donde:<dl> k<sub>d</sub> = constante de iluminación difusa. Especificado por el usuario.  
![símbolo de vector normal.](images/point-spec-mathchar-n.png) = Vector de unidad normal de superficie, una función de x e y.  
![símbolo de vector claro.](images/distant-spec-mathchar-l.png) = Vector de unidad que apunta de la superficie a la luz.  
L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub> = el color claro en los componentes RGB.  
</dl>

## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                                     | Tipo y valor predeterminado                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> Posición de la luz de D2D1 \_ SPOTDIFFUSE \_ \_ \_<br/>           | \_Vector D2D1 \_ 3F<br/> {0.0 f, 0.0 f, 0.0 f}<br/>                                   | Posición de la luz de la fuente de luz del punto. La propiedad es una D2D1 \_ Vector \_ 3F definida como (x, y, z). Las unidades están en píxeles independientes del dispositivo (DIP) y no están enlazadas.<br/>                                                                                                                                                                                                                   |
| PointsAt<br/> D2D1 \_ SPOTDIFFUSE \_ prop \_ Points \_ at<br/>                     | \_Vector D2D1 \_ 3F<br/> {0.0 f, 0.0 f, 0.0 f}<br/>                                   | Donde se centra la luz focal. La propiedad se expone como un \_ Vector D2D1 \_ 3F con (x, y, z). Las unidades están en DIP y los valores están sin enlazar.<br/>                                                                                                                                                                                                                                          |
| Foco<br/> D2D1 \_ SPOTDIFFUSE \_ prop \_ Focus<br/>                             | FLOAT<br/> 1,0 f<br/>                                                            | Foco de la luz focal. Esta propiedad es sin unidades y se define entre 0 y 200.<br/>                                                                                                                                                                                                                                                                                                      |
| LimitingConeAngle<br/> D2D1 \_ SPOTDIFFUSE \_ prop \_ limite \_ \_ angular<br/> | FLOAT<br/> 90.0 f<br/>                                                           | Ángulo de cono que restringe la región en la que se proyecta la luz. No se proyecta luz fuera del cono. El ángulo del cono de limitación es el ángulo entre el eje de luz focal (el eje entre las propiedades *LightPosition* y *PointsAt* ) y el cono de luz focal. Esta propiedad se define en grados y debe estar comprendida entre 0 y 90 grados.<br/>                                            |
| DiffuseConstant<br/> D2D1 \_ SPOTDIFFUSE \_ prop ( \_ \_ constante difusa)<br/>       | FLOAT<br/> 1,0 f<br/>                                                            | La proporción de reflexión difusa con respecto a la cantidad de luz entrante. Esta propiedad debe estar comprendida entre 0 y 10.000 y no es una unidad. <br/>                                                                                                                                                                                                                                                                     |
| SurfaceScale<br/> \_Escala de \_ superficie de prop \_ \_ de D2D1 SPOTDIFFUSE<br/>             | FLOAT<br/> 1,0 f<br/>                                                            | Factor de escala en la dirección Z. La escala de superficie es sin unidades y debe estar comprendida entre 0 y 10.000.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> D2D1 \_ SPOTDIFFUSE \_ prop \_ color<br/>                             | \_Vector D2D1 \_ 3F<br/> {1.0 f, 1.0 f, 1.0 f}<br/>                                   | Color de la luz entrante. Esta propiedad se expone como Vector 3 (R, G, B) y se usa para calcular L<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. <br/>                                                                                                                                                                                                                                         |
| KernelUnitLength<br/> Longitud de la \_ unidad de kernel de prop D2D1 SPOTDIFFUSE \_ \_ \_ \_<br/>   | \_Vector D2D1 \_ 2F<br/> {1.0 f, 1.0 f}<br/>                                         | Tamaño de un elemento en el kernel de Sobel que se usa para generar la superficie normal en la dirección X e y. Esta propiedad se asigna a los valores DX y DY en el degradado Sobel. Esta propiedad es un \_ Vector D2D1 \_ 2F (longitud de unidad de kernel X, longitud de unidad de kernel y) y se define en (DIP/unidad de kernel). El efecto utiliza la interpolación bilineal para escalar el mapa de bits para que coincida con el tamaño de los elementos de kernel.<br/> |
| ModoDeLaEscala<br/> \_Modo de \_ \_ escalado de propiedades \_ de D2D1 SPOTDIFFUSE<br/>                   | \_Modo de \_ escala D2D1 SPOTDIFFUSE \_<br/> \_Modo de \_ escala \_ \_ lineal de D2D1 SPOTDIFFUSE<br/> | El modo de interpolación que el efecto usa para escalar la imagen a la longitud de unidad de kernel correspondiente. Hay seis modos de escala que abarcan la calidad y la velocidad. Consulte [modos de escala](#scale-modes) para obtener más información.<br/>                                                                                                                                                                                  |



 

## <a name="scale-modes"></a>Modos de escala



| Enumeración                                           | Descripción                                                                                                                                                                                          |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ el \_ modo de escalado SPOTDIFFUSE \_ \_ más cercano \_     | Muestrea el punto único más cercano y lo usa. Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| \_Modo de \_ escala \_ \_ lineal de D2D1 SPOTDIFFUSE                | Utiliza un ejemplo de cuatro puntos y una interpolación lineal. Este modo genera una imagen de mayor calidad que el vecino más cercano.                                                                                   |
| D2D1 \_ \_ modo de escala SPOTDIFFUSE \_ \_ cúbico                 | Usa un kernel cúbico de ejemplo 16 para la interpolación. Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ SPOTDIFFUSE en \_ modo de escala lineal de \_ \_ varios \_ ejemplos \_ | Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado. Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.                                              |
| \_Modo de \_ escala D2D1 SPOTDIFFUSE \_ \_           | Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ SPOTDIFFUSE, \_ modo de escalado de \_ \_ alta \_ calidad \_ cúbico  | Usa un kernel cúbico de alta calidad de tamaño variable para realizar una downscale previa de la imagen si downscaling está implicado en la matriz de transformación. A continuación, usa el modo de interpolación cúbico para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el efecto tiene como valor predeterminado D2D1 \_ SPOTDIFFUSE \_ modo de escala \_ \_ lineal.

 

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

 


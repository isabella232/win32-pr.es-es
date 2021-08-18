---
title: Efecto de iluminación difusa puntual
description: Use el efecto de iluminación difusa al descubierto para crear una imagen que parece ser una superficie no reflectante con donde la fuente de luz se limita a un cono de luz dirigido y la luz se dispersa en todas las direcciones.
ms.assetid: 9048D664-28DB-4DB6-9B95-3A61A1EDF5EC
keywords:
- efecto de iluminación difusa de spot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ee0032351ce5409aabf75eaa36cd79362b8e51b85edb26d2d1d06ca9346bfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075395"
---
# <a name="spot-diffuse-lighting-effect"></a>Efecto de iluminación difusa puntual

Use el efecto de iluminación difusa al descubierto para crear una imagen que parece ser una superficie no reflectante con donde la fuente de luz se limita a un cono de luz dirigido y la luz se dispersa en todas las direcciones. Este efecto usa el canal alfa como mapa de alto y enciende la imagen con una fuente de luz de spot.

El color del mapa de bits de salida es el resultado del color claro, la posición de la luz y la geometría de la superficie. La salida del canal alfa para cada píxel con iluminación difusa siempre es 1,0.

El CLSID para este efecto es CLSID \_ D2D1SpotDiffuse.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Modos de escalado](#scale-modes)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de iluminación difuso de spot.

![captura de pantalla de ejemplo de efecto que muestra ](images/spot-diffuse-example.png)

El efecto calcula que los valores de píxel de salida finales se calculan mediante estas ecuaciones:

![cálculo de mapa de bits de salida](images/spot-diffuse-formula.png)

Donde:<dl> k<sub>d</sub> = constante de iluminación difusa. Especificado por el usuario.  
![símbolo de vector normal.](images/point-spec-mathchar-n.png) = vector de unidad normal de superficie, una función de x e y.  
![símbolo de vector claro.](images/distant-spec-mathchar-l.png) = vector de unidad que apunta desde la superficie a la luz.  
L<sub>r</sub>, L<sub>g</sub>, L<sub>b</sub> = el color claro en los componentes RGB.  
</dl>

## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                                     | Tipo y valor predeterminado                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ LIGHT \_ POSITION<br/>           | D2D1 \_ VECTOR \_ 3F<br/> {0.0f, 0.0f, 0.0f}<br/>                                   | Posición de la luz del origen de luz de punto. La propiedad es un VECTOR 3F D2D1 \_ \_ definido como (x, y, z). Las unidades están en píxeles independientes del dispositivo (DIP) y están sin enlazar.<br/>                                                                                                                                                                                                                   |
| PointsAt<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ POINTS \_ AT<br/>                     | D2D1 \_ VECTOR \_ 3F<br/> {0.0f, 0.0f, 0.0f}<br/>                                   | Donde se centra la luz de spot. La propiedad se expone como D2D1 \_ VECTOR \_ 3F con (x, y, z). Las unidades están en DIP y los valores están sin enlazar.<br/>                                                                                                                                                                                                                                          |
| Foco<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ FOCUS<br/>                             | FLOAT<br/> 1,0f<br/>                                                            | Foco de la luz de spot. Esta propiedad no tiene unidad y se define entre 0 y 200.<br/>                                                                                                                                                                                                                                                                                                      |
| LimitingConeAngle<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ LIMITING \_ CONE \_ ANGLE<br/> | FLOAT<br/> 90,0f<br/>                                                           | Ángulo de cono que restringe la región donde se proyecta la luz. No se proyecta ninguna luz fuera del cono. El ángulo de cono limitador es el ángulo entre el eje claro de spot (el eje entre las propiedades *LightPosition* y *PointsAt)* y el cono claro de spot. Esta propiedad se define en grados y debe estar entre 0 y 90 grados.<br/>                                            |
| DiffuseConstant<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ DIFUSO \_ CONSTANTE<br/>       | FLOAT<br/> 1,0f<br/>                                                            | Proporción de reflexión difusa con la cantidad de luz entrante. Esta propiedad debe estar entre 0 y 10 000 y no tiene unidad. <br/>                                                                                                                                                                                                                                                                     |
| SurfaceScale<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ SURFACE \_ SCALE<br/>             | FLOAT<br/> 1,0f<br/>                                                            | Factor de escala en la dirección Z. La escala de la superficie no tiene unidad y debe estar entre 0 y 10 000.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ COLOR<br/>                             | D2D1 \_ VECTOR \_ 3F<br/> {1.0f, 1.0f, 1.0f}<br/>                                   | Color de la luz entrante. Esta propiedad se expone como vector 3 (R, G, B) y se usa para calcular L<sub>R</sub>, L<sub>G</sub>, L<sub>B</sub>. <br/>                                                                                                                                                                                                                                         |
| KernelUnitLength<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ KERNEL \_ UNIT \_ LENGTH<br/>   | D2D1 \_ VECTOR \_ 2F<br/> {1.0f, 1.0f}<br/>                                         | Tamaño de un elemento en el kernel de Sobel que se usa para generar la superficie normal en la dirección X e Y. Esta propiedad se asigna a los valores dx y dy en el degradado sobel. Esta propiedad es D2D1 \_ VECTOR \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) y se define en (DIP/Unidad de kernel). El efecto usa la interpolación bilineal para escalar el mapa de bits para que coincida con el tamaño de los elementos del kernel.<br/> |
| Scalemode<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ SCALE \_ MODE<br/>                   | D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE<br/> D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ LINEAR<br/> | Modo de interpolación que el efecto usa para escalar la imagen a la longitud de unidad de kernel correspondiente. Hay seis modos de escala que varían en calidad y velocidad. Consulte [Modos de escalado](#scale-modes) para obtener más información.<br/>                                                                                                                                                                                  |



 

## <a name="scale-modes"></a>Modos de escalado



| Enumeración                                           | Descripción                                                                                                                                                                                          |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ NEAREST \_ NEIGHBOR     | Muestrea el punto más cercano y lo usa. Este modo usa menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ LINEAR                | Usa una muestra de cuatro puntos y una interpolación lineal. Este modo genera una imagen de mayor calidad que el vecino más próximo.                                                                                   |
| D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ CUBIC                 | Usa un kernel cúbica de 16 muestras para la interpolación. Este modo usa el mayor tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 muestras lineales dentro de un solo píxel para un buen suavizado de alias perimetral. Este modo es bueno para reducir verticalmente en pequeñas cantidades en imágenes con pocos píxeles.                                              |
| D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ ANISOTROPIC           | Usa el filtrado anisotropico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ HIGH \_ QUALITY \_ CUBIC  | Usa un kernel cúbica de alta calidad de tamaño variable para realizar una escala previa a la baja de la imagen si la escala hacia abajo está implicada en la matriz de transformación. A continuación, usa el modo de interpolación cúbica para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el valor predeterminado del efecto es D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ LINEAR.

 

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

 


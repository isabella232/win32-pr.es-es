---
title: Efecto de iluminación especular distante
description: Use el efecto de iluminación especular lejana para crear una imagen que parece ser una superficie reflectante en la que la fuente de luz parece estar procedente de una distancia larga (como el sol o las luces de sobrecarga).
ms.assetid: 74D71A2D-8D1D-4FDE-898A-2D2F5A8D5D31
keywords:
- iluminación especular lejana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a02bbf6e928691f88de3adc41fc3ae84cbc1e7df69b3b5998ca903a7556d29d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768855"
---
# <a name="distant-specular-lighting-effect"></a>Efecto de iluminación especular distante

Use el efecto de iluminación especular lejana para crear una imagen que parece ser una superficie reflectante en la que la fuente de luz parece estar procedente de una distancia larga (como el sol o las luces de sobrecarga). Este efecto usa el canal alfa como mapa de alto y enciende la imagen con una fuente de luz lejana.

El color del mapa de bits de salida es el resultado del color claro, la posición de la luz y la geometría de la superficie. La salida del canal alfa para cada píxel con iluminación especular es el máximo de las salidas de canales rojo, verde y azul para ese píxel.

El CLSID para este efecto es CLSID \_ D2D1DistantSpecular.

-   [Imagen de ejemplo](#example-image)
-   [Fuente de luz lejana](#distant-light-source)
-   [Propiedades de efecto](#effect-properties)
-   [Modos de escalado](#scale-modes)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de iluminación lejana-especular.

![Captura de pantalla de ejemplo de efecto que muestra las imágenes de entrada y salida del efecto de iluminación especular lejana. ](images/distant-spec-example.png)

El mapa de bits de salida final se puede calcular mediante las ecuaciones siguientes.

![cálculo de mapa de bits de salida](images/distant-spec-formula1.png)

where <dl> ¿K? = constante de iluminación especular.  
![símbolo normal de superficie. ](images/point-spec-mathchar-n.png) = vector de unidad normal de superficie.  
![símbolo de vector medio. ](images/point-spec-mathchar-h.png) = vector de unidad "a medio camino" entre el vector de unidad de ojo y el vector de unidad de luz.  
C<sub>r</sub>, C<sub>g</sub>, C<sub>b</sub> = color claro en componentes RGB.  
</dl>

## <a name="distant-light-source"></a>Fuente de luz lejana

La imagen aquí muestra un ejemplo de la dirección de la luz desde una fuente de luz lejana.

![fuente de luz lejana](images/distant-spec-lightsource.png)

El efecto usa los parámetros azimuth y elevation para calcular el vector de luz. ![Vector l.](images/distant-spec-mathchar-l.png) mediante las ecuaciones siguientes:

![cálculo de vector claro](images/distant-spec-formula2.png)

donde Light?, Light<sub>y</sub>y Light<sub>z</sub> son los valores de la posición de la luz de entrada.

## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Acimut<br/> D2D1 \_ DISTANTSPECULAR \_ PROP \_ AZIMUTH<br/>                       | Ángulo de dirección de la fuente de luz en el plano XY con respecto al eje X en la dirección del reloj del contador. Las unidades están en grados y deben estar entre 0 y 360 grados.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 0,0f.<br/>                                                                                                                                                                              |
| Elevation<br/> ELEVACIÓN DE PROP LEJANA DE \_ D2D1SPECULAR \_ \_<br/>                   | Ángulo de dirección de la fuente de luz en el plano YZ con respecto al eje Y en la dirección del reloj del contador. Las unidades están en grados y deben estar entre 0 y 360 grados. <br/> El tipo es FLOAT.<br/> El valor predeterminado es 0,0f.<br/>                                                                                                                                                                             |
| SpecularExponent<br/> EXPONENTE ESPECULAR ESPECULAR DE PROPIEDAD \_ ESPECULAR LEJANA D2D1 \_ \_ \_<br/>   | Exponente del término especular en la ecuación de iluminación de Phong. Un valor mayor corresponde a una superficie más reflectante. El valor no tiene unidad y debe estar entre 1,0 y 128. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                          |
| SpecularConstant<br/> D2D1 \_ DISTANTSPECULAR \_ PROP \_ SPECULAR \_ CONSTANT<br/>   | Proporción de reflexión especular con la luz entrante. El valor no tiene unidad y debe estar entre 0 y 10 000. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                             |
| SurfaceScale<br/> D2D1 \_ DISTANTSPECULAR \_ PROP \_ SURFACE \_ SCALE<br/>           | Factor de escala en la dirección Z. El valor no tiene unidad y debe estar entre 0 y 10 000. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                |
| Color<br/> COLOR DE PROP \_ LEJANA D2D1SPECULAR \_ \_<br/>                           | Color de la luz entrante. Esta propiedad se expone como D2D1 \_ VECTOR \_ 3F (R, G, B) y<sub></sub>se usa para calcular L<sub>R,</sub>L<sub>G,</sub>L B . El tipo es D2D1 \_ VECTOR \_ 3F.<br/> El valor predeterminado es {1.0f, 1.0f, 1.0f}.<br/>                                                                                                                                                                                       |
| KernelUnitLength<br/> D2D1 \_ DISTANTSPECULAR \_ PROP \_ KERNEL \_ UNIT \_ LENGTH<br/> | Tamaño de un elemento en el kernel de Sobel que se usa para generar la superficie normal en la dirección X e Y. Esta propiedad es un vector D2D1 2F (longitud de unidad de kernel X, longitud de unidad de kernel Y) y se define en (píxeles independientes del dispositivo \_ \_ (DIP)/unidad de kernel). El efecto usa la interpolación bilineal para escalar el mapa de bits para que coincida con el tamaño de los elementos del kernel. El tipo es D2D1 \_ VECTOR \_ 2F.<br/> El valor predeterminado es {1.0f, 1.0f}.<br/> |
| Scalemode<br/> D2D1 \_ DISTANTSPECULAR \_ PROP \_ SCALE \_ MODE<br/>                 | Modo de interpolación que el efecto usa para escalar la imagen a la longitud de unidad de kernel correspondiente. Hay seis modos de escala que varían en calidad y velocidad.<br/> El tipo es D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE.<br/> El valor predeterminado es D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ LINEAR.<br/>                                                                                                                                 |



 

## <a name="scale-modes"></a>Modos de escalado



| Enumeración                                               | Descripción                                                                                                                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ NEAREST \_ NEIGHBOR     | Muestrea el punto más cercano y lo usa. Este modo usa menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ LINEAR                | Usa una muestra de cuatro puntos y una interpolación lineal. Este modo genera una imagen de mayor calidad que el vecino más próximo.                                                                                   |
| D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ CUBIC                 | Usa un kernel cúbica de 16 muestras para la interpolación. Este modo usa el mayor tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 muestras lineales dentro de un solo píxel para un buen suavizado de alias perimetral. Este modo es bueno para reducir verticalmente en pequeñas cantidades en imágenes con pocos píxeles.                                              |
| D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ ANISOTROPIC           | Usa el filtrado anisotropico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ HIGH \_ QUALITY \_ CUBIC  | Usa un kernel cúbica de alta calidad de tamaño variable para realizar una escala previa a la baja de la imagen si la escala hacia abajo está implicada en la matriz de transformación. A continuación, usa el modo de interpolación cúbica para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el valor predeterminado del efecto es D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ LINEAR.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Header                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


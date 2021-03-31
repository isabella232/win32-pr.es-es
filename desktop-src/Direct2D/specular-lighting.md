---
title: Efecto de iluminación especular puntual
description: Use el efecto luz de iluminación puntual para crear una imagen que parezca una superficie reflectante en la que la fuente de luz esté limitada a un cono dirigido de luz.
ms.assetid: B6E24036-1548-4B9E-A8FE-8B87D4DBF97A
keywords:
- iluminación especular
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f2482d9631de7383c26e791d13f1571f247fa6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079245"
---
# <a name="spot-specular-lighting-effect"></a>Efecto de iluminación especular puntual

Use el efecto luz de iluminación puntual para crear una imagen que parezca una superficie reflectante en la que la fuente de luz esté limitada a un cono dirigido de luz. Este efecto usa el canal alfa como mapa de alto y enciende la imagen con una fuente de luz puntual.

El color del mapa de bits de salida es el resultado del color claro, la posición de la luz, la dirección del cono y la geometría de la superficie según la parte especular del modelo de iluminación Phong. La salida del canal alfa para cada píxel con iluminación especular es el máximo de las salidas de canal rojo, verde y azul para ese píxel.

El CLSID para este efecto es CLSID \_ D2D1SpotSpecular.

-   [Imagen de ejemplo](#example-image)
-   [Fuente de luz puntual](#spot-light-source)
-   [Propiedades del efecto](#effect-properties)
-   [Modos de escala](#scale-modes)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de luz especular puntual.

![captura de pantalla de ejemplo de efecto.](images/spot-spec-example.png)

La luz especular hace referencia a la luz que se refleja en una dirección determinada.

![un diagrama de los vectores utilizados para cacluate una salida de luz especular para un mapa de bits.](images/point-spec-reflected1.png)

El efecto calcula los valores finales de píxeles de salida que se calculan mediante las ecuaciones aquí:

![ecuaciones de píxeles de salida.](images/spot-formula1.png)

where

![definiciones de variables.](images/spot-formula2.png)

## <a name="spot-light-source"></a>Fuente de luz puntual

Una fuente de luz puntual emite luz en un cono en una dirección específica y no emite luz fuera del cono.

La fuente de luz focal calcula el vector de luz L y el vector medio H de la misma manera que el efecto [especular de punto](point-specular.md) .

El efecto calcula el color claro, L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub>, como una función de la posición de la fuente de luz, tal como se muestra aquí con las ecuaciones:

![ecuación de fuente de luz puntual](images/spot-formula3.png)

Vector ![símbolo de vector claro.](images/spot-mathchar-l.png) se define mediante estas ecuaciones:

![ecuación: Vector](images/spot-formula4.png)

Vector ![símbolo de vector t](images/spot-mathchar-t.png) se define mediante estas ecuaciones:

![ecuación: Vector 2](images/spot-formula5.png)

## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> Posición de la luz de D2D1 \_ SPOTSPECULAR \_ \_ \_<br/>             | Posición de la luz de la fuente de luz del punto. La propiedad es una D2D1 \_ Vector \_ 3F definida como (x, y, z). Las unidades están en píxeles independientes del dispositivo (DIP) y no están enlazadas. El tipo es D2D1 \_ Vector \_ 3F.<br/> El valor predeterminado es {0.0 f, 0.0 f, 0.0 f}.<br/>                                                                                                                                                                                                              |
| PointsAt<br/> D2D1 \_ SPOTSPECULAR \_ prop \_ Points \_ at<br/>                       | Donde se centra la luz focal. La propiedad se expone como un \_ Vector D2D1 \_ 3F con (x, y, z). Las unidades están en DIP y los valores están sin enlazar. El tipo es D2D1 \_ Vector \_ 3F.<br/> El valor predeterminado es {0.0 f, 0.0 f, 0.0 f}.<br/>                                                                                                                                                                                                                                     |
| Foco<br/> D2D1 \_ SPOTSPECULAR \_ prop \_ Focus<br/>                               | Foco de la luz focal. Esta propiedad es sin unidades y se define entre 0 y 200. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                          |
| LimitingConeAngle<br/> D2D1 de la \_ \_ propuesta especular \_ \_ \_ \_<br/> | Ángulo de cono que restringe la región en la que se proyecta la luz. No se proyecta luz fuera del cono. El ángulo del cono de limitación es el ángulo entre el eje de luz focal (el eje entre las propiedades *LightPosition* y *PointsAt* ) y el cono de luz focal. Esta propiedad se define en grados y debe estar comprendida entre 0 y 90 grados. El tipo es FLOAT.<br/> El valor predeterminado es 90.0 f.<br/>                                                               |
| SpecularExponent<br/> \_ \_ \_ Exponente especular de D2D1 SPOTSPECULAR \_<br/>       | Exponente para el término especular de la ecuación de iluminación Phong. Un valor mayor corresponde a una superficie más reflectante. Este valor no tiene unidades y debe estar entre 1,0 y 128. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                               |
| SpecularConstant<br/> D2D1 \_ SPOTSPECULAR \_ prop \_ ( \_ constante especular)<br/>       | La proporción de reflexión especular con respecto a la luz entrante. El valor es una unidad y debe estar entre 0 y 10.000. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                                   |
| SurfaceScale<br/> \_Escala de \_ superficie de prop \_ \_ de D2D1 SPOTSPECULAR<br/>               | Factor de escala en la dirección Z para generar un mapa de alto. El valor es una unidad y debe estar entre 0 y 10.000. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> D2D1 \_ SPOTSPECULAR \_ prop \_ color<br/>                               | Color de la luz entrante. Esta propiedad se expone como Vector 3 (R, G, B) y se usa para calcular L<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. El tipo es D2D1 \_ Vector \_ 3F.<br/> El valor predeterminado es {1.0 f, 1.0 f, 1.0 f.<br/>                                                                                                                                                                                                                                     |
| KernelUnitLength<br/> Longitud de la \_ unidad de kernel de prop D2D1 SPOTSPECULAR \_ \_ \_ \_<br/>     | Tamaño de un elemento en el kernel de Sobel que se usa para generar la superficie normal en la dirección X e y. Esta propiedad se asigna a los valores DX y DY en el degradado Sobel. Esta propiedad es un \_ Vector D2D1 \_ 2F (longitud de unidad de kernel X, longitud de unidad de kernel y) y se define en (DIP/unidad de kernel). El efecto utiliza la interpolación bilineal para escalar el mapa de bits para que coincida con el tamaño de los elementos de kernel. El tipo es D2D1 \_ Vector \_ 2F.<br/> El valor predeterminado es {1.0 f, 1.0 f}.<br/> |
| ModoDeLaEscala<br/> \_Modo de \_ \_ escalado de propiedades \_ de D2D1 SPOTSPECULAR<br/>                     | El modo de interpolación que el efecto usa para escalar la imagen a la longitud de unidad de kernel correspondiente. Hay seis modos de escala que abarcan la calidad y la velocidad. Consulte [modos de escala](#scale-modes) para obtener más información. <br/> El tipo es D2D1 \_ SPOTSPECULAR \_ Scale \_ mode.<br/> El valor predeterminado es D2D1 \_ SPOTSPECULAR en \_ modo de escala \_ \_ lineal.<br/>                                                                                                                             |



 

## <a name="scale-modes"></a>Modos de escala



| Enumeración                                            | Descripción                                                                                                                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ el \_ modo de escalado SPOTSPECULAR \_ \_ más cercano \_     | Muestrea el punto único más cercano y lo usa. Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| \_Modo de \_ escala \_ \_ lineal de D2D1 SPOTSPECULAR                | Utiliza un ejemplo de cuatro puntos y una interpolación lineal. Este modo genera una imagen de mayor calidad que el vecino más cercano.                                                                                   |
| D2D1 \_ \_ modo de escala SPOTSPECULAR \_ \_ cúbico                 | Usa un kernel cúbico de ejemplo 16 para la interpolación. Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ SPOTSPECULAR en \_ modo de escala lineal de \_ \_ varios \_ ejemplos \_ | Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado. Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.                                              |
| \_Modo de \_ escala D2D1 SPOTSPECULAR \_ \_           | Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ SPOTSPECULAR, \_ modo de escalado de \_ \_ alta \_ calidad \_ cúbico  | Usa un kernel cúbico de alta calidad de tamaño variable para realizar una downscale previa de la imagen si downscaling está implicado en la matriz de transformación. A continuación, usa el modo de interpolación cúbico para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el efecto tiene como valor predeterminado D2D1 \_ SPOTSPECULAR \_ modo de escala \_ \_ lineal.

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

 


---
title: Efecto de iluminación especular puntual
description: Use el efecto de iluminación spot-specular para crear una imagen que parece ser una superficie reflectante donde la fuente de luz se limita a un cono de luz dirigido.
ms.assetid: B6E24036-1548-4B9E-A8FE-8B87D4DBF97A
keywords:
- iluminación especular de spot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9edc4c75eaa17369ba0d0d9f1838d8857053def9aaab3dacceb8bf761b9c04c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000410"
---
# <a name="spot-specular-lighting-effect"></a>Efecto de iluminación especular puntual

Use el efecto de iluminación spot-specular para crear una imagen que parece ser una superficie reflectante donde la fuente de luz se limita a un cono de luz dirigido. Este efecto usa el canal alfa como mapa de altura y enciende la imagen con una fuente de luz de punto.

El color del mapa de bits de salida es el resultado del color claro, la posición de la luz, la dirección del cono y la geometría de la superficie según la parte especular del modelo de iluminación Pong. La salida del canal alfa para cada píxel con iluminación especular es el máximo de las salidas de canales rojo, verde y azul para ese píxel.

El CLSID para este efecto es CLSID \_ D2D1SpotSpecular.

-   [Imagen de ejemplo](#example-image)
-   [Fuente de luz de spot](#spot-light-source)
-   [Propiedades de efecto](#effect-properties)
-   [Modos de escalado](#scale-modes)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de iluminación especular de spot.

![captura de pantalla del ejemplo de efecto.](images/spot-spec-example.png)

La luz especular hace referencia a la luz que se refleja en una dirección determinada.

![diagrama de los vectores usados para generar una salida de iluminación especular para un mapa de bits.](images/point-spec-reflected1.png)

El efecto calcula que los valores de píxel de salida finales se calculan mediante las ecuaciones siguientes:

![ecuaciones de píxeles de salida.](images/spot-formula1.png)

where

![definiciones de variable.](images/spot-formula2.png)

## <a name="spot-light-source"></a>Fuente de luz de spot

Una fuente de luz puntual emite luz en un cono en una dirección específica y no emite luz fuera del cono.

La fuente de luz de spot calcula el vector de luz L y el vector medio H de la misma manera que el [efecto especular de punto.](point-specular.md)

El efecto calcula el color claro, L<sub>r</sub>, L<sub>g</sub>, L<sub>b</sub>, como una función de la posición de la fuente de luz como se muestra con las ecuaciones aquí:

![ecuación de la fuente de luz de spot](images/spot-formula3.png)

El vector ![símbolo de vector claro.](images/spot-mathchar-l.png) se define mediante estas ecuaciones:

![ecuación: vector](images/spot-formula4.png)

El vector ![Símbolo de vector t](images/spot-mathchar-t.png) se define mediante estas ecuaciones:

![ecuación: vector 2](images/spot-formula5.png)

## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> D2D1 \_ SPOTSPECULAR \_ PROP \_ LIGHT \_ POSITION<br/>             | Posición de luz de la fuente de luz de punto. La propiedad es un vector 3F D2D1 \_ \_ definido como (x, y, z). Las unidades están en píxeles independientes del dispositivo (DIP) y están sin enlazar. El tipo es D2D1 \_ VECTOR \_ 3F.<br/> El valor predeterminado es {0.0f, 0.0f, 0.0f}.<br/>                                                                                                                                                                                                              |
| PointsAt<br/> D2D1 \_ SPOTSPECULAR \_ PROP \_ POINTS \_ AT<br/>                       | Donde se centra la luz de spot. La propiedad se expone como D2D1 \_ VECTOR \_ 3F con (x, y, z). Las unidades están en DIP y los valores no están unidos. El tipo es D2D1 \_ VECTOR \_ 3F.<br/> El valor predeterminado es {0.0f, 0.0f, 0.0f}.<br/>                                                                                                                                                                                                                                     |
| Foco<br/> FOCO DE PROP \_ DE SPOTSPECULAR D2D1 \_ \_<br/>                               | Foco de la luz de spot. Esta propiedad no tiene unidad y se define entre 0 y 200. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                                                          |
| LimitingConeAngle<br/> ÁNGULO DE CONO LIMITADOR DE PROP \_ \_ \_ \_ ESPECULAR \_ DE \_ SPOT D2D1<br/> | Ángulo de cono que restringe la región donde se proyecta la luz. No se proyecta ninguna luz fuera del cono. El ángulo de cono limitador es el ángulo entre el eje claro de spot (el eje entre las propiedades *LightPosition* y *PointsAt)* y el cono claro de spot. Esta propiedad se define en grados y debe estar entre 0 y 90 grados. El tipo es FLOAT.<br/> El valor predeterminado es 90,0f.<br/>                                                               |
| SpecularExponent<br/> EXPONENTE \_ ESPECULAR ESPECULAR DE PROP \_ \_ SPECULAR DE D2D1 SPOTSPECULAR \_<br/>       | Exponente del término especular en la ecuación de iluminación de Pong. Un valor mayor corresponde a una superficie más reflectante. Este valor no tiene unidad y debe estar entre 1,0 y 128. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                               |
| SpecularConstant<br/> D2D1 \_ SPOTSPECULAR \_ PROP \_ SPECULAR \_ CONSTANT<br/>       | Proporción de reflexión especular con la luz entrante. El valor no tiene unidad y debe estar entre 0 y 10 000. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                                   |
| SurfaceScale<br/> D2D1 \_ SPOTSPECULAR \_ PROP \_ SURFACE \_ SCALE<br/>               | Factor de escala en la dirección Z para generar un mapa de altura. El valor no tiene unidad y debe estar entre 0 y 10 000. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> COLOR DE PROP \_ DE SPOTSPECULAR D2D1 \_ \_<br/>                               | Color de la luz entrante. Esta propiedad se expone como vector 3 (R, G, B) y se usa para calcular L<sub>R</sub>, L<sub>G</sub>, L<sub>B</sub>. El tipo es D2D1 \_ VECTOR \_ 3F.<br/> El valor predeterminado es {1.0f, 1.0f, 1.0f}.<br/>                                                                                                                                                                                                                                     |
| KernelUnitLength<br/> LONGITUD DE UNIDAD DE KERNEL DE PROP SPOTSPECULAR D2D1 \_ \_ \_ \_ \_<br/>     | Tamaño de un elemento en el kernel de Sobel usado para generar la superficie normal en la dirección X e Y. Esta propiedad se asigna a los valores dx y dy del degradado Sobel. Esta propiedad es D2D1 VECTOR 2F (longitud de unidad de kernel X, longitud de unidad de kernel Y) y se define \_ \_ en (DIP/unidad de kernel). El efecto usa la interpolación bilineal para escalar el mapa de bits para que coincida con el tamaño de los elementos del kernel. El tipo es D2D1 \_ VECTOR \_ 2F.<br/> El valor predeterminado es {1.0f, 1.0f}.<br/> |
| Scalemode<br/> D2D1 \_ SPOTSPECULAR \_ PROP \_ SCALE \_ MODE<br/>                     | Modo de interpolación que el efecto usa para escalar la imagen a la longitud de unidad de kernel correspondiente. Hay seis modos de escala que varían en calidad y velocidad. Consulte [Modos de escalado](#scale-modes) para obtener más información. <br/> El tipo es D2D1 \_ SPOTSPECULAR \_ SCALE \_ MODE.<br/> El valor predeterminado es D2D1 \_ SPOTSPECULAR \_ SCALE \_ MODE \_ LINEAR.<br/>                                                                                                                             |



 

## <a name="scale-modes"></a>Modos de escalado



| Enumeración                                            | Descripción                                                                                                                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ SPOTSPECULAR \_ SCALE \_ MODE \_ NEAREST \_ NEIGHBOR     | Muestrea el punto único más cercano y lo usa. Este modo usa menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| D2D1 \_ SPOTSPECULAR \_ SCALE \_ MODE \_ LINEAR                | Usa una muestra de cuatro puntos e interpolación lineal. Este modo genera una imagen de mayor calidad que el vecino más próximo.                                                                                   |
| D2D1 \_ SPOTSPECULAR \_ SCALE \_ MODE \_ CUBIC                 | Usa un kernel cúbica de 16 muestras para la interpolación. Este modo usa el mayor tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ SPOTSPECULAR \_ SCALE \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 muestras lineales dentro de un solo píxel para un buen suavizado de alias perimetral. Este modo es bueno para reducir verticalmente en pequeñas cantidades en imágenes con pocos píxeles.                                              |
| D2D1 \_ SPOTSPECULAR \_ SCALE \_ MODE \_ ANISOTROPIC           | Usa el filtrado anisotropico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ SPOTSPECULAR \_ SCALE \_ MODE \_ HIGH \_ QUALITY \_ CUBIC  | Usa un kernel cúbica de alta calidad de tamaño variable para realizar una escala previa a la baja de la imagen si la escalación está implicada en la matriz de transformación. A continuación, usa el modo de interpolación cúbica para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el valor predeterminado del efecto es D2D1 \_ SPOTSPECULAR \_ SCALE \_ MODE \_ LINEAR.

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

 


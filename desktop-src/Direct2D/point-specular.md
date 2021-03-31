---
title: Efecto de iluminación especular puntual
description: Use el efecto de luz especular de punto para crear una imagen que parezca una superficie reflectante.
ms.assetid: 89E22FD0-BB7F-465F-A79C-056CA9F14F5D
keywords:
- efecto de luz especular de punto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 355c573888604af8dfac443f4f53554a8a780071
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996709"
---
# <a name="point-specular-lighting-effect"></a>Efecto de iluminación especular puntual

Use el efecto de luz especular de punto para crear una imagen que parezca una superficie reflectante. El efecto usa el canal alfa de la imagen como un mapa de alto y una fuente de luz puntual que se coloca, y calcula la reflexión y la luz según la parte especular del modelo de iluminación Phong.

El color del mapa de bits de salida es el resultado del color claro, la posición de la luz y la geometría de la superficie. La salida del canal alfa para cada píxel con iluminación especular es el máximo de las salidas de canal rojo, verde y azul para ese píxel.

El CLSID para este efecto es CLSID \_ D2D1PointSpecular.

-   [Imagen de ejemplo](#example-image)
-   [Origen de luz puntual](#point-light-source)
-   [Asignación de alto y vector normal](#height-map-and-normal-vector)
-   [Constante de iluminación especular y exponente](#specular-lighting-constant-and-exponent)
-   [Propiedades del efecto](#effect-properties)
-   [Modos de escala](#scales-modes)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de iluminación especular de punto.

![captura de pantalla de ejemplo de efecto que muestra las imágenes de entrada y salida del efecto de iluminación especular de punto.](images/point-spec-example.png)

La luz especular hace referencia a la luz que se refleja en una dirección específica según el modelo de iluminación Phong.

![un diagrama de los vectores utilizados para cacluate una salida de luz especular para un mapa de bits.](images/point-spec-reflected1.png)

El efecto calcula los valores finales de los píxeles de salida mediante las ecuaciones aquí:

![ecuaciones para calcular los valores finales de los píxeles. ](images/point-spec-formula-output.png)

where<dl> k? = constante de iluminación especular.  
![símbolo de vector de unidad normal de superficie. ](images/point-spec-mathchar-n.png) = Vector de unidad normal de superficie que es una función de x e y. Consulte [asignación de alto y vector normal](#height-map-and-normal-vector) para los cálculos.  
![símbolo de vector de unidad de la mitad. ](images/point-spec-mathchar-h.png) = Vector de unidad "medio" entre el vector de unidad ocular y el vector de unidad de luz. Vea [fuente de luz de punto](#point-light-source) para los cálculos.  
L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub> = el color claro en los componentes RGB.  
</dl>

La constante de iluminación especular se establece como la propiedad *SpecularConstant* y el color claro como la propiedad *color* .

## <a name="point-light-source"></a>Origen de luz puntual

Una fuente de luz puntual emite luz en todas las direcciones como en la imagen aquí.

![luz puntual que emite luz en todas las direcciones.](images/point-spec-light.png)

La posición de la fuente de luz se establece mediante la propiedad *LightPosition* . El efecto calcula el vector de luz, L, para una fuente de luz de punto mediante las ecuaciones aquí:

![ecuación del vector de luz.](images/point-spec-formula3.png)

donde Light?, Light<sub>y</sub>y Light<sub>z</sub> son la posición de la luz de entrada. El efecto calcula el vector de la mitad del ![ símbolo del vector medio.](images/point-spec-mathchar-h.png) tal como se define en el modelo de iluminación Phong, mediante la ecuación aquí. El modelo de iluminación supone que el vector ocular, ![ el símbolo del vector ocular ](images/point-spec-mathchar-e.png) , se encuentra en (0, 0, 1).

![ecuación de vector a la mitad.](images/point-spec-formula4.png)

Tanto L como H se normalizan en vectores de longitud de unidad.

## <a name="height-map-and-normal-vector"></a>Asignación de alto y vector normal

El efecto genera un mapa de alto para la imagen de entrada en función de su canal alfa.

El componente alto (Z) se calcula con la ecuación:

![la ecuación para calcular el alto (z) de la superficie.](images/point-spec-formula6.png)

El efecto calcula la superficie normal, ![símbolo de vector normal.](images/point-spec-mathchar-n.png), para el mapa de bits de entrada mediante un degradado Sobel.

## <a name="specular-lighting-constant-and-exponent"></a>Constante de iluminación especular y exponente

La luz especular representa la luz que se refleja en la superficie del mapa del alto de la imagen. Especifique la propiedad *SpecularExponent* que determina la cantidad de reflexión especular del mapa de bits.

Los exponentes mayores representan objetos shinier y reflejan la luz en una forma más centrada.

¿La propiedad *SpecularConstant* K? define la cantidad de luz reflejada como una relación de la luz entrante.

## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> Posición de la luz de D2D1 \_ POINTSPECULAR \_ \_ \_<br/>         | Posición de la luz de la fuente de luz del punto. La propiedad es una D2D1 \_ Vector \_ 3F definida como (x, y, z). Las unidades están en píxeles independientes del dispositivo (DIP) y los valores son sin y sin límite. El tipo es D2D1 \_ Vector \_ 3F.<br/> El valor predeterminado es {0.0 f, 0.0 f, 0.0 f}.<br/>                                                                                                                                                                                      |
| SpecularExponent<br/> \_ \_ \_ Exponente especular de D2D1 POINTSPECULAR \_<br/>   | Exponente para el término especular de la ecuación de iluminación Phong. Un valor mayor corresponde a una superficie más reflectante. Este valor no tiene unidades y debe estar entre 1,0 y 128. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                               |
| SpecularConstant<br/> D2D1 \_ POINTSPECULAR \_ prop \_ ( \_ constante especular)<br/>   | La proporción de reflexión especular con respecto a la luz entrante. El valor es una unidad y debe estar entre 0 y 10.000. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                                   |
| SurfaceScale<br/> \_Escala de \_ superficie de prop \_ \_ de D2D1 POINTSPECULAR<br/>           | Factor de escala en la dirección Z para generar un mapa de alto. El valor es una unidad y debe estar entre 0 y 10.000. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> D2D1 \_ POINTSPECULAR \_ prop \_ color<br/>                           | Color de la luz entrante. Esta propiedad se expone como vector D2D1 \_ \_ 3F (R, G, B) y se usa para calcular l<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. El tipo es D2D1 \_ Vector \_ 3F.<br/> El valor predeterminado es {1.0 f, 1.0 f, 1.0 f.<br/>                                                                                                                                                                                                                             |
| KernelUnitLength<br/> Longitud de la \_ unidad de kernel de prop D2D1 POINTSPECULAR \_ \_ \_ \_<br/> | Tamaño de un elemento en el kernel de Sobel que se usa para generar la superficie normal en las direcciones X e y. Esta propiedad se asigna a los valores DX y DY en el degradado Sobel. Esta propiedad es un \_ Vector D2D1 \_ 2F (longitud de unidad de kernel X, longitud de unidad de kernel y) y se define en (DIP/unidad de kernel). El efecto utiliza la interpolación bilineal para escalar el mapa de bits para que coincida con el tamaño de los elementos de kernel. El tipo es D2D1 \_ Vector \_ 2F.<br/> El valor predeterminado es {1.0 f, 1.0 f}.<br/> |
| ModoDeLaEscala<br/> \_Modo de \_ \_ escalado de propiedades \_ de D2D1 POINTSPECULAR<br/>                 | El modo de interpolación que el efecto usa para escalar la imagen a la longitud de unidad de kernel correspondiente. Hay seis modos de escala que abarcan la calidad y la velocidad. Consulte [modos de escala](#scales-modes) para obtener más información. <br/> El tipo es D2D1 \_ POINTSPECULAR \_ Scale \_ mode.<br/> El valor predeterminado es D2D1 \_ POINTSPECULAR en \_ modo de escala \_ \_ lineal.<br/>                                                                                                                          |



 

## <a name="scales-modes"></a>Modos de escala



| Enumeración                                             | Descripción                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ el \_ modo de escalado POINTSPECULAR \_ \_ más cercano \_     | Muestrea el punto único más cercano y lo usa. Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| \_Modo de \_ escala \_ \_ lineal de D2D1 POINTSPECULAR                | Utiliza un ejemplo de cuatro puntos y una interpolación lineal. Este modo genera una imagen de mayor calidad que el vecino más cercano.                                                                                   |
| D2D1 \_ \_ modo de escala POINTSPECULAR \_ \_ cúbico                 | Usa un kernel cúbico de ejemplo 16 para la interpolación. Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ POINTSPECULAR en \_ modo de escala lineal de \_ \_ varios \_ ejemplos \_ | Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado. Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.                                              |
| \_Modo de \_ escala D2D1 POINTSPECULAR \_ \_           | Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ POINTSPECULAR, \_ modo de escalado de \_ \_ alta \_ calidad \_ cúbico  | Usa un kernel cúbico de alta calidad de tamaño variable para realizar una downscale previa de la imagen si downscaling está implicado en la matriz de transformación. A continuación, usa el modo de interpolación cúbico para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el efecto tiene como valor predeterminado D2D1 \_ POINTSPECULAR \_ modo de escala \_ \_ lineal.

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

 


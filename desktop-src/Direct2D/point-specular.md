---
title: Efecto de iluminación especular puntual
description: Use el efecto de iluminación especular de punto para crear una imagen que parece ser una superficie reflectante.
ms.assetid: 89E22FD0-BB7F-465F-A79C-056CA9F14F5D
keywords:
- efecto de iluminación especular de punto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37adb0c6ea0ca946abf819730dcc378f421bf2c220dc0ab8d41916f570501d0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075189"
---
# <a name="point-specular-lighting-effect"></a>Efecto de iluminación especular puntual

Use el efecto de iluminación especular de punto para crear una imagen que parece ser una superficie reflectante. El efecto usa el canal alfa de la imagen como un mapa de alto y una fuente de luz de punto que se coloca, y calcula la reflexión y la luz según la parte especular del modelo de iluminación Phong.

El color del mapa de bits de salida es el resultado del color claro, la posición de la luz y la geometría de la superficie. La salida del canal alfa para cada píxel con iluminación especular es el máximo de las salidas de canales rojo, verde y azul para ese píxel.

El CLSID para este efecto es CLSID \_ D2D1PointSpecular.

-   [Imagen de ejemplo](#example-image)
-   [Fuente de luz de punto](#point-light-source)
-   [Mapa de alto y vector normal](#height-map-and-normal-vector)
-   [Constante de iluminación especular y exponente](#specular-lighting-constant-and-exponent)
-   [Propiedades de efecto](#effect-properties)
-   [Modos de escalado](#scales-modes)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de iluminación especular de punto.

![captura de pantalla de ejemplo de efecto que muestra las imágenes de entrada y salida del efecto de iluminación especular de punto.](images/point-spec-example.png)

La luz especular hace referencia a la luz que se refleja en una dirección específica según el modelo de iluminación Phong.

![diagrama de los vectores usados para generar una salida de iluminación especular para un mapa de bits.](images/point-spec-reflected1.png)

El efecto calcula los valores finales de píxeles de salida mediante las ecuaciones siguientes:

![ecuaciones para calcular los valores de píxel final. ](images/point-spec-formula-output.png)

where<dl> ¿K? = constante de iluminación especular.  
![símbolo de vector de unidad normal de superficie. ](images/point-spec-mathchar-n.png) = vector de unidad normal de superficie que es una función de x e y. Consulte [Mapa de alto y vector normal](#height-map-and-normal-vector) para los cálculos.  
![símbolo vectorial de la unidad a medio camino. ](images/point-spec-mathchar-h.png) = vector de unidad "a medio camino" entre el vector de unidad de ojo y el vector de unidad de luz. Consulte [Point light source (Origen de](#point-light-source) luz de punto) para ver los cálculos.  
L<sub>r</sub>, L<sub>g</sub>, L<sub>b</sub> = el color claro en los componentes RGB.  
</dl>

Establezca la constante de iluminación especular como la *propiedad SpecularConstant* y el color claro como *la propiedad Color.*

## <a name="point-light-source"></a>Fuente de luz de punto

Una fuente de luz de punto emite luz en todas las direcciones, como en la imagen aquí.

![una luz de punto que emite luz en todas las direcciones.](images/point-spec-light.png)

La posición del origen de luz se establece mediante la *propiedad LightPosition.* El efecto calcula el vector de luz, L , para una fuente de luz de punto mediante las ecuaciones siguientes:

![la ecuación de vector claro.](images/point-spec-formula3.png)

donde Light?, Light<sub>y</sub>y Light<sub>z</sub> son la posición de la luz de entrada. El efecto calcula el vector medio, símbolo ![ de vector medio.](images/point-spec-mathchar-h.png) tal como se define en el modelo de iluminación de Phong, usando la ecuación aquí. El modelo de iluminación supone que el vector de los ojos, el símbolo de vector de ojo ![ , se encuentra en ](images/point-spec-mathchar-e.png) (0,0,1).

![ecuación de vector medio.](images/point-spec-formula4.png)

Tanto L como H se normalizan en vectores de longitud unitaria.

## <a name="height-map-and-normal-vector"></a>Mapa de alto y vector normal

El efecto genera un mapa de alto para la imagen de entrada en función de su canal alfa.

El componente de alto (Z) se calcula mediante la ecuación:

![ecuación para calcular el alto (z) de la superficie.](images/point-spec-formula6.png)

El efecto calcula la superficie normal, ![símbolo de vector normal.](images/point-spec-mathchar-n.png), para el mapa de bits de entrada mediante un degradado Sobel.

## <a name="specular-lighting-constant-and-exponent"></a>Constante de iluminación especular y exponente

La luz especular representa la luz que se refleja desde la superficie del mapa de alto de la imagen. Especifique la propiedad *SpecularExponent* que determina la cantidad de reflexión especular del mapa de bits.

Los exponentes más grandes representan objetos más grandes y reflejan la luz en una forma más centrada.

¿La *propiedad SpecularConstant* K? define la cantidad de luz reflejada como una proporción de la luz entrante.

## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ LIGHT \_ POSITION<br/>         | Posición de la luz del origen de luz de punto. La propiedad es un VECTOR 3F D2D1 \_ \_ definido como (x, y, z). Las unidades están en píxeles independientes del dispositivo (DIP) y los valores son sin unidad y sin enlazar. El tipo es D2D1 \_ VECTOR \_ 3F.<br/> El valor predeterminado es {0.0f, 0.0f, 0.0f}.<br/>                                                                                                                                                                                      |
| SpecularExponent<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ SPECULAR \_ EXPONENT<br/>   | Exponente del término especular en la ecuación de iluminación de Phong. Un valor mayor corresponde a una superficie más reflectante. Este valor no tiene unidad y debe estar entre 1,0 y 128. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                               |
| SpecularConstant<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ SPECULAR \_ CONSTANT<br/>   | Proporción de reflexión especular con la luz entrante. El valor no tiene unidad y debe estar entre 0 y 10 000. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                                   |
| SurfaceScale<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ SURFACE \_ SCALE<br/>           | Factor de escala en la dirección Z para generar un mapa de alto. El valor no tiene unidad y debe estar entre 0 y 10 000. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ COLOR<br/>                           | Color de la luz entrante. Esta propiedad se expone como D2D1 \_ VECTOR \_ 3F (R, G, B) y<sub></sub>se usa para calcular L<sub>R,</sub>L<sub>G,</sub>L B . El tipo es D2D1 \_ VECTOR \_ 3F.<br/> El valor predeterminado es {1.0f, 1.0f, 1.0f}.<br/>                                                                                                                                                                                                                             |
| KernelUnitLength<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ KERNEL \_ UNIT \_ LENGTH<br/> | Tamaño de un elemento en el kernel de Sobel que se usa para generar la superficie normal en las direcciones X e Y. Esta propiedad se asigna a los valores dx y dy en el degradado sobel. Esta propiedad es D2D1 \_ VECTOR \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) y se define en (DIP/Unidad de kernel). El efecto usa la interpolación bilineal para escalar el mapa de bits para que coincida con el tamaño de los elementos del kernel. El tipo es D2D1 \_ VECTOR \_ 2F.<br/> El valor predeterminado es {1.0f, 1.0f}.<br/> |
| Scalemode<br/> D2D1 \_ POINTSPECULAR \_ PROP \_ SCALE \_ MODE<br/>                 | Modo de interpolación que el efecto usa para escalar la imagen a la longitud de unidad de kernel correspondiente. Hay seis modos de escala que varían en calidad y velocidad. Consulte [Modos de escalado](#scales-modes) para obtener más información. <br/> El tipo es D2D1 \_ POINTSPECULAR \_ SCALE \_ MODE.<br/> El valor predeterminado es D2D1 \_ POINTSPECULAR \_ SCALE \_ MODE \_ LINEAR.<br/>                                                                                                                          |



 

## <a name="scales-modes"></a>Modos de escalado



| Enumeración                                             | Descripción                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ POINTSPECULAR \_ SCALE \_ MODE \_ NEAREST \_ NEIGHBOR     | Muestrea el punto único más cercano y lo usa. Este modo usa menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| D2D1 \_ POINTSPECULAR \_ SCALE \_ MODE \_ LINEAR                | Usa una muestra de cuatro puntos e interpolación lineal. Este modo genera una imagen de mayor calidad que el vecino más próximo.                                                                                   |
| D2D1 \_ POINTSPECULAR \_ SCALE \_ MODE \_ CUBIC                 | Usa un kernel cúbica de 16 muestras para la interpolación. Este modo usa el mayor tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ POINTSPECULAR \_ SCALE \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 muestras lineales dentro de un solo píxel para un buen suavizado de alias perimetral. Este modo es bueno para reducir verticalmente en pequeñas cantidades en imágenes con pocos píxeles.                                              |
| D2D1 \_ POINTSPECULAR \_ SCALE \_ MODE \_ ANISOTROPIC           | Usa el filtrado anisotropico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ POINTSPECULAR \_ SCALE \_ MODE \_ HIGH \_ QUALITY \_ CUBIC  | Usa un kernel cúbica de alta calidad de tamaño variable para realizar una escala previa a la baja de la imagen si la escalación está implicada en la matriz de transformación. A continuación, usa el modo de interpolación cúbica para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el valor predeterminado del efecto es D2D1 \_ POINTSPECULAR \_ SCALE \_ MODE \_ LINEAR.

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

 


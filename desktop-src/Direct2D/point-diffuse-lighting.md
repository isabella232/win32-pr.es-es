---
title: Efecto de iluminación difusa puntual
description: Use el efecto de iluminación difuso de punto para crear una imagen que parece ser una superficie no reflectante con luz dispersa en todas las direcciones. Este efecto usa el canal alfa como mapa de alto y enciende la imagen con una fuente de luz de punto.
ms.assetid: C98A4962-B9EB-4095-9AC4-F1C32C574892
keywords:
- efecto de iluminación difusa de punto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de97edfa6c2166d5c29649aabfe97761440f8f18
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162653"
---
# <a name="point-diffuse-lighting-effect"></a>Efecto de iluminación difusa puntual

Use el efecto de iluminación difuso de punto para crear una imagen que parece ser una superficie no reflectante con luz dispersa en todas las direcciones. Este efecto usa el canal alfa como mapa de alto y enciende la imagen con una fuente de luz de punto.

El color del mapa de bits de salida es el resultado del color claro, la posición de la luz y la geometría de la superficie. La salida del canal alfa para cada píxel con iluminación difusa siempre es 1,0.

El CLSID para este efecto es CLSID \_ D2D1PointDiffuse. Para usar este efecto, agregue dxguid.lib a las dependencias del vinculador.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Modos de escalado](#scale-modes)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de iluminación difuso de punto.

![Captura de pantalla de ejemplo de efecto que muestra las imágenes de entrada y salida del efecto de iluminación difuso de punto.](images/point-diffuse-example.png)

La iluminación difusa hace referencia a la luz que se refleja en varias direcciones, como se muestra aquí.

![la luz de iluminación difusa se dispersa en todas las direcciones.](images/point-diffuse-lighting.png)

El efecto calcula que los valores de píxel de salida finales se calculan mediante estas ecuaciones:

![cálculos de mapa de bits de salida.](images/point-diffuse-formula1.png)

Donde:<dl> k<sub>d</sub> = constante de iluminación difusa. Especificado por el usuario.  
![símbolo de vector normal de superficie.](images/point-spec-mathchar-n.png) = vector de unidad normal de superficie, una función de x e y.  
![símbolo de vector de unidad.](images/distant-spec-mathchar-l.png) = vector de unidad que apunta desde la superficie a la luz.  
L<sub>r</sub>, L<sub>g</sub>, L<sub>b</sub> = color claro en componentes RGB.  
</dl>

## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> D2D1 \_ POINTDIFFUSE \_ PROP \_ LIGHT \_ POSITION<br/>         | Posición de la luz del origen de luz de punto. La propiedad es un vector D2D1 \_ \_ 3F definido como (x, y, z). Las unidades están en píxeles independientes del dispositivo (DIP) y están sin enlazar. <br/> El tipo es D2D1 \_ VECTOR \_ 3F.<br/> El valor predeterminado es {0.0f, 0.0f, 0.0f}.<br/>                                                                                                                                                                                                              |
| DiffuseConstant<br/> D2D1 \_ POINTDIFFUSE \_ PROP \_ DIFUSO \_ CONSTANTE<br/>     | Proporción de reflexión difusa con la cantidad de luz entrante. Esta propiedad debe estar entre 0 y 10 000 y no tiene unidad. <br/> El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                          |
| SurfaceScale<br/> D2D1 \_ POINTDIFFUSE \_ PROP \_ SURFACE \_ SCALE<br/>           | Factor de escala en la dirección Z. La escala de la superficie no tiene unidad y debe estar entre 0 y 10 000.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                                               |
| Color<br/> D2D1 \_ POINTDIFFUSE \_ PROP \_ COLOR<br/>                           | Color de la luz entrante. Esta propiedad se expone como vector 3 (R, G, B) y se usa para calcular L<sub>R</sub>, L<sub>G</sub>, L<sub>B</sub>. <br/> El tipo es D2D1 \_ VECTOR \_ 3F.<br/> El valor predeterminado es {1.0f, 1.0f, 1.0f}.<br/>                                                                                                                                                                                                                                     |
| KernelUnitLength<br/> D2D1 \_ POINTDIFFUSE \_ PROP \_ KERNEL \_ UNIT \_ LENGTH<br/> | Tamaño de un elemento en el kernel de Sobel que se usa para generar la superficie normal en la dirección X e Y. Esta propiedad se asigna a los valores dx y dy en el degradado sobel. Esta propiedad es D2D1 \_ VECTOR \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) y se define en (DIP/Unidad de kernel). El efecto usa la interpolación bilineal para escalar el mapa de bits para que coincida con el tamaño de los elementos del kernel. <br/> El tipo es D2D1 \_ VECTOR \_ 2F.<br/> El valor predeterminado es {1.0f, 1.0f}.<br/> |
| Scalemode<br/> D2D1 \_ POINTDIFFUSE \_ PROP \_ SCALE \_ MODE<br/>                 | Modo de interpolación que el efecto usa para escalar la imagen a la longitud de unidad de kernel correspondiente. Hay seis modos de escala que varían en calidad y velocidad. Consulte [Modos de escalado](#scale-modes) para obtener más información. <br/> El tipo es D2D1 \_ POINTDIFFUSE \_ SCALE \_ MODE.<br/> El valor predeterminado es D2D1 \_ POINTDIFFUSE \_ SCALE \_ MODE \_ LINEAR.<br/>                                                                                                                                         |



 

## <a name="scale-modes"></a>Modos de escalado



| Enumeración                                            | Descripción                                                                                                                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ POINTDIFFUSE \_ SCALE \_ MODE \_ NEAREST \_ NEIGHBOR     | Muestrea el punto más cercano y lo usa. Este modo usa menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| D2D1 \_ POINTDIFFUSE \_ SCALE \_ MODE \_ LINEAR                | Usa una muestra de cuatro puntos y una interpolación lineal. Este modo genera una imagen de mayor calidad que el vecino más próximo.                                                                                   |
| D2D1 \_ POINTDIFFUSE \_ SCALE \_ MODE \_ CUBIC                 | Usa un kernel cúbica de 16 muestras para la interpolación. Este modo usa el mayor tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ POINTDIFFUSE \_ SCALE \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 muestras lineales dentro de un solo píxel para un suavizado de alias de borde bueno. Este modo es bueno para reducir verticalmente en pequeñas cantidades en imágenes con pocos píxeles.                                              |
| D2D1 \_ POINTDIFFUSE \_ SCALE \_ MODE \_ ANISOTROPIC           | Usa el filtrado anisotropico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ POINTDIFFUSE \_ SCALE \_ MODE \_ HIGH \_ QUALITY \_ CUBIC  | Usa un kernel cúbica de alta calidad de tamaño variable para realizar una escala previa a la baja de la imagen si la escala hacia abajo está implicada en la matriz de transformación. A continuación, usa el modo de interpolación cúbica para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el efecto tiene como valor predeterminado D2D1 \_ POINTDIFFUSE \_ SCALE \_ MODE \_ LINEAR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio \| Windows store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio Windows aplicaciones de la \| Tienda\] |
| Encabezado                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


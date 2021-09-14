---
title: Efecto de escala
description: Use este efecto para escalar o reducir verticalmente una imagen. El efecto tiene seis modos de escalado vecino más cercano, lineal, cúbico, lineal de varias muestras, anisotropo y cúbico de alta calidad.
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- efecto de escala
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db3a4ef93fcdd2e93580157e0bb73b172975fe4a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163234"
---
# <a name="scale-effect"></a>Efecto de escala

Use este efecto para escalar o reducir verticalmente una imagen. El efecto tiene seis modos de escalado: vecino más próximo, lineal, cúbico, lineal de varias muestras, anisotropico y cúbico de alta calidad.

El CLSID para este efecto es CLSID \_ D2D1Scale.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
    -   [Modos de borde](#border-modes)
-   [Modos de interpolación](#interpolation-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En este ejemplo se muestra el efecto de escala zooming in 2 times the input and cropping to the original size (Acercar el efecto de escala en 2 veces la entrada y recortar al tamaño original).



| Antes                                                     |
|------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg) |
| Después                                                      |
| ![la imagen después de la transformación.](images/22-scale.png)     |



 


```C++
ComPtr<ID2D1Effect> scaleEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Scale, &scaleEffect);

scaleEffect->SetInput(0, bitmap);

scaleEffect->SetValue(D2D1_SCALE_PROP_CENTER_POINT, D2D1::Vector2F(256.0f, 192.0f));
scaleEffect->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(2.0f, 2.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(scaleEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propiedades de efecto




| Enumeración de nombre para mostrar e índice | Descripción | 
|------------------------------------|-------------|
| Escala<br /> D2D1_SCALE_PROP_SCALE<br /> | La cantidad de escala en la dirección X e Y como proporción del tamaño de salida con respecto al tamaño de entrada. Esta propiedad es D2D1_VECTOR_2Fdefined como: (escala X, escala Y). Las cantidades de escala son FLOAT, sin unidad y deben ser positivas o 0.<br /> El tipo es D2D1_VECTOR_2F.<br /> El valor predeterminado es {1.0f, 1.0f}.<br /> | 
| CenterPoint<br /> D2D1_SCALE_PROP_CENTER_POINT<br /> | Punto central de escalado de imágenes. Esta propiedad es una D2D1_VECTOR_2F definida como: (punto X, punto Y). Las unidades están en DIP.<br /> Use la propiedad de punto central para escalar alrededor de un punto distinto de la esquina superior izquierda.<br /> El tipo es D2D1_VECTOR_2F.<br /> El valor predeterminado es {0.0f, 0.0f}.<br /> | 
| BorderMode<br /> D2D1_SCALE_PROP_BORDER_MODE<br /> | Modo que se usa para calcular el borde de la imagen, de forma flexible o dura. Consulte <a href="#border-modes">Modos de borde</a> para obtener más información. <br /> El tipo es D2D1_BORDER_MODE.<br /> El valor predeterminado es D2D1_BORDER_MODE_SOFT.<br /> | 
| Nitidez<br /> D2D1_SCALE_PROP_SHARPNESS<br /> | En el modo de interpolación cúbica de alta calidad, el nivel de ni sharpness del filtro de escalado como un valor float entre 0 y 1. Los valores no tienen unidad. Puede usar la niguidad para ajustar la calidad de una imagen al reducir verticalmente la imagen.<br /> El factor de niguidad afecta a la forma del kernel. Cuanto mayor sea el factor de nifilidad, menor será el kernel.<br /><blockquote>[!Note]<br />Esta propiedad solo afecta al modo de interpolación cúbica de alta calidad.</blockquote><br /> El tipo es FLOAT.<br /> El valor predeterminado es 0,0f.<br /> | 
| InterpolationMode<br /> D2D1_SCALE_PROP_INTERPOLATION_MODE<br /> | Modo de interpolación que el efecto usa para escalar la imagen. Hay 6 modos de escala que varían en calidad y velocidad. Consulte <a href="#interpolation-modes">Modos de interpolación</a> para obtener más información. <br /> El tipo es D2D1_SCALE_INTERPOLATION_MODE.<br /> El valor predeterminado es D2D1_SCALE_INTERPOLATION_MODE_LINEAR.<br /> | 




 

### <a name="border-modes"></a>Modos de borde



| Nombre                     | Descripción                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODO DE BORDE D2D1 \_ \_ \_ SOFT | El efecto aplica un panel a la imagen de entrada con píxeles negros transparentes para las muestras fuera de los límites de entrada cuando se aplica el kernel de convolución. Esto crea un borde flexible para la imagen y, en el proceso, expande el mapa de bits de salida según el tamaño del kernel.<br/> |
| D2D1 \_ BORDER \_ MODE \_ HARD | El efecto extiende la imagen de entrada con una transformación de borde de tipo reflejo para muestras fuera de los límites de entrada. El tamaño del mapa de bits de salida es igual al tamaño del mapa de bits de entrada.<br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a>Modos de interpolación



| Enumeración                                             | Descripción                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ SCALE \_ INTERPOLATION \_ MODE \_ NEAREST \_ NEIGHBOR     | Muestrea el punto más cercano y lo usa. Este modo usa menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| MODO DE INTERPOLACIÓN DE ESCALA D2D1 \_ \_ \_ \_ LINEAL                | Usa una muestra de cuatro puntos y una interpolación lineal. Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad.                                           |
| MODO DE INTERPOLACIÓN DE ESCALA D2D1 \_ \_ \_ \_ CÚBICA                 | Usa un kernel cúbica de 16 muestras para la interpolación. Este modo usa el mayor tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| MODO DE INTERPOLACIÓN DE ESCALA D2D1 \_ \_ MULTI SAMPLE \_ \_ \_ \_ LINEAR | Usa 4 muestras lineales dentro de un solo píxel para un suavizado de alias de borde bueno. Este modo es bueno para reducir verticalmente en pequeñas cantidades en imágenes con pocos píxeles.                                              |
| MODO DE INTERPOLACIÓN DE ESCALA D2D1 \_ \_ \_ \_ ANISOTROPIC           | Usa el filtrado anisotropico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| MODO DE INTERPOLACIÓN DE ESCALA D2D1 \_ \_ \_ \_ \_ CÚBICA DE ALTA \_ CALIDAD  | Usa un kernel cúbica de alta calidad de tamaño variable para realizar una escala previa a la baja de la imagen si la escala hacia abajo está implicada en la matriz de transformación. A continuación, usa el modo de interpolación cúbica para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el efecto tiene como valor predeterminado D2D1 \_ SCALE \_ INTERPOLATION MODE LINEAR (LINEAL DEL MODO DE INTERPOLACIÓN \_ DE ESCALA \_ D2D1).

 

> [!Note]  
> El modo anisotropico genera mapas MIP al escalar; sin embargo, si establece la propiedad **Cached** en true en los efectos que se introducen en este efecto, los mapas MIP no se generarán cada vez para imágenes lo suficientemente pequeñas.

 

## <a name="output-bitmap"></a>Mapa de bits de salida

La ubicación y el tamaño del mapa de bits de salida dependen del factor de escala especificado y del punto central.

Puede calcular el tamaño del mapa de bits de salida mediante esta ecuación:<dl> BitmapSize? (Píxeles)=¿Escala? \* ¿Tamaño de mapa de bits original? (DIP) \* (UserDPI/96)  
BitmapSize<sub>y</sub>(píxeles)=Escala<sub>y tamaño de</sub>mapa de bits original \* <sub>y</sub> (DIP) \* (UserDPI/96)  
</dl>

El efecto redondea fracciones de píxeles hasta el píxel entero más cercano.

La ubicación del mapa de bits es (0, 0) o el valor de la propiedad de punto central.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio Windows aplicaciones de la \| Tienda\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio Windows aplicaciones de la \| Tienda\] |
| Encabezado                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


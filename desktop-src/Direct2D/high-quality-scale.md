---
title: Efecto de escala
description: Utilice este efecto para escalar o reducir verticalmente una imagen. El efecto tiene seis modos de escalado más cercanos, lineal, cúbico, Multimuestra lineal, anisotrópico y de alta calidad cúbicos.
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- efecto de escala
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3af77bc24db387fff0854e0432c270fa2ce6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422231"
---
# <a name="scale-effect"></a>Efecto de escala

Utilice este efecto para escalar o reducir verticalmente una imagen. El efecto tiene seis modos de escala: vecino más cercano, lineal, cúbico, Multimuestra lineal, anisotrópico y de alta calidad cúbico.

El CLSID para este efecto es CLSID \_ D2D1Scale.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
    -   [Modos de borde](#border-modes)
-   [Modos de interpolación](#interpolation-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En este ejemplo se muestra el efecto de escala de zoom en 2 veces la entrada y recortada al tamaño original.



| Antes                                                     |
|------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg) |
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



## <a name="effect-properties"></a>Propiedades del efecto



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Enumeración de índice y nombre para mostrar</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Escala<br/> D2D1_SCALE_PROP_SCALE<br/></td>
<td>La cantidad de escala en la dirección X e y como una relación entre el tamaño de salida y el tamaño de entrada. Esta propiedad es D2D1_VECTOR_2Fdefined: (escala X, escala Y). Las cantidades de escala son FLOAT, sin unidades y deben ser positivas o 0.<br/> El tipo es D2D1_VECTOR_2F.<br/> El valor predeterminado es {1.0 f, 1.0 f}.<br/></td>
</tr>
<tr class="even">
<td>CenterPoint<br/> D2D1_SCALE_PROP_CENTER_POINT<br/></td>
<td>Punto central de escalado de imagen. Esta propiedad es una D2D1_VECTOR_2F definida como: (punto X, punto Y). Las unidades están en DIP.<br/> Use la propiedad punto central para escalar alrededor de un punto que no sea la esquina superior izquierda.<br/> El tipo es D2D1_VECTOR_2F.<br/> El valor predeterminado es {0.0 f, 0.0 f}.<br/></td>
</tr>
<tr class="odd">
<td>BorderMode<br/> D2D1_SCALE_PROP_BORDER_MODE<br/></td>
<td>El modo que se usa para calcular el borde de la imagen, es decir, es flexible o difícil. Vea <a href="#border-modes">modos de borde</a> para obtener más información. <br/> El tipo es D2D1_BORDER_MODE.<br/> El valor predeterminado es D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="even">
<td>Nitidez<br/> D2D1_SCALE_PROP_SHARPNESS<br/></td>
<td>En el modo de interpolación cúbico de alta calidad, el nivel de nitidez del filtro de escalado es un valor de tipo float entre 0 y 1. Los valores son no unitarias. Puede usar la nitidez para ajustar la calidad de una imagen al reducir la escala de la imagen.<br/> El factor de nitidez afecta a la forma del kernel. Cuanto mayor sea el factor de nitidez, menor será el kernel.<br/>
<blockquote>
[!Note]<br />
Esta propiedad solo afecta al modo de interpolación cúbico de alta calidad.
</blockquote>
<br/> El tipo es FLOAT.<br/> El valor predeterminado es 0.0 f.<br/></td>
</tr>
<tr class="odd">
<td>InterpolationMode<br/> D2D1_SCALE_PROP_INTERPOLATION_MODE<br/></td>
<td>El modo de interpolación que el efecto usa para escalar la imagen. Hay 6 modos de escala que abarcan la calidad y la velocidad. Vea <a href="#interpolation-modes">modos de interpolación</a> para obtener más información. <br/> El tipo es D2D1_SCALE_INTERPOLATION_MODE.<br/> El valor predeterminado es D2D1_SCALE_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="border-modes"></a>Modos de borde



| Nombre                     | Descripción                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ modo de borde \_ \_ flexible | El efecto rellena la imagen de entrada con píxeles negros transparentes para muestras fuera de los límites de entrada cuando aplica el kernel de circunvolución. Esto crea un borde flexible para la imagen y, en el proceso, expande el mapa de bits de salida por el tamaño del kernel.<br/> |
| D2D1 \_ del \_ modo de borde \_ | El efecto extiende la imagen de entrada con una transformación de borde de tipo de reflejo para las muestras fuera de los límites de entrada. El tamaño del mapa de bits de salida es igual al tamaño del mapa de bits de entrada.<br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a>Modos de interpolación



| Enumeración                                             | Descripción                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ modo de interpolación de escala de la \_ \_ \_ proximidad más cercano \_     | Muestrea el punto único más cercano y lo usa. Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| \_ \_ \_ Modo lineal de interpolación de escala D2D1 \_                | Utiliza un ejemplo de cuatro puntos y una interpolación lineal. Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad.                                           |
| \_Modo de \_ interpolación de escala D2D1 \_ \_ cúbico                 | Usa un kernel cúbico de ejemplo 16 para la interpolación. Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| \_Modo de \_ interpolación de escala D2D1 \_ \_ \_ Multimuestra \_ lineal | Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado. Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.                                              |
| \_Modo de \_ interpolación de escala D2D1 \_ \_ anisotrópico           | Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ modo de interpolación de escala de \_ \_ \_ alta \_ calidad \_ cúbico  | Usa un kernel cúbico de alta calidad de tamaño variable para realizar una downscale previa de la imagen si downscaling está implicado en la matriz de transformación. A continuación, usa el modo de interpolación cúbico para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el efecto tiene como valor predeterminado el \_ modo de interpolación de escala D2D1 \_ \_ \_ lineal.

 

> [!Note]  
> El modo anisotrópico genera mapas MIP al escalar; sin embargo, si establece la propiedad **Cached** en true en los efectos que se aplican a este efecto, no se generarán los mapas MIP cada vez para imágenes suficientemente pequeñas.

 

## <a name="output-bitmap"></a>Mapa de bits de salida

La ubicación y el tamaño del mapa de bits de salida dependen del factor de escala especificado y del punto central.

Puede calcular el tamaño del mapa de bits de salida con esta ecuación:<dl> BitmapSize? (Píxeles) = escala \* ¿Tamaño del mapa de bits original? (DIP) \* (UserDPI/96)  
BitmapSize<sub>y</sub>(píxeles) =<sub></sub> \* tamaño del mapa de bits original<sub>y</sub> (DIP) \* (UserDPI/96)  
</dl>

El efecto redondea las fracciones de píxeles hasta el píxel entero más próximo.

La ubicación del mapa de bits es (0,0) o el valor de la propiedad de punto central.

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

 


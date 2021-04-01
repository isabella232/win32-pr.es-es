---
title: Efecto de transformación afín 2D
description: El efecto de transformación afín 2D aplica una transformación espacial a una imagen basada en una matriz de 3X2 mediante la transformación de matriz de Direct2D y cualquiera de los seis modos de interpolación.
ms.assetid: E8973EBE-764C-4220-BB1E-3BFD4853582D
keywords:
- Efecto de transformación afín 2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3017992d34cd98095f01192ea948684a6b52e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151247"
---
# <a name="2d-affine-transform-effect"></a>Efecto de transformación afín 2D

El efecto de transformación afín 2D aplica una transformación espacial a una imagen basada en una matriz de 3X2 mediante la [transformación](direct2d-transforms-overview.md) de matriz de Direct2D y cualquiera de los seis modos de interpolación. Puede usar este efecto para girar, escalar, sesgar o traducir una imagen. O bien, puede combinar estas operaciones. Las transferencias afines conservan las líneas paralelas y la proporción de distancias entre los tres puntos de una imagen.

El CLSID para este efecto es CLSID \_ D2D12DAffineTransform.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Modos de borde](#border-modes)
-   [Modos de interpolación](#interpolation-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                             |
|--------------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)         |
| Después                                                              |
| ![la imagen después de la transformación.](images/21-2daffinetransform.png) |



 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInput(0, bitmap);

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,   0.1f, 0.9f,   8.0f, 45.0f);

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



Este efecto realiza esta operación matricial:

![operación de matriz afín](images/affine-matrix-calculation.png)

Aunque la matriz de entrada se define como una matriz 3x2, la última columna se rellena con 0, 0 y 1 para generar una matriz cuadrada. Esto permite la multiplicación de matrices, por lo que las transformaciones se pueden concatenar en una sola matriz.

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
<td>InterpolationMode<br/> D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE<br/></td>
<td>El modo de interpolación usado para escalar la imagen. Hay 6 modos de escala que abarcan la calidad y la velocidad.<br/> El tipo es D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.<br/> El valor predeterminado es D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
<tr class="even">
<td>BorderMode<br/> D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE<br/></td>
<td>El modo que se usa para calcular el borde de la imagen, es decir, es flexible o difícil. Vea <a href="https://www.bing.com/search?q=Border+modes">modos de borde</a> para obtener más información. <br/> El tipo es D2D1_BORDER_MODE.<br/> El valor predeterminado es D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="odd">
<td>TransformMatrix<br/> D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX<br/></td>
<td>Matriz de 3x2 que se va a usar para transformar la imagen mediante la <a href="direct2d-transforms-overview.md">transformación</a>de matriz de Direct2D. <br/> El tipo es D2D1_MATRIX_3X2_F.<br/> El valor predeterminado es Matrix3x2F:: Identity ().<br/></td>
</tr>
<tr class="even">
<td>Nitidez<br/> D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS<br/></td>
<td>En el modo de interpolación cúbico de alta calidad, el nivel de nitidez del filtro de escalado es un valor de tipo float entre 0 y 1. Los valores son no unitarias. Puede usar la nitidez para ajustar la calidad de una imagen al escalar la imagen.<br/> El factor de nitidez afecta a la forma del kernel. Cuanto mayor sea el factor de nitidez, menor será el kernel. <br/>
<blockquote>
[!Note]<br />
Esta propiedad solo afecta al modo de interpolación cúbico de alta calidad.
</blockquote>
<br/> El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="border-modes"></a>Modos de borde



| Nombre                     | Descripción                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ modo de borde \_ \_ flexible | El efecto rellena la imagen con píxeles negros transparentes mientras se interpola, lo que da lugar a un borde flexible.<br/> |
| D2D1 \_ del \_ modo de borde \_ | El efecto fija la salida al tamaño de la imagen de entrada. <br/>                                         |



 

## <a name="interpolation-modes"></a>Modos de interpolación



| Enumeración                                                         | Descripción                                                                                                                                                                                          |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ el \_ modo de interpolación 2DAFFINETRANSFORM \_ \_ más cercano \_     | Muestrea el punto único más cercano y lo usa. Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| D2D1 \_ \_ modo de interpolación 2DAFFINETRANSFORM \_ \_ lineal                | Utiliza un ejemplo de cuatro puntos y una interpolación lineal. Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad.                                           |
| D2D1 \_ \_ modo de interpolación 2DAFFINETRANSFORM \_ \_ cúbico                 | Usa un kernel cúbico de ejemplo 16 para la interpolación. Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ 2DAFFINETRANSFORM \_ modo de interpolación \_ \_ lineal de varios \_ ejemplos \_ | Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado. Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.                                              |
| D2D1 \_ \_ modo de interpolación 2DAFFINETRANSFORM \_ \_ anisotrópico           | Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ 2DAFFINETRANSFORM \_ modo de interpolación de \_ \_ alta \_ calidad \_ cúbico  | Usa un kernel cúbico de alta calidad de tamaño variable para realizar una downscale previa de la imagen si downscaling está implicado en la matriz de transformación. A continuación, usa el modo de interpolación cúbico para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el efecto tiene como valor predeterminado el \_ \_ modo de interpolación D2D1 2DAFFINETRANSFORM \_ \_ lineal.

 

> [!Note]  
> El modo anisotrópico genera mapas MIP al escalar; sin embargo, si establece la propiedad **Cached** en true en los efectos que se aplican a este efecto, no se generarán los mapas MIP cada vez para imágenes suficientemente pequeñas.

 

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del mapa de bits de salida depende de la matriz de transformación que se aplica a la imagen.

El efecto realiza la operación de transformación y, a continuación, aplica un cuadro de límite alrededor del resultado. El mapa de bits de salida es el tamaño del cuadro de límite.

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

 


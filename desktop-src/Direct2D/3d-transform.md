---
title: Efecto de transformación 3D
description: Utilice el efecto transformación 3D para aplicar una matriz de transformación 4x4 arbitraria a una imagen.
ms.assetid: BC2F2837-40F0-4293-A190-8B5F81BB01B6
keywords:
- efecto transformación 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabe0c2c220038802b5218b54187a1ff89268bfa
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104570407"
---
# <a name="3d-transform-effect"></a>Efecto de transformación 3D

Utilice el efecto transformación 3D para aplicar una matriz de transformación 4x4 arbitraria a una imagen.

Este efecto aplica la matriz (M?) que se proporciona a los vértices de esquina de la imagen de origen ( \[ x y z 1 \] ) mediante este cálculo:

\[x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \] = \[ x y z 1 \] \* M?

El CLSID para este efecto es CLSID \_ D2D13DTransform.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
    -   [Modos de interpolación](#interpolation-modes)
    -   [Modos de borde](#border-modes)
-   [4x4 Transform Matrix (clase)](#4x4-transform-matrix-class)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                        |
|---------------------------------------------------------------|
| ![la imagen antes de la transformación.](images/default-before.jpg) |
| Después                                                         |
| ![la imagen después de la transformación.](images/24-3dtransform.png)  |



 


```C++
ComPtr<ID2D1Effect> D2D13DTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DTransform, &D2D13DTransformEffect);

D2D13DTransformEffect->SetInput(0, bitmap);

// You can use the helper methods in D2D1::Matrix4x4F to create common matrix transformations.
D2D1_MATRIX_4X4_F matrix = 
    D2D1::Matrix4x4F::Translation(0.0f, -192.0f, 0.0f) *
    D2D1::Matrix4x4F::RotationY(30.0f) *
    D2D1::Matrix4x4F::Translation(0.0f, 192.0f, 0.0f);

D2D13DTransformEffect->SetValue(D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(D2D13DTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propiedades del efecto



<table>
<thead>
<tr class="header">
<th>Enumeración de índice y nombre para mostrar</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>InterpolationMode<br/> D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE<br/></td>
<td>El modo de interpolación que el efecto usa en la imagen. Hay 5 modos de escala que abarcan la calidad y la velocidad.<br/> El tipo es D2D1_3DTRANSFORM_INTERPOLATION_MODE.<br/> El valor predeterminado es D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
<tr class="even">
<td>BorderMode<br/> D2D1_3DTRANSFORM_PROP_BORDER_MODE<br/></td>
<td>El modo que se usa para calcular el borde de la imagen, es decir, es flexible o difícil. Vea <a href="https://www.bing.com/search?q=Border+modes">modos de borde</a> para obtener más información.<br/> El tipo es D2D1_BORDER_MODE.<br/> El valor predeterminado es D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="odd">
<td>TransformMatrix<br/> D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX<br/></td>
<td>Matriz de transformación 4x4 aplicada al plano de proyección. El siguiente cálculo de matriz se utiliza para asignar puntos de un sistema de coordenadas 3D al sistema de coordenadas 2D transformado. <br/><img src="images/3d-transform-matrix1.png" alt="3D Depth Matrix" />Donde:<dl> X, Y, Z = coordenadas del plano de proyección de entrada<br />
M<sub>x, y</sub> = transformar elementos de matriz<br />
X, Y, Z = coordenadas del plano de proyección de salida<br />
</dl> <br/> Los elementos individuales de la matriz no están limitados y no tienen unidades. <br/> El tipo es D2D1_MATRIX_4X4_F.<br/> El valor predeterminado es Matrix4x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1).<br/></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-modes"></a>Modos de interpolación



| Enumeración                                                   | Descripción                                                                                                                                                |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ el \_ modo de interpolación 3DTRANSFORM \_ \_ más cercano \_     | Muestrea el punto único más cercano y lo usa. Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                 |
| D2D1 \_ \_ modo de interpolación 3DTRANSFORM \_ \_ lineal                | Utiliza un ejemplo de cuatro puntos y una interpolación lineal. Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad. |
| D2D1 \_ \_ modo de interpolación 3DTRANSFORM \_ \_ cúbico                 | Usa un kernel cúbico de ejemplo 16 para la interpolación. Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.                              |
| D2D1 \_ 3DTRANSFORM \_ modo de interpolación \_ \_ lineal de varios \_ ejemplos \_ | Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado. Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.    |
| D2D1 \_ \_ modo de interpolación 3DTRANSFORM \_ \_ anisotrópico           | Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.                                                           |



 

> [!Note]  
> Si no selecciona un modo, el efecto tiene como valor predeterminado el \_ \_ modo de interpolación D2D1 3DTRANSFORM \_ \_ lineal.

 

> [!Note]  
> El modo anisotrópico genera mapas MIP al escalar; sin embargo, si establece la propiedad **Cached** en true en los efectos que se aplican a este efecto, no se generarán los mapas MIP cada vez para imágenes suficientemente pequeñas.

 

### <a name="border-modes"></a>Modos de borde



| Nombre                     | Descripción                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ modo de borde \_ \_ flexible | El efecto rellena la imagen con píxeles negros transparentes mientras se interpola, lo que da lugar a un borde flexible.<br/> |
| D2D1 \_ del \_ modo de borde \_ | El efecto fija la salida al tamaño de la imagen de entrada. <br/>                                         |



 

## <a name="4x4-transform-matrix-class"></a>4x4 Transform Matrix (clase)

Direct2D proporciona una clase de matriz 4x4 para proporcionar funciones auxiliares para transformar la imagen en tres dimensiones. Vea el tema [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) para obtener más información y una descripción de todos los miembros de clase.



| Función                                | Descripción                                                                                    | Matrix                                                 |
|-----------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Matrix4x4F:: Scale (X, Y, Z)              | Genera una matriz de transformación que escala el plano de proyección en la dirección X, y y/o Z. | ![matriz scale3d](images/3d-transform-matrix2.png)     |
| SkewX (X)                                | Genera una matriz de transformación que sesga el plano de proyección en la dirección X.               | ![Muestra una matriz de sesgo en la dirección X.](images/matrix4x4-skewx.png)             |
| Sesgado (Y)                                | Genera una matriz de transformación que sesga el plano de proyección en la dirección Y.               | ![matriz de sesgo](images/matrix4x4-skewy.png)             |
| Traducción (X, Y, Z)                    | Genera una matriz de transformación que convierte el plano de proyección en la dirección X, Y o Z. | ![convertir matriz](images/3d-transform-matrix4.png)   |
| RotationX (X)                            | Genera una matriz de transformación que gira el plano de proyección sobre el eje X.               | ![rotar matriz x](images/3d-transform-matrix5.png)    |
| Rotación (Y)                            | Genera una matriz de transformación que gira el plano de proyección sobre el eje Y.               | ![rotar matriz y](images/3d-transform-matrix6.png)    |
| RotationZ (Z)                            | Genera una matriz de transformación que gira el plano de proyección sobre el eje Z.               | ![rotar matriz z](images/3d-transform-matrix7.png)    |
| PerspectiveProjection (D)                | Transformación de perspectiva con un valor de profundidad de D.                                          | ![matriz de perspectiva](images/3d-transform-matrix8.png) |
| RotationArbitraryAxis (X, Y, Z, grados) | Gira el plano de proyección sobre el eje especificado.                                       |                                                        |



 

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

 


---
title: Efecto de transformación 3D
description: Use el efecto de transformación 3D para aplicar una matriz de transformación 4x4 arbitraria a una imagen.
ms.assetid: BC2F2837-40F0-4293-A190-8B5F81BB01B6
keywords:
- Efecto de transformación 3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabe0c2c220038802b5218b54187a1ff89268bfa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164262"
---
# <a name="3d-transform-effect"></a>Efecto de transformación 3D

Use el efecto de transformación 3D para aplicar una matriz de transformación 4x4 arbitraria a una imagen.

Este efecto aplica la matriz (M?) que se proporciona a los vértices de la esquina de la imagen de origen \[ (x y z 1) \] mediante este cálculo:

\[x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 x y \] = \[ z 1 \] \* M?

El CLSID para este efecto es CLSID \_ D2D13DTransform.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
    -   [Modos de interpolación](#interpolation-modes)
    -   [Modos de borde](#border-modes)
-   [Matriz de transformación 4x4 (clase)](#4x4-transform-matrix-class)
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



## <a name="effect-properties"></a>Propiedades de efecto



<table>
<thead>
<tr class="header">
<th>Enumeración de nombre para mostrar e índice</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>InterpolationMode<br/> D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE<br/></td>
<td>Modo de interpolación que el efecto usa en la imagen. Hay cinco modos de escala que varían en calidad y velocidad.<br/> El tipo es D2D1_3DTRANSFORM_INTERPOLATION_MODE.<br/> El valor predeterminado es D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
<tr class="even">
<td>BorderMode<br/> D2D1_3DTRANSFORM_PROP_BORDER_MODE<br/></td>
<td>Modo que se usa para calcular el borde de la imagen, de forma flexible o dura. Consulte <a href="https://www.bing.com/search?q=Border+modes">Modos de borde</a> para obtener más información.<br/> El tipo es D2D1_BORDER_MODE.<br/> El valor predeterminado es D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="odd">
<td>TransformMatrix<br/> D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX<br/></td>
<td>Matriz de transformación 4x4 aplicada al plano de proyección. El siguiente cálculo de matriz se usa para asignar puntos de un sistema de coordenadas 3D al sistema de coordenadas 2D transformado. <br/><img src="images/3d-transform-matrix1.png" alt="3D Depth Matrix" />Donde:<dl> X, Y, Z = Coordenadas del plano de proyección de entrada<br />
M<sub>x,y</sub> = Transformar elementos de matriz<br />
Coordenadas del plano de proyección de X, Y, Z =Salida<br />
</dl> <br/> Los elementos de matriz individuales no están enlazados y no tienen unidad. <br/> El tipo es D2D1_MATRIX_4X4_F.<br/> El valor predeterminado es Matrix4x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 1).<br/></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-modes"></a>Modos de interpolación



| Enumeración                                                   | Descripción                                                                                                                                                |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ MODO DE INTERPOLACIÓN 3DTRANSFORM \_ VECINO MÁS \_ \_ \_ CERCANO     | Muestrea el punto único más cercano y lo usa. Este modo usa menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                 |
| D2D1 \_ MODO DE INTERPOLACIÓN 3DTRANSFORM \_ \_ \_ LINEAL                | Usa una muestra de cuatro puntos e interpolación lineal. Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad. |
| D2D1 \_ 3DTRANSFORM \_ INTERPOLATION \_ MODE \_ CUBIC                 | Usa un kernel cúbica de 16 muestras para la interpolación. Este modo usa el mayor tiempo de procesamiento, pero genera una imagen de mayor calidad.                              |
| MODO DE \_ INTERPOLACIÓN 3DTRANSFORM D2D1 \_ \_ MULTI SAMPLE \_ \_ \_ LINEAR | Usa 4 muestras lineales dentro de un solo píxel para un buen suavizado de alias perimetral. Este modo es bueno para reducir verticalmente en pequeñas cantidades en imágenes con pocos píxeles.    |
| MODO DE \_ INTERPOLACIÓN D2D1 3DTRANSFORM \_ \_ \_ ANISOTROPIC           | Usa el filtrado anisotropico para muestrear un patrón según la forma transformada del mapa de bits.                                                           |



 

> [!Note]  
> Si no selecciona un modo, el efecto tiene como valor predeterminado D2D1 \_ 3DTRANSFORM \_ INTERPOLATION \_ MODE \_ LINEAR.

 

> [!Note]  
> El modo anisotropico genera mapas mipmap al escalar; sin embargo, si establece la propiedad **Cached** en true en los efectos que se introducen en este efecto, los mapas mipmap no se generarán cada vez para imágenes lo suficientemente pequeñas.

 

### <a name="border-modes"></a>Modos de borde



| Nombre                     | Descripción                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| MODO DE BORDE D2D1 \_ \_ \_ SOFT | El efecto abate la imagen con píxeles negros transparentes a medida que se interpola, lo que da lugar a un borde suave.<br/> |
| D2D1 \_ BORDER \_ MODE \_ HARD | El efecto fija la salida al tamaño de la imagen de entrada. <br/>                                         |



 

## <a name="4x4-transform-matrix-class"></a>Matriz de transformación 4x4 (clase)

Direct2D proporciona una clase de matriz 4x4 para proporcionar funciones auxiliares para transformar la imagen en 3 dimensiones. Consulte el [**tema Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) para obtener más información y una descripción de todos los miembros de clase.



| Función                                | Descripción                                                                                    | Matriz                                                 |
|-----------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Matrix4x4F::Scale(X, Y, Z)              | Genera una matriz de transformación que escala el plano de proyección en la dirección X, Y o Z. | ![Matriz scale3d](images/3d-transform-matrix2.png)     |
| SkewX(X)                                | Genera una matriz de transformación que sesga el plano de proyección en la dirección X.               | ![Muestra una matriz de sesgo en la dirección X.](images/matrix4x4-skewx.png)             |
| Skewy(Y)                                | Genera una matriz de transformación que sesga el plano de proyección en la dirección Y.               | ![Matriz de sesgo](images/matrix4x4-skewy.png)             |
| Translation(X, Y, Z)                    | Genera una matriz de transformación que convierte el plano de proyección en la dirección X, Y o Z. | ![traducir matriz](images/3d-transform-matrix4.png)   |
| RotationX(X)                            | Genera una matriz de transformación que gira el plano de proyección sobre el eje X.               | ![rotación de la matriz x](images/3d-transform-matrix5.png)    |
| RotationY(Y)                            | Genera una matriz de transformación que gira el plano de proyección sobre el eje Y.               | ![Matriz de rotación y](images/3d-transform-matrix6.png)    |
| RotationZ(Z)                            | Genera una matriz de transformación que gira el plano de proyección sobre el eje Z.               | ![Matriz de rotación z](images/3d-transform-matrix7.png)    |
| PerspectiveProjection(D)                | Transformación de perspectiva con un valor de profundidad de D.                                          | ![Matriz de perspectiva](images/3d-transform-matrix8.png) |
| RotationArbitraryAxis(X, Y, Z, degrees) | Gira el plano de proyección sobre el eje que especifique.                                       |                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio \| Windows store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio \| Windows store\] |
| Encabezado                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


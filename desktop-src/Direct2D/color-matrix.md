---
title: Efecto de la matriz de colores
description: Use el efecto de matriz de colores para modificar los valores RGBA de un mapa de bits.
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- efecto de la matriz de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8bb461698e4f8b39eef3bed57fc21947f3cc1175c1bdf4f990629db87e1c5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653314"
---
# <a name="color-matrix-effect"></a>Efecto de la matriz de colores

Use el efecto de matriz de colores para modificar los valores RGBA de un mapa de bits.

Puede usar este efecto para:

-   Quitar un canal de color de una imagen.
-   Reduzca el color de una imagen.
-   Intercambiar canales de color.
-   Combinar canales de color.

Muchos efectos integrados son especializaciones de la matriz de colores que están optimizadas para el uso previsto de los efectos. Algunos ejemplos [son la saturación,](saturation.md) [la rotación de](hue-rotate.md) [matiz, la sepia](sepia-effect.md)y [la temperatura y el tono.](temperature-and-tint-effect.md)

El CLSID para este efecto es CLSID \_ D2D1ColorMatrix.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Modos alfa](#alpha-modes)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de la matriz de colores que intercambia los canales rojo y azul.



| Antes                                                       |
|--------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg)   |
| Después                                                        |
| ![la imagen después de la transformación.](images/15-colormatrix.png) |



 


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect);

colorMatrixEffect->SetInput(0, bitmap);
D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



Este efecto multiplica los valores RGBA de la imagen por una matriz principal de columna de 5x4, como se muestra en esta ecuación.

![una definición de matriz de ejemplo.](images/color-matrix-formula.png)

Este efecto funciona en imágenes alfa rectas y premultiplicadas.

## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Colormatrix<br/> D2D1 \_ COLORMATRIX \_ PROP \_ COLOR \_ MATRIX<br/> | Matriz 5x4 de valores float. Los elementos de la matriz no están enlazados y no tienen unidad.<br/> El valor predeterminado es la matriz de identidad.<br/> El tipo es D2D1 \_ MATRIX \_ 5X4 \_ F.<br/> El valor predeterminado es Matrix5x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0). <br/>                                                                                                                                                                                                                        |
| AlphaMode<br/> D2D1 \_ COLORMATRIX \_ PROP \_ ALPHA \_ MODE<br/>     | Modo alfa de la salida. Consulte [Modos alfa](#alpha-modes) para obtener más información. <br/> El tipo es D2D1 \_ COLORMATRIX \_ ALPHA \_ MODE.<br/> El valor predeterminado es D2D1 \_ COLORMATRIX \_ ALPHA \_ MODE \_ PREMULTIPLIED.<br/>                                                                                                                                                                                                                                                                                                    |
| ClampOutput<br/> SALIDA DE LA FIJACIÓN DE \_ PROP DE COLORMATRIX D2D1 \_ \_ \_<br/> | Si el efecto fija los valores de color a entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto en el gráfico. El efecto fija los valores antes de que multipliese el alfa .<br/> Si establece esta opción en TRUE, el efecto fijará los valores. Si establece esta opción en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no tienen una precisión lo suficientemente alta.<br/> El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/> |



 

## <a name="alpha-modes"></a>Modos alfa



| Nombre                                          | Descripción                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| D2D1 \_ COLORMATRIX \_ ALPHA \_ MODE \_ PREMULTIPLIED | El efecto desmultiplica la entrada, aplica la matriz de colores y premultiplica la salida.<br/> |
| D2D1 \_ COLORMATRIX \_ ALPHA \_ MODE \_ STRAIGHT      | El efecto aplica la matriz de colores directamente a la entrada y no multiplica previamente la salida.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Header                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


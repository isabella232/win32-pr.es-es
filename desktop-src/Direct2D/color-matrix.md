---
title: Efecto de la matriz de colores
description: Utilice el efecto de la matriz de colores para modificar los valores RGBA de un mapa de bits.
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- efecto de la matriz de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1078b1858bc68396546e1036c717e01acb1069c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079248"
---
# <a name="color-matrix-effect"></a>Efecto de la matriz de colores

Utilice el efecto de la matriz de colores para modificar los valores RGBA de un mapa de bits.

Puede usar este efecto para:

-   Quitar un canal de color de una imagen.
-   Reduzca el color de una imagen.
-   Intercambie los canales de color.
-   Combinar canales de color.

Muchos efectos integrados son especializaciones de la matriz de colores que están optimizadas para el uso previsto de los efectos. Entre los ejemplos se incluyen [saturación](saturation.md), [matiz, rotación](hue-rotate.md), [sepia](sepia-effect.md)y [temperatura y matiz](temperature-and-tint-effect.md).

El CLSID para este efecto es CLSID \_ D2D1ColorMatrix.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Modos alfa](#alpha-modes)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de la matriz de colores que intercambia los canales rojo y azul.



| Antes                                                       |
|--------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)   |
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



Este efecto multiplica los valores RGBA de la imagen por una matriz de columnas principales de 5x4, como se muestra en esta ecuación.

![una definición de matriz de ejemplo.](images/color-matrix-formula.png)

Este efecto funciona en imágenes alfa directas y premultiplicadas.

## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ColorMatrix<br/> \_Matriz de colores D2D1 COLORMATRIX \_ prop \_ \_<br/> | Matriz 5x4 de valores float. Los elementos de la matriz no están enlazados y no tienen unidades.<br/> El valor predeterminado es la matriz de identidad.<br/> El tipo es D2D1 \_ Matrix \_ 5x4 \_ F.<br/> El valor predeterminado es Matrix5x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0). <br/>                                                                                                                                                                                                                        |
| AlphaMode<br/> \_ \_ Modo alfa de prop D2D1 COLORMATRIX \_ \_<br/>     | Modo alfa de la salida. Vea [modos alfa](#alpha-modes) para obtener más información. <br/> El tipo es D2D1 \_ COLORMATRIX \_ alpha \_ .<br/> El valor predeterminado es el \_ \_ modo alfa D2D1 COLORMATRIX \_ \_ premultiplicado.<br/>                                                                                                                                                                                                                                                                                                    |
| ClampOutput<br/> Salida de la abrazadera de prop de D2D1 \_ COLORMATRIX \_ \_ \_<br/> | Si el efecto fija los valores de color entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto del gráfico. El efecto fija los valores antes de que premultiplique el alfa.<br/> Si establece este valor en TRUE, el efecto fijará los valores. Si se establece en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no son de precisión lo suficientemente alta.<br/> El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/> |



 

## <a name="alpha-modes"></a>Modos alfa



| Nombre                                          | Descripción                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Premultiplicado por el \_ \_ modo alfa D2D1 COLORMATRIX \_ \_ | El efecto anula la multiplicación de la entrada, aplica la matriz de colores y premultiplica el resultado.<br/> |
| \_ \_ Modo alfa D2D1 \_ COLORMATRIX \_ recto      | El efecto aplica la matriz de colores directamente a la entrada y no multiplica la salida.<br/> |



 

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

 


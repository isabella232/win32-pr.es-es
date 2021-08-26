---
title: Efecto de transformación afín 2D
description: El efecto de transformación afín 2D aplica una transformación espacial a una imagen basada en una matriz 3X2 mediante la transformación de matriz de Direct2D y cualquiera de los seis modos de interpolación.
ms.assetid: E8973EBE-764C-4220-BB1E-3BFD4853582D
keywords:
- Efecto de transformación afín 2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 337168db7a422a8a22785316d2af1960e3a78b2f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478101"
---
# <a name="2d-affine-transform-effect"></a>Efecto de transformación afín 2D

El efecto de transformación afín 2D aplica una transformación espacial a una imagen basada [](direct2d-transforms-overview.md) en una matriz 3X2 mediante la transformación de matriz de Direct2D y cualquiera de los seis modos de interpolación. Puede usar este efecto para girar, escalar, sesgar o traducir una imagen. O bien, puede combinar estas operaciones. Las transferencias afín conservan las líneas paralelas y la proporción de distancias entre los tres puntos de una imagen.

El CLSID para este efecto es CLSID \_ D2D12DAffineTransform.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Modos de borde](#border-modes)
-   [Modos de interpolación](#interpolation-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                             |
|--------------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg)         |
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



Este efecto realiza esta operación de matriz:

![Operación de matriz afín](images/affine-matrix-calculation.png)

Aunque la matriz de entrada se define como una matriz de 3x2, la última columna se agrega con 0, 0 y 1 para generar una matriz cuadrada. Esto permite la multiplicación de matrices, por lo que las transformaciones se pueden concatenar en una sola matriz.

## <a name="effect-properties"></a>Propiedades de efecto




| Enumeración de nombre para mostrar e índice | Descripción | 
|------------------------------------|-------------|
| InterpolationMode<br /> D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE<br /> | Modo de interpolación utilizado para escalar la imagen. Hay 6 modos de escala que varían en calidad y velocidad.<br /> El tipo es D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.<br /> El valor predeterminado es D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.<br /> | 
| BorderMode<br /> D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE<br /> | Modo que se usa para calcular el borde de la imagen, de forma flexible o dura. Consulte <a href="https://www.bing.com/search?q=Border+modes">Modos de borde</a> para obtener más información. <br /> El tipo es D2D1_BORDER_MODE.<br /> El valor predeterminado es D2D1_BORDER_MODE_SOFT.<br /> | 
| TransformMatrix<br /> D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX<br /> | Matriz 3x2 para transformar la imagen mediante la transformación de la matriz <a href="direct2d-transforms-overview.md">de</a>Direct2D . <br /> El tipo es D2D1_MATRIX_3X2_F.<br /> El valor predeterminado es Matrix3x2F::Identity().<br /> | 
| Nitidez<br /> D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS<br /> | En el modo de interpolación cúbica de alta calidad, el nivel de niguedad del filtro de escalado como un valor float entre 0 y 1. Los valores no tienen unidad. Puede usar la nidez para ajustar la calidad de una imagen al escalar la imagen.<br /> El factor de niguidad afecta a la forma del kernel. Cuanto mayor sea el factor de nidez, menor será el kernel. <br /><blockquote>[!Note]<br />Esta propiedad solo afecta al modo de interpolación cúbica de alta calidad.</blockquote><br /> El tipo es FLOAT.<br /> El valor predeterminado es 1,0f.<br /> | 




 

## <a name="border-modes"></a>Modos de borde



| Nombre                     | Descripción                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| MODO DE BORDE D2D1 \_ \_ \_ SOFT | El efecto abate la imagen con píxeles negros transparentes a medida que se interpola, lo que da lugar a un borde suave.<br/> |
| D2D1 \_ BORDER \_ MODE \_ HARD | El efecto fija la salida al tamaño de la imagen de entrada. <br/>                                         |



 

## <a name="interpolation-modes"></a>Modos de interpolación



| Enumeración                                                         | Descripción                                                                                                                                                                                          |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 2DAFFINETRANSFORM \_ MODO DE INTERPOLACIÓN VECINO MÁS \_ \_ \_ PRÓXIMO     | Muestrea el punto único más cercano y lo usa. Este modo usa menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| D2D1 \_ 2DAFFINETRANSFORM \_ MODO DE INTERPOLACIÓN \_ \_ LINEAL                | Usa una muestra de cuatro puntos e interpolación lineal. Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad.                                           |
| D2D1 \_ 2DAFFINETRANSFORM \_ MODO DE INTERPOLACIÓN \_ \_ CÚBICA                 | Usa un kernel cúbica de 16 muestras para la interpolación. Este modo usa el mayor tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ 2DAFFINETRANSFORM \_ INTERPOLATION \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 muestras lineales dentro de un solo píxel para un buen suavizado de alias perimetral. Este modo es bueno para reducir verticalmente en pequeñas cantidades en imágenes con pocos píxeles.                                              |
| D2D1 \_ 2DAFFINETRANSFORM \_ INTERPOLATION \_ MODE \_ ANISOTROPIC           | Usa el filtrado anisotropico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ 2DAFFINETRANSFORM \_ MODO DE INTERPOLACIÓN \_ \_ \_ CÚBICA DE ALTA \_ CALIDAD  | Usa un kernel cúbica de alta calidad de tamaño variable para realizar una escala previa a la baja de la imagen si la escala hacia abajo está implicada en la matriz de transformación. A continuación, usa el modo de interpolación cúbica para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el valor predeterminado del efecto es D2D1 \_ 2DAFFINETRANSFORM \_ INTERPOLATION \_ MODE \_ LINEAR.

 

> [!Note]  
> El modo anisotropico genera mapas mipmap al escalar; sin embargo, si establece la propiedad **Cached** en true en los efectos que se introducen en este efecto, los mapas mipmap no se generarán cada vez para imágenes lo suficientemente pequeñas.

 

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del mapa de bits de salida depende de la matriz de transformación que se aplica a la imagen.

El efecto realiza la operación de transformación y, a continuación, aplica un rectángulo delimitador alrededor del resultado. El mapa de bits de salida es el tamaño del cuadro de límite.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Encabezado                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


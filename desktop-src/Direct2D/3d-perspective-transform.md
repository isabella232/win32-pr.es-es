---
title: Efecto de transformación de perspectiva 3D
description: Use el efecto de transformación de perspectiva 3D para girar la imagen en 3 dimensiones como si se ve desde una distancia.
ms.assetid: 0E1A940E-2DCA-4772-BB68-7E5EF5CEF833
keywords:
- Efecto de transformación de perspectiva 3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed2b1c5131319dd711d2c7802a0bfabceaaa32e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164266"
---
# <a name="3d-perspective-transform-effect"></a>Efecto de transformación de perspectiva 3D

Use el efecto de transformación de perspectiva 3D para girar la imagen en 3 dimensiones como si se ve desde una distancia.

La transformación de perspectiva 3D es más cómoda que el efecto de transformación 3D, pero solo expone un subconjunto de la funcionalidad. Puede calcular una matriz de transformación 3D completa y aplicar una matriz de transformación más arbitraria a una imagen mediante el efecto [de transformación 3D.](3d-transform.md)

El CLSID para este efecto es CLSID \_ D2D13DPerspectiveTransform.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Modos de interpolación](#interpolation-modes)
-   [Modos de borde](#border-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                               |
|----------------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg)           |
| Después                                                                |
| ![la imagen después del efecto.](images/23-3dperspectivetransform.png) |



 


```C++
ComPtr<ID2D1Effect> perspectiveTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DPerspectiveTransform, &perspectiveTransformEffect);

perspectiveTransformEffect->SetInput(0, bitmap);

perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN, D2D1::Vector3F(0.0f, 192.0f, 0.0f));
perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION, D2D1::Vector3F(0.0f, 30.0f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(perspectiveTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                                              | Descripción                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InterpolationMode<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ INTERPOLATION \_ MODE<br/> | Modo de interpolación que el efecto usa en la imagen. Hay cinco modos de escala que varían en calidad y velocidad.<br/> El tipo es D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE.<br/> El valor predeterminado es D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ LINEAR.<br/>              |
| BorderMode<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ BORDER \_ MODE<br/>               | Modo que se usa para calcular el borde de la imagen, de forma flexible o dura. Consulte [Modos de borde](https://www.bing.com/search?q=Border+modes) para obtener más información.<br/> El tipo es D2D1 \_ BORDER \_ MODE.<br/> El valor predeterminado es D2D1 \_ BORDER \_ MODE \_ SOFT.<br/>                                                              |
| Profundidad<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ DEPTH<br/>                           | Distancia entre *PerspectiveOrigin* y el plano de proyección. El valor especificado en LOSP y debe ser mayor que 0.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 1000.0f.<br/>                                                                                               |
| PerspectiveOrigin<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ PERSPECTIVE \_ ORIGIN<br/> | Ubicación X e Y del visor en la escena 3D. Esta propiedad es una D2D1 \_ VECTOR \_ 2F definida como: (punto X, punto Y). Las unidades están en DIP.<br/> Establezca el valor Z con la *propiedad Depth.*<br/> El tipo es D2D1 \_ VECTOR \_ 2F.<br/> El valor predeterminado es {0,0f, 0,0f}.<br/> |
| LocalOffset<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ LOCAL \_ OFFSET<br/>             | Una traducción que el efecto realiza antes de girar el plano de proyección. Esta propiedad es un vector 3F D2D1 \_ \_ definido como: (X, Y, Z). Las unidades están en DIP.<br/> El tipo es D2D1 \_ VECTOR \_ 3F.<br/> El valor predeterminado es {0.0f, 0.0f, 0.0f}.<br/>                                        |
| GlobalOffset<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ GLOBAL \_ OFFSET<br/>           | Una traducción que el efecto realiza después de girar el plano de proyección. Esta propiedad es un vector 3F D2D1 \_ \_ definido como: (X, Y, Z). Las unidades están en DIP.<br/> El tipo es D2D1 \_ VECTOR \_ 3F.<br/> El valor predeterminado es {0.0f, 0.0f, 0.0f}.<br/>                                         |
| RotationOrigin<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ ROTATION \_ ORIGIN<br/>       | Punto central de la rotación que realiza el efecto. Esta propiedad es un vector 3F D2D1 \_ \_ definido como: (X, Y, Z). Las unidades están en DIP.<br/> El tipo es D2D1 \_ VECTOR \_ 3F.<br/> El valor predeterminado es {0.0f, 0.0f, 0.0f}.<br/>                                                            |
| Rotación<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ ROTATION<br/>                     | Ángulos de rotación para cada eje. Esta propiedad es un vector 3F D2D1 \_ \_ definido como: (X, Y, Z). Las unidades están en grados.<br/> El tipo es D2D1 \_ VECTOR \_ 3F.<br/> El valor predeterminado es {0.0f, 0.0f, 0.0f}.<br/>                                                                         |



 

## <a name="interpolation-modes"></a>Modos de interpolación



| Enumeración                                                              | Descripción                                                                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ NEAREST \_ NEIGHBOR     | Muestrea el punto único más cercano y lo usa. Este modo usa menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                 |
| D2D1 \_ MODO DE INTERPOLACIÓN 3DPERSPECTIVETRANSFORM \_ \_ \_ LINEAR                | Usa una muestra de cuatro puntos e interpolación lineal. Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad. |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ CUBIC                 | Usa un kernel cúbica de 16 muestras para la interpolación. Este modo usa el mayor tiempo de procesamiento, pero genera una imagen de mayor calidad.                              |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 muestras lineales dentro de un solo píxel para un buen suavizado de alias perimetral. Este modo es bueno para reducir verticalmente en pequeñas cantidades en imágenes con pocos píxeles.    |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ ANISOTROPIC           | Usa el filtrado anisotropico para muestrear un patrón según la forma transformada del mapa de bits.                                                           |



 

> [!Note]  
> Si no selecciona un modo, el efecto tiene como valor predeterminado D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ LINEAR.

 

> [!Note]  
> El modo anisotropico genera mapas mipmap al escalar; sin embargo, si establece la propiedad **Cached** en true en los efectos que se introducen en este efecto, los mapas mipmap no se generarán cada vez para imágenes lo suficientemente pequeñas.

 

## <a name="border-modes"></a>Modos de borde



| Nombre                     | Descripción                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| MODO DE BORDE D2D1 \_ \_ \_ SOFT | El efecto abate la imagen con píxeles negro transparentes a medida que se interpola, lo que da lugar a un borde suave.<br/> |
| D2D1 \_ BORDER \_ MODE \_ HARD | El efecto fija la salida al tamaño de la imagen de entrada. <br/>                                         |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del mapa de bits de salida depende de la matriz de transformación que se aplica a la imagen.

El efecto realiza la operación de transformación y, a continuación, aplica un cuadro de límite alrededor del resultado. El mapa de bits de salida es el tamaño del cuadro de límite.

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

 


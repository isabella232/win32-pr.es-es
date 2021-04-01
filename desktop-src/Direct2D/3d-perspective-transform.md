---
title: Efecto de transformación de perspectiva 3D
description: Use el efecto transformación de perspectiva 3D para girar la imagen en tres dimensiones, como si se viera desde una distancia.
ms.assetid: 0E1A940E-2DCA-4772-BB68-7E5EF5CEF833
keywords:
- efecto de transformación de perspectiva 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed2b1c5131319dd711d2c7802a0bfabceaaa32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905671"
---
# <a name="3d-perspective-transform-effect"></a>Efecto de transformación de perspectiva 3D

Use el efecto transformación de perspectiva 3D para girar la imagen en tres dimensiones, como si se viera desde una distancia.

La transformación perspectiva 3D es más cómoda que el efecto transformación 3D, pero solo expone un subconjunto de la funcionalidad. Puede calcular una matriz de transformación 3D completa y aplicar una matriz de transformación más arbitraria a una imagen mediante el efecto [transformación 3D](3d-transform.md) .

El CLSID para este efecto es CLSID \_ D2D13DPerspectiveTransform.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Modos de interpolación](#interpolation-modes)
-   [Modos de borde](#border-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                               |
|----------------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)           |
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



## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                                              | Descripción                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InterpolationMode<br/> \_Modo de \_ \_ interpolación de \_ propiedades de D2D1 3DPERSPECTIVETRANSFORM<br/> | El modo de interpolación que el efecto usa en la imagen. Hay 5 modos de escala que abarcan la calidad y la velocidad.<br/> El tipo es D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modo de interpolación \_ .<br/> El valor predeterminado es D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modo de interpolación \_ \_ lineal.<br/>              |
| BorderMode<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ \_ modo de borde \_ de la Prop<br/>               | El modo que se usa para calcular el borde de la imagen, es decir, es flexible o difícil. Vea [modos de borde](https://www.bing.com/search?q=Border+modes) para obtener más información.<br/> El tipo es D2D1 \_ Border \_ mode.<br/> El valor predeterminado es el \_ modo de borde D2D1 \_ \_ .<br/>                                                              |
| Profundidad<br/> Profundidad de la D2D1 \_ 3DPERSPECTIVETRANSFORM \_ \_<br/>                           | Distancia entre el *PerspectiveOrigin* y el plano de proyección. El valor especificado en DIP y debe ser mayor que 0.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 1000.0 f.<br/>                                                                                               |
| PerspectiveOrigin<br/> Origen de la perspectiva de D2D1 \_ 3DPERSPECTIVETRANSFORM \_ \_ \_<br/> | La ubicación X e y del visor en la escena 3D. Esta propiedad es un vector D2D1 se \_ \_ define como: (punto X, punto Y). Las unidades están en DIP.<br/> Establezca el valor Z con la propiedad *Depth* .<br/> El tipo es \_ Vector D2D1 \_ 2F.<br/> El valor predeterminado es {0.0 f, 0.0 f}.<br/> |
| LocalOffset<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ prop \_ \_ desplazamiento local<br/>             | Traducción que realiza el efecto antes de girar el plano de proyección. Esta propiedad es una D2D1 \_ Vector \_ 3F definida como: (X, Y, Z). Las unidades están en DIP.<br/> El tipo es D2D1 \_ Vector \_ 3F.<br/> El valor predeterminado es {0.0 f, 0.0 f, 0.0 f}.<br/>                                        |
| GlobalOffset<br/> \_ \_ \_ Desplazamiento global de prop \_ de D2D1 3DPERSPECTIVETRANSFORM<br/>           | Traducción que realiza el efecto después de girar el plano de proyección. Esta propiedad es una D2D1 \_ Vector \_ 3F definida como: (X, Y, Z). Las unidades están en DIP.<br/> El tipo es D2D1 \_ Vector \_ 3F.<br/> El valor predeterminado es {0.0 f, 0.0 f, 0.0 f}.<br/>                                         |
| RotationOrigin<br/> \_Origen de \_ rotación de propiedades \_ \_ de D2D1 3DPERSPECTIVETRANSFORM<br/>       | Punto central de la rotación que realiza el efecto. Esta propiedad es una D2D1 \_ Vector \_ 3F definida como: (X, Y, Z). Las unidades están en DIP.<br/> El tipo es D2D1 \_ Vector \_ 3F.<br/> El valor predeterminado es {0.0 f, 0.0 f, 0.0 f}.<br/>                                                            |
| Rotación<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ prop \_ giro<br/>                     | Ángulos de rotación de cada eje. Esta propiedad es una D2D1 \_ Vector \_ 3F definida como: (X, Y, Z). Las unidades están en grados.<br/> El tipo es D2D1 \_ Vector \_ 3F.<br/> El valor predeterminado es {0.0 f, 0.0 f, 0.0 f}.<br/>                                                                         |



 

## <a name="interpolation-modes"></a>Modos de interpolación



| Enumeración                                                              | Descripción                                                                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ el \_ modo de interpolación 3DPERSPECTIVETRANSFORM \_ \_ más cercano \_     | Muestrea el punto único más cercano y lo usa. Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                 |
| D2D1 \_ \_ modo de interpolación 3DPERSPECTIVETRANSFORM \_ \_ lineal                | Utiliza un ejemplo de cuatro puntos y una interpolación lineal. Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad. |
| D2D1 \_ \_ modo de interpolación 3DPERSPECTIVETRANSFORM \_ \_ cúbico                 | Usa un kernel cúbico de ejemplo 16 para la interpolación. Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.                              |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modo de interpolación \_ \_ lineal de varios \_ ejemplos \_ | Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado. Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.    |
| D2D1 \_ \_ modo de interpolación 3DPERSPECTIVETRANSFORM \_ \_ anisotrópico           | Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.                                                           |



 

> [!Note]  
> Si no selecciona un modo, el efecto tiene como valor predeterminado el \_ \_ modo de interpolación D2D1 3DPERSPECTIVETRANSFORM \_ \_ lineal.

 

> [!Note]  
> El modo anisotrópico genera mapas MIP al escalar; sin embargo, si establece la propiedad **Cached** en true en los efectos que se aplican a este efecto, no se generarán los mapas MIP cada vez para imágenes suficientemente pequeñas.

 

## <a name="border-modes"></a>Modos de borde



| Nombre                     | Descripción                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ modo de borde \_ \_ flexible | El efecto rellena la imagen con píxeles negros transparentes mientras se interpola, lo que da lugar a un borde flexible.<br/> |
| D2D1 \_ del \_ modo de borde \_ | El efecto fija la salida al tamaño de la imagen de entrada. <br/>                                         |



 

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

 


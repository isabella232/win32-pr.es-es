---
title: Efecto Rotatation de matiz
description: Use el efecto girar matiz para modificar el matiz de una imagen aplicando una matriz de colores basada en el ángulo de rotación.
ms.assetid: D322DB2C-2B8B-4101-BFB2-97E49CAC7BF6
keywords:
- efecto Rotatation de matiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525dbe8fc94377080fbae34b80252c84c05073ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104565405"
---
# <a name="hue-rotatation-effect"></a>Efecto Rotatation de matiz

Use el efecto girar matiz para modificar el matiz de una imagen aplicando una matriz de colores basada en el ángulo de rotación.

El CLSID para este efecto es CLSID \_ D2D1HueRotation.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto rotar matiz con un ángulo de giro de 270 grados.



| Antes                                                       |
|--------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)   |
| Después                                                        |
| ![la imagen después de la transformación.](images/17-huerotation.png) |



 


```C++
ComPtr<ID2D1Effect> hueRotationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueRotation, &hueRotationEffect);

hueRotationEffect->SetInput(0, bitmap);
hueRotationEffect->SetValue(D2D1_HUEROTATION_PROP_ANGLE, 270.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueRotationEffect.Get());
m_d2dContext->EndDraw();
```



El efecto calcula una matriz de colores basándose en el ángulo de rotación (*?*) que se especifica con la propiedad de ángulo de propiedades de D2D1 \_ HUEROTATION \_ \_ . Estas son las ecuaciones de la matriz.

![cálculos de rotación de matiz](images/hue-formula.png)

La matriz creada depende solo del ángulo de rotación. Puede usar el efecto de la [matriz de colores](color-matrix.md) si necesita una matriz específica.

## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                         | Tipo y valor predeterminado           | Descripción                              |
|------------------------------------------------------------|----------------------------------|------------------------------------------|
| Ángulo<br/> Ángulo de la D2D1 \_ HUEROTATION \_ \_<br/> | FLOAT<br/> 0,0F<br/> | Ángulo para girar el matiz, en grados. |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del mapa de bits de salida es el mismo que el tamaño del mapa de bits de entrada.

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

 


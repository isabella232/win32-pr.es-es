---
title: Efecto de saturación
description: Utilice este efecto para modificar la saturación de una imagen.
ms.assetid: 03A374D9-BED4-49ED-B90E-21193909C8AB
keywords:
- efecto de saturación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6912e64c9297a3554b4785128e1282a3974d36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079246"
---
# <a name="saturation-effect"></a>Efecto de saturación

Utilice este efecto para modificar la saturación de una imagen. El efecto de saturación es una especialización del efecto de la [matriz de colores](color-matrix.md) .

El CLSID para este efecto es CLSID \_ D2D1Saturation.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de saturación con una saturación del 0%.



| Antes                                                      |
|-------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)  |
| Después                                                       |
| ![la imagen después de la transformación.](images/16-saturation.png) |



 


```C++
ComPtr<ID2D1Effect> saturationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Saturation, &saturationEffect);

saturationEffect->SetInput(0, bitmap);

saturationEffect->SetValue(D2D1_SATURATION_PROP_SATURATION, 0.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(saturationEffect.Get());
m_d2dContext->EndDraw();
```



El efecto calcula una matriz de colores basándose en el valor de saturación que se muestra *aquí (en* la ecuación) que se especifica con la propiedad de saturación D2D1 saturación de saturación \_ \_ \_ . La ecuación de la matriz se muestra aquí.

![fórmula para calcular una matriz de saturación.](images/saturation-formula.png)

La matriz creada depende solo del valor de saturación. Puede usar el efecto de la [matriz de colores](color-matrix.md) si necesita una matriz específica.

Este efecto consume y genera imágenes alfa premultiplicadas. El efecto no funcionará en imágenes alfa rectas a menos que sean totalmente opacas.

## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                  | Tipo y valor predeterminado           | Descripción                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Saturación<br/> Saturación de D2D1 \_ saturación de saturación \_ \_<br/> | FLOAT<br/> 0.5 f<br/> | Saturación de la imagen. Puede establecer la saturación en un valor entre 0 y 1. Si se establece en 1, la imagen de salida está completamente saturada. Si se establece en 0, la imagen de salida es monocroma. El valor de saturación no es una unidad. |



 

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

 


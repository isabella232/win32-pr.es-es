---
title: Efecto de saturación
description: Use este efecto para modificar la saturación de una imagen.
ms.assetid: 03A374D9-BED4-49ED-B90E-21193909C8AB
keywords:
- efecto de saturación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5f9a4bff56ed47a0ca182dab855899d98022252c6f20c250aef693451df4c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665047"
---
# <a name="saturation-effect"></a>Efecto de saturación

Use este efecto para modificar la saturación de una imagen. El efecto de saturación es una especialización del [efecto de matriz de](color-matrix.md) colores.

El CLSID para este efecto es CLSID \_ D2D1Saturation.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestran las imágenes de entrada y salida del efecto de saturación con una saturación del 0 %.



| Antes                                                      |
|-------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg)  |
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



El efecto calcula una matriz de colores en función del valor de saturación *(s* en la ecuación aquí) que especifique con la propiedad \_ SATURACIÓN DE PROP SATURATION de D2D1. \_ \_ La ecuación de matriz se muestra aquí.

![fórmula para calcular una matriz de saturación.](images/saturation-formula.png)

La matriz creada depende solo del valor de saturación. Puede usar el efecto [de matriz de](color-matrix.md) colores si necesita una matriz específica.

Este efecto consume y genera imágenes alfa premultiplicadas. El efecto no funcionará en imágenes alfa rectas a menos que sean totalmente opacas.

## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                  | Tipo y valor predeterminado           | Descripción                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Saturación<br/> SATURACIÓN DE SATURACIÓN D2D1 \_ \_ SATURACIÓN \_<br/> | FLOAT<br/> 0,5f<br/> | Saturación de la imagen. Puede establecer la saturación en un valor entre 0 y 1. Si lo establece en 1, la imagen de salida está totalmente saturada. Si lo establece en 0, la imagen de salida es monocromática. El valor de saturación no tiene unidad. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio \| Windows store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio \| Windows store\] |
| Header                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


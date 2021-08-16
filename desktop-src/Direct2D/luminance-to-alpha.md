---
title: Efecto de luminosidad a alfa
description: Use la luminosidad para el efecto alfa para establecer el canal alfa en la luminosidad de la imagen y establezca los canales de color en 0.
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- efecto de luminosidad a alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803070fea76b47c1334803a4e7f8fef510cc77c8b3bc05c8477b572cb0451670
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825266"
---
# <a name="luminance-to-alpha-effect"></a>Efecto de luminosidad a alfa

Use la luminosidad para el efecto alfa para establecer el canal alfa en la luminosidad de la imagen y establezca los canales de color en 0. Puede usar la salida de este efecto para crear una superposición semitransparente basada en el brillo de la imagen de entrada. O bien, puede usarlo para crear una máscara de imagen.

> [!Note]  
> Este efecto no tiene propiedades.

 

El CLSID para este efecto es CLSID \_ D2D1LuminanceToAlpha.

## <a name="example-image"></a>Imagen de ejemplo

En este ejemplo se muestra la salida de la luminosidad al efecto alfa compuesto sobre una superficie blanca para mostrar opacidad.



| Antes                                                            |
|-------------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg)        |
| Después                                                             |
| ![la imagen después de la transformación.](images/18-luminancetoalpha.png) |



 


```C++
ComPtr<ID2D1Effect> luminanceToAlphaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LuminanceToAlpha, &luminanceToAlphaEffect);

luminanceToAlphaEffect->SetInput(0, bitmap);

// LuminanceToAlpha result is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);
floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, luminanceToAlphaEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



Este efecto establece el canal alfa de la salida en la luminosidad de la imagen de entrada mediante esta matriz de colores.

![la matriz de colores que el efecto usa para establecer el canal alfa.](images/luminance-to-alpha-math1.png)

Este efecto consume y genera imágenes alfa premultiplicadas. El efecto no funcionará en imágenes alfa rectas a menos que sean totalmente opacas.

> [!Note]
>
> Dado que las imágenes se almacenan en un formato compensado por gamma, antes de calcular la luminosidad de una imagen, primero debe realizar la corrección gamma inversa para obtener los valores de color verdaderos de la imagen. Dado que las imágenes se almacenan normalmente en 2,2 gamma, puede usar el efecto de transferencia Gamma con un exponente de (1/2.2) y, a continuación, usar la salida de ese efecto.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Header                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

La salida tiene el mismo tamaño que la imagen de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 

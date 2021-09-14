---
title: Efecto de luminosidad a alfa
description: Use la luminosidad para el efecto alfa para establecer el canal alfa en la luminosidad de la imagen y establezca los canales de color en 0.
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- efecto de luminosidad a alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb4c6fb78a1d49498b2adab6716d41e93d30deb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162709"
---
# <a name="luminance-to-alpha-effect"></a>Efecto de luminosidad a alfa

Use la luminosidad para el efecto alfa para establecer el canal alfa en la luminosidad de la imagen y establezca los canales de color en 0. Puede usar la salida de este efecto para crear una superposición semitransparente basada en el brillo de la imagen de entrada. O bien, puede usarlo para crear una máscara de imagen.

> [!Note]  
> Este efecto no tiene propiedades.

 

El CLSID para este efecto es CLSID \_ D2D1LuminanceToAlpha.

## <a name="example-image"></a>Imagen de ejemplo

En este ejemplo se muestra la salida del efecto de luminosidad a alfa compuesto sobre una superficie blanca para mostrar la opacidad.



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
> Dado que las imágenes se almacenan en un formato compensado por gamma, antes de calcular la luminosidad de una imagen, primero debe realizar una corrección gamma inversa para obtener los valores de color verdaderos de la imagen. Puesto que las imágenes se almacenan normalmente en 2,2 gamma, puede usar el efecto de transferencia Gamma con un exponente de (1/2.2) y, a continuación, usar la salida de ese efecto.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio Windows aplicaciones de la \| Tienda\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio Windows aplicaciones de la \| Tienda\] |
| Encabezado                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

La salida tiene el mismo tamaño que la imagen de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 

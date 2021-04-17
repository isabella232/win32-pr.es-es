---
title: Luminancia a efecto alfa
description: Use la luminancia para el efecto alfa para establecer el canal alfa en la luminancia de la imagen y establezca los canales de color en 0.
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- luminancia a efecto alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb4c6fb78a1d49498b2adab6716d41e93d30deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104558401"
---
# <a name="luminance-to-alpha-effect"></a>Luminancia a efecto alfa

Use la luminancia para el efecto alfa para establecer el canal alfa en la luminancia de la imagen y establezca los canales de color en 0. Puede usar la salida de este efecto para crear una superposición semitransparente basada en el brillo de la imagen de entrada. También puede utilizarlo para crear una máscara de imagen.

> [!Note]  
> Este efecto no tiene propiedades.

 

El CLSID para este efecto es CLSID \_ D2D1LuminanceToAlpha.

## <a name="example-image"></a>Imagen de ejemplo

En este ejemplo se muestra la salida de la luminancia al efecto alfa compuesto sobre una superficie blanca para mostrar la opacidad.



| Antes                                                            |
|-------------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)        |
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



Este efecto establece el canal alfa de la salida en la luminancia de la imagen de entrada mediante esta matriz de colores.

![matriz de colores que el efecto utiliza para establecer el canal alfa.](images/luminance-to-alpha-math1.png)

Este efecto consume y genera imágenes alfa premultiplicadas. El efecto no funcionará en imágenes alfa rectas a menos que sean totalmente opacas.

> [!Note]
>
> Dado que las imágenes se almacenan en un formato compensado para la gamma, antes de calcular la luminancia de una imagen, primero debe realizar una corrección de gamma inversa para obtener los valores de color verdaderos de la imagen. Puesto que las imágenes se almacenan normalmente en gamma 2,2, puede usar el efecto de transferencia gamma con un exponente de (1/2.2) y, a continuación, utilizar la salida de ese efecto.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Servidor mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Encabezado                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

La salida tiene el mismo tamaño que la imagen de entrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 

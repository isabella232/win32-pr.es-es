---
title: Efecto de desbordamiento
description: Use el efecto de desbordamiento para generar un mapa de bits basado en el color y el valor alfa especificados. Puede usar este efecto cuando desee un color específico como entrada para un efecto, como un color de fondo.
ms.assetid: F80A6DC0-E18C-4324-BE4A-FE40C5722988
keywords:
- efecto de desbordamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92d34a41c0913a0d250fc24467b37b0d347b4ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163281"
---
# <a name="flood-effect"></a>Efecto de desbordamiento

Use el efecto de desbordamiento para generar un mapa de bits basado en el color y el valor alfa especificados. Puede usar este efecto cuando desee un color específico como entrada para un efecto, como un color de fondo.

> [!Note]  
> El efecto pasa a lo largo del valor de color especificado según lo especificado. Debe multiplicar manualmente los valores previamente si planea pasar la salida a los efectos que esperan una entrada multiplicada previamente.

 

El CLSID para este efecto es CLSID \_ D2D1Flood.

El efecto de desbordamiento no tiene ninguna imagen de entrada.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

![imagen de ejemplo del efecto de desbordamiento que da como resultado verde.](images/20-flood.png)


```C++
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(0.0f, 1.0f, 0.0f, 1.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(floodEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Color<br/> COLOR DE PROP \_ DE DESBORDAMIENTO D2D1 \_ \_<br/> | Color y opacidad del mapa de bits. Esta propiedad es D2D1 \_ VECTOR \_ 4F. Los valores individuales de cada canal son de tipo FLOAT, sin enlazar y sin unidad. El efecto no modifica los valores de los canales.<br/> Los valores RGBA de cada canal oscilan entre 0 y 1.<br/> El tipo es D2D1 \_ VECTOR \_ 4F.<br/> El valor predeterminado es {0.0f, 0.0f, 0.0f, 1.0f}.<br/> |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

Este efecto genera un mapa de bits de tamaño lógico infinito.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Encabezado                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


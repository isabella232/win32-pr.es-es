---
title: Efecto de saturación
description: Utilice el efecto de saturación para generar un mapa de bits basado en el color y el valor alfa especificados. Puede usar este efecto si desea un color específico como entrada para un efecto, como un color de fondo.
ms.assetid: F80A6DC0-E18C-4324-BE4A-FE40C5722988
keywords:
- efecto de saturación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92d34a41c0913a0d250fc24467b37b0d347b4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996775"
---
# <a name="flood-effect"></a>Efecto de saturación

Utilice el efecto de saturación para generar un mapa de bits basado en el color y el valor alfa especificados. Puede usar este efecto si desea un color específico como entrada para un efecto, como un color de fondo.

> [!Note]  
> El efecto pasa a lo largo del valor de color especificado según lo especificado. Debe multiplicar manualmente los valores si planea pasar el resultado a efectos que esperan una entrada previamente multiplicada.

 

El CLSID para este efecto es CLSID \_ D2D1Flood.

El efecto de saturación no tiene ninguna imagen de entrada.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

![imagen de ejemplo del efecto de saturación que presenta el color verde.](images/20-flood.png)


```C++
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(0.0f, 1.0f, 0.0f, 1.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(floodEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Color<br/> COLOR de D2D1 \_ inundaciones \_ \_<br/> | Color y opacidad del mapa de bits. Esta propiedad es un D2D1 \_ Vector \_ 4F. Los valores individuales de cada canal son de tipo FLOAT, unbounded y sin unidades. El efecto no modifica los valores de los canales.<br/> Los valores RGBA para cada canal oscilan entre 0 y 1.<br/> El tipo es D2D1 \_ Vector \_ 4F.<br/> El valor predeterminado es {0.0 f, 0.0 f, 0.0 f, 1.0 f.<br/> |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

Este efecto genera un mapa de bits de tamaño lógico infinito.

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

 


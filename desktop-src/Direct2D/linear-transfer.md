---
title: Efecto de transferencia lineal
description: Use el efecto de transferencia lineal para asignar las intensidades de color de una imagen mediante una función lineal creada a partir de una lista de valores que proporcione para cada canal.
ms.assetid: 22DC496E-2958-4726-A74D-B3DE934F507C
keywords:
- efecto de transferencia lineal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcb2bb688d1e8ebf4b1b1ebfdd531d900755b46840bada2bade49d957ed0f6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119385304"
---
# <a name="linear-transfer-effect"></a>Efecto de transferencia lineal

Use el efecto de transferencia lineal para asignar las intensidades de color de una imagen mediante una función lineal creada a partir de una lista de valores que proporcione para cada canal.

El CLSID para este efecto es CLSID \_ D2D1LinearTransfer.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                          |
|-----------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg)      |
| Después                                                           |
| ![la imagen después de la transformación.](images/13-lineartransfer.png) |



 


```C++
ComPtr<ID2D1Effect> linearTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LinearTransfer, &linearTransferEffect);

linearTransferEffect->SetInput(0, bitmap);

linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_RED_Y_INTERCEPT, -1.0f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_RED_SLOPE, 2.5f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_GREEN_Y_INTERCEPT, -1.0f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_GREEN_SLOPE, 5.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(linearTransferEffect.Get());
m_d2dContext->EndDraw();
```



La función de transferencia lineal se crea en función de la pendiente y la intersección de Y para cada canal que especifique. La intensidad de píxeles de salida C se calcula con la ecuación: C' = mC + B, donde m es la pendiente de la función lineal y B es la intersección Y de la función lineal.

Este efecto funciona en imágenes alfa rectas y premultiplicadas. El efecto genera mapas de bits alfa premultiplicados.

## <a name="effect-properties"></a>Propiedades de efecto

> [!Note]  
> Para todos los canales de las propiedades de transferencia lineal:
>
> -   La intersección Y no está limitada y no tiene unidad.
> -   La pendiente no está limitada y no tiene unidad.

 



| Enumeración de nombre para mostrar e índice                                                    | Tipo y valor predeterminado           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ RED \_ Y \_ INTERCEPT<br/>     | FLOAT<br/> 0,0f<br/> | Intercepción Y de la función lineal para el canal rojo.                                                                                                                                                                                                                                                                                                                                                                                                   |
| RedSlope<br/> PENDIENTE ROJA DE LA PROPIEDAD LINEARTRANSFER D2D1 \_ \_ \_ \_<br/>                 | FLOAT<br/> 1.0f<br/> | Pendiente de la función lineal para el canal rojo.                                                                                                                                                                                                                                                                                                                                                                                                         |
| RedDisable<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ RED \_ DISABLE<br/>             | BOOL<br/> FALSE<br/> | Si establece esta opción en TRUE, el efecto no aplica la función de transferencia al canal rojo. Si establece esta opción en FALSE, el efecto aplica la función RedLinearTransfer al canal rojo.                                                                                                                                                                                                                                                                    |
| GreenYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ GREEN \_ Y \_ INTERCEPT<br/> | FLOAT<br/> 0,0f<br/> | Intercepción Y de la función lineal para el canal verde.                                                                                                                                                                                                                                                                                                                                                                                                 |
| GreenSlope<br/> PENDIENTE VERDE DE LA PROPIEDAD LINEARTRANSFER D2D1 \_ \_ \_ \_<br/>             | FLOAT<br/> 1.0f<br/> | Pendiente de la función lineal para el canal verde.                                                                                                                                                                                                                                                                                                                                                                                                       |
| GreenDisable<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ GREEN \_ DISABLE<br/>         | BOOL<br/> FALSE<br/> | Si establece esta opción en TRUE, el efecto no aplica la función de transferencia al canal verde. Si se establece en FALSE, se aplica la función GreenLinearTransfer al canal verde.                                                                                                                                                                                                                                                                      |
| BlueYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ BLUE \_ Y \_ INTERCEPT<br/>   | FLOAT<br/> 0,0f<br/> | Intercepción Y de la función lineal para el canal azul.                                                                                                                                                                                                                                                                                                                                                                                                  |
| BlueSlope<br/> PENDIENTE AZUL DE LA PROPIEDAD LINEARTRANSFER D2D1 \_ \_ \_ \_<br/>               | FLOAT<br/> 1.0f<br/> | Pendiente de la función lineal para el canal azul.                                                                                                                                                                                                                                                                                                                                                                                                        |
| BlueDisable<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ BLUE \_ DISABLE<br/>           | BOOL<br/> FALSE<br/> | Si establece esta opción en TRUE, el efecto no aplica la función de transferencia al canal Azul. Si se establece en FALSE, se aplica la función BlueLinearTransfer al canal Azul.                                                                                                                                                                                                                                                                         |
| AlphaYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ ALPHA \_ Y \_ INTERCEPT<br/> | FLOAT<br/> 0,0f<br/> | Intercepción Y de la función lineal para el canal Alfa.                                                                                                                                                                                                                                                                                                                                                                                                 |
| AlfaSlope<br/> PENDIENTE ALFA DE LA PROPIEDAD \_ LINEARTRANSFER \_ \_ D2D1 \_<br/>             | FLOAT<br/> 0,0f<br/> | Pendiente de la función lineal para el canal Alfa.                                                                                                                                                                                                                                                                                                                                                                                                       |
| AlphaDisable<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ ALPHA \_ DISABLE<br/>         | BOOL<br/> FALSE<br/> | Si establece esta opción en TRUE, el efecto no aplica la función de transferencia al canal Alfa. Si se establece en FALSE, se aplica la función AlphaLinearTransfer al canal Alfa.                                                                                                                                                                                                                                                                      |
| ClampOutput<br/> SALIDA DE LA FIJACIÓN DE \_ \_ PROP \_ DE LINEARTRANSFER D2D1 \_<br/>           | BOOL<br/> FALSE<br/> | Si el efecto fija los valores de color a entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto en el gráfico. El efecto fija los valores antes de que multipliese el alfa .<br/> Si establece esta opción en TRUE, el efecto fijará los valores. Si establece esta opción en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no tienen una precisión lo suficientemente alta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows store\] |
| Header                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


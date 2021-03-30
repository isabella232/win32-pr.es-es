---
title: Efecto de transferencia lineal
description: Utilice el efecto de transferencia lineal para asignar las intensidades de color de una imagen mediante una función lineal creada a partir de una lista de valores que se proporciona para cada canal.
ms.assetid: 22DC496E-2958-4726-A74D-B3DE934F507C
keywords:
- efecto de transferencia lineal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfedbb79f057ee871ce23cc086034afc3e6cdda0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804111"
---
# <a name="linear-transfer-effect"></a>Efecto de transferencia lineal

Utilice el efecto de transferencia lineal para asignar las intensidades de color de una imagen mediante una función lineal creada a partir de una lista de valores que se proporciona para cada canal.

El CLSID para este efecto es CLSID \_ D2D1LinearTransfer.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                          |
|-----------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)      |
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



La función de transferencia lineal se crea basándose en la pendiente y en la intersección de y para cada canal que especifique. La intensidad de píxeles de salida C se calcula con la ecuación: C ' = mC + B, donde m es la pendiente de la función lineal y B es la intersección Y de la función lineal.

Este efecto funciona en imágenes alfa directas y premultiplicadas. El efecto genera mapas de bits alfa premultiplicados.

## <a name="effect-properties"></a>Propiedades del efecto

> [!Note]  
> Para todos los canales de las propiedades de transferencia lineal:
>
> -   La intercepción y no está enlazada y no tiene unidades.
> -   La pendiente no está enlazada y no tiene unidades.

 



| Enumeración de índice y nombre para mostrar                                                    | Tipo y valor predeterminado           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ rojo \_ Y \_ Intercept<br/>     | FLOAT<br/> 0,0F<br/> | La intersección Y de la función lineal para el canal rojo.                                                                                                                                                                                                                                                                                                                                                                                                   |
| RedSlope<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ . \_ pendiente roja<br/>                 | FLOAT<br/> 1,0 f<br/> | La pendiente de la función lineal para el canal rojo.                                                                                                                                                                                                                                                                                                                                                                                                         |
| RedDisable<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ rojo \_ deshabilitado<br/>             | BOOL<br/> false<br/> | Si se establece en TRUE, el efecto no aplica la función de transferencia al canal rojo. Si se establece en FALSE, el efecto aplica la función RedLinearTransfer al canal rojo.                                                                                                                                                                                                                                                                    |
| GreenYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ verde \_ Y \_ Intercept<br/> | FLOAT<br/> 0,0F<br/> | La intersección Y de la función lineal para el canal verde.                                                                                                                                                                                                                                                                                                                                                                                                 |
| GreenSlope<br/> D2D1 \_ LINEARTRANSFER \_ ( \_ \_ pendiente verde)<br/>             | FLOAT<br/> 1,0 f<br/> | La pendiente de la función lineal para el canal verde.                                                                                                                                                                                                                                                                                                                                                                                                       |
| GreenDisable<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ verde \_ deshabilitada<br/>         | BOOL<br/> false<br/> | Si se establece en TRUE, el efecto no aplica la función de transferencia al canal verde. Si se establece en FALSE, se aplica la función GreenLinearTransfer al canal verde.                                                                                                                                                                                                                                                                      |
| BlueYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ azul \_ Y \_ Intercept<br/>   | FLOAT<br/> 0,0F<br/> | La intersección Y de la función lineal para el canal azul.                                                                                                                                                                                                                                                                                                                                                                                                  |
| BlueSlope<br/> \_ \_ \_ Inclinación azul de la D2D1 LINEARTRANSFER \_<br/>               | FLOAT<br/> 1,0 f<br/> | La pendiente de la función lineal para el canal azul.                                                                                                                                                                                                                                                                                                                                                                                                        |
| BlueDisable<br/> Deshabilitar D2D1 de LINEARTRANSFER de la \_ \_ prop \_ azul \_<br/>           | BOOL<br/> false<br/> | Si se establece en TRUE, el efecto no aplica la función de transferencia al canal azul. Si se establece en FALSE, se aplica la función BlueLinearTransfer al canal azul.                                                                                                                                                                                                                                                                         |
| AlphaYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ alfa \_ Y \_ Intercept<br/> | FLOAT<br/> 0,0F<br/> | La intersección Y de la función lineal para el canal alfa.                                                                                                                                                                                                                                                                                                                                                                                                 |
| AlphaSlope<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ ( \_ pendiente alfa)<br/>             | FLOAT<br/> 0,0F<br/> | La pendiente de la función lineal para el canal alfa.                                                                                                                                                                                                                                                                                                                                                                                                       |
| AlphaDisable<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ alpha \_ deshabilitada<br/>         | BOOL<br/> false<br/> | Si se establece en TRUE, el efecto no aplica la función de transferencia al canal alfa. Si se establece en FALSE, se aplica la función AlphaLinearTransfer al canal alfa.                                                                                                                                                                                                                                                                      |
| ClampOutput<br/> Salida de la abrazadera de D2D1 \_ LINEARTRANSFER \_ \_ \_<br/>           | BOOL<br/> false<br/> | Si el efecto fija los valores de color entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto del gráfico. El efecto fija los valores antes de que premultiplique el alfa.<br/> Si establece este valor en TRUE, el efecto fijará los valores. Si se establece en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no son de precisión lo suficientemente alta.<br/> |



 

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

 


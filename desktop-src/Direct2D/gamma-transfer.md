---
title: Efecto de transferencia gamma
description: Use el efecto de transferencia gamma para asignar las intensidades de color de una imagen mediante una función gamma creada con una amplitud, exponente y desplazamiento que proporcione para cada canal.
ms.assetid: 0E0455CA-CFCA-4C4F-9DFA-1DB6A5205F6A
keywords:
- efecto de transferencia gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b806ac8f59efe1b3fad3b61edc7f88f72b143f9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163266"
---
# <a name="gamma-transfer-effect"></a>Efecto de transferencia gamma

Use el efecto de transferencia gamma para asignar las intensidades de color de una imagen mediante una función gamma creada con una amplitud, exponente y desplazamiento que proporcione para cada canal.

El CLSID para este efecto es CLSID \_ D2D1GammaTransfer. Para usar este efecto, agregue dxguid.lib a las dependencias del vinculador.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                         |
|----------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg)     |
| Después                                                          |
| ![la imagen después de la transformación.](images/14-gammatransfer.png) |



 


```C++
ComPtr<ID2D1Effect> gammaTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GammaTransfer, &gammaTransferEffect);

gammaTransferEffect->SetInput(0, bitmap);

gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, 0.25f);
gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_EXPONENT, 0.25f);
gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_EXPONENT, 0.25f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gammaTransferEffect.Get());
m_d2dContext->EndDraw();
```



Este efecto aplica una función de transferencia gamma basada en la ecuación aquí.

La intensidad de píxeles de entrada se representa como C y la intensidad de píxeles de salida como C'. C' = Amplitude \* C<sup>Exponent</sup> + Offset

Este efecto funciona en imágenes alfa rectas y premultiplicadas. El efecto genera mapas de bits alfa premultiplicados.

## <a name="effect-properties"></a>Propiedades de efecto

> [!Note]  
> Para todos los canales de las propiedades de transferencia gamma:
>
> -   El valor de amplitud no está limitado y no tiene unidad.
> -   El valor del exponente no está enlazado y no tiene unidad.
> -   El valor de desplazamiento no está enlazado y no tiene unidad.

 



| Enumeración de nombre para mostrar e índice                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedAmplitude<br/> AMPLITUD ROJA DE PROP GAMMATRANSFER D2D1 \_ \_ \_ \_<br/>     | Amplitud de la función de transferencia gamma para el canal rojo. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| RedExponent<br/> EXPONENTE ROJO D2D1 \_ GAMMATRANSFER \_ PROP \_ \_<br/>       | Exponente de la función de transferencia gamma para el canal rojo. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| RedOffset<br/> D2D1 \_ GAMMATRANSFER \_ PROP \_ RED \_ OFFSET<br/>           | Desplazamiento de la función de transferencia gamma para el canal rojo. El tipo es FLOAT.<br/> El valor predeterminado es 0,0f.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| RedDisable<br/> D2D1 \_ GAMMATRANSFER \_ PROP \_ RED \_ DISABLE<br/>         | Si establece esta opción en TRUE, no se aplica la función de transferencia al canal rojo. Se usa una función de transferencia de identidad. Si se establece en FALSE, se aplica la función de transferencia gamma al canal rojo. El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/>                                                                                                                                                                                                                                                |
| GreenAmplitude<br/> AMPLITUD VERDE DE PROP GAMMATRANSFER D2D1 \_ \_ \_ \_<br/> | Amplitud de la función de transferencia gamma para el canal verde. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| GreenExponent<br/> EXPONENTE VERDE D2D1 \_ GAMMATRANSFER \_ PROP \_ \_<br/>   | Exponente de la función de transferencia gamma para el canal verde. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| GreenOffset<br/> D2D1 \_ GAMMATRANSFER \_ PROP \_ GREEN \_ OFFSET<br/>       | Desplazamiento de la función de transferencia gamma para el canal verde. El tipo es FLOAT.<br/> El valor predeterminado es 0,0f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| GreenDisable<br/> D2D1 \_ GAMMATRANSFER \_ PROP \_ GREEN \_ DISABLE<br/>     | Si establece esta opción en TRUE, no se aplica la función de transferencia al canal verde. Se usa una función de transferencia de identidad. Si se establece en FALSE, se aplica la función de transferencia gamma al canal verde. El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/>                                                                                                                                                                                                                                            |
| BlueAmplitude<br/> AMPLITUD AZUL DE PROP GAMMATRANSFER D2D1 \_ \_ \_ \_<br/>   | Amplitud de la función de transferencia gamma para el canal azul. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| BlueExponent<br/> EXPONENTE AZUL DE \_ PROP GAMMATRANSFER D2D1 \_ \_ \_<br/>     | Exponente de la función de transferencia gamma para el canal azul. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| BlueOffset<br/> D2D1 \_ GAMMATRANSFER \_ PROP \_ BLUE \_ OFFSET<br/>         | Desplazamiento de la función de transferencia gamma para el canal azul. El tipo es FLOAT.<br/> El valor predeterminado es 0,0f.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| BlueDisable<br/> D2D1 \_ GAMMATRANSFER \_ PROP \_ BLUE \_ DISABLE<br/>       | Si se establece en TRUE, no se aplica la función de transferencia al canal Azul. Se usa una función de transferencia de identidad. Si se establece en FALSE, se aplica la función de transferencia gamma al canal azul. El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/>                                                                                                                                                                                                                                              |
| AlphaAmplitude<br/> AMPLITUD ALFA DE PROP GAMMATRANSFER D2D1 \_ \_ \_ \_<br/> | Amplitud de la función de transferencia gamma para el canal alfa. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| AlphaExponent<br/> EXPONENTE ALFA DE \_ PROP \_ \_ GAMMATRANSFER D2D1 \_<br/>   | Exponente de la función de transferencia gamma para el canal alfa. El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| AlphaOffset<br/> D2D1 \_ GAMMATRANSFER \_ PROP \_ ALPHA \_ OFFSET<br/>       | Desplazamiento de la función de transferencia gamma para el canal alfa. El tipo es FLOAT.<br/> El valor predeterminado es 0,0f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| AlphaDisable<br/> D2D1 \_ GAMMATRANSFER \_ PROP \_ ALPHA \_ DISABLE<br/>     | Si establece esta opción en TRUE, no se aplica la función de transferencia al canal alfa. Se usa una función de transferencia de identidad. Si establece esta opción en FALSE, se aplica la función de transferencia gamma al canal alfa. El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/>                                                                                                                                                                                                                                            |
| ClampOutput<br/> SALIDA DE LA FIJACIÓN DE \_ PROP DE GAMMATRANSFER D2D1 \_ \_ \_<br/>       | Si el efecto fija los valores de color a entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto en el gráfico. El efecto fija los valores antes de multiplicar previamente el alfa .<br/> Si establece esta opción en TRUE, el efecto fijará los valores. Si establece esta opción en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no tienen una precisión lo suficientemente alta.<br/> El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/> |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del mapa de bits de salida es el mismo que el tamaño del mapa de bits de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio Windows aplicaciones de la \| Tienda\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio Windows aplicaciones de la \| Tienda\] |
| Encabezado                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


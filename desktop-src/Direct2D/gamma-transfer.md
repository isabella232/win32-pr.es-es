---
title: Efecto de transferencia gamma
description: Use el efecto de transferencia gamma para asignar las intensidades de color de una imagen mediante una función gamma creada mediante una amplitud, un exponente y un desplazamiento que proporcione para cada canal.
ms.assetid: 0E0455CA-CFCA-4C4F-9DFA-1DB6A5205F6A
keywords:
- efecto de transferencia gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b806ac8f59efe1b3fad3b61edc7f88f72b143f9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905436"
---
# <a name="gamma-transfer-effect"></a>Efecto de transferencia gamma

Use el efecto de transferencia gamma para asignar las intensidades de color de una imagen mediante una función gamma creada mediante una amplitud, un exponente y un desplazamiento que proporcione para cada canal.

El CLSID para este efecto es CLSID \_ D2D1GammaTransfer. Para usar este efecto, agregue dxguid. lib a las dependencias del enlazador.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                         |
|----------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)     |
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

La intensidad del píxel de entrada se representa como C y la intensidad del píxel de salida como C. C ' = \* <sup>exponente</sup> de amplitud C + desplazamiento

Este efecto funciona en imágenes alfa directas y premultiplicadas. El efecto genera mapas de bits alfa premultiplicados.

## <a name="effect-properties"></a>Propiedades del efecto

> [!Note]  
> Para todos los canales de las propiedades de transferencia gamma:
>
> -   El valor de amplitud no está limitado y no tiene unidades.
> -   El valor del exponente no está limitado y no tiene unidades.
> -   El valor de desplazamiento no está limitado y no tiene unidades.

 



| Enumeración de índice y nombre para mostrar                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedAmplitude<br/> \_ \_ \_ Amplitud roja de D2D1 \_ GAMMATRANSFER<br/>     | Amplitud de la función de transferencia gamma para el canal rojo. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| RedExponent<br/> \_ \_ \_ Exponente rojo de D2D1 GAMMATRANSFER prop \_<br/>       | Exponente de la función de transferencia gamma para el canal rojo. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| RedOffset<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ \_ desplazamiento rojo<br/>           | Desplazamiento de la función de transferencia gamma para el canal rojo. El tipo es FLOAT.<br/> El valor predeterminado es 0.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| RedDisable<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ rojo \_ deshabilitado<br/>         | Si se establece en TRUE, no se aplica la función de transferencia al canal rojo. Se utiliza una función de transferencia de identidad. Si se establece en FALSE, se aplica la función de transferencia gamma al canal rojo. El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/>                                                                                                                                                                                                                                                |
| GreenAmplitude<br/> \_ \_ \_ Amplitud verde de D2D1 \_ GAMMATRANSFER<br/> | Amplitud de la función de transferencia gamma para el canal verde. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| GreenExponent<br/> \_ \_ \_ Exponente verde \_ de D2D1 GAMMATRANSFER<br/>   | Exponente de la función de transferencia gamma para el canal verde. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| GreenOffset<br/> Desplazamiento verde de D2D1 \_ GAMMATRANSFER \_ prop \_ \_<br/>       | Desplazamiento de la función de transferencia gamma para el canal verde. El tipo es FLOAT.<br/> El valor predeterminado es 0.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| GreenDisable<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ verde \_ deshabilitada<br/>     | Si se establece en TRUE, no se aplica la función de transferencia al canal verde. Se utiliza una función de transferencia de identidad. Si se establece en FALSE, se aplica la función de transferencia gamma al canal verde. El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/>                                                                                                                                                                                                                                            |
| BlueAmplitude<br/> \_ \_ \_ Amplitud azul de D2D1 \_ GAMMATRANSFER<br/>   | Amplitud de la función de transferencia gamma para el canal azul. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| BlueExponent<br/> \_ \_ \_ Exponente azul de D2D1 GAMMATRANSFER prop \_<br/>     | Exponente de la función de transferencia gamma para el canal azul. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| BlueOffset<br/> Desplazamiento azul de la D2D1 \_ GAMMATRANSFER \_ prop \_ \_<br/>         | Desplazamiento de la función de transferencia gamma para el canal azul. El tipo es FLOAT.<br/> El valor predeterminado es 0.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| BlueDisable<br/> Deshabilitar D2D1 de GAMMATRANSFER de la \_ \_ prop \_ azul \_<br/>       | Si se establece en TRUE, no se aplica la función de transferencia al canal azul. Se utiliza una función de transferencia de identidad. Si se establece en FALSE, se aplica la función de transferencia gamma al canal azul. El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/>                                                                                                                                                                                                                                              |
| AlphaAmplitude<br/> \_ \_ \_ Amplitud alfa de D2D1 \_ GAMMATRANSFER<br/> | Amplitud de la función de transferencia gamma para el canal alfa. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| AlphaExponent<br/> \_ \_ \_ Exponente alfa \_ de D2D1 GAMMATRANSFER<br/>   | Exponente de la función de transferencia gamma para el canal alfa. El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| AlphaOffset<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ el \_ desplazamiento alfa<br/>       | Desplazamiento de la función de transferencia gamma para el canal alfa. El tipo es FLOAT.<br/> El valor predeterminado es 0.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| AlphaDisable<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ alpha \_ deshabilitada<br/>     | Si se establece en TRUE, no se aplica la función de transferencia al canal alfa. Se utiliza una función de transferencia de identidad. Si se establece en FALSE, se aplica la función de transferencia gamma al canal alfa. El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/>                                                                                                                                                                                                                                            |
| ClampOutput<br/> Salida de la abrazadera de D2D1 \_ GAMMATRANSFER \_ \_ \_<br/>       | Si el efecto fija los valores de color entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto del gráfico. El efecto fija los valores antes de que premultiplique el alfa.<br/> Si establece este valor en TRUE, el efecto fijará los valores. Si se establece en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no son de precisión lo suficientemente alta.<br/> El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/> |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del mapa de bits de salida es el mismo que el tamaño del mapa de bits de entrada.

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

 


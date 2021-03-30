---
title: Efecto de Desenfoque direccional
description: El efecto de Desenfoque direccional es similar al desenfoque gaussiano, salvo que puede sesgar el desenfoque en una dirección determinada.
ms.assetid: 59328FA4-5C27-4A81-AAB2-C5B25B3615C6
keywords:
- Desenfoque direccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e1c098d17929563cf69f4e61416fa0d93a88dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801040"
---
# <a name="directional-blur-effect"></a>Efecto de Desenfoque direccional

El efecto de Desenfoque direccional es similar al [Desenfoque gaussiano](gaussian-blur.md), salvo que puede sesgar el desenfoque en una dirección determinada. Puede usar este efecto para que una imagen tenga un aspecto como si estuviera en movimiento o para resaltar una imagen animada.

El CLSID para este efecto es CLSID \_ D2D1DirectionalBlur.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Modos de optimización](#optimization-modes)
-   [Modos de borde](#border-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                          |
|-----------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)      |
| Después                                                           |
| ![la imagen después de la transformación.](images/2-directionalblur.png) |



 


```C++
ComPtr<ID2D1Effect> directionalBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DirectionalBlur, &directionalBlurEffect);

directionalBlurEffect->SetInput(0, bitmap);
directionalBlurEffect->SetValue(D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, 7.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(directionalBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation<br/> \_ \_ \_ Desviación estándar de la D2D1 DIRECTIONALBLUR \_<br/> | Cantidad de desenfoque que se va a aplicar a la imagen. Puede calcular el radio de desenfoque del kernel multiplicando la desviación estándar por 3. Las unidades de la desviación estándar y el radio de desenfoque son DIP. Un valor de 0 DIP deshabilita este efecto. El tipo es FLOAT.<br/> El valor predeterminado es 3.0 f.<br/>                                                                            |
| Ángulo<br/> Ángulo de la D2D1 \_ DIRECTIONALBLUR \_ \_<br/>                           | Ángulo del desenfoque con respecto al eje x, en sentido contrario a las agujas del reloj. Las unidades se especifican en grados.<br/> El kernel de desenfoque se genera primero mediante el mismo proceso que para el efecto [Desenfoque gaussiano](gaussian-blur.md) . Después, los valores de kernel se transforman según el ángulo de desenfoque.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 0.0 f.<br/> |
| Optimization<br/> Optimización de D2D1 \_ DIRECTIONALBLUR \_ \_<br/>             | Modo de optimización. Vea [modos de optimización](#optimization-modes) para obtener más información.<br/> El tipo es D2D1 \_ DIRECTIONALBLUR \_ Optimization.<br/> El valor predeterminado es D2D1 \_ DIRECTIONALBLUR \_ optimizado de optimización \_ . <br/>                                                                                                                                                         |
| BorderMode<br/> D2D1 \_ DIRECTIONALBLUR \_ \_ modo de borde \_ de la Prop<br/>               | El modo que se usa para calcular el borde de la imagen, es decir, es flexible o difícil. Vea [modos de borde](#border-modes) para obtener más información.<br/> El tipo es D2D1 \_ Border \_ mode.<br/> El valor predeterminado es D2D1 \_ Border \_ Mode \_ .<br/>                                                                                                                                                                 |



 

## <a name="optimization-modes"></a>Modos de optimización



| Nombre                                          | Descripción                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Velocidad de optimización de D2D1 \_ DIRECTIONALBLUR \_ \_    | Aplica las optimizaciones internas, como el escalado previo en radios relativamente pequeños. Utiliza el filtrado lineal.                                  |
| Optimización de D2D1 \_ DIRECTIONALBLUR \_ \_ equilibrada | Usa los mismos umbrales de optimización que el modo de velocidad, pero utiliza el filtrado trilineal.                                                    |
| Calidad de optimización de D2D1 \_ DIRECTIONALBLUR \_ \_  | Solo usa optimizaciones internas con radios de desenfoque grandes, donde es menos probable que las aproximaciones sean visibles. Utiliza el filtrado trilineal. |



 

## <a name="border-modes"></a>Modos de borde



| Nombre                     | Descripción                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ modo de borde \_ \_ flexible | El efecto rellena la imagen con píxeles negros transparentes cuando aplica el kernel de desenfoque, lo que da lugar a un borde flexible. <br/>                                                                                             |
| D2D1 \_ del \_ modo de borde \_ | El efecto fija la salida al tamaño de la imagen de entrada. Cuando el efecto aplica el kernel de desenfoque, extiende la imagen de entrada con una transformación de borde de tipo de reflejo para las muestras fuera de los límites de entrada.<br/> |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del mapa de bits de salida aumenta en función de la desviación estándar, el ángulo del efecto y el modo de borde. Si el modo de borde se establece en el \_ modo de borde D2D1 \_ \_ , aumenta el tamaño del mapa de bits de salida en función del tamaño del kernel de desenfoque, representado en píxeles. Estas ecuaciones se pueden usar para calcular el tamaño del mapa de bits de salida.



| Requisito | Value |
|------------------------|-------------------------------------------------------------------|
| Crecimiento de mapa de bits de salida X | StandardDeviation (DIP) \* 6 \* ((PPP del usuario)/96) \* cos (ángulo)) |
| Crecimiento de mapa de bits de salida Y | StandardDeviation (DIP) \* 6 \* ((PPP del usuario)/96) \* sin (ángulo) |



 

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

 


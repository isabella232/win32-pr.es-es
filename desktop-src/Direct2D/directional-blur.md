---
title: Efecto de desenfoque direccional
description: El efecto de desenfoque direccional es similar al desenfoque gaussiano, salvo que se puede sesgar el desenfoque en una dirección determinada.
ms.assetid: 59328FA4-5C27-4A81-AAB2-C5B25B3615C6
keywords:
- desenfoque direccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e1c098d17929563cf69f4e61416fa0d93a88dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163333"
---
# <a name="directional-blur-effect"></a>Efecto de desenfoque direccional

El efecto de desenfoque direccional es similar al [desenfoque gaussiano,](gaussian-blur.md)salvo que se puede sesgar el desenfoque en una dirección determinada. Puede usar este efecto para que una imagen tenga un aspecto similar a si está en movimiento o para resaltar una imagen animada.

El CLSID para este efecto es CLSID \_ D2D1DirectionalBlur.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Modos de optimización](#optimization-modes)
-   [Modos de borde](#border-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo



| Antes                                                          |
|-----------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg)      |
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



## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation<br/> DESVIACIÓN ESTÁNDAR DE LA PROPIEDAD DIRECTIONALBLUR D2D1 \_ \_ \_ \_<br/> | Cantidad de desenfoque que se va a aplicar a la imagen. Puede calcular el radio de desenfoque del kernel multiplicando la desviación estándar por 3. Las unidades de desviación estándar y radio de desenfoque son DIP. Un valor de 0 DIP deshabilita este efecto. El tipo es FLOAT.<br/> El valor predeterminado es 3,0f.<br/>                                                                            |
| Ángulo<br/> ÁNGULO DE PROP \_ DIRECCIONAL D2D1BLUR \_ \_<br/>                           | Ángulo del desenfoque con respecto al eje X, en la dirección en sentido contrario a las agujas del reloj. Las unidades se especifican en grados.<br/> El kernel de desenfoque se genera primero con el mismo proceso que para el [efecto de desenfoque gaussiano.](gaussian-blur.md) A continuación, los valores del kernel se transforman según el ángulo de desenfoque.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 0,0f.<br/> |
| Optimization<br/> OPTIMIZACIÓN DE LA PROPIEDAD DIRECTIONALBLUR D2D1 \_ \_ \_<br/>             | Modo de optimización. Consulte [Modos de optimización](#optimization-modes) para obtener más información.<br/> El tipo es D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION.<br/> El valor predeterminado es D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION \_ BALANCED. <br/>                                                                                                                                                         |
| BorderMode<br/> D2D1 \_ DIRECTIONALBLUR \_ PROP \_ BORDER \_ MODE<br/>               | Modo que se usa para calcular el borde de la imagen, de forma flexible o dura. Consulte [Modos de borde](#border-modes) para obtener más información.<br/> El tipo es D2D1 \_ BORDER \_ MODE.<br/> El valor predeterminado es D2D1 \_ BORDER \_ MODE \_ SOFT.<br/>                                                                                                                                                                 |



 

## <a name="optimization-modes"></a>Modos de optimización



| Nombre                                          | Descripción                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| VELOCIDAD DE OPTIMIZACIÓN \_ DIRECTIONALBLUR D2D1 \_ \_    | Aplica optimizaciones internas, como el escalado previo a radios relativamente pequeños. Usa el filtrado lineal.                                  |
| D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION \_ BALANCED | Usa los mismos umbrales de optimización que el modo velocidad, pero usa el filtrado trilineal.                                                    |
| D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION \_ QUALITY  | Solo usa optimizaciones internas con radios de desenfoque grandes, donde es menos probable que las aproximaciones sean visibles. Usa el filtrado trilineal. |



 

## <a name="border-modes"></a>Modos de borde



| Nombre                     | Descripción                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODO DE BORDE D2D1 \_ \_ \_ SOFT | El efecto aplica píxeles de color negro transparente a la imagen a medida que aplica el kernel de desenfoque, lo que da lugar a un borde suave. <br/>                                                                                             |
| D2D1 \_ BORDER \_ MODE \_ HARD | El efecto fija la salida al tamaño de la imagen de entrada. Cuando el efecto aplica el kernel de desenfoque, extiende la imagen de entrada con una transformación de borde de tipo reflejo para muestras fuera de los límites de entrada.<br/> |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del mapa de bits de salida aumenta en función de la desviación estándar, el ángulo del efecto y el modo de borde. Si el modo de borde se establece en D2D1 BORDER MODE SOFT, el tamaño del mapa de bits de salida aumenta según el tamaño del kernel de desenfoque, representado \_ \_ en \_ píxeles. Estas ecuaciones se pueden usar para calcular el tamaño del mapa de bits de salida.



| Requisito | Value |
|------------------------|-------------------------------------------------------------------|
| Crecimiento del mapa de bits de salida X | StandardDeviation (DIP) \* 6 \* ((User DPI) / 96) \* cos(Angle)) |
| Crecimiento del mapa de bits de salida Y | StandardDeviation (DIP) \* 6 \* ((PPP de usuario) / 96) \* sin(Angle)) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio \| Windows store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio \| Windows store\] |
| Encabezado                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 


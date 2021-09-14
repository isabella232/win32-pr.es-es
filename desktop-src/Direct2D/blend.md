---
title: Efecto de fusión
description: Use el efecto blend para combinar 2 imágenes. Este efecto tiene 26 modos de combinación.
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- efecto blend
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853043123c6eea9a87656a7450b1295236ed5d6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164245"
---
# <a name="blend-effect"></a>Efecto de fusión

Use el efecto blend para combinar 2 imágenes. Este efecto tiene 26 modos de combinación.

El CLSID para este efecto es CLSID \_ D2D1Blend.

-   [Ejemplos de combinación](#blending-examples)
-   [Propiedades de efecto](#effect-properties)
-   [Modos de blend](#blend-modes)
-   [Conversiones de espacios de color HSL](#hsl-color-space-conversions)
    -   [Conversión de RGB a HSL](#converting-from-rgb-to-hsl)
    -   [Conversión de HSL a RGB](#converting-from-hsl-to-rgb)
-   [Mapa de bits de salida](#output-bitmap)
-   [Código de ejemplo](#sample-code)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="blending-examples"></a>Ejemplos de combinación

Esta es una imagen de ejemplo de cada modo de combinación del efecto de mezcla. En la sección siguiente se muestra una lista completa de los modos de combinación y las propiedades de modo correspondientes.

![captura de pantalla de ejemplo de efecto de todos los modos de combinación disponibles.](images/blend-modes.png)

Este es otro ejemplo de uso del modo de exclusión.



| Antes de la imagen 1                                                             |
|----------------------------------------------------------------------------|
| ![la primera imagen de origen antes del efecto.](images/default-before.jpg)    |
| Antes de la imagen 2                                                             |
| ![la segunda imagen antes del efecto.](images/4-arthimetic-composite2.jpg) |
| Después                                                                      |
| ![la imagen después de la transformación.](images/5-blend.png)                      |



 


```C++
ComPtr<ID2D1Effect> blendEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Blend, &blendEffect);

blendEffect->SetInput(0, bitmap);
blendEffect->SetInput(1, bitmapTwo);
blendEffect->SetValue(D2D1_BLEND_PROP_MODE, D2D1_BLEND_MODE_EXCLUSION);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(blendEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                 | Descripción                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode<br/> D2D1 \_ BLEND \_ PROP \_ MODE<br/> | Modo de combinación utilizado para el efecto. Consulte [Modos de Blend](#blend-modes) para obtener más información. El tipo es D2D1 \_ BLEND \_ MODE.<br/> El valor predeterminado es D2D1 \_ BLEND \_ MODE \_ MULTIPLY.<br/> |



 

## <a name="blend-modes"></a>Modos de fusión

En la tabla siguiente se muestran todos los modos de combinación de este efecto. Las funciones auxiliares necesarias para calcular la salida del efecto se encuentran en la sección siguiente.

Color: O <sub>PRGB</sub>  =  *f*(F <sub>RGB</sub>, B <sub>RGB</sub>) F A \* B <sub></sub> \* <sub>A</sub> + F <sub>RGB</sub> \* F <sub>A</sub> \* (1 - B <sub>A</sub>) + B <sub>RGB</sub> \* B <sub>A</sub> \* (1 - F <sub>A</sub>)

Alfa: O<sub>A</sub> = F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>A</sub>

Donde:

-   O<sub>PRGB es</sub> el color de salida multiplicado previamente
-   O<sub>A</sub> es alfa de salida
-   B<sub>RGB es</sub> el color de destino no multiplicado previamente
-   B<sub>A es</sub> alfa de destino
-   F<sub>RGB es</sub> el color de origen no multiplicado previamente
-   F<sub>A es</sub> alfa de origen
-   *f*(S <sub>RGB</sub>, D <sub>RGB</sub>) es una función de combinación que varía por modo de mezcla

Algunos de los modos de combinación requieren la conversión a y desde el espacio de color matiz, saturación, luminosidad (HSL) a RGB.




| Enumeración | Ecuación | 
|-------------|----------|
| D2D1_BLEND_MODE_DARKEN | Fórmula de combinación básica solo para alfa. <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /> | 
| D2D1_BLEND_MODE_MULTIPLY | Fórmula de combinación básica solo para alfa. <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /> | 
| D2D1_BLEND_MODE_COLOR_BURN | Fórmulas de combinación básicas <em>con f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /> | 
| D2D1_BLEND_MODE_LINEAR_BURN | Fórmulas de combinación básicas <em>con f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /> | 
| D2D1_BLEND_MODE_DARKER_COLOR | Fórmula de combinación básica solo para alfa. <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /> | 
| D2D1_BLEND_MODE_LIGHTEN | Fórmula de combinación básica solo para alfa. <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /> | 
| D2D1_BLEND_MODE_SCREEN | Fórmula de combinación básica solo para alfa. <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /> | 
| D2D1_BLEND_MODE_COLOR_DODGE | Fórmulas de combinación básicas <em>con f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /> | 
| D2D1_BLEND_MODE_LINEAR_DODGE | Fórmulas de combinación básicas <em>con f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /> | 
| D2D1_BLEND_MODE_LIGHTER_COLOR | Fórmula de combinación básica solo para alfa. <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /> | 
| D2D1_BLEND_MODE_OVERLAY | Fórmulas de combinación básicas <em>con f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /> | 
| D2D1_BLEND_MODE_SOFT_LIGHT | Fórmulas de combinación básicas <em>con f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /> | 
| D2D1_BLEND_MODE_HARD_LIGHT | Fórmulas de combinación básicas <em>con f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /> | 
| D2D1_BLEND_MODE_VIVID_LIGHT | Fórmulas de combinación básicas <em>con f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /> | 
| D2D1_BLEND_MODE_LINEAR_LIGHT | Fórmulas de combinación básicas <em>con f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /> | 
| D2D1_BLEND_MODE_PIN_LIGHT | Fórmulas de combinación básicas <em>con f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /> | 
| D2D1_BLEND_MODE_HARD_MIX | Fórmulas de combinación básicas <em>con f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /> | 
| D2D1_BLEND_MODE_DIFFERENCE | Fórmulas de combinación básicas <em>con f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = abs(F<sub>RGB</sub> - B<sub>RGB</sub>) | 
| D2D1_BLEND_MODE_EXCLUSION | Fórmulas de mezcla básicas <em>con f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + B<sub>RGB</sub>   2 * F<sub>RGB</sub> * B<sub>RGB</sub> | 
| D2D1_BLEND_MODE_HUE | Fórmula de combinación básica solo para alfa. <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /> | 
| D2D1_BLEND_MODE_SATURATION | Fórmula de combinación básica solo para alfa. <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /> | 
| D2D1_BLEND_MODE_COLOR | Fórmula de combinación básica solo para alfa. <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /> | 
| D2D1_BLEND_MODE_LUMINOSITY | Fórmula de combinación básica solo para alfa. <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /> | 
| D2D1_BLEND_MODE_DISSOLVE | Con estas premisas:<ul><li>Una coordenada de escena XY para el píxel actual</li><li>Generador de números pseudo aleatorios determinista rand(XY) basado en la coordenada de valor de ed. XY, con distribución no sesgo de valores de [0, 1]</li></ul><br /><img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br /> | 
| D2D1_BLEND_MODE_SUBTRACT | Fórmula de mezcla básica solo para alfa. <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /> | 
| D2D1_BLEND_MODE_DIVISION | Fórmula de mezcla básica solo para alfa. <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /> | 




 

> [!Note]  
> Para todos los modos de Blend, el valor de salida se multiplica previamente y se fija en el \[ intervalo 0, 1 \] .

 

## <a name="hsl-color-space-conversions"></a>Conversiones de espacio de color HSL

El componente de luminosidad se calcula con los pesos RGB aquí:

-   *k*<sub>R</sub> = 0,30
-   *k*<sub>G</sub> = 0,59
-   *k*<sub>B</sub> = 0,11

### <a name="converting-from-rgb-to-hsl"></a>Conversión de RGB a HSL

![fórmula matemática que describe la transformación de color rgb a color hsl.](images/blend-rgb-to-hsl-1.png)

Esto coloca *S* y *L en* el intervalo \[ 0.0, 1.0 y H en el \] intervalo  \[ -1.0, 5.0 \] .

### <a name="converting-from-hsl-to-rgb"></a>Conversión de HSL a RGB

Para convertir la otra manera en que usamos el inverso de los cálculos anteriores.

Si *S* = 0, *R*  =  *G*  =  *B*  =  *L*

De lo contrario, hay seis casos dependientes de hue:

Si *H* es mayor que 0, los valores se encuentran en el sector rojo/después, *donde R*  >  *B*  >  *G*.

![ecuación matemática paso uno de los seis que convierten el color hsl a rgb.](images/blend-hsl-to-rgb-1rm.png)

Si *H* es mayor o igual que 0 y menor que 1, los valores se encuentran en el sector rojo/amarillo donde *R*  >  *G*  >  *B*.

![ecuación matemática, paso dos de seis, que convierte el color hsl en rgb.](images/blend-hsl-to-rgb-1ry.png)

Si *H* es mayor o igual que 1 y menor que 2, los valores se encuentran en el sector amarillo/verde donde *G*  >  *R*  >  *B*.

![ecuación matemática, paso tres de seis, que convierte el color hsl en rgb.](images/blend-hsl-to-rgb-1yg.png)

Si *H* es mayor o igual que 2 y menor que 3, los valores se encuentran en el sector verde/verde-verde donde *G*  >  *B*  >  *R*.

![ecuación matemática, paso cuatro de seis, que convierte el color hsl en rgb.](images/blend-hsl-to-rgb-1gc.png)

Si *H* es mayor o igual que 3 y menor que 4, los valores se encuentran en el sector azul/azul donde *B*  >  *G*  >  *R*.

![ecuación matemática, paso cinco de seis, que convierte el color hsl a rgb.](images/blend-hsl-to-rgb-1cb.png)

Si *H* es mayor o igual que 4, los valores se encuentran en el sector blue/blue/magenta donde *B*  >  *R*  >  *G*.

![ecuación matemática, paso seis de seis, que convierte el color hsl en rgb.](images/blend-hsl-to-rgb-1bm.png)

Dado que los modos de combinación hacen combinaciones arbitrarias de componentes HSL de dos colores diferentes, es habitual que el valor RGB convertido esté fuera de la gama, es decir, uno o varios componentes de canal pueden estar fuera del intervalo legal de \[ 0,0, 1,0 \] . Estos colores se han vuelto a la gama al reducir mínimamente la saturación, conservando al mismo tiempo el matiz y la luminosidad:

![fórmula matemática que describe las correcciones necesarias para instancias fuera de la gama.](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a>Mapa de bits de salida

El mapa de bits de salida para este efecto siempre es el tamaño de la unión de las dos imágenes de entrada.

## <a name="sample-code"></a>Código de ejemplo

Para obtener un ejemplo de este efecto, descargue el ejemplo de modos de efecto compuesto [de Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).

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

 


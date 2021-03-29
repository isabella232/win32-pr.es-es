---
title: Efecto de fusión
description: Use el efecto de mezcla para combinar dos imágenes. Este efecto tiene 26 modos de mezcla.
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- efecto de mezcla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e248d1f7f41721d173510b8d10feac9be2e08f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905579"
---
# <a name="blend-effect"></a>Efecto de fusión

Use el efecto de mezcla para combinar dos imágenes. Este efecto tiene 26 modos de mezcla.

El CLSID para este efecto es CLSID \_ D2D1Blend.

-   [Ejemplos de fusión](#blending-examples)
-   [Propiedades del efecto](#effect-properties)
-   [Modos de fusión](#blend-modes)
-   [Conversiones de espacio de color HSL](#hsl-color-space-conversions)
    -   [Convertir de RGB a HSL](#converting-from-rgb-to-hsl)
    -   [Convertir de HSL a RGB](#converting-from-hsl-to-rgb)
-   [Mapa de bits de salida](#output-bitmap)
-   [Código de ejemplo](#sample-code)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="blending-examples"></a>Ejemplos de fusión

Esta es una imagen de ejemplo de cada modo de mezcla del efecto de mezcla. En la siguiente sección se muestra una lista completa de los modos de mezcla y las propiedades de modo correspondientes.

![captura de pantalla de ejemplo de efecto de todos los modos de fusión disponibles.](images/blend-modes.png)

Este es otro ejemplo que usa el modo de exclusión.



| Antes de la imagen 1                                                             |
|----------------------------------------------------------------------------|
| ![primera imagen de origen antes del efecto.](images/default-before.jpg)    |
| Antes de la imagen 2                                                             |
| ![segunda imagen anterior al efecto.](images/4-arthimetic-composite2.jpg) |
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



## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                 | Descripción                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode<br/> Modo de D2D1 \_ Blend \_ \_<br/> | Modo de mezcla que se usa para el efecto. Vea [modos de mezcla](#blend-modes) para obtener más información. El tipo es D2D1 \_ Blend \_ mode.<br/> El valor predeterminado es D2D1 \_ Blend \_ Mode \_ multiplicate.<br/> |



 

## <a name="blend-modes"></a>Modos de fusión

En la tabla siguiente se muestran todos los modos de Blend de este efecto. Las funciones auxiliares necesarias para calcular el resultado del efecto se encuentran en la sección siguiente.

Color: O <sub>PRGB</sub>  =  *f*(f <sub>RGB</sub>, B <sub>RGB</sub>) \* f <sub>a</sub> \* B <sub>a</sub> + f <sub>RGB</sub> \* f <sub>a</sub> \* (1-B <sub>a</sub>) + B <sub>RGB</sub> \* b <sub>a</sub> \* (1-f <sub>a</sub>)

Alfa: O<sub>a</sub> = F<sub>a</sub> \* (1-B<sub>a</sub>) + B<sub>a</sub>

Donde:

-   O<sub>PRGB</sub> es el color de salida multiplicado previamente
-   O es alfa<sub>de</sub> salida
-   B<sub>RGB</sub> es el color de destino no multiplicado previamente
-   B<sub>A es el</sub> destino Alfa
-   F<sub>RGB</sub> es el color de origen sin premultiplicado
-   F<sub>A</sub> es alfa de origen
-   *f*(S <sub>RGB</sub>, D <sub>RGB</sub>) es una función de Blend que varía según el modo de mezcla.

Algunos de los modos de mezcla requieren la conversión del espacio de colores Hue, saturación y luminosidad (HSL) a RGB.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Enumeración</th>
<th>Ecuación</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D2D1_BLEND_MODE_DARKEN</td>
<td>Fórmula básica de Blend solo para alpha. <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_MULTIPLY</td>
<td>Fórmula básica de Blend solo para alpha. <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_COLOR_BURN</td>
<td>Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_LINEAR_BURN</td>
<td>Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_DARKER_COLOR</td>
<td>Fórmula básica de Blend solo para alpha. <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_LIGHTEN</td>
<td>Fórmula básica de Blend solo para alpha. <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_SCREEN</td>
<td>Fórmula básica de Blend solo para alpha. <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_COLOR_DODGE</td>
<td>Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_LINEAR_DODGE</td>
<td>Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_LIGHTER_COLOR</td>
<td>Fórmula básica de Blend solo para alpha. <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_OVERLAY</td>
<td>Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_SOFT_LIGHT</td>
<td>Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_HARD_LIGHT</td>
<td>Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_VIVID_LIGHT</td>
<td>Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_LINEAR_LIGHT</td>
<td>Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_PIN_LIGHT</td>
<td>Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_HARD_MIX</td>
<td>Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_DIFFERENCE</td>
<td>Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = ABS (f<sub>RGB</sub> - B<sub>RGB</sub>)</td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_EXCLUSION</td>
<td>Fórmulas básicas de Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + b<sub>RGB</sub>   2 * f<sub>RGB</sub> * b<sub>RGB</sub></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_HUE</td>
<td>Fórmula básica de Blend solo para alpha. <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_SATURATION</td>
<td>Fórmula básica de Blend solo para alpha. <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_COLOR</td>
<td>Fórmula básica de Blend solo para alpha. <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_LUMINOSITY</td>
<td>Fórmula básica de Blend solo para alpha. <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_DISSOLVE</td>
<td>Con estas premisas:
<ul>
<li>Coordenadas de la escena XY para el píxel actual.</li>
<li>El generador de números pseudoaleatorios deterministas Rand (XY) basado en la coordenada de inicialización XY, con distribución no sesgada de valores de [0, 1]</li>
</ul>
<br/> <img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br/></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_SUBTRACT</td>
<td>Fórmula básica de Blend solo para alpha. <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_DIVISION</td>
<td>Fórmula básica de Blend solo para alpha. <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> En todos los modos de fusión, el valor de salida se multiplica previamente y se fija en el intervalo de \[ 0, 1 \] .

 

## <a name="hsl-color-space-conversions"></a>Conversiones de espacio de color HSL

El componente luminosidad se calcula con los pesos RGB aquí:

-   *k*<sub>R</sub> = 0,30
-   *k*<sub>G</sub> = 0,59
-   *k*<sub>B</sub> = 0,11

### <a name="converting-from-rgb-to-hsl"></a>Convertir de RGB a HSL

![fórmula matemática que describe la transformación de color RGB a color HSL.](images/blend-rgb-to-hsl-1.png)

Esto coloca *S* y *L* en el intervalo \[ 0,0, 1,0 \] y *H* en el intervalo \[ -1,0, 5,0 \] .

### <a name="converting-from-hsl-to-rgb"></a>Convertir de HSL a RGB

Para convertir la otra manera, usamos el inverso de los cálculos anteriores.

Si *S* = 0, entonces *R*  =  *G*  =  *B*  =  *L*

De lo contrario, hay seis casos dependientes de matiz:

Si *H* es mayor que 0, los valores se encuentran en el sector rojo/magenta donde *R*  >  *B*  >  *G*.

![equaiton matemático paso 1 de seis conversión del color HSL a RGB.](images/blend-hsl-to-rgb-1rm.png)

Si *H* es mayor o igual que 0 y menor que 1, los valores se encuentran en el sector rojo/amarillo donde *R*  >  *G*  >  *B*.

![equaiton matemático paso 2 de seis conversión del color HSL a RGB.](images/blend-hsl-to-rgb-1ry.png)

Si *H* es mayor o igual que 1 y menor que 2, los valores se encuentran en el sector amarillo/verde donde *G*  >  *R*  >  *B*.

![equaiton matemático paso tres de seis conversión del color HSL a RGB.](images/blend-hsl-to-rgb-1yg.png)

Si *H* es mayor o igual que 2 y menor que 3, los valores se encuentran en el sector verde/aguamarina donde *G*  >  *B*  >  *R*.

![equaiton matemático paso cuatro de seis conversión del color HSL a RGB.](images/blend-hsl-to-rgb-1gc.png)

Si *H* es mayor o igual que 3 y menor que 4, los valores se encuentran en el sector cian/azul donde *B*  >  *G*  >  *R*.

![equaiton matemático paso cinco de seis conversión del color HSL a RGB.](images/blend-hsl-to-rgb-1cb.png)

Si *H* es mayor o igual que 4, los valores se encuentran en el sector azul/magenta donde *B*  >  *R*  >  *G*.

![equaiton matemático paso seis de seis conversión del color HSL a RGB.](images/blend-hsl-to-rgb-1bm.png)

Dado que los modos de mezcla realizan combinaciones arbitrarias de componentes HSL de dos colores diferentes, es habitual que el valor RGB convertido sea fuera de gama, es decir, uno o varios componentes del canal pueden estar fuera del intervalo legal de \[ 0,0, 1,0 \] . Estos colores se vuelven a la gama reduciendo mínimamente la saturación, al tiempo que se conservan el matiz y la luminosidad:

![fórmula matemática que describe las correcciones necesarias para las instancias fuera de la gama.](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a>Mapa de bits de salida

El mapa de bits de salida para este efecto es siempre el tamaño de la Unión de las dos imágenes de entrada.

## <a name="sample-code"></a>Código de ejemplo

Para obtener un ejemplo de este efecto, descargue el [ejemplo de modos de efecto compuesto de Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).

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

 


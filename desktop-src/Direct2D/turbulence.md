---
title: Efecto de refluencia
description: Use el efecto de rebulencia para generar un mapa de bits basado en la función de ruido perlin.
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- efecto de bombilla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f2aa58be48c759956fe3522812d7ad6c3e9989
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162526"
---
# <a name="turbulence-effect"></a>Efecto de refluencia

Use el efecto de rebulencia para generar un mapa de bits basado en la función de ruido perlin.

El efecto de refluencia no tiene ninguna imagen de entrada.

El CLSID para este efecto es CLSID \_ D2D1Turbulence.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Modos de ruido](#noise-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

![captura de pantalla de ejemplo de efecto que muestra la salida del efecto de la lebulencia.](images/32-turbulence.png)

El efecto Desalencia calcula la suma de uno o más octágdos de la función de ruido de Perlin. El ruido de perlin es una función pseudo aleatoria cuyo valor depende de la frecuencia, la posición y el valor de ed. El efecto genera los valores RGBA mediante una de estas ecuaciones.

Si selecciona el modo de ruido D2D1 \_ LEBULENCE \_ \_ NOISEUAL \_ SUM, el efecto usa esta ecuación.

![Captura de pantalla que muestra la función de refluencia usada para generar un mapa de bits.](images/turbulence-equation1.png)

Si selecciona el modo de ruido \_ D2D1FLUBULENCE \_ \_ NOISEFLUBULENCE, el efecto usa esta ecuación.

![la función de rebulencia usada para generar un mapa de bits.](images/turbulence-equation2.png)

> [!Note]  
> La `PerlinNoise` función tiene un intervalo de \[ -1, 1 \] .

 

Este efecto genera valores de píxel en alfa premultiplicado.

## <a name="effect-properties"></a>Propiedades de efecto




| Enumeración de nombre para mostrar e índice | Descripción | 
|------------------------------------|-------------|
| Offset<br /> D2D1_TURBULENCE_PROP_OFFSET<br /> | Coordenadas donde se genera la salida de la bombilla.<br /> El algoritmo utilizado para generar el ruido de Perlin depende de la posición, por lo que un desplazamiento diferente da como resultado una salida diferente. Esta propiedad no está limitada y las unidades se especifican en dip. <br /><blockquote>[!Note]<br />El desplazamiento no tiene el mismo efecto que una traducción porque la salida de la función de ruido es infinita y la función se ajustará alrededor del icono.</blockquote><br /> El tipo es D2D1_VECTOR_2F.<br /> El valor predeterminado es {0.0f, 0.0f}.<br /> | 
| Size<br /> D2D1_TURBULENCE_PROP_SIZE<br /> | Tamaño de la salida de la bombilla.<br /> Esta propiedad no está limitada y las unidades se especifican en dip. <br /><br /> El tipo es D2D1_VECTOR_2F.<br /> El valor predeterminado es {0.0f, 0.0f}.<br /> | 
| BaseFrequency<br /> D2D1_TURBULENCE_PROP_BASE_FREQUENCY<br /> | Frecuencias base en la dirección X e Y. Esta propiedad es float y debe ser mayor que 0. Las unidades se especifican en 1/DIP. <br /> Un valor de 1 (1/DIP) para la frecuencia base hace que el ruido de Perlin complete un ciclo completo entre dos píxeles. La interpolación sencilla de estos píxeles da como resultado píxeles completamente aleatorios, ya que no hay ninguna correlación entre ellos.<br /> Un valor de 0,1 (1/DIP) para la frecuencia base, la función de ruido de Perlin se repite cada 10 DIP. Esto da como resultado una correlación entre píxeles y el efecto típico de la lebulencia es visible.<br /> El tipo es D2D1_VECTOR_2F.<br /> El valor predeterminado es {0.01f, 0.01f}.<br /> | 
| NumOctaves<br /> D2D1_TURBULENCE_PROP_NUM_OCTAVES<br /> | Número de octaves para la función de ruido. Esta propiedad es un UINT32 y debe ser mayor que 0.<br /> El tipo es UINT32.<br /> El valor predeterminado es 1.<br /> | 
| Seed<br /> D2D1_TURBULENCE_PROP_SEED<br /> | Valor de valor de ed. para el generador pseudo aleatorio. Esta propiedad no está enlazar.<br /> El tipo es UINT32.<br /> El valor predeterminado es 0.<br /> | 
| Ruido<br /> D2D1_TURBULENCE_PROP_NOISE<br /> | Modo de ruido de rebulencia. Esta propiedad puede ser <em>sum o</em> <em>vabulence</em>. Indica si se va a generar un mapa de bits basado en ruido de Varon o en la función Vabulence. Consulte <a href="#noise-modes">Modos de ruido</a> para obtener más información. <br /> El tipo es D2D1_TURBULENCE_NOISE.<br /> El valor predeterminado es D2D1_TURBULENCE_NOISE_FRACTAL_SUM.<br /> | 
| Unida<br /> D2D1_TURBULENCE_PROP_STITCHABLE<br /> | Activa o desactiva la unión. La frecuencia base se ajusta para que se pueda unir el mapa de bits de salida. Esto resulta útil si desea crear un mosaico de varias copias de la salida del efecto de rebulencia.<ul><li>True El mapa de bits de salida puede estar en mosaico (mediante el efecto de mosaico) sin la apariencia de las juntas. La frecuencia base se ajusta para que se pueda unir el mapa de bits de salida.</li><li>False La frecuencia base no se ajusta, por lo que pueden aparecer las juntas entre los iconos si el mapa de bits está en mosaico.</li></ul><br /> El tipo es BOOL.<br /> El valor predeterminado es FALSE.<br /> | 




 

## <a name="noise-modes"></a>Modos de ruido



| Enumeración                           | Descripción                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| D2D1 \_ LEBULENCE \_ NOISE \_ SUM \_ | Calcula una suma de los octaves, desplazando el intervalo de salida \[ de -1, 1 , a \] \[ 0, 1 \] . |
| REFLUBULENCIA DE RUIDO DE \_ REFLUENCIA D2D1 \_ \_   | Calcula una suma del valor absoluto de cada octave.                                  |



 

> [!Note]  
> Ninguno de los dos modo contiene una fijación explícita de los valores de salida.

 

## <a name="output-bitmap"></a>Mapa de bits de salida

Este efecto genera un mapa de bits de tamaño lógico infinito.

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

 


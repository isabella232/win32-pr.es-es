---
title: Efecto de turbulencia
description: Use el efecto turbulencia para generar un mapa de bits basado en la función de ruido de Perlen.
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- efecto de turbulencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f67f615ec5b68ca285a048b68bc7bc8eab6e24
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104564507"
---
# <a name="turbulence-effect"></a>Efecto de turbulencia

Use el efecto turbulencia para generar un mapa de bits basado en la función de ruido de Perlen.

El efecto de turbulencia no tiene ninguna imagen de entrada.

El CLSID para este efecto es CLSID \_ D2D1Turbulence.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Modos de ruido](#noise-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

![captura de pantalla de ejemplo de efecto que muestra la salida del efecto de turbulencia.](images/32-turbulence.png)

El efecto de turbulencia calcula la suma de una o más octava de la función de ruido de Perlen. Perlen ruido es una función pseudoaleatorios cuyo valor depende de la frecuencia, la posición y el valor de inicialización. El efecto genera los valores RGBA mediante una de estas ecuaciones.

Si selecciona el modo de \_ ruido de D2D1 turbulencia \_ ruido \_ fractal \_ de la suma de ruido, el efecto utiliza esta ecuación.

![Captura de pantalla que muestra la función de turbulencias usada para generar un mapa de bits.](images/turbulence-equation1.png)

Si selecciona el modo de \_ \_ ruido de \_ turbulencias de ruido de D2D1, el efecto utiliza esta ecuación.

![la función turbulencias que se usa para generar un mapa de bits.](images/turbulence-equation2.png)

> [!Note]  
> La `PerlinNoise` función tiene un intervalo de \[ -1, 1 \] .

 

Este efecto produce valores de píxeles en alfa premultiplicado.

## <a name="effect-properties"></a>Propiedades del efecto



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Enumeración de índice y nombre para mostrar</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Offset<br/> D2D1_TURBULENCE_PROP_OFFSET<br/></td>
<td>Coordenadas donde se genera la salida de turbulencias.<br/> El algoritmo utilizado para generar el ruido de Perl es dependiente de la posición, por lo que un desplazamiento diferente da como resultado una salida diferente. Esta propiedad no está enlazada y las unidades se especifican en DIP <br/>
<blockquote>
[!Note]<br />
El desplazamiento no tiene el mismo efecto que una traducción porque la salida de la función de ruido es infinita y la función se ajustará alrededor del mosaico.
</blockquote>
<br/> El tipo es D2D1_VECTOR_2F.<br/> El valor predeterminado es {0.0 f, 0.0 f}.<br/></td>
</tr>
<tr class="even">
<td>Tamaño<br/> D2D1_TURBULENCE_PROP_SIZE<br/></td>
<td>Tamaño de la salida de turbulencia.<br/> Esta propiedad no está enlazada y las unidades se especifican en DIP <br/>
<br/> El tipo es D2D1_VECTOR_2F.<br/> El valor predeterminado es {0.0 f, 0.0 f}.<br/></td>
</tr>
<tr class="odd">
<td>BaseFrequency<br/> D2D1_TURBULENCE_PROP_BASE_FREQUENCY<br/></td>
<td>Frecuencias base en la dirección X e y. Esta propiedad es de tipo float y debe ser mayor que 0. Las unidades se especifican en 1/DIP. <br/> Un valor de 1 (1/DIP) para la frecuencia base da lugar a que el ruido de Perl complete un ciclo completo entre dos píxeles. La interpolación de facilidad para estos píxeles produce píxeles totalmente aleatorios, ya que no hay ninguna correlación entre los píxeles.<br/> Un valor de 0.1 (1/DIP) para la frecuencia de base, la función de ruido de Perl se repite cada 10 dip. Esto da como resultado una correlación entre píxeles y el efecto de turbulencia típico es visible.<br/> El tipo es D2D1_VECTOR_2F.<br/> El valor predeterminado es {0,01 f, 0,01 f}.<br/></td>
</tr>
<tr class="even">
<td>NumOctaves<br/> D2D1_TURBULENCE_PROP_NUM_OCTAVES<br/></td>
<td>El número de octavas para la función de ruido. Esta propiedad es un UINT32 y debe ser mayor que 0.<br/> El tipo es UINT32.<br/> El valor predeterminado es 1.<br/></td>
</tr>
<tr class="odd">
<td>Seed<br/> D2D1_TURBULENCE_PROP_SEED<br/></td>
<td>Inicialización del generador pseudoaleatorios. Esta propiedad no está enlazada.<br/> El tipo es UINT32.<br/> El valor predeterminado es 0.<br/></td>
</tr>
<tr class="even">
<td>Ruido<br/> D2D1_TURBULENCE_PROP_NOISE<br/></td>
<td>Modo de ruido de turbulencia. Esta propiedad puede ser <em>SUM</em> o <em>turbulencia</em>. Indica si se debe generar un mapa de bits basado en ruido fractal o en la función turbulencias. Vea <a href="#noise-modes">modos de ruido</a> para obtener más información. <br/> El tipo es D2D1_TURBULENCE_NOISE.<br/> El valor predeterminado es D2D1_TURBULENCE_NOISE_FRACTAL_SUM.<br/></td>
</tr>
<tr class="odd">
<td>Que se pudo unir<br/> D2D1_TURBULENCE_PROP_STITCHABLE<br/></td>
<td>Activa o desactiva la Unión. La frecuencia base se ajusta para que se pueda unir el mapa de bits de salida. Esto resulta útil si desea colocar en mosaico varias copias de la salida del efecto de turbulencias.
<ul>
<li>True el mapa de bits de salida se puede colocar en mosaico (con el efecto de mosaico) sin la apariencia de las costuras. La frecuencia base se ajusta para que se pueda unir el mapa de bits de salida.</li>
<li>False: no se ajusta la frecuencia base, por lo que pueden aparecer juntas entre mosaicos si el mapa de bits está en mosaico.</li>
</ul>
<br/> El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="noise-modes"></a>Modos de ruido



| Enumeración                           | Descripción                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| D2D1 \_ turbulencia \_ ruido \_ fractal- \_ suma | Calcula una suma de las octavas, desplazando el intervalo de salida de \[ -1, 1 \] , a \[ 0, 1 \] . |
| Turbulencia de ruido de D2D1 de \_ turbulencias \_ \_   | Calcula una suma del valor absoluto de cada octava.                                  |



 

> [!Note]  
> Ninguno de los modos contiene una abrazadera explícita de los valores de salida.

 

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

 


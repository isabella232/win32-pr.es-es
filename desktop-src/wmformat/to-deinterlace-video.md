---
title: Para Desentrelazar vídeo
description: Para Desentrelazar vídeo
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- SDK de Windows Media Format, vídeo desentrelazado
- Windows Media Format SDK, Telecine inverso
- SDK de Windows Media Format, telecine
- Advanced Systems Format (ASF), vídeo desentrelazado
- ASF (formato de sistemas avanzados), vídeo desentrelazado
- Advanced Systems Format (ASF), Telecine inverso
- ASF (formato de sistemas avanzados), Telecine inverso
- Advanced Systems Format (ASF), telecine
- ASF (formato de sistemas avanzados), telecine
- vídeo desentrelazado
- Telecine inverso, acerca de
- Telecine, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580b8425e5807fefdfa889fcd08deedb4143cf39
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077330"
---
# <a name="to-deinterlace-video"></a>Para Desentrelazar vídeo

Algunos orígenes de vídeo, como las tarjetas de captura de vídeo, proporcionan datos de vídeo para la visualización entrelazada. Cada fotograma de vídeo entrelazado se compone de dos campos. El campo superior contiene la primera línea de vídeo y todas las demás líneas a partir de entonces. El campo inferior contiene la segunda línea de vídeo y todas las demás líneas posteriores. Por lo tanto, un campo contiene todas las líneas pares y la otra contiene todas las líneas con número impar. Los campos que componen un fotograma representan tiempos de presentación ligeramente diferentes, de modo que, cuando se intercalan, no forman una imagen estática.

Si desea mostrar vídeo en un monitor de equipo, cada fotograma del vídeo debe mostrarse como una imagen (este método de visualización de vídeo de un fotograma completo a la vez se denomina vídeo *progresivo* ). Si muestra vídeo entrelazado progresivamente, es posible que los fotogramas no tengan el aspecto correcto, debido a la diferencia de tiempo entre los dos campos. El códec de Windows Media Video y el códec de perfil avanzado de Windows Media Video admiten una característica de preprocesamiento que convierte el contenido entrelazado en fotogramas progresivos.

Para que el vídeo de entrada desentrelazado de códecs, llame al método [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) . La configuración que se va a usar es g \_ wszDeinterlaceMode. Establezca el modo de desentrelazado en uno de los siguientes valores.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WM_DM_NOTINTERLACED</td>
<td>La entrada es progresiva. Use esta opción para detener el desentrelazado cuando haya establecido previamente el modo de desentrelazado en otro valor.</td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_NORMAL</td>
<td>Seleccione este modo para mezclar los campos pares e impares de un fotograma entrelazado (mediante un mecanismo de compensación de movimiento). Privilegios<br/>
<ul>
<li>Los artefactos entrelazados de la pantalla progresiva se reducen significativamente.</li>
<li>El códec de Windows Media Video produce un vídeo comprimido de mayor calidad.</li>
</ul></td>
</tr>
<tr class="odd">
<td>WM_DM_DEINTERLACE_HALFSIZE</td>
<td>Seleccione este modo cuando la resolución de salida sea la mitad o menos de la resolución de entrada. Por ejemplo, use este modo cuando la resolución de vídeo de entrada sea 640 x 480 píxeles y la resolución de vídeo de salida sea de 320 x 240 píxeles. Privilegios<br/>
<ul>
<li>Los artefactos entrelazados de la pantalla progresiva se reducen significativamente.</li>
</ul></td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</td>
<td>Seleccione este modo cuando la resolución de salida sea la mitad o menos de la resolución de entrada y la <a href="wmformat-glossary.md"><em>velocidad de fotogramas</em></a> de salida sea el doble de alta. Por ejemplo, use este modo cuando la resolución de vídeo de entrada sea 640 x 480 píxeles en 30 fotogramas entrelazados/s y la resolución de vídeo de salida sea de 320 x 240 píxeles en 60 fotogramas/s. Privilegios<br/>
<ul>
<li>Esto produce fotogramas progresivos de alta calidad, ya que cada campo se convierte en un fotograma y, por tanto, no es necesario mezclar ninguna información.</li>
<li>Se captura el movimiento completo de los campos entrelazados.</li>
</ul></td>
</tr>
<tr class="odd">
<td>WM_DM_DEINTERLACE_INVERSETELECINE</td>
<td>Seleccione este modo para convertir el vídeo de 30 fotogramas/seg en los 24 fotogramas por segundo de la película original. Privilegios<br/>
<ul>
<li>La calidad de compresión mejora significativamente porque solo es necesario codificar 24 fotogramas por segundo en lugar de 30 fotogramas por segundo.</li>
<li>Dado que el resultado es progresivo, se realizan las mismas ventajas de compresión y visualización del desentrelazado.</li>
</ul></td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</td>
<td>Seleccione este modo cuando la resolución de salida vertical sea la mitad, o menos, de la resolución vertical de entrada y la <a href="wmformat-glossary.md"><em>velocidad de fotogramas</em></a> de salida sea dos veces superior. Por ejemplo, la resolución de vídeo vertical de entrada es 640 x 480 píxeles en 30 fotogramas entrelazados/s y la resolución de vídeo vertical de salida es de 320 x 240 píxeles en 60 fotogramas/s. Privilegios<br/>
<ul>
<li>Esto produce fotogramas progresivos de alta calidad, ya que cada campo se convierte en un fotograma y, por tanto, no es necesario mezclar ninguna información.</li>
<li>Se captura el movimiento completo de los campos entrelazados.</li>
</ul></td>
</tr>
</tbody>
</table>



 

En el caso de contenido mixto, establezca el modo de desentrelazado según sea necesario antes de pasar muestras de un nuevo tipo. Por ejemplo, para iniciar la codificación con una entrada progresiva, no es necesario establecer ningún modo de desentrelazado. Si algunos ejemplos requieren desentrelazado normal, debe establecer el modo de desentrelazado en WM \_ DM \_ desentrelazado \_ normal. Para procesar más ejemplos progresivos, debe establecer el modo de desentrelazado en WM \_ DM \_ NOTINTERLACED.

## <a name="inverse-telecine-settings"></a>Configuración de telecine inversa

Para obtener una descripción de telecine inversa, consulte [para usar telecine inversa](to-use-inverse-telecine.md).

Si establece el modo de desentrelazado en \_ INVERSETELECINE de WM DM \_ \_ , puede especificar el patrón de telecine del primer fotograma de entrada mediante una llamada a [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting). La configuración que se va a usar es g \_ wszInitialPatternForInverseTelecine. Establezca el patrón inicial en uno de los valores siguientes.



| Value                                              | Descripción                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ deshabilitación del \_ \_ modo coherente de WM DM                | Especifica que el medio de entrada ha pasado por el proceso de telecine, pero que los fotogramas ya no se encuentran en un patrón de predicción. Esto normalmente indica que el medio se editó después del procesamiento de telecine. Cuando se usa esta opción, el códec intenta reconstruir los fotogramas originales por sí mismo. |
| \_ \_ \_ \_ la primera trama de WM DM en el \_ \_ clip \_ es \_ AA \_    | Especifica que el campo superior del marco AA es el primer ejemplo.                                                                                                                                                                                                                                             |
| \_ \_ \_ \_ la primera trama de WM DM en el \_ \_ clip \_ es \_ BB \_    | Especifica que el campo superior del marco BB es el primer ejemplo.                                                                                                                                                                                                                                             |
| \_ \_ \_ la primera trama de WM DM it \_ en el \_ \_ clip \_ es \_ BC \_ Top    | Especifica que el campo superior del fotograma BC es el primer ejemplo.                                                                                                                                                                                                                                             |
| \_ \_ \_ \_ la primera trama de WM DM en el \_ \_ clip es el \_ \_ CD \_ superior    | Especifica que el campo superior del fotograma del CD es el primer ejemplo.                                                                                                                                                                                                                                             |
| \_ \_ \_ \_ la primera trama de WM DM en el \_ \_ clip \_ es DD en la \_ \_ parte superior    | Especifica que el campo superior del marco DD es el primer ejemplo.                                                                                                                                                                                                                                             |
| \_ \_ \_ \_ la primera trama de WM DM en el \_ \_ clip \_ es \_ AA \_ inferior | Especifica que el campo inferior del marco AA es el primer ejemplo.                                                                                                                                                                                                                                          |
| \_ \_ \_ \_ la primera trama de WM DM en el \_ \_ clip \_ es \_ BB \_ inferior | Especifica que el campo inferior del marco BB es el primer ejemplo.                                                                                                                                                                                                                                          |
| \_ \_ \_ \_ la primera trama \_ de \_ \_ \_ \_ WM DM | Especifica que el campo inferior del fotograma BC es el primer ejemplo.                                                                                                                                                                                                                                          |
| \_ \_ trama de WM \_ DM \_ en primer lugar en el \_ \_ clip es el \_ \_ CD \_ inferior | Especifica que el campo inferior del fotograma del CD es el primer ejemplo.                                                                                                                                                                                                                                          |
| \_ \_ \_ \_ la primera trama de WM DM en el \_ \_ clip \_ es DD de la \_ \_ parte inferior | Especifica que el campo inferior del marco DD es el primer ejemplo.                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Temas avanzados**](advanced-topics.md)
</dt> </dl>

 

 






---
title: Vídeo para desinterlace
description: Vídeo para desinterlace
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- Windows SDK de formato multimedia, vídeo desenlazado
- Windows SDK de formato multimedia, televisa inversa
- Windows SDK de formato multimedia, televisa
- Formato de sistemas avanzados (ASF), vídeo desenlazado
- ASF (formato de sistemas avanzados), vídeo desenlazado
- Formato de sistemas avanzados (ASF), televisa inversa
- ASF (formato de sistemas avanzados), televisa inversa
- Formato de sistemas avanzados (ASF), televisa
- ASF (formato de sistemas avanzados), televisa
- vídeo desenlazado
- televisa inversa, acerca de
- televisa,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ef1d1a6fcee3bf43d2fb4451d4ef129e595471e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359898"
---
# <a name="to-deinterlace-video"></a>Vídeo para desinterlace

Algunos orígenes de vídeo, como las tarjetas de captura de vídeo, proporcionan datos de vídeo para la presentación entrelazada. Cada fotograma de vídeo entrelazado se conste de dos campos. El campo superior contiene la primera línea de vídeo y todas las demás líneas a partir de entonces. El campo inferior contiene la segunda línea de vídeo y todas las demás líneas a partir de entonces. Por lo tanto, un campo contiene todas las líneas numeradas uniformes y el otro contiene todas las líneas numeradas impares. Los campos que conforman un marco representan tiempos de presentación ligeramente diferentes para que, cuando se intercalan, no forme una imagen estática.

Si desea mostrar vídeo en un monitor de equipo, cada fotograma del vídeo debe mostrarse como una imagen (este método de mostrar vídeo de un fotograma entero a la vez se denomina vídeo *progresiva).* Si muestra vídeo entrelazado progresivamente, es posible que los fotogramas no parezcan correctos, debido a la diferencia de tiempo entre los dos campos. El códec Windows Media Video y el códec Windows Perfil avanzado de vídeo multimedia admiten una característica de preprocesamiento que convierte el contenido entrelazado en fotogramas progresivas.

Para que el códec desinterese el vídeo de entrada, llame al método [**IWMWriterAdvanced2::SetInputSetting.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) El valor que se va a usar \_ es g wszDeinterlaceMode. Establezca el modo de desenlazado en uno de los valores siguientes.




| Value | Descripción | 
|-------|-------------|
| WM_DM_NOTINTERLACED | La entrada es progresiva. Use esta opción para detener el desenlazado cuando haya establecido previamente el modo de desenlazado en otro valor. | 
| WM_DM_DEINTERLACE_NORMAL | Seleccione este modo para combinar los campos par e impar de un marco entrelazado (mediante un mecanismo de compensación de movimiento). Ventajas:<br /><ul><li>Los artefactos de intercalación de la pantalla progresiva se reducen significativamente.</li><li>El códec Windows Media Video genera vídeo comprimido de mayor calidad.</li></ul> | 
| WM_DM_DEINTERLACE_HALFSIZE | Seleccione este modo cuando la resolución de salida sea la mitad o menos de la resolución de entrada. Por ejemplo, use este modo cuando la resolución de vídeo de entrada sea de 640 x 480 píxeles y la resolución de vídeo de salida sea de 320 x 240 píxeles. Ventajas:<br /><ul><li>Los artefactos de intercalación de la pantalla progresiva se reducen significativamente.</li></ul> | 
| WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE | Seleccione este modo cuando la resolución de salida sea la mitad o menos de la resolución de entrada y la velocidad de fotogramas de <a href="wmformat-glossary.md"><em>salida</em></a> sea el doble de alta. Por ejemplo, use este modo cuando la resolución de vídeo de entrada sea de 640 x 480 píxeles a 30 fotogramas entrelazados por segundo y la resolución de vídeo de salida sea de 320 x 240 píxeles a 60 fotogramas/s. Ventajas:<br /><ul><li>Esto genera fotogramas progresivas de alta calidad, ya que cada campo se convierte en un marco y, por tanto, no es necesario combinar ninguna información.</li><li>Se captura el movimiento completo de los campos entrelazados.</li></ul> | 
| WM_DM_DEINTERLACE_INVERSETELECINE | Seleccione este modo para convertir el vídeo televisado de 30 fotogramas por segundo en los 24 fotogramas por segundo de la película original. Ventajas:<br /><ul><li>La calidad de compresión mejora significativamente porque solo es necesario codificar 24 fotogramas por segundo en lugar de 30 fotogramas por segundo.</li><li>Dado que el resultado es progresiva, se realizan las mismas ventajas de compresión y visualización del desenlazado.</li></ul> | 
| WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE | Seleccione este modo cuando la resolución de salida vertical sea la mitad o menos de la resolución vertical de entrada y la velocidad de fotogramas de salida <a href="wmformat-glossary.md"><em>sea</em></a> el doble de alta. Por ejemplo, la resolución de vídeo vertical de entrada es de 640 x 480 píxeles a 30 fotogramas entrelazados por segundo y la resolución de vídeo vertical de salida es de 320 x 240 píxeles a 60 fotogramas/s. Ventajas:<br /><ul><li>Esto genera fotogramas progresivas de alta calidad, ya que cada campo se convierte en un marco y, por tanto, no es necesario combinar ninguna información.</li><li>Se captura el movimiento completo de los campos entrelazados.</li></ul> | 




 

Para contenido mixto, establezca el modo de desenlazado según sea necesario antes de pasar ejemplos de un nuevo tipo. Por ejemplo, para iniciar la codificación con entrada progresiva, no es necesario establecer ningún modo de desenlazado. Si algunos ejemplos requieren desinterlazado normal, debe establecer el modo de desinterlazado en WM \_ DM \_ DEINTERLACE \_ NORMAL. Para procesar muestras progresivas adicionales, debe establecer el modo de desenlazado en WM \_ DM \_ NOTINTERLACED.

## <a name="inverse-telecine-settings"></a>Inverse Televersión Configuración

Para obtener una descripción de la televisa inversa, vea [To Use Inverse Televersión](to-use-inverse-telecine.md).

Si establece el modo de desinterlazado en WM DM DEINTERLACE INVERSETELEVERSIÓN, puede especificar el patrón televisa del primer fotograma de entrada llamando a \_ \_ \_ [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting). El valor que se va a usar \_ es g wszInitialPatternForInverseTeleversión. Establezca el patrón inicial en uno de los valores siguientes.



| Value                                              | Descripción                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WM \_ DM DESHABILITA EL MODO \_ \_ \_ \_ COHERENTE                | Especifica que el medio de entrada ha pasado por el proceso de televisa, pero que los fotogramas ya no están en un patrón de predicción. Esto suele indicar que el medio se editó después del procesamiento de televisa. Cuando se usa esta configuración, el códec intenta reconstruir los fotogramas originales por sí mismo. |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ AA \_ TOP    | Especifica que el campo superior del marco AA es el primer ejemplo.                                                                                                                                                                                                                                             |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ BB \_ TOP    | Especifica que el campo superior del marco BB es el primer ejemplo.                                                                                                                                                                                                                                             |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ BC \_ TOP    | Especifica que el campo superior del marco BC es el primer ejemplo.                                                                                                                                                                                                                                             |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ CD \_ TOP    | Especifica que el campo superior del marco de CD es el primer ejemplo.                                                                                                                                                                                                                                             |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ DD \_ TOP    | Especifica que el campo superior del marco DD es el primer ejemplo.                                                                                                                                                                                                                                             |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ AA \_ BOTTOM | Especifica que el campo inferior del marco AA es el primer ejemplo.                                                                                                                                                                                                                                          |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ BB \_ BOTTOM | Especifica que el campo inferior del marco BB es el primer ejemplo.                                                                                                                                                                                                                                          |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ BC \_ BOTTOM | Especifica que el campo inferior del marco BC es el primer ejemplo.                                                                                                                                                                                                                                          |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ CD \_ BOTTOM | Especifica que el campo inferior del marco de CD es el primer ejemplo.                                                                                                                                                                                                                                          |
| WM \_ DM \_ IT \_ FIRST \_ FRAME \_ IN \_ CLIP \_ IS \_ DD \_ BOTTOM | Especifica que el campo inferior del marco DD es el primer ejemplo.                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Temas avanzados**](advanced-topics.md)
</dt> </dl>

 

 






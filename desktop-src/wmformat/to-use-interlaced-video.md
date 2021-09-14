---
title: Para usar vídeo entrelazado
description: Para usar vídeo entrelazado
ms.assetid: cb77bac7-bea8-4f1b-8302-fee9a43d4815
keywords:
- Windows SDK de formato multimedia, vídeo entrelazado
- Windows SDK de formato multimedia, codificación de vídeo entrelazada
- Windows SDK de formato multimedia, codificación de vídeo entrelazado
- Windows SDK de formato multimedia, decoding entrelazado de vídeo
- Windows SDK de formato multimedia, orden de campo
- Formato de sistemas avanzados (ASF), vídeo entrelazado
- ASF (formato de sistemas avanzados), vídeo entrelazado
- Formato de sistemas avanzados (ASF), codificación de vídeo entrelazada
- ASF (formato de sistemas avanzados), codificación de vídeo entrelazada
- Formato de sistemas avanzados (ASF), codificación de vídeo entrelazado
- ASF (formato de sistemas avanzados), codificación de vídeo entrelazado
- Formato de sistemas avanzados (ASF), decoding interlaced video (Vídeo entrelazado)
- ASF (formato de sistemas avanzados), vídeo entrelazado decoding
- Formato de sistemas avanzados (ASF), orden de campo
- ASF (formato de sistemas avanzados), orden de campo
- vídeo entrelazado, acerca de
- vídeo entrelazado, codificación
- vídeo entrelazado, decoding
- vídeo entrelazado, orden de campo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a093ddd6d9d9487ffcd4b73e1f5c75b849cdcdc1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262116"
---
# <a name="to-use-interlaced-video"></a>Para usar vídeo entrelazado

Hay dos tipos básicos de codificación de vídeo: progresiva e entrelazada. En la codificación progresiva, cada fotograma es una representación codificada de un fotograma de vídeo. En la codificación entrelazada, cada fotograma es una representación codificada de todas las filas pares de píxeles del vídeo o de todas las filas impares. Cada marco entrelazado se denomina *campo*, por lo que hay campos impares e incluso campos. Una pantalla entrelazada (como un televisor) representa los campos de uno en uno, alternando campos. Una pantalla progresiva representa fotogramas a la vez.

El códec Windows perfil avanzado de Media Video 9 proporciona compatibilidad para mantener el entrelazado en secuencias comprimidas.

## <a name="when-to-use-interlaced-video"></a>Cuándo usar vídeo entrelazado

La codificación de vídeo entrelazado solo es útil cuando el contenido se muestra en un dispositivo entrelazado. Es posible que sea necesario entrelazar el contenido que está pensado para ser visto en un televisor (a través de un set-top box u otro dispositivo). El contenido que está pensado para visualizarse exclusivamente en una pantalla de equipo no debe codificarse como entrelazado.

Para codificar vídeo entrelazado como vídeo progresiva, debe configurar los valores de entrada. Para obtener más información, vea [To Deinterlace Video](to-deinterlace-video.md).

## <a name="field-order"></a>Orden de campos

La mayoría de los orígenes de vídeo entrelazados, como las tarjetas de captura de vídeo, ofrecen ejemplos de vídeo que incluyen ambos campos intercalados entre sí. El resultado es como un fotograma completo de vídeo, salvo que las líneas impares e uniformes se desplazan ligeramente en el tiempo. No hay ningún estándar universal en cuanto a qué campo del ejemplo de vídeo intercalado se produce primero en el tiempo.

Debe permitir que los usuarios especifiquen el orden de los campos al pasar muestras entrelazadas a la aplicación.

## <a name="encoding-interlaced-video"></a>Codificación de vídeo entrelazado

Para usar la codificación entrelazada, realice los pasos siguientes:

1.  Configure la secuencia de vídeo en el perfil para usar la extensión de unidad de datos de tipo de contenido llamando al [**método IWMStreamConfig2::AddDataUnitExtension.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) El GUID de extensión de ejemplo para la extensión de tipo de contenido es WM \_ SampleExtensionsGUID \_ ContentType.
2.  Establezca la secuencia en el perfil y configure el escritor con el perfil como normal.
3.  Antes de pasar ejemplos entrelazados al escritor, llame al método [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) para establecer la configuración de entrada \_ g wszInterlacedCoding en **TRUE.**
4.  Para cada ejemplo entrelazado que pase al escritor, llame al método [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) para establecer el tipo de contenido. Los valores de tipo de contenido son combinaciones de las marcas de la tabla siguiente.



| Marca                         | Descripción                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WM \_ CT \_ ENTRELAZADO           | Establezca siempre esta marca al codificar contenido entrelazado. Si usa esta marca sin establecer una marca de orden de campo (WM CT BOTTOM FIELD FIRST o WM CT TOP FIELD FIRST), el códec asumirá que el campo superior \_ \_ es el \_ \_ \_ \_ \_ \_ primero. Si el códec usa el orden de campo incorrecto, no debería haber ningún impacto en la calidad de la imagen, pero la eficacia de codificación se verá afectada. |
| WM \_ CT \_ BOTTOM \_ FIELD \_ FIRST | Cuando se combina con la marca WM \_ CT INTERLACED, esta marca indica que el campo inferior (el campo que comienza con la segunda línea del ejemplo) se produce \_ primero en el tiempo.                                                                                                                                                                                          |
| WM \_ CT \_ TOP \_ FIELD \_ FIRST    | Cuando se combina con la marca WM \_ CT INTERLACED, esta marca indica que el campo superior (el campo que empieza por la primera línea del ejemplo) se produce \_ primero en el tiempo.                                                                                                                                                                                              |
| WM \_ CT \_ REPEAT \_ FIRST \_ FIELD | Indica que el primer campo del ejemplo debe repetirse durante la reproducción. Esta marca se usa para el vídeo creado a partir de la película por el proceso de televisación. Si no se establece ninguna marca de orden de campo junto con esta marca, se supone que el campo superior se produce primero en el tiempo.<br/>                                                                             |



 

> [!Note]  
> Si no se establece la marca \_ WM CT INTERLACED, se supone que el ejemplo \_ contiene un fotograma de vídeo progresiva.

 

## <a name="decoding-interlaced-video"></a>Decoding Interlaced Video

Al descodear vídeo entrelazado, debe establecer la configuración g \_ wszAllowInterlacedOutput en **TRUE** mediante el método [**IWMReaderAdvanced2::SetOutputSetting.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) De lo contrario, el códec entregará fotogramas progresivas.

La extensión de unidad de datos de tipo de contenido se mantiene en los ejemplos de salida. Debe pasar la orientación del campo al dispositivo de representación para garantizar una reproducción adecuada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Temas avanzados**](advanced-topics.md)
</dt> </dl>

 

 






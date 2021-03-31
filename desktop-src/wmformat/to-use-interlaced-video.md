---
title: Para usar vídeo entrelazado
description: Para usar vídeo entrelazado
ms.assetid: cb77bac7-bea8-4f1b-8302-fee9a43d4815
keywords:
- SDK de Windows Media Format, vídeo entrelazado
- SDK de Windows Media Format, codificación de vídeo entrelazada
- SDK de Windows Media Format, codificación de vídeo entrelazado
- SDK de Windows Media Format, descodificación de vídeo entrelazado
- SDK de Windows Media Format, orden de campo
- Advanced Systems Format (ASF), vídeo entrelazado
- ASF (formato de sistemas avanzados), vídeo entrelazado
- Advanced Systems Format (ASF), codificación de vídeo entrelazada
- ASF (formato de sistemas avanzados), codificación de vídeo entrelazada
- Advanced Systems Format (ASF), codificación de vídeo entrelazado
- ASF (formato de sistemas avanzados), vídeo entrelazado de codificación
- Advanced Systems Format (ASF), descodificación de vídeo entrelazado
- ASF (formato de sistemas avanzados), descodificación de vídeo entrelazado
- Advanced Systems Format (ASF), orden de campo
- ASF (formato de sistemas avanzados), orden de campo
- vídeo entrelazado, acerca de
- vídeo entrelazado, codificación
- vídeo entrelazado, descodificación
- vídeo entrelazado, orden de los campos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a093ddd6d9d9487ffcd4b73e1f5c75b849cdcdc1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103904408"
---
# <a name="to-use-interlaced-video"></a>Para usar vídeo entrelazado

Hay dos tipos básicos de codificación de vídeo: progresiva y entrelazada. En la codificación progresiva, cada fotograma es una representación codificada de un fotograma de vídeo. En la codificación entrelazada, cada fotograma es una representación codificada de todas las filas de píxeles pares del vídeo o de todas las filas impares. Cada fotograma entrelazado se denomina *campo*, por lo que hay campos impares e incluso campos. Una pantalla entrelazada (como un televisor) representa los campos de uno en uno, alternando los campos. Una pantalla progresiva representa fotogramas a la vez.

El códec de perfil avanzado de Windows Media Video 9 proporciona compatibilidad para mantener el entrelazado en secuencias comprimidas.

## <a name="when-to-use-interlaced-video"></a>Cuándo usar vídeo entrelazado

El vídeo entrelazado de codificación solo es útil cuando el contenido se muestra en un dispositivo entrelazado. Es posible que sea necesario entrelazar el contenido que se va a ver en un televisor (a través de un decodificador u otro dispositivo). El contenido que se va a ver exclusivamente en una pantalla del equipo no se debe codificar como entrelazado.

Para codificar vídeo entrelazado como vídeo progresivo, debe configurar los valores de entrada. Para obtener más información, vea [para Desentrelazar vídeo](to-deinterlace-video.md).

## <a name="field-order"></a>Orden de campos

La mayoría de los orígenes de vídeo entrelazado, como las tarjetas de captura de vídeo, ofrecen ejemplos de vídeo que incluyen ambos campos intercalados entre sí. El resultado es como un marco completo de vídeo, con la excepción de que las líneas impares e impares se desplazan ligeramente en el tiempo. No hay ningún estándar universal en el que el campo de la muestra de vídeo intercalado se produce primero en el tiempo.

Debe permitir que los usuarios especifiquen el orden de los campos al pasar ejemplos entrelazados a la aplicación.

## <a name="encoding-interlaced-video"></a>Vídeo entrelazado de codificación

Para usar la codificación entrelazada, realice los pasos siguientes:

1.  Configure la secuencia de vídeo en el perfil para usar la extensión de unidad de datos de tipo de contenido llamando al método [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) . El GUID de la extensión de ejemplo para la extensión de tipo de contenido es de WM \_ SampleExtensionsGUID \_ ContentType.
2.  Establezca la secuencia en el perfil y configure el escritor con el perfil como normal.
3.  Antes de pasar ejemplos entrelazados al escritor, llame al método [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) para establecer el valor de \_ entrada g wszInterlacedCoding en **true**.
4.  Para cada ejemplo entrelazado que pase al escritor, llame al método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) para establecer el tipo de contenido. Los valores de tipo de contenido son combinaciones de las marcas de la tabla siguiente.



| Marca                         | Descripción                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WM \_ CT \_ entrelazado           | Establezca siempre esta marca al codificar contenido entrelazado. Si usa esta marca sin establecer primero una marca de orden de campo (primer campo de WM \_ CT \_ \_ \_ o primero el \_ campo de nivel superior de WM CT \_ ), \_ \_ el códec asumirá que el campo superior es el primero. Si el códec usa el orden de campo incorrecto, no debería haber ningún impacto en la calidad de la imagen, pero la eficacia de la codificación se verá afectada. |
| \_campo inferior CT de WM \_ \_ \_ primero | Cuando se combina con la \_ marca de WM CT \_ , este marcador indica que el campo inferior (el campo que comienza con la segunda línea del ejemplo) se produce primero en el tiempo.                                                                                                                                                                                          |
| \_ \_ \_ primer campo SUP CT \_    | Cuando se combina con la \_ marca WM CT \_ , esta marca indica que el campo superior (el campo que comienza con la primera línea del ejemplo) se produce primero en el tiempo.                                                                                                                                                                                              |
| \_ \_ \_ primer campo de repetición CT de WM \_ | Indica que el primer campo del ejemplo debe repetirse en la reproducción. Esta marca se usa para el vídeo que ha creado a partir de la película mediante el proceso de telecine. Si no se establece ninguna marca de orden de campo junto con esta marca, se supone que el campo superior se produce por primera vez.<br/>                                                                             |



 

> [!Note]  
> Si \_ \_ no se establece la marca de WM CT, se supone que el ejemplo contiene un fotograma de vídeo progresivo.

 

## <a name="decoding-interlaced-video"></a>Descodificación de vídeo entrelazado

Al descodificar vídeo entrelazado, debe establecer el valor de g \_ wszAllowInterlacedOutput en **true** mediante el método [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) . De lo contrario, el códec proporcionará tramas progresivas.

La extensión de unidad de datos de tipo de contenido se mantiene en los ejemplos de salida. Debe pasar la orientación del campo al dispositivo de representación para asegurarse de que la reproducción sea correcta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Temas avanzados**](advanced-topics.md)
</dt> </dl>

 

 






---
description: Codificación de vídeo entrelazada
ms.assetid: 7695d4e3-4a75-4972-ab02-bc532d6a4dce
title: Codificación de vídeo entrelazada (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fafacb56f29964e81b040c59cdb75d8ebb35830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002804"
---
# <a name="interlaced-video-encoding-microsoft-media-foundation"></a>Codificación de vídeo entrelazada (Microsoft Media Foundation)

Los datos de vídeo pensados para su uso con equipos suelen ser *progresivos*, lo que significa que cada fotograma se codifica como una sola imagen. Algunos dispositivos, como los televisores, no muestran un fotograma a la vez, sino como dos imágenes. Una de las imágenes, o campos, contiene todas las filas con un número par. El otro campo contiene los datos de todas las filas con números impares. El vídeo codificado con más de un campo por fotograma se denomina entrelazado, ya que se representa cambiando entre el campo par y el campo impar.

En el pasado, el contenido de vídeo entrelazado siempre se desentrelazaba antes de la codificación con el códec de Windows Media Video. Sin embargo, a partir de Windows Media 9 series, el codificador de vídeo admite la compresión de contenido entrelazado sin convertirlo primero a progresiva. Es importante mantener el entrelazado en un archivo codificado si el contenido se representa en una pantalla entrelazada, como un televisor. Esta característica es de mayor importancia, ya que la compatibilidad con el contenido basado en Windows Media se extiende a reproductores de DVD, decodificadores y otros dispositivos electrónicos domésticos.

La forma más sencilla de codificar y proporcionar vídeo entrelazado es desarrollar la aplicación con el SDK de Windows Media Format y almacenar el contenido en archivos ASF. La información entrelazada sobre los fotogramas se pasa al códec mediante extensiones de unidad de datos, que funcionan bien con el contenido ASF, pero son un poco más complicados de admitir en otros contenedores. Para obtener más información acerca de las extensiones de unidad de datos, consulte [uso de extensiones de unidad de datos](usingdataunitextensions.md).

La compatibilidad con la codificación entrelazada implica dos pasos principales: obtener la información del marco para el codificador y entregar la información a la aplicación de representación. Estos pasos se describen en los párrafos siguientes.

## <a name="interlaced-video-and-the-encoder"></a>Vídeo entrelazado y codificador

El primer paso en la codificación de vídeo con entrelazado mantenido es configurar el codificador para codificar los campos entrelazados. Para ello, establezca la propiedad [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) en **true**. Esto prepara al codificador para recibir ejemplos entrelazados. Cada ejemplo de entrada debe contener ambos campos.

Cada ejemplo que se procesa con el codificador después de activar la codificación entrelazada debe tener una extensión de unidad de datos adjunta. Se supone que las muestras sin la extensión de unidad de datos esperada son progresivas. El GUID que identifica la extensión es D590DC20-07BC-436C-9CF7-F3BBFBF1A4DC. Los valores que pasan los objetos del SDK de Windows Media Format se definen en la tabla siguiente.



| Value      | Descripción                                                                                                                              |
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000020 | Especifica que el ejemplo se codifica primero con el campo inferior. Este valor solo es significativo cuando se combina con el valor entrelazado. |
| 0x00000040 | Especifica que el ejemplo se codifica primero con el campo superior. Este valor solo es significativo cuando se combina con el valor entrelazado.    |
| 0x00000080 | Especifica que el ejemplo está entrelazado. Este es el único valor que es significativo para el códec DMOs.                                    |



 

Uno de los dos primeros valores siempre se combina con 0x80 usando **una operación OR** bit a bit antes de establecerse en el ejemplo. Sin embargo, el codificador solo comprueba 0x80 y no tiene en cuenta el resto de la extensión. Si la extensión identifica el ejemplo como entrelazado, el codificador mantiene el entrelazado de ejemplo en el flujo comprimido e inserta una marca de indicación en la secuencia para que el descodificador pueda identificar fotogramas entrelazados. Cada ejemplo entrelazado está marcado, de modo que el contenido de origen que es una combinación de progresivo e entrelazado se puede codificar en un flujo.

El objeto Windows Media Format SDK Writer incluye las extensiones de unidad de datos de tipo de contenido de los ejemplos que escribe en la sección de datos del contenedor ASF para su uso en el momento de la representación.

## <a name="reading-and-rendering-interlaced-video"></a>Lectura y representación de vídeo entrelazado

El descodificador identifica las muestras entrelazadas basadas en la marca establecida en la secuencia por el codificador. De forma predeterminada, el descodificador desentrelaza los ejemplos y proporciona salidas progresivas. La aplicación de reproducción puede configurar el descodificador para procesar las salidas con el entrelazado mantenido estableciendo la propiedad de [ \_ \_ desentrelazado del descodificador de MFPKEY](mfpkey-decoder-deinterlacingproperty.md) .

La dificultad de la reproducción de vídeo entrelazado se produce después de que el descodificador entregue los ejemplos. El representador (tarjeta de vídeo o chip en un dispositivo) no puede mostrar correctamente el contenido del vídeo sin conocer qué campo es. En aplicaciones que usan el SDK de Windows Media Format, la extensión de unidad de datos de tipo de contenido se recupera de los ejemplos sin comprimir y se puede pasar al dispositivo.

Cuando se usan los objetos de códec directamente, ninguno de estos datos es automático. Debe implementar la compatibilidad con la extensión de unidad de datos, tanto en los objetos de búfer como en el contenedor que usa para el contenido codificado. Los tipos más comunes de contenedores de medios (como AVI) no admiten metadatos de nivel de ejemplo. Puede implementar su propio sistema para almacenar los datos en el archivo y asociarlo a ejemplos individuales, pero solo un lector personalizado podrá recuperarlo.

> [!Note]  
> Establecer la [propiedad \_ INTERLACEDCODINGENABLED de MFPKEY](mfpkey-interlacedcodingenabledproperty.md) en **true** y, a continuación, no enviar ningún ejemplo con la extensión de unidad de datos de tipo de contenido adjunta puede hacer que el codificador se bloquee. Establezca el codificador para la codificación entrelazada solo si tiene ejemplos entrelazados para entregarlos.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 




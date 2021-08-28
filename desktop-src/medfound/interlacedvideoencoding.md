---
description: Codificación de vídeo entrelazada
ms.assetid: 7695d4e3-4a75-4972-ab02-bc532d6a4dce
title: Codificación de vídeo entrelazada (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15269aca3f2878504fef56c62b1a1d70ecd89295c237164ba864b15aaae371d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724395"
---
# <a name="interlaced-video-encoding-microsoft-media-foundation"></a>Codificación de vídeo entrelazada (Microsoft Media Foundation)

Los datos de vídeo diseñados para su uso con equipos suelen ser *progresivas,* lo que significa que cada fotograma se codifica como una sola imagen. Algunos dispositivos, como las televisión, no muestran un marco a la vez, sino como dos imágenes. Una de las imágenes, o campos, contiene todas las filas numeradas uniformes. El otro campo contiene los datos de todas las filas impares numeradas. El vídeo codificado con más de un campo por fotograma se denomina entrelazado, ya que se representa cambiando entre el campo par y el campo impar.

En el pasado, el contenido de vídeo entrelazado siempre se desenlazaba antes de codificar con el códec Windows Media Video. Sin embargo, Windows la serie Media 9, el codificador de vídeo admite la compresión de contenido entrelazado sin convertirlo primero en progresiva. Mantener el entrelazado en un archivo codificado es importante si el contenido se representa alguna vez en una pantalla entrelazada, como una televisión. Esta característica es de importancia creciente, ya que la compatibilidad con Windows contenido basado en multimedia se distribuye a reproductores de DVD, set-top box y otros dispositivos electrónicos particulares.

La manera más fácil de codificar y entregar vídeo entrelazado es desarrollar la aplicación mediante el SDK de formato multimedia de Windows y almacenar el contenido en archivos ASF. La información entrelazada sobre los fotogramas se pasa al códec mediante extensiones de unidad de datos, que funcionan bien para el contenido de ASF, pero son un poco más complicadas de admitir en otros contenedores. Para obtener más información sobre las extensiones de unidad de datos, vea [Usar extensiones de unidad de datos](usingdataunitextensions.md).

Admitir la codificación entrelazada implica dos pasos principales: obtener la información de fotogramas al codificador y entregar la información a la aplicación de representación. Estos pasos se describen en los párrafos siguientes.

## <a name="interlaced-video-and-the-encoder"></a>Vídeo entrelazado y el codificador

El primer paso para codificar vídeo con entrelazado mantenido es configurar el codificador para codificar campos entrelazados. Para ello, establezca la [propiedad \_ MFPKEY INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) en **TRUE.** Esto prepara el codificador para recibir muestras entrelazadas. Cada ejemplo de entrada debe contener ambos campos.

Cada ejemplo que procese con el codificador después de activar la codificación entrelazada debe tener asociada una extensión de unidad de datos. Se supone que los ejemplos sin la extensión de unidad de datos esperada son progresivas. El GUID que identifica la extensión es D590DC20-07BC-436C-9CF7-F3BBFBF1A4DC. Los valores pasados por los objetos del SDK Windows Media Format se definen en la tabla siguiente.



| Valor      | Descripción                                                                                                                              |
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000020 | Especifica que el ejemplo se codifica primero con el campo inferior. Este valor solo es significativo cuando se combina con el valor entrelazado. |
| 0x00000040 | Especifica que el ejemplo se codifica primero con el campo superior. Este valor solo es significativo cuando se combina con el valor entrelazado.    |
| 0x00000080 | Especifica que el ejemplo está entrelazado. Este es el único valor que es significativo para las DDO de códec.                                    |



 

Uno de los dos primeros valores siempre se combina con 0x80 un **OR** bit a bit antes de establecerse en el ejemplo. Sin embargo, el codificador solo comprueba si 0x80 y no tiene en cuenta el resto de la extensión. Si la extensión identifica la muestra como entrelazada, el codificador mantiene el entrelazado de ejemplo en la secuencia comprimida e inserta una marca de indicación en la secuencia para que el descodificador pueda identificar fotogramas entrelazados. Cada muestra entrelazada está marcada, por lo que el contenido de origen que es una combinación de progresiva e entrelazada se puede codificar en una secuencia juntos.

El objeto de escritura del SDK de Windows Media Format incluye las extensiones de unidad de datos del tipo de contenido en los ejemplos que escribe en la sección de datos del contenedor de ASF para su uso en el momento de la representación.

## <a name="reading-and-rendering-interlaced-video"></a>Lectura y representación de vídeo entrelazado

El descodificador identifica muestras entrelazadas en función de la marca establecida en la secuencia por el codificador. De forma predeterminada, el descodificador desenlaza las muestras y ofrece salidas progresivas. La aplicación player puede configurar el descodificador para procesar salidas con entrelazado mantenido estableciendo la propiedad [MFPKEY \_ DECODER \_ DEINTERLACING.](mfpkey-decoder-deinterlacingproperty.md)

La dificultad de la reproducción de vídeo entrelazada surge después de que el descodificador entregue los ejemplos. El representador (tarjeta de vídeo o chip en un dispositivo) no puede mostrar correctamente el contenido del vídeo sin saber qué campo es cuál. En las aplicaciones que usan el SDK de Windows Media Format, la extensión de unidad de datos del tipo de contenido se recupera de los ejemplos sin comprimir y se puede pasar al dispositivo.

Cuando se usan directamente los objetos de códec, ninguna de estas transferencias de datos es automática. Debe implementar la compatibilidad con la extensión de unidad de datos, tanto en los objetos de búfer como en el contenedor que use para el contenido codificado. Los tipos más comunes de contenedores multimedia (como AVI) no admiten metadatos de nivel de ejemplo. Puede implementar su propio sistema para almacenar los datos en el archivo y asociarlos a ejemplos individuales, pero solo un lector personalizado podría recuperarlos.

> [!Note]  
> Establecer la [propiedad \_ MFPKEY INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) en **TRUE** y, a continuación, no enviar ningún ejemplo con la extensión de unidad de datos content-type asociada puede provocar que el codificador se bloquea. Establezca el codificador para la codificación entrelazada solo si tiene muestras entrelazadas para entregar.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 




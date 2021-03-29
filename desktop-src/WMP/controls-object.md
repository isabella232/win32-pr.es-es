---
title: Controls (objeto)
description: El objeto Controls proporciona una manera de manipular la reproducción de archivos multimedia con las siguientes propiedades y métodos.
ms.assetid: bcc1e768-4fa6-4c82-a12f-52c9bfb4c10c
keywords:
- Objetos de control Media Player de Windows
topic_type:
- apiref
api_name:
- Controls Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bac91c522c95c1b45565ca013a000022c73bcc4
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "103784486"
---
# <a name="controls-object"></a>Controls (objeto)

El objeto **Controls** proporciona una manera de manipular la reproducción de archivos multimedia con las siguientes propiedades y métodos.

El objeto **Controls** admite las siguientes propiedades.



| Propiedad                                                            | Descripción                                                                                                                                       |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [audioLanguageCount](controls-audiolanguagecount.md)               | Recupera el número de idiomas de audio admitidos.                                                                                                |
| [currentAudioLanguage](controls-currentaudiolanguage.md)           | Especifica o recupera el identificador de configuración regional (LCID) del idioma de audio para la reproducción.                                                            |
| [currentAudioLanguageIndex](controls-currentaudiolanguageindex.md) | Especifica o recupera el índice basado en uno que corresponde al lenguaje de audio para la reproducción.                                                   |
| [currentItem](controls-currentitem.md)                             | Especifica o recupera el elemento multimedia actual.                                                                                                    |
| [currentMarker](controls-currentmarker.md)                         | Especifica o recupera el número de marcador actual.                                                                                                 |
| [currentPosition](controls-currentposition.md)                     | Especifica o recupera la posición actual en el elemento multimedia en segundos desde el principio.                                                      |
| [currentPositionString](controls-currentpositionstring.md)         | Recupera la posición actual en el elemento multimedia como una **cadena**.                                                                                 |
| [currentPositionTimecode](controls-currentpositiontimecode.md)     | Especifica o recupera la posición actual en el elemento multimedia actual mediante un formato de código de tiempo. Esta propiedad admite actualmente código de tiempo SMPTE. |
| [isAvailable](controls-isavailable.md)                             | Recupera si un tipo de información especificado está disponible o se puede realizar una acción determinada.                                                |



 

El objeto **Controls** admite los métodos siguientes.



| Método                                                                  | Descripción                                                                                      |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [fastForward](controls-fastforward.md)                                 | Inicia la reproducción rápida del elemento multimedia en la dirección de avance.                                     |
| [fastReverse](controls-fastreverse.md)                                 | Inicia la reproducción rápida del elemento multimedia en la dirección inversa.                                     |
| [getAudioLanguageDescription](controls-getaudiolanguagedescription.md) | Recupera la descripción del idioma de audio correspondiente al índice basado en uno especificado. |
| [getAudioLanguageID](controls-getaudiolanguageid.md)                   | Recupera el LCID para un índice de idioma de audio especificado.                                         |
| [getLanguageName](controls-getlanguagename.md)                         | Recupera el nombre del idioma de audio con el LCID especificado.                                |
| [siguiente](controls-next.md)                                               | Establece el elemento actual en el elemento siguiente de la lista de reproducción.                                          |
| [pause](controls-pause.md)                                             | Pausa la reproducción del elemento multimedia.                                                            |
| [reproducción](controls-play.md)                                               | Hace que el elemento multimedia empiece a reproducirse.                                                          |
| [playItem](controls-playitem.md)                                       | Hace que el elemento multimedia actual empiece a reproducir o reanuda la reproducción de un elemento en pausa.                |
| [previous](controls-previous.md)                                       | Establece el elemento actual en el elemento anterior de la lista de reproducción.                                      |
| [pasar](controls-step.md)                                               | Hace que el elemento multimedia de vídeo actual inmovilice la reproducción en el fotograma siguiente.                        |
| [stop](controls-stop.md)                                               | Detiene la reproducción del elemento multimedia.                                                             |



 

Se tiene acceso al objeto de **controles** a través de la propiedad siguiente.



| Object                      | Propiedad                        |
|-----------------------------|---------------------------------|
| [Reproductor](player-object.md) | [permite](player-controls.md) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





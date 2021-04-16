---
description: La propiedad KaraokeAudioPresentationMode establece o recupera la combinación de altavoces derecha izquierda para los canales de karaoke auxiliares.
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: Propiedad KaraokeAudioPresentationMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429f15c99d58136d4c423c4f66b19d12c93802a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686288"
---
# <a name="karaokeaudiopresentationmode-property"></a>Propiedad KaraokeAudioPresentationMode

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `KaraokeAudioPresentationMode` propiedad establece o recupera la combinación de altavoces derecha izquierda para los canales de karaoke auxiliares.

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que contiene un conjunto de marcas de bits que indican cómo se downmixed los canales de karaoke auxiliares a los altavoces izquierdo y derecho.

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura/escritura y su valor predeterminado es cero.

Los canales de audio están basados en cero, por lo que los canales 0 y 1 suelen representar los canales de altavoz derecho e izquierdo y los canales 2 a 4 son los tres canales de karaoke auxiliares. Cuando el objeto MSWebDVD entra en el modo de karaoke, silencia automáticamente los canales 2 y superiores. Use operaciones OR bit a bit para establecer **el bit adecuado** con el fin de enviar un canal auxiliar al altavoz izquierdo, altavoz derecho, ambos altavoces (ambos bits en) o sin altavoces (ambos bits desactivados). Estos bits están desactivados de forma predeterminada siempre que el navegador de DVD entra en el modo de karaoke. En la tabla siguiente se proporciona el valor de los bits y su acción correspondiente.



| Value  | Descripción                            |
|--------|----------------------------------------|
| 0x0004 | Canal 2 de downmix al altavoz izquierdo  |
| 0x0008 | Downmix Channel 3 al altavoz izquierdo  |
| 0x0010 | Canal 4 de downmix al altavoz izquierdo  |
| 0x0400 | Downmix Channel 2 al altavoz derecho |
| 0x0800 | Downmix Channel 3 al altavoz derecho |
| 0x1000 | Downmix Channel 4 al altavoz derecho |



 

 

 




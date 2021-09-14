---
description: La propiedadAudioAudioPresentationMode establece o recupera la combinación de altavoces de derecha a izquierda para los canales auxiliares.
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: PropiedadAudioPresentationMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429f15c99d58136d4c423c4f66b19d12c93802a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061047"
---
# <a name="karaokeaudiopresentationmode-property"></a>PropiedadAudioPresentationMode

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La propiedad establece o recupera la combinación del altavoz `KaraokeAudioPresentationMode` derecho-izquierdo para los canales auxiliares de canal.

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que contiene un conjunto de marcas de bits que indican cómo se mezclan los canales auxiliares de canal a la izquierda y a la derecha.

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura y escritura con un valor predeterminado de cero.

Los canales de audio son de base cero, por lo que los canales 0 y 1 suelen representar los canales de altavoz derecho e izquierdo, y los canales 2 a 4 son los tres canales auxiliares de canal auxiliar. Cuando el objeto MSWebDVD entra en modo de espera, silencia automáticamente los canales 2 y superiores. Use operaciones **OR** bit a bit para establecer el bit adecuado con el fin de enviar un canal auxiliar al hablante izquierdo, al altavoz derecho, a ambos altavoces (ambos bits en) o a ningún hablante (ambos bits desactivados). Todos estos bits están desactivados de forma predeterminada cada vez que el navegador de DVD entra en modo de navegación. El valor de los bits y su acción correspondiente se da en la tabla siguiente.



| Value  | Descripción                            |
|--------|----------------------------------------|
| 0x0004 | Canal 2 de la mezcla hacia abajo en el altavoz izquierdo  |
| 0x0008 | Canal 3 de la mezcla hacia abajo en el altavoz izquierdo  |
| 0x0010 | Canal 4 de la mezcla hacia abajo en el altavoz izquierdo  |
| 0x0400 | Canal 2 de la mezcla hacia abajo en el altavoz derecho |
| 0x0800 | Canal 3 de la mezcla hacia abajo en el altavoz derecho |
| 0x1000 | Canal 4 de la mezcla hacia abajo en el altavoz derecho |



 

 

 




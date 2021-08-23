---
description: La propiedadAudioAudioPresentationMode establece o recupera la combinación de altavoces de derecha a izquierda para los canales auxiliares.
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: PropiedadAudioPresentationMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af634a3beaade7e497cdc6d158ccf1121ebb09542bdec92ceaae823b1b91ccdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952384"
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

## <a name="remarks"></a>Comentarios

Esta propiedad es de lectura y escritura con un valor predeterminado de cero.

Los canales de audio son de base cero, por lo que los canales 0 y 1 suelen representar los canales de altavoz derecho e izquierdo, y los canales del 2 al 4 son los tres canales auxiliares. Cuando el objeto MSWebDVD entra en modo de espera, silencia automáticamente los canales 2 y superiores. Use operaciones **OR** bit a bit para establecer el bit adecuado con el fin de enviar un canal auxiliar al hablante izquierdo, al altavoz derecho, a ambos altavoces (ambos bits en) o a ningún hablante (ambos bits desactivados). Todos estos bits están desactivados de forma predeterminada cada vez que el navegador de DVD entra en modo de espera. El valor de los bits y su acción correspondiente se da en la tabla siguiente.



| Value  | Descripción                            |
|--------|----------------------------------------|
| 0x0004 | Canal 2 de la mezcla hacia abajo en el altavoz izquierdo  |
| 0x0008 | Canal 3 de la mezcla hacia abajo en el altavoz izquierdo  |
| 0x0010 | Canal 4 de la mezcla hacia abajo en el altavoz izquierdo  |
| 0x0400 | Canal 2 de la mezcla hacia abajo en el altavoz derecho |
| 0x0800 | Canal 3 de la mezcla hacia abajo en el altavoz derecho |
| 0x1000 | Canal 4 de la mezcla hacia abajo en el altavoz derecho |



 

 

 




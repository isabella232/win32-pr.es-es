---
title: Anidar metaarchivos
description: Anidar metaarchivos
ms.assetid: fa355c98-31e2-4bb9-ad67-fd9a727300c3
keywords:
- Metaarchivos de Windows Media, anidamiento
- Metaarchivos de Windows Media, hacer referencia a otros metaarchivos
- anidar metaarchivos
- metaarchivos, anidamiento
- metaarchivos, hacer referencia a otros metaarchivos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3cd5743424858c4bbcd6f66952f4275ea82d947e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356747"
---
# <a name="nesting-metafiles"></a>Anidar metaarchivos

Un metarchivo puede hacer referencia A otro metarchivo. Para hacer referencia a otro metarchivo, use el elemento **ENTRYREF** . Un elemento **ENTRYREF** del metarchivo principal apunta a un metarchivo externo.

El control Media Player de Windows procesa los elementos de **entrada** del metarchivo al que se hace referencia como si estuvieran incluidos en el metarchivo principal situado en la posición del elemento **ENTRYREF** . Sin embargo, omite cualquier elemento de **entrada** del metarchivo al que se hace referencia que tenga el atributo **SKIPIFREF** establecido en sí.

Los controles Windows Media Player 7,0, 7,1 y Windows Media Player para Windows XP omiten los elementos **ENTRYREF** del metarchivo al que se hace referencia. Por lo tanto, los metaarchivos solo se pueden anidar un nivel en profundidad con estas versiones. Estas versiones también omiten el elemento **ASX** y sus atributos en el archivo al que se hace referencia. Windows Media Player 9 series o posterior admiten la anidación de metaarchivos hasta 5 de profundidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> </dl>

 

 





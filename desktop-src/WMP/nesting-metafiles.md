---
title: Anidamiento de metarchivos
description: Anidamiento de metarchivos
ms.assetid: fa355c98-31e2-4bb9-ad67-fd9a727300c3
keywords:
- Windows Metarchivos multimedia, anidamiento
- Windows Metarchivos multimedia, referencia a otros metarchivos
- anidamiento de metarchivos
- metarchivos, anidamiento
- metarchivos, que hacen referencia a otros metarchivos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29a45bf545f839e111970b31d5faddd039959b7148a331fa5e347913b67327e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574278"
---
# <a name="nesting-metafiles"></a>Anidamiento de metarchivos

Un metarchivo puede hacer referencia a otro metarchivo. Para hacer referencia a otro metarchivo, use **el elemento ENTRYREF.** Un **elemento ENTRYREF** del metarchivo principal apunta a un metarchivo externo.

El Reproductor de Windows Media control procesa los elementos **ENTRY** del metarchivo al que se hace referencia como si estuvieran incluidos en el metarchivo principal en la posición del **elemento ENTRYREF.** Sin embargo, omite los elementos **ENTRY** del metarchivo al que se hace referencia que tienen el atributo **SKIPIFREF** establecido en YES.

Los Reproductor de Windows Media 7.0, 7.1 y Reproductor de Windows Media para Windows XP omiten los elementos **ENTRYREF** del metarchivo al que se hace referencia. Por lo tanto, los metarchivos solo se pueden anidar en profundidad de un nivel mediante estas versiones. Estas versiones también omiten **el elemento ASX** y sus atributos en el archivo al que se hace referencia. Reproductor de Windows Media serie 9 o posterior admite el anidamiento de metarchivos de hasta 5 de profundidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> </dl>

 

 





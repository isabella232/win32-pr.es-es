---
title: ITTSBufNotifySinkW
description: ITTSBufNotifySinkW
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a1ce3013ba1d8acf01f79b4f71d2d5088f4d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994530"
---
# <a name="ittsbufnotifysinkw"></a>ITTSBufNotifySinkW

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El motor debe llamar a través del **marcador**. Durante el preprocesamiento de la salida de voz, el código del agente de Microsoft inserta marcadores entre "palabras" y usa la llegada de esos marcadores para impulsar el ritmo del texto del globo de palabras. Aunque SAPI no requiere nada más que la llegada de esos marcadores en algún momento antes del final del utterance, los marcadores se deben devolver de forma relativamente puntual para admitir Microsoft Agent.

Tenga en cuenta que no hay un concepto estricto de "Word" en algunos lenguajes, como el japonés. El método [**Speak**](speak-method.md) de Microsoft Agent define una "palabra" como una cadena de símbolos conectada que tiene un significado y una pronunciación aislada. El agente de Microsoft utiliza código de análisis bastante sencillo para determinar qué es una "palabra": busca símbolos separados por espacios en blanco. Por lo tanto, hay tres "palabras" en la cadena inglesa "The 101 Dalmatians": "The", "101" y "Dalmatians". El texto incluido en la etiqueta de mapa del agente de Microsoft se trata como una única "palabra" para la presentación.

 

 





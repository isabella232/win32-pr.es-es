---
title: ITTSBufNotifySinkW
description: ITTSBufNotifySinkW
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de27451826a232092bc74e630a54621a004cc15e44ad4a9a7d3377509ff00ca5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476722"
---
# <a name="ittsbufnotifysinkw"></a>ITTSBufNotifySinkW

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

El motor debe llamar a través **de BookMark**. Durante el preprocesamiento de la salida de voz, el código de Microsoft Agent inserta marcadores entre "palabras" y usa la llegada de esos marcadores para impulsar el ritmo del texto en el globo de palabras. Aunque SAPI no requiere nada más que la llegada de esos marcadores en algún momento antes del final de la expresión, los marcadores deben devolverse de forma relativamente oportuna para admitir Microsoft Agent.

Tenga en cuenta que no hay ningún concepto estricto de "palabra" en algunos idiomas, como el japonés. El método [**Speak**](speak-method.md) de Microsoft Agent define una "palabra" como una cadena conectada de símbolos que tiene un significado y una pronunciación de forma aislada. Microsoft Agent usa código de análisis bastante sencillo para determinar qué es una "palabra": busca símbolos separados por espacios en blanco. Por lo tanto, hay tres "palabras" en la cadena en inglés "The 101 Dalmatians": "the", "one hundred and one" y "Dalmatians". El texto incluido en la etiqueta Mapa de Microsoft Agent se trata como una sola "palabra" con fines de presentación.

 

 





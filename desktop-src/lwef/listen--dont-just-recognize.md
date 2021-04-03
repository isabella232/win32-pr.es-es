---
title: Escuche, no reconozca simplemente
description: Escuche, no reconozca simplemente
ms.assetid: 74bb2122-98c1-4a51-b894-93e1481aa46b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e972a8c98460e58d0f7080d7de7641fb856c8317
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779410"
---
# <a name="listen-dont-just-recognize"></a>Escuche, no reconozca simplemente

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

La comunicación correcta implica más que el reconocimiento de palabras. El proceso de diálogo implica el intercambio de pilas para señalar la toma y la comprensión. Los caracteres pueden mejorar las interfaces de conversación proporcionando indicaciones como las inclinaciones de cabeza, nodos o sacudidas para indicar cuándo el motor de voz está en el estado escuchando y cuándo se reconoce algo. Por ejemplo, el agente de Microsoft Reproduce animaciones asignadas al estado de **escucha** cuando un usuario presiona la tecla de escucha de inserciones en la conversación y las animaciones asignadas al estado de la **audición** cuando se detecta un utterance. Al definir su propio carácter, asegúrese de crear y asignar animaciones adecuadas a estos Estados. Para obtener más información sobre el diseño de caracteres, vea [diseñar caracteres para el agente de Microsoft](designing-characters-for-microsoft-agent.md).

Además de las señales no verbales, una conversación implica un contexto común entre las partes que intervienen. Del mismo modo, es más probable que los escenarios de entrada de voz con caracteres tengan éxito cuando el contexto esté bien establecido. Establecer el contexto le permite interpretar mejor las frases de sonido similares, como "comprobar en el correo" y "comprobar mi correo". También puede permitir que el usuario realice consultas en el contexto proporcionando un comando, como "Help" o "Where I", al que responde restatendo el contexto actual, como la última acción realizada por la aplicación.

El agente de Microsoft proporciona interfaces que permiten obtener acceso a la mejor coincidencia y a las dos mejores alternativas siguientes devueltas por el motor de reconocimiento de voz. Además, puede tener acceso a las puntuaciones de confianza para todas las coincidencias. Puede usar esta información para determinar mejor lo que se ha hablado. Por ejemplo, si las puntuaciones de confianza de la mejor coincidencia y la primera alternativa están cerca, puede indicar que el motor de voz tenía dificultades para distinguir la diferencia entre ellos. En tal caso, es posible que desee pedir al usuario que repita o vuelva a formular la solicitud en un esfuerzo por mejorar el rendimiento. Sin embargo, si la mejor coincidencia y la primera o la segunda alternativas devuelven el mismo comando, refuerza la indicación del reconocimiento correcto.

La naturaleza de una conversación o diálogo implica que debe haber una respuesta a la entrada de voz. Por lo tanto, siempre se debe responder a la entrada de un usuario con comentarios verbales o visuales que indican que se ha realizado una acción o que se ha producido un problema, o bien proporciona una respuesta adecuada.

 

 





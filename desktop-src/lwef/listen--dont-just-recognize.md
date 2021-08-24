---
title: Listen, Dont Just Recognize
description: Listen, Dont Just Recognize
ms.assetid: 74bb2122-98c1-4a51-b894-93e1481aa46b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b226b9172b10c70e4e699a98df49acc002dcd5add95986c9efbdf9e8f057648d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888095"
---
# <a name="listen-dont-just-recognize"></a>Listen, Dont Just Recognize

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

La comunicación correcta implica más que el reconocimiento de palabras. El proceso de diálogo implica intercambiar indicaciones para indicar la toma de decisiones y la comprensión. Los caracteres pueden mejorar las interfaces conversacionales proporcionando indicaciones como inclinaciones de la cabeza, aserciones o agites para indicar cuándo el motor de voz está en estado de escucha y cuándo se reconoce algo. Por ejemplo, Microsoft Agent reproduce  animaciones asignadas al estado De escucha cuando un usuario presiona  la tecla de escucha push-to-talk y las animaciones asignadas al estado De escucha cuando se detecta una expresión. Al definir su propio carácter, asegúrese de crear y asignar animaciones adecuadas a estos estados. Para obtener más información sobre el diseño de caracteres, [vea Designing Characters for Microsoft Agent](designing-characters-for-microsoft-agent.md).

Además de las indicaciones no verbales, una conversación implica un contexto común entre las partes conversadores. De forma similar, los escenarios de entrada de voz con caracteres tienen más probabilidades de tener éxito cuando el contexto está bien establecido. Establecer el contexto le permite interpretar mejor frases similares, como "check's in the mail" y "check my mail". También puede permitir que el usuario consulte el contexto proporcionando un comando, como "Ayuda" o "Dónde estoy", al que responde reestableciendo el contexto actual, como la última acción que realizó la aplicación.

Microsoft Agent proporciona interfaces que permiten acceder a la mejor coincidencia y a las dos siguientes mejores alternativas devueltas por el motor de reconocimiento de voz. Además, puede acceder a las puntuaciones de confianza para todas las coincidencias. Puede usar esta información para determinar mejor lo que se ha hablado. Por ejemplo, si las puntuaciones de confianza de la mejor coincidencia y la primera alternativa están cerca, puede indicar que el motor de voz tuvo dificultades para distinguir la diferencia entre ellas. En tal caso, es posible que quiera pedir al usuario que repita o vuelva a cambiar la solicitud en un esfuerzo por mejorar el rendimiento. Sin embargo, si la mejor coincidencia y la primera o segunda alternativas devuelven el mismo comando, reforzará la indicación del reconocimiento correcto.

La naturaleza de una conversación o diálogo implica que debe haber una respuesta a la entrada hablada. Por lo tanto, siempre se debe responder a la entrada de un usuario con comentarios verbales o visuales que indiquen que se realizó una acción o se encontró un problema, o que proporciona una respuesta adecuada.

 

 





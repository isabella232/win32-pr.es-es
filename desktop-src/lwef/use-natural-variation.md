---
title: Usar variación natural
description: Usar variación natural
ms.assetid: 5d5750e4-cf30-43dc-9419-7e6bbdb9aa5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd2d35afeb168dc8839ba259f0079434b487c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148773"
---
# <a name="use-natural-variation"></a>Usar variación natural

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Mientras que la coherencia de la presentación en la interfaz convencional de la aplicación, como los menús y los cuadros de diálogo, hace que la interfaz sea más predecible, varíe la animación y la salida de voz en la interfaz del carácter. La variación adecuada de las respuestas del carácter proporciona una interfaz más natural. Si un carácter siempre dirige exactamente al usuario de la misma manera; por ejemplo, siempre diciendo las mismas palabras, es probable que el usuario tenga en cuenta el carácter aburrido, disinterested o, incluso, a la fuerza. La comunicación humana rara vez implica una repetición precisa. Incluso cuando se repite algo en una situación similar, podríamos cambiar el texto, gestos o expresiones faciales.

El agente de Microsoft le permite compilar en una variación de un carácter. Al definir animaciones de un carácter, puede usar las probabilidades de bifurcación en cualquier fotograma de animación para cambiar una animación cuando se reproduzca. También puede asignar varias animaciones a cada Estado. El agente de Microsoft elige aleatoriamente una de las animaciones asignadas cada vez que inicia un estado. En el caso de la salida de voz, también puede incluir caracteres de barra vertical en el texto de salida para modificar automáticamente el texto que se habla. Por ejemplo, el agente de Microsoft seleccionará aleatoriamente una de las instrucciones siguientes al procesar este texto como parte del método [**Speak**](speak-method.md) :

"Puedo decir esto. \| Lo puedo decir. \| Puedo decir algo más ".

 

 





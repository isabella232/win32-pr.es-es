---
title: Usar variación natural
description: Usar variación natural
ms.assetid: 5d5750e4-cf30-43dc-9419-7e6bbdb9aa5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6259730599966205f4751c4ada9b8ef361cedf6d1a1a59dd1ce7d67aaf0fb448
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474513"
---
# <a name="use-natural-variation"></a>Usar variación natural

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Aunque la coherencia de la presentación en la interfaz convencional de la aplicación, como los menús y los cuadros de diálogo, hace que la interfaz sea más predecible, varía la animación y la salida hablada en la interfaz del carácter. La variación adecuada de las respuestas del carácter proporciona una interfaz más natural. Si un carácter siempre se dirige al usuario exactamente de la misma manera; Por ejemplo, si siempre dice las mismas palabras, es probable que el usuario considere que el carácter es pesado, desinteresado o incluso desconfiado. La comunicación humana rara vez implica una repetición precisa. Incluso cuando se repite algo en una situación similar, podemos cambiar las palabras, los gestos o la expresión facial.

Microsoft Agent permite compilar en alguna variación para un carácter. Al definir las animaciones de un carácter, puede usar probabilidades de bifurcación en cualquier fotograma de animación para cambiar una animación cuando se reproduce. También puede asignar varias animaciones a cada estado. Microsoft Agent elige aleatoriamente una de las animaciones asignadas cada vez que inicia un estado. Para la salida de voz, también puede incluir caracteres de barra vertical en el texto de salida para variar automáticamente el texto hablado. Por ejemplo, Microsoft Agent seleccionará aleatoriamente una de las siguientes instrucciones al procesar este texto como parte del [**método Speak:**](speak-method.md)

"Puedo decir esto. \| Puedo decir eso. \| Puedo decir otra cosa".

 

 





---
title: Compatibilidad con globos de palabras
description: Compatibilidad con globos de palabras
ms.assetid: deac032f-0480-4a0d-bc69-e26f12666bbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78316c509ece6fc8f9b0cefd50b1564a50697a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268538"
---
# <a name="word-balloon-support"></a>Compatibilidad con globos de palabras

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

La salida de voz también puede aparecer como una salida de texto en forma de globo de palabra animado. Se puede utilizar para complementar la salida hablada de un carácter o como una alternativa a la salida de audio cuando se usa el método [**Speak**](speak-method.md) .

![sí, globo de palabra maestra](images/f3ballon.gif)

También puede usar un globo de palabras para comunicar qué es un carácter "pensando" con el método de [**reflexión**](think-method.md) . Esto muestra el texto que se proporciona en un globo "pensamiento" todavía. El método de **reflexión** también difiere del método [**Speak**](speak-method.md) en que no genera ninguna salida de audio.

Los globos de palabra solo admiten la comunicación con leyenda del carácter, no los datos proporcionados por el usuario. Por lo tanto, el globo de palabras no admite controles de entrada. Sin embargo, puede proporcionar fácilmente datos proporcionados por el usuario para un carácter, mediante interfaces del lenguaje de programación u otros servicios de entrada proporcionados por el agente de Microsoft, como el menú emergente.

Al definir un carácter, puede especificar si desea incluir la compatibilidad con globos de palabras. Sin embargo, si usa un carácter que incluye compatibilidad con globos de palabras, no puede deshabilitar la compatibilidad.

 

 





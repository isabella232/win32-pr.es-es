---
title: Compatibilidad con globos de palabras
description: Compatibilidad con globos de palabras
ms.assetid: deac032f-0480-4a0d-bc69-e26f12666bbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aea0fbd2f73aefb1cedb7c57fc6359849c050761448fc45a9b4c90ea477f53f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066726"
---
# <a name="word-balloon-support"></a>Compatibilidad con globos de palabras

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

La salida hablada también puede aparecer como salida textual en forma de globo de palabras de animación. Se puede usar para complementar la salida hablada de un carácter o como alternativa a la salida de audio cuando se usa el [**método Speak.**](speak-method.md)

![sí, globo de palabra maestra](images/f3ballon.gif)

También puede usar un globo de palabras para comunicar lo que un carácter está "pensando" mediante el [**método Think.**](think-method.md) Se muestra el texto que se proporciona en un globo todavía "pensado". El **método Think** también difiere del método [**Speak**](speak-method.md) en que no genera ninguna salida de audio.

Los globos de palabras solo admiten la comunicación con subtítulos del carácter, no la entrada del usuario. Por lo tanto, el globo de palabras no admite controles de entrada. Sin embargo, puede proporcionar fácilmente la entrada del usuario para un carácter, mediante interfaces del lenguaje de programación u otros servicios de entrada proporcionados por Microsoft Agent, como el menú emergente.

Al definir un carácter, puede especificar si se debe incluir la compatibilidad con globos de palabras. Sin embargo, si usa un carácter que incluye compatibilidad con globos de palabras, no puede deshabilitar la compatibilidad.

 

 





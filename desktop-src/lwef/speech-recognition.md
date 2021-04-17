---
title: Reconocimiento de voz
description: Reconocimiento de voz
ms.assetid: cb5ac509-12a4-4ca4-8776-424568cf780d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5c037ced96c386a5e0baf18eeba258422e0193
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704800"
---
# <a name="speech-recognition"></a>Reconocimiento de voz

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El reconocimiento de voz proporciona una interfaz muy natural y familiar para interactuar con los caracteres. Sin embargo, la entrada de voz también presenta muchos desafíos. Los motores de voz operan actualmente sin partes sustanciales del repertorio de comunicación de voz humana, como gestos, Intonation y expresiones faciales. Además, la voz natural normalmente no está enlazada. Es fácil que el orador supere el vocabulario actual, o la *gramática*, del motor. De forma similar, el orden de las palabras o las palabras puede variar para cualquier solicitud o respuesta determinada. Además, los motores de reconocimiento de voz a menudo deben tratar las grandes variaciones en el entorno del hablante. Por ejemplo, el ruido de fondo, la calidad del micrófono y la ubicación pueden afectar a la calidad de la entrada. De forma similar, las pronunciaciones de altavoces diferentes o incluso las variaciones del mismo orador, como cuando el altavoz tiene un frío, dificulta la conversión de los datos acústicos en una comprensión de representación. Por último, los motores de voz también deben tratar con palabras o frases de sonido similares en un idioma, como "nuevo", "sabía" y "GNU", o "Wreck una buena playa" y "reconocer la voz".

La voz no es siempre la mejor forma de entrada para una tarea. Debido a la naturaleza de la toma de voz, a menudo puede ser más lenta que otras formas de entrada. Al igual que el teclado, la entrada de voz es una interfaz pobre para apuntar a menos que se proporcione algún tipo de representación de tecla de tecla. Por lo tanto, considere siempre si la voz es la entrada más adecuada para una tarea. Es mejor evitar el uso de voz como interfaz exclusiva para cualquier tarea. Proporcionan otras formas de obtener acceso a cualquier funcionalidad básica mediante métodos como el mouse o el teclado. Además, aproveche la naturaleza multimodal del uso de voz en la interfaz visual combinando la entrada de voz con información visual que ayuda a especificar el contexto y las opciones.

Por último, el uso correcto de la entrada de voz se debe a una parte de la calidad de la tecnología. Incluso el reconocimiento humano, que supera cualquier tecnología de reconocimiento actual, a veces produce un error. Sin embargo, en la comunicación humana usamos estrategias que mejoran la probabilidad de éxito y que proporcionan recuperación de errores cuando algo sale mal. Por lo tanto, la eficacia de la entrada de voz también depende de la calidad de la interfaz de usuario que la presenta.

Estudiar modelos humanos de interacción de voz puede ser útil al diseñar interfaces de voz más naturales. Grabar cuadros de diálogo de voz humanos reales para escenarios concretos puede ayudarle a comprender mejor las construcciones y patrones usados, así como formas eficaces de comentarios y recuperación de errores. Puede ayudar a determinar el vocabulario adecuado que se debe usar (para la entrada y la salida). Es mejor diseñar una interfaz de voz basada en el modo en que los usuarios hablan realmente que simplemente derivarla de la interfaz gráfica en la que funciona.

Tenga en cuenta que el agente de Microsoft usa Microsoft Speech API (SAPI) para admitir el reconocimiento de voz. Esto permite usar el agente de Microsoft con una variedad de motores compatibles. Aunque el agente de Microsoft especifica ciertas interfaces básicas, los requisitos de rendimiento y la calidad de un motor pueden variar.

La voz no es el único medio para admitir interfaces de conversación. También puede utilizar el procesamiento en lenguaje natural de la entrada del teclado en lugar de o además de la voz. En esas situaciones, puede seguir aplicando normalmente directrices para la entrada de voz.

-   [Escuche, no reconozca simplemente](listen--dont-just-recognize.md)
-   [Clarificar y limitar las opciones](clarify-and-limit-choices.md)
-   [Proporcionar una recuperación de errores](provide-good-error-recovery.md)

 

 





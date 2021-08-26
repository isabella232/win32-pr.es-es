---
title: Reconocimiento de voz
description: Reconocimiento de voz
ms.assetid: cb5ac509-12a4-4ca4-8776-424568cf780d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd36ea5754d53ceda2761635ecb838fdfb0328617827ca90fc969af915b4ea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960855"
---
# <a name="speech-recognition"></a>Reconocimiento de voz

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

El reconocimiento de voz proporciona una interfaz muy natural y familiar para interactuar con caracteres. Sin embargo, la entrada de voz también presenta muchos desafíos. Actualmente, los motores de voz funcionan sin partes sustanciales de la comunicación de voz humana, como gestos, en intonación y expresiones faciales. Además, la voz natural suele estar sin enlazar. Es fácil para el hablante superar el vocabulario actual, o *gramática,* del motor. Del mismo modo, el orden de las palabras o las palabras puede variar para cualquier solicitud o respuesta determinada. Además, los motores de reconocimiento de voz a menudo deben tratar con grandes variaciones en el entorno del hablante. Por ejemplo, el ruido de fondo, la calidad del micrófono y la ubicación pueden afectar a la calidad de la entrada. De forma similar, las diferentes pronunciaciones del hablante o incluso las variaciones del mismo hablante, como cuando el hablante tiene un frío, hacen que sea un desafío convertir los datos acústicos en una comprensión representacional. Por último, los motores de voz también deben tratar con palabras o frases similares que suenan en un idioma, como "nuevo", "conocido" y "gnu", o "para que una buena costa" y "reconozca la voz".

La voz no siempre es la mejor forma de entrada para una tarea. Debido a la naturaleza de turnos de voz, a menudo puede ser más lenta que otras formas de entrada. Al igual que el teclado, la entrada de voz es una interfaz deficiente para apuntar a menos que se proporciona algún tipo de representación mnemotécnica. Por lo tanto, considere siempre si la voz es la entrada más adecuada para una tarea. Es mejor evitar el uso de voz como interfaz exclusiva para cualquier tarea. Proporcione otras formas de acceder a cualquier funcionalidad básica mediante métodos como el mouse o el teclado. Además, aproveche la naturaleza multimodal del uso de voz en la interfaz visual mediante la combinación de la entrada de voz con información visual que ayuda a especificar el contexto y las opciones.

Por último, el uso correcto de la entrada de voz solo se debe en parte a la calidad de la tecnología. Incluso el reconocimiento humano, que supera cualquier tecnología de reconocimiento actual, a veces produce un error. Sin embargo, en la comunicación humana usamos estrategias que mejoran la probabilidad de éxito y que proporcionan recuperación de errores cuando algo sale mal. Por lo tanto, la eficacia de la entrada de voz también depende de la calidad de la interfaz de usuario que la presenta.

El estudio de modelos humanos de interacción de voz puede ser útil al diseñar interfaces de voz más naturales. La grabación de diálogos de voz reales para escenarios concretos puede ayudarle a comprender mejor las construcciones y patrones usados, así como formas eficaces de comentarios y recuperación de errores. Puede ayudar a determinar el vocabulario adecuado que se va a usar (para entrada y salida). Es mejor diseñar una interfaz de voz en función de cómo habla realmente la gente que simplemente derivarla de la interfaz gráfica en la que opera.

Tenga en cuenta que Microsoft Agent usa Microsoft Speech API (SAPI) para admitir el reconocimiento de voz. Esto permite que Microsoft Agent se utilice con una variedad de motores compatibles. Aunque Microsoft Agent especifica determinadas interfaces básicas, los requisitos de rendimiento y la calidad de un motor pueden variar.

La voz no es el único medio de admitir interfaces conversacionales. También puede usar el procesamiento en lenguaje natural de la entrada de teclado en lugar de o además de voz. En esas situaciones, todavía puede aplicar generalmente directrices para la entrada de voz.

-   [Listen, Don't Just Recognize](listen--dont-just-recognize.md)
-   [Aclaración y limitación de opciones](clarify-and-limit-choices.md)
-   [Proporcionar una buena recuperación de errores](provide-good-error-recovery.md)

 

 





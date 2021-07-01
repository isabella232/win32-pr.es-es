---
title: Aclaración y limitación de opciones
description: Aclaración y limitación de opciones
ms.assetid: 4ec3ca01-231b-4a45-aae1-fba5b2ba0033
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 953001d706089244d6366c8dab0cdb580a2d72ca
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118480"
---
# <a name="clarify-and-limit-choices"></a>Aclaración y limitación de opciones

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

El reconocimiento de voz es más correcto cuando el usuario aprende el intervalo de gramática adecuada. También funciona mejor cuando el intervalo de opciones es limitado. Entre menos abierta sea la entrada, mejor podrá analizar el motor de voz la entrada de información acústica.

Microsoft Agent incluye varias disposiciones integradas que aumentan el éxito de la entrada de voz. La primera es la ventana Comandos que se muestra cuando el usuario dice "Abrir ventana comandos" o "¿Qué puedo decir?". (o cuando el usuario elige Abrir ventana comandos en el menú emergente del carácter). La ventana Comandos sirve como guía visual de la gramática activa del motor de voz. También reduce los errores de reconocimiento activando solo la gramática de voz de la aplicación activa de entrada y los comandos globales de Microsoft Agent. Por lo tanto, la gramática activa del motor de voz se aplica al contexto inmediato. Para obtener más información sobre la ventana Comandos, vea [Microsoft Agent Programming Interface Overview](microsoft-agent-programming-interface-overview.md).

Al crear comandos habilitados para voz de Microsoft Agent, puede crear el texto del título que aparece en la ventana Comandos, así como su texto de voz (gramática), las palabras que el motor debe usar para buscar coincidencias con este comando. Intente siempre que los comandos son lo más distintivos posible. Cuanto mayor sea la diferencia entre la redacción de comandos, especialmente para el texto de voz, más probable es que el motor de voz pueda discriminar entre los comandos hablados y proporcionar una coincidencia precisa. Evite también comandos de una sola palabra o muy cortos. Por lo general, una mayor información acústica en una expresión hablada ofrece al motor una mejor oportunidad de hacer una coincidencia precisa.

Al definir el texto de voz de un comando, proporcione una variedad razonable de palabras. Las solicitudes que significan lo mismo se pueden frases muy diferentes, como se muestra en el ejemplo siguiente:

Agregue algo de pepperoni.

Me gustaría algo de pepperoni.

¿Podría agregar algo de pepperoni?

Pepperoni, por favor.

Microsoft Agent permite especificar fácilmente alternativas u palabras opcionales para la gramática de voz de la aplicación. Puede incluir palabras o frases alternativas entre paréntesis, separados por un carácter de barra vertical. Puede definir palabras opcionales si las incluye entre caracteres entre corchetes. También puede anidar alternativas u palabras opcionales. Además, también puede usar puntos suspensivos (...) en texto de voz como marcador de posición para cualquier palabra. Sin embargo, el uso de puntos suspensivos con demasiada frecuencia puede dificultar que el motor distinga entre distintos comandos de voz. En cualquier caso, asegúrese siempre de que el texto de voz incluya al menos una palabra distintiva para cada comando que no sea opcional. Normalmente, debe coincidir con una palabra o palabras en el texto del título que defina que aparece en la ventana Comandos.

Aunque puede incluir símbolos, signos de puntuación o abreviaturas en el texto del título, evite que se incluyan en el texto de voz. Muchos motores de reconocimiento de voz no pueden controlar símbolos y abreviaturas o pueden usarlos para establecer parámetros de entrada especiales. Además, deletree los números. Esto también garantiza una compatibilidad de reconocimiento más confiable.

También puede usar avisos de directiva para evitar la entrada de fin abierto. La directiva solicita implícitamente que se haga referencia a las opciones o se especifiquen explícitamente, como se muestra en los ejemplos siguientes:



| Prompt                                           | Evaluación                                                    |
|--------------------------------------------|-----------------------------------------------------|
| ¿Qué quieres?                          | Demasiado general, una solicitud abierta                  |
| Elija un estilo de pizza o un ingrediente.        | Bueno, si las opciones son visibles, pero siguen siendo generales     |
| Diga "Sayan", "Chicago" o "The Works". | Mejor, una directiva explícita con opciones específicas |



 

Esto guía al usuario hacia la emisión de un comando válido. Al sugerir las palabras o frases, es más probable que pueda obtener las palabras esperadas a cambio. Para evitar repeticiones poco naturales, cambie la redacción o acorte el original para su posterior presentación a medida que el usuario se vuelve más experimentado con el estilo de entrada. Los avisos de directiva también se pueden usar en situaciones en las que el usuario no puede emitir un comando dentro de un tiempo prescrito o no puede proporcionar un comando esperado. Los mensajes de directiva se pueden proporcionar mediante la salida de voz, las interfaces de aplicación o ambos. La clave es ayudar al usuario a conocer las opciones adecuadas.

La redacción influye en el éxito de un aviso. Por ejemplo, el mensaje "¿Desea pedir la pizza?" podría generar una respuesta "Sí" o "No", pero también podría generar una solicitud de pedido. Defina avisos que no sean ambiguos o que se preparen para aceptar una mayor variedad de respuestas posibles. Además, tenga en cuenta la tendencia de las personas a imitar palabras y construcciones que escuchan. Esto se puede usar a menudo para ayudar a provocar una respuesta adecuada, como en el ejemplo siguiente:

**Usuario:** Muéseme todos los mensajes de Paul.

**Carácter:**

Es más probable que se pueda obtener el nombre completo de una de las partes con el posible prefijo "Quiero decir" o "Quiero decir".

Dado que los caracteres de Microsoft Agent funcionan dentro de la interfaz visual de Microsoft Windows, puede usar elementos visuales para proporcionar avisos de directiva para la entrada de voz. Por ejemplo, puede tener el gesto de carácter en una lista de opciones y solicitar que el usuario seleccione una, o mostrar opciones en un cuadro de diálogo o ventana de mensaje. Esto tiene dos ventajas: sugiere explícitamente las palabras que quiere que el usuario diga y proporciona una manera alternativa para que el usuario responda.

También puede usar otros modos de interacción para sugerir sutilmente a los usuarios la gramática de voz adecuada, como se muestra en el ejemplo siguiente:

**Usuario:** (hace clic en la opción de pizza estilo Hawái con el mouse)

**Carácter:** Pizza de estilo hawái.

**Usuario:** (hace clic en la opción De queso adicional con el mouse)

**Carácter:** Agregue "Queso adicional".

Otro factor importante en la entrada de voz correcta es la indicación al usuario cuando el motor está listo para la entrada, ya que muchos motores de voz solo permiten una sola expresión a la vez. Microsoft Agent proporciona compatibilidad para esto de dos maneras. En primer lugar, si la tarjeta de sonido admite MIDI, Microsoft Agent genera un tono breve para indicar cuándo está disponible el canal de entrada de voz. En segundo lugar, la ventana Sugerencia de escucha muestra un mensaje de texto adecuado cuando el carácter (motor de voz) está escuchando la entrada. Además, esta sugerencia muestra lo que ha oído el motor.

 

 





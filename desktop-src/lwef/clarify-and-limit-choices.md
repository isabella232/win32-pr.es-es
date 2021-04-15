---
title: Clarificar y limitar las opciones
description: Clarificar y limitar las opciones
ms.assetid: 4ec3ca01-231b-4a45-aae1-fba5b2ba0033
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ed5f95c2e516f304ffa28bcca1d9fd67a9169
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714213"
---
# <a name="clarify-and-limit-choices"></a>Clarificar y limitar las opciones

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El reconocimiento de voz se vuelve más eficaz cuando el usuario aprende el intervalo de gramática adecuado. También funciona mejor cuando el intervalo de opciones es limitado. Cuanto menos abierto sea la entrada, mejor será el motor de voz el que puede analizar la entrada de información acústica.

Microsoft Agent incluye varias disposiciones integradas que aumentan el éxito de la entrada de voz. La primera es la ventana comandos que se muestra cuando el usuario dice, "Abrir ventana comandos" o "¿Qué puedo decir?". (o cuando el usuario elige abrir la ventana comandos en el menú emergente del carácter). La ventana comandos sirve como guía visual para la gramática activa del motor de voz. También reduce los errores de reconocimiento activando solo la gramática de voz de la aplicación de entrada-actividad y los comandos globales del agente de Microsoft. Por lo tanto, la gramática activa del motor de voz se aplica al contexto inmediato. Para obtener más información sobre la ventana comandos, vea [Introducción a la interfaz de programación del agente de Microsoft](microsoft-agent-programming-interface-overview.md).

Al crear comandos de Microsoft Agent habilitados para voz, puede crear el texto de título que aparece en la ventana comandos, así como su texto de voz (gramática), las palabras que el motor debe utilizar para hacer coincidir este comando. Intente siempre que los comandos sean lo más distintivos posible. Cuanto mayor sea la diferencia entre las palabras de los comandos, especialmente en el caso del texto de la voz, más probable será que el motor de voz pueda discriminar entre los comandos leídos y proporcionar una coincidencia exacta. Evite también comandos de una sola palabra o muy breve. Por lo general, una información más acústica en una utterance oral proporciona al motor una mejor oportunidad de hacer una coincidencia exacta.

Al definir el texto de la voz de un comando, proporcione una variedad razonable de palabras. Las solicitudes que significan lo mismo pueden ser frases muy diferentes, como se muestra en el ejemplo siguiente:

Agregue algunos pepperoni.

Me gustaría algunos pepperoni.

¿Se puede Agregar algún pepperoni?

Pepperoni, por favor.

Microsoft Agent le permite especificar fácilmente alternativas u palabras opcionales para la gramática de voz de la aplicación. Puede incluir palabras o frases alternativas entre paréntesis, separadas por un carácter de barra vertical. Puede definir palabras opcionales mediante su inclusión entre corchetes. También puede anidar alternativas u palabras opcionales. Además, también puede usar puntos suspensivos (...) en el texto de la voz como un marcador de posición para cualquier palabra. Sin embargo, el uso de elipses con demasiada frecuencia puede dificultar que el motor distinga entre distintos comandos de voz. En cualquier caso, asegúrese siempre de que el texto de voz incluye al menos una palabra distintiva para cada comando que no sea opcional. Normalmente, debe coincidir con una palabra o palabras del texto de título que defina que aparezca en la ventana comandos.

Aunque puede incluir símbolos, signos de puntuación o abreviaturas en el texto de la leyenda, evite que se incluyan en el texto de la voz. Muchos motores de reconocimiento de voz no pueden controlar símbolos y abreviaturas, o pueden usarlos para establecer parámetros de entrada especiales. Además, los números se deletrean. Esto también garantiza un soporte de reconocimiento más confiable.

También puede usar solicitudes de directiva para evitar la entrada de cierre. Las solicitudes de directiva hacen referencia implícitamente a las opciones o las indican explícitamente, como se muestra en los ejemplos siguientes:



|                                            |                                                     |
|--------------------------------------------|-----------------------------------------------------|
| ¿Qué quieres?                          | Demasiado general, una solicitud abierta                  |
| Elija un estilo o ingrediente de pizza.        | Bueno, si las opciones son visibles pero siguen siendo generales     |
| Por ejemplo, "Hawai", "Chicago" o "The Works." | Mejor, una directiva explícita con opciones específicas |



 

Esto guía al usuario para que emita un comando válido. Al sugerir las palabras o la frase, es más probable que se produzca el texto esperado en la devolución. Para evitar la repetición no natural, cambie el texto o acorte el original para la presentación posterior a medida que el usuario se vuelva más experimentado con el estilo de entrada. Las solicitudes de directiva también se pueden usar en situaciones en las que el usuario no pueda emitir un comando dentro de un tiempo establecido o no pueda proporcionar un comando esperado. Se pueden proporcionar mensajes de Directiva mediante la salida de voz, las interfaces de aplicación o ambos. La clave ayuda al usuario a conocer las opciones adecuadas.

El texto influye en el éxito de un mensaje. Por ejemplo, el mensaje "¿desea solicitar la pizza?" puede generar una respuesta "sí" o "no", pero también puede generar una solicitud de pedido. Defina los mensajes que no sean ambiguos o Prepárese para aceptar una mayor variedad de respuestas posibles. Además, tenga en cuenta la tendencia de que los usuarios imiten palabras y construcciones que escuchan. A menudo, esto se puede usar para ayudar a provocar una respuesta adecuada como en el ejemplo siguiente:



|            |                                 |
|------------|---------------------------------|
| User:      | Mostrar todos los mensajes de Paul. |
| Óptico |                                 |



 

Es más probable que se produzca el nombre completo de una de las partes con el prefijo posible de "I Mean" o "I".

Dado que los caracteres de Microsoft Agent funcionan dentro de la interfaz visual de Microsoft Windows, puede usar elementos visuales para proporcionar indicaciones de directiva para la entrada de voz. Por ejemplo, puede tener el gesto de caracteres en una lista de opciones y solicitar que el usuario seleccione una o mostrar las opciones en un cuadro de diálogo o ventana de mensaje. Esto tiene dos ventajas: sugiere explícitamente las palabras que desea que el usuario hable y proporciona una forma alternativa de que el usuario responda.

También puede usar otros modos de interacción para sugerir sutilmente a los usuarios la gramática de voz adecuada, tal como se muestra en el ejemplo siguiente:



|            |                                                     |
|------------|-----------------------------------------------------|
| User:      | (Haga clic en la opción de pizza de estilo Hawai con el mouse) |
| Óptico | Pizza de estilo Hawai.                               |
| User:      | (Haga clic en la opción de queso adicional con el mouse)         |
| Óptico | Agregue "queso adicional".                                 |



 

Otro factor importante en la entrada de voz correcta es cueing el usuario cuando el motor está listo para la entrada, ya que muchos motores de voz solo permiten un utterance a la vez. El agente de Microsoft proporciona compatibilidad para esto de dos maneras. En primer lugar, si la tarjeta de sonido es compatible con MIDI, Microsoft Agent genera un breve tono para indicar cuándo está disponible el canal de entrada de voz. En segundo lugar, la ventana de la sugerencia de escucha muestra un mensaje de texto adecuado cuando el carácter (motor de voz) está escuchando entradas. Además, esta sugerencia muestra lo que el motor ha escuchado.

 

 





---
title: Proporcionar una recuperación de errores
description: Proporcionar una recuperación de errores
ms.assetid: 48e00638-9274-49db-93ec-ed444f526441
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a2abc32e1bdf6422e2d8d6422a17e0b881c6ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104074973"
---
# <a name="provide-good-error-recovery"></a>Proporcionar una recuperación de errores

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Como con cualquier interfaz bien diseñada, el proceso interactivo debe minimizar las circunstancias que conducen a errores. Sin embargo, rara vez es posible eliminar todos los errores, por lo que es esencial admitir una recuperación de errores para mantener la confianza y el interés del usuario. En general, la recuperación de errores implica detectar un error, determinar la causa y definir una manera de resolver el error. Los usuarios responden mejor a las interfaces que son cooperativas, que funcionan con el usuario para realizar una tarea.

El primer paso para la recuperación de errores de voz es detectar la condición de error. Se puede producir un error en el reconocimiento de voz debido a diversos errores. Las condiciones de error se pueden detectar normalmente como resultado de una entrada no válida, una corrección o cancelación explícita del usuario o la repetición del usuario.

Se produce un *error de rechazo* cuando el motor de reconocimiento no tiene ninguna coincidencia con lo que ha dicho usuario. El ruido de fondo o los primeros inicios son también las causas comunes de los errores de reconocimiento, por lo que solicitar al usuario que repita un comando suele ser una buena solución inicial. Sin embargo, si la frase está fuera de la gramática activa actual, pedir al usuario que vuelva a formular la solicitud puede resolver el problema. La diferencia en el texto puede dar lugar a una coincidencia con algo en la gramática actual. La enumeración o la sugerencia de las opciones de entrada previstas adecuadas es otra alternativa.

Una buena estrategia para la recuperación de errores de rechazo es combinar estas técnicas para que el usuario vuelva a realizar el seguimiento, ofreciendo cada vez más ayuda si el error persiste. Por ejemplo, puede empezar por responder al error inicial con una interrogación como "¿EH?" o "What?" o bien, un gesto de mano. Una respuesta corta aumenta la probabilidad de que la instrucción repetida del usuario no genere un error porque el usuario habló demasiado pronto. Tras un error repetido, la solicitud subsiguiente a reformular mejora la posibilidad de buscar coincidencias con algo en la gramática dada. A partir de aquí, proporcionar mensajes explícitos de comandos aceptados aumenta aún más la posibilidad de una coincidencia. Esta técnica se muestra en el ejemplo siguiente:



|            |                                                                            |
|------------|----------------------------------------------------------------------------|
| User:      | Me gustaría una pizza de estilo Chicago con anchovies.                             |
| Óptico | (Mano a lengüeta) ¿Verdad?                                                         |
| User:      | Quiero una pizza de Chicago con anchovies.                                     |
| Óptico | (Sacudida de cabeza) Vuelva a formular la solicitud.                                 |
| User:      | Dije pizza de Chicago, con anchovies.                                      |
| Óptico | (Shrug) Lo siento. Indique el estilo de pizza que quiera.                    |
| User:      | Chicago, con anchovies.                                                   |
| Óptico | Todavía no tiene suerte. Esto es lo que puede decir: "Chicago", "Hawai" o "Combo". |



 

Para que el control de errores resulte más natural, asegúrese de proporcionar un grado de variación aleatoria al responder a los errores. Además, una reacción de usuario natural a cualquier solicitud para repetir una respuesta es exagerar o aumentar el volumen al repetir la instrucción. Puede que le resulte útil recordar ocasionalmente al usuario hablar con normalidad, ya que la exageración o el aumento del volumen pueden dificultar el reconocimiento del motor de voz.

La asistencia progresiva debe hacer más que la atención del usuario. debe guiar al usuario para que hable en la gramática actual mediante la entrega sucesiva de mensajes más informativos. Las interfaces que parecen estar intentando comprender fomentan un alto grado de satisfacción y tolerancia del usuario.

Los *errores de sustitución*, en los que el motor de voz reconoce la entrada pero coincide con el comando equivocado, son más difíciles de resolver, ya que el motor de voz detecta un utterance coincidente. También puede producirse una falta de coincidencia si el motor de voz interpreta sonidos extraños como entrada válida (también conocido como *error de inserción*). En estas situaciones, se necesita la asistencia del usuario para identificar la condición de error. Para ello, puede repetir lo que el motor de voz devolvió y pedir al usuario que lo confirme antes de continuar:



|            |                                                   |
|------------|---------------------------------------------------|
| User:      | Me gustaría una pizza de estilo Chicago.                   |
| Óptico | ¿Dijo que le gustaría una "pizza de estilo Chicago"?   |
| User:      | Sí.                                              |
| Óptico | ¿Qué ingredientes adicionales desea incluir? |
| User:      | Anchovies.                                        |
| Óptico | ¿Dijo "anchovies"?                          |
| User:      | Sí.                                              |



 

Sin embargo, el uso de esta técnica para cada utterance se vuelve ineficaz y una tarea ardua. Para controlar esto, restrinja la confirmación a situaciones que tengan consecuencias negativas significativas o aumente la complejidad de la tarea inmediata. Si es fácil para el usuario realizar o invertir los cambios, es posible que pueda evitar solicitar la confirmación de sus elecciones. Del mismo modo, si hace que las opciones sean visibles, es posible que no tenga que proporcionar una corrección explícita. Por ejemplo, la elección de un elemento de una lista puede no requerir la comprobación porque el usuario puede ver los resultados y cambiarlos fácilmente. También puede usar calificaciones alternativas y de confianza para proporcionar un umbral de confirmación. Puede ajustar el umbral manteniendo un historial de las acciones del usuario en una situación determinada y eliminando la comprobación basada en una confirmación de usuario coherente. Por último, tenga en cuenta la naturaleza multimoda de la interfaz. La confirmación del mouse o del teclado también puede ser adecuada.

Elija cuidadosamente el texto de las confirmaciones. Por ejemplo, "¿dijo...?" o "Creo que dijo..." son mejores que "¿realmente desea...?" Dado que las frases anteriores implican que se está consultando la precisión de la escucha (reconocimiento) del carácter, no es posible que el usuario haya incorrecto.

Considere también la gramática de una respuesta. Por ejemplo, una respuesta negativa es probable que genere un error de rechazo, lo que requiere un mensaje adicional, tal como se muestra en el ejemplo siguiente:



|            |                          |
|------------|--------------------------|
| User:      | Me gustaría algunos pepperoni. |
| Óptico | ¿Dijo "sin jamón"?    |
| User:      | No, dije pepperoni.    |
| Óptico | ¿Verdad?                     |
| User:      | Pepperoni.               |



 

La modificación de la gramática para incluir prefijos para controlar las variaciones de respuesta naturales aumenta la eficacia del proceso de recuperación, especialmente cuando el usuario no confirma la solicitud de comprobación. En este ejemplo, la confirmación se podría haber controlado en un solo paso mediante la modificación de la gramática de "pepperoni" incluyendo también "no dije pepperoni", "dije pepperoni" y "no pepperoni".

También puede controlar los errores de sustitución usando las coincidencias alternativas devueltas por el motor de voz como confirmación correctiva:



|           |                                                                                        |
|-----------|----------------------------------------------------------------------------------------|
| User (Usuario)      | Me gustaría algunos pepperoni.                                                               |
| Carácter | (Oye "sin jamón" como mejor coincidencia, "pepperoni" como primera alternativa) ¿Dijo "sin jamón"? |
| User (Usuario)      | No, pepperoni.                                                                         |
| Carácter | (Sigue escuchando "sin jamón" como mejor coincidencia, pero ahora ofrece la primera alternativa). "Pepperoni"?    |



 

Del mismo modo, puede mantener un historial de errores de sustitución comunes y, si un error determinado es frecuente, ofrecer la alternativa la primera vez.

En cualquier situación de error de reconocimiento, evite culpa el usuario. Si el carácter sugiere o incluso implica que el usuario es culpable, o el carácter parece diferente al error, el usuario puede quedar inofensivo. Aquí también, elija cuidadosamente el texto que acepta explícitamente la responsabilidad, es adecuado para la situación y utiliza variedad para crear una respuesta más natural. Al expresar un disculpa, evite palabras ambiguas como "vaya" o "Oh-oh" que podría interpretarse como culpa al usuario. En su lugar, use frases como "lo siento" o "mi error". Los errores repetidos o más graves pueden utilizar un disculpa más elaborado, como "me siento realmente." Considere también la personalidad del carácter al determinar el tipo de respuesta. Otra opción es culpar una situación externa. Los comentarios como, por ejemplo, "chico, se descartan allí", toman el culpa del usuario y el carácter. Recordar el usuario de la naturaleza cooperativa de la interacción puede ser útil también: considerar frases como, "veamos lo que podemos hacer para realizar este trabajo".

El agente de Microsoft también admite algunos comentarios automáticos para el reconocimiento. Cuando se detecta un utterance, la sugerencia de escucha muestra el texto de la voz de la mejor coincidencia. Puede establecer su propio texto para que se muestre en función de la configuración de confianza de un comando que defina.

Debido a un error potencial, siempre se requiere confirmación para las opciones que tienen consecuencias negativas graves y son irreversibles. Naturalmente, querrá solicitar la confirmación cuando los resultados de una acción puedan ser destructivos. Sin embargo, considere la posibilidad de solicitar también la confirmación de situaciones que anulen cualquier proceso o operación prolongada.

 

 





---
title: Proporcionar una buena recuperación de errores
description: Proporcionar una buena recuperación de errores
ms.assetid: 48e00638-9274-49db-93ec-ed444f526441
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486e6db4365e9a279c844e7637ca3281a66b51a2e47d6d2d74d374ab4c55f146
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246925"
---
# <a name="provide-good-error-recovery"></a>Proporcionar una buena recuperación de errores

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Al igual que con cualquier interfaz bien diseñada, el proceso interactivo debe minimizar las circunstancias que conducen a errores. Sin embargo, rara vez es posible eliminar todos los errores, por lo que admitir una buena recuperación de errores es esencial para mantener la confianza y el interés del usuario. En general, la recuperación de errores implica detectar un error, determinar la causa y definir una manera de resolver el error. Los usuarios responden mejor a las interfaces que son cooperativas y que funcionan con el usuario para realizar una tarea.

El primer paso en la recuperación de errores de voz es detectar la condición de error. El reconocimiento de voz puede producir un error debido a una variedad de errores. Normalmente, las condiciones de error se pueden detectar como resultado de una entrada no válida, una corrección o cancelación explícitas del usuario o una repetición del usuario.

Se *produce un error* de rechazo cuando el motor de reconocimiento no coincide con lo que ha dicho el usuario. El ruido de fondo o los inicios tempranos también son causas comunes de errores de reconocimiento, por lo que pedir al usuario que repita un comando suele ser una buena solución inicial. Sin embargo, si la frase está fuera de la gramática activa actual, pedir al usuario que retrase la solicitud puede resolver el problema. La diferencia en la redacción puede dar lugar a una coincidencia con algo en la gramática actual. Enumerar o sugerir las opciones de entrada esperadas adecuadas es otra alternativa.

Una buena estrategia para la recuperación de errores de rechazo consiste en combinar estas técnicas para que el usuario vuelva a realizar el seguimiento, lo que ofrece cada vez más ayuda si el error persiste. Por ejemplo, puede empezar respondiendo al error inicial con un interrogativo como "¿Qué es?" o "¿Qué?" o un gesto de mano a oído. Una respuesta corta aumenta la probabilidad de que la instrucción repetida del usuario no produzca un error porque el usuario ha hablado demasiado pronto. Si se produce un error repetido, la solicitud posterior para volver a realizar la reherración mejora la posibilidad de que coincida con algo dentro de la gramática dada. Desde aquí, proporcionar avisos explícitos de comandos aceptados aumenta aún más la posibilidad de una coincidencia. Esta técnica se muestra en el ejemplo siguiente:

**Usuario:** me gustaría una pizza de estilo Chicago con anchoas.

**Carácter:**(mano a oído) ¿Mano a oído?

**Usuario:** quiero una pizza de Chicago con anchoas.

**Carácter**: (agite la cabeza) Reanude la solicitud.

**Usuario:** he dicho pizza de Chicago, con anchoas.

**Carácter**: (Shrug) Lo sentimos. Cuénteme el estilo de pizza que quiere.

**Usuario:** Chicago, con anchoas.

**Carácter:** todavía no hay suerte. Esto es lo que puede decir: "Chicago", "Chicago" o "Combo".

Para que el control de errores sea más natural, asegúrese de proporcionar un grado de variación aleatoria al responder a los errores. Además, una reacción natural del usuario a cualquier solicitud para repetir una respuesta es volver a incoar o aumentar el volumen al repetir la instrucción. En ocasiones, puede resultar útil recordar al usuario que hable con normalidad y claridad, ya que la sobrecosión o el aumento del volumen pueden dificultar el reconocimiento de las palabras por parte del motor de voz.

La asistencia progresiva debe hacer algo más que poner el error en la atención del usuario. debe guiar al usuario para que hable en la gramática actual proporcionando sucesivamente mensajes más informativos. Las interfaces que parecen estar intentando comprender fomentan un alto grado de satisfacción y tolerancia del usuario.

*Los errores de* sustitución , donde el motor de voz reconoce la entrada pero coincide con el comando incorrecto, son más difíciles de resolver porque el motor de voz detecta una expresión correspondiente. También puede producirse una discrepancia cuando el motor de voz interpreta sonidos extraños como entrada válida (también conocida como error *de inserción).* En estas situaciones, se necesita ayuda del usuario para identificar la condición de error. Para ello, puede repetir lo que devolvió el motor de voz y pedir al usuario que lo confirme antes de continuar:

**Usuario:** me gustaría una pizza de estilo Chicago.

**Carácter:**¿Ha dicho que le gustaría una "pizza de estilo Chicago"?

**Usuario:** Sí.

**Carácter:**¿Qué ingredientes adicionales le gustaría?

**Usuario:** Anchoas.

**Carácter:**¿Ha dicho "anchoas"?

**Usuario:** Sí.

Sin embargo, el uso de esta técnica para cada expresión se vuelve ineficaz y agotador. Para controlar esto, restrinja la confirmación a situaciones que tengan consecuencias negativas significativas o aumente la complejidad de la tarea inmediata. Si es fácil que el usuario realice o revierta cambios, puede evitar solicitar confirmación de sus opciones. Del mismo modo, si hace que las opciones sean visibles, es posible que no tenga que proporcionar una corrección explícita. Por ejemplo, elegir un elemento de una lista puede no requerir comprobación porque el usuario puede ver los resultados y cambiarlos fácilmente. También puede usar la confianza y las puntuaciones alternativas para proporcionar un umbral para la confirmación. Puede ajustar el umbral si mantiene un historial de las acciones del usuario en una situación determinada y elimina la verificación en función de la confirmación coherente del usuario. Por último, tenga en cuenta la naturaleza multimodal de la interfaz. La confirmación del mouse o el teclado también puede ser adecuada.

Elija cuidadosamente el texto de las confirmaciones. Por ejemplo, "¿Ha dicho...?" o "Creo que has dicho..." son mejores que "¿Realmente desea...?" dado que las frases anteriores implican que se está consultando la precisión de la escucha (reconocimiento) del carácter, no que el usuario pueda tener una falta de escucha.

Considere también la gramática para obtener una respuesta. Por ejemplo, es probable que una respuesta negativa genere un error de rechazo, lo que requiere un mensaje adicional como se muestra en el ejemplo siguiente:

**Usuario:** me gustaría algo de pepperoni.

**Carácter:**¿Ha dicho "no hay jamón"?

**Usuario:** No, he dicho pepperoni.

**Carácter:**¿Descándalo?

**Usuario:** Pepperoni.

La modificación de la gramática para incluir prefijos para controlar las variaciones de respuesta natural aumenta la eficacia del proceso de recuperación, especialmente cuando el usuario no confirma el mensaje de verificación. En este ejemplo, la confirmación se podría haber manipulado en un solo paso modificando la gramática de "pepperoni" incluyendo también "no he dicho pepperoni", "He dicho pepperoni" y "no pepperoni".

También puede controlar los errores de sustitución mediante las coincidencias alternativas devueltas por el motor de voz como confirmación correctiva:

**Usuario:** me gustaría algo de pepperoni.

**Carácter:**(Escucha "no hay jamón" como mejor coincidencia, "pepperoni" como primera alternativa) ¿Ha dicho "no hay jamón"?

**Usuario:** No, pepperoni.

**Carácter:**(todavía escucha "no hay jamón" como mejor coincidencia, pero ahora ofrece la primera alternativa) "Pepperoni"?

Del mismo modo, puede mantener un historial de errores de sustitución comunes y, si un error determinado es frecuente, ofrecer la alternativa la primera vez.

En cualquier situación de error de reconocimiento, evite culpar al usuario. Si el carácter sugiere o incluso implica que el usuario es el responsable, o el carácter parece indiferente al error, el usuario puede ser ofendido. Aquí también, elija cuidadosamente las palabras que acepten explícitamente la responsabilidad, sea adecuada para la situación y use la variedad para crear una respuesta más natural. Al expresar un sentimiento, evite palabras ambiguas como "oops" o "oh-oh" que se podrían interpretar como blasfedades para el usuario. En su lugar, use frases como "Lo sentimos" o "Mi error". Los errores repetidos o más graves podrían usar una elaboración más elaborado como "Realmente lo sentimos por eso". Tenga en cuenta también la personalidad del carácter al determinar el tipo de respuesta. Otra opción es culpar a una situación externa. Los comentarios como "Niños, hace ruido ahí fuera", quitan la culpa del usuario y del carácter. Recordar al usuario la naturaleza cooperativa de la interacción también puede ser útil: considere frases como "Veamos lo que podemos hacer para que esto funcione".

Microsoft Agent también admite algunos comentarios automáticos para el reconocimiento. Cuando se detecta una expresión, la sugerencia de escucha muestra el texto de voz de la mejor coincidencia escuchada. Puede establecer su propio texto para mostrarlo en función de la configuración de confianza de un comando que defina.

Debido al potencial de error, siempre se requiere confirmación para las opciones que tienen consecuencias negativas graves y son irreversibles. Por supuesto, querrá requerir confirmación cuando los resultados de una acción puedan ser destructivos. Sin embargo, considere también la posibilidad de requerir confirmación para situaciones que anulan cualquier proceso o operación largo.

 

 





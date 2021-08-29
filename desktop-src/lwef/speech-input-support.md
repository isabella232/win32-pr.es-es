---
title: Compatibilidad con la entrada de voz
description: Compatibilidad con la entrada de voz
ms.assetid: 4702b941-fcc9-4d00-aba2-eca624b6d417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd777f5dca0df91a4660249b0cdda380f2f20c37ba5c1c38a04264bb871ab3bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746256"
---
# <a name="speech-input-support"></a>Compatibilidad con la entrada de voz

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Además de admitir la interacción con el mouse y el teclado, Microsoft Agent incluye compatibilidad directa con la entrada de voz. Dado que la compatibilidad de Microsoft Agent con la entrada de voz se basa en Microsoft SAPI (interfaz de programación de aplicaciones de voz), puede usar Microsoft Agent con el comando de reconocimiento de voz y los motores de control que incluyen la compatibilidad necesaria para SAPI. Para más información sobre los requisitos del motor de voz, consulte [Requisitos de compatibilidad del motor de voz.](requirements-for-speech-recognition-engines.md)

Microsoft proporciona un motor de reconocimiento de voz de comandos y control que puede usar con Microsoft Agent. Para obtener más información, vea [Selección del motor de voz.](speech-engine-selection.md)

El usuario puede iniciar la entrada de voz presionando y manteniendo presionada la tecla de acceso rápido De escucha push-to-talk. En este modo de escucha, si el motor de voz recibe el principio de la entrada hablada, mantiene abierto el canal de audio hasta que detecta el final de la expresión. Sin embargo, cuando no recibe la entrada, no bloquea la salida de audio. Esto permite al usuario emitir varios comandos de voz mientras mantiene presionada la tecla y el carácter puede responder cuando el usuario no habla.

El modo de escucha se ha quedados de espera una vez que el usuario libera la clave de escucha. El usuario puede ajustar el tiempo de espera para este modo mediante opciones avanzadas de caracteres. No se puede establecer este tiempo de espera desde el código de la aplicación cliente.

Si un carácter intenta hablar mientras el usuario habla, se produce un error en la salida de audio del carácter, aunque el texto todavía se puede mostrar en su globo de palabras. Si el carácter tiene el canal de audio mientras se presiona la tecla Listening, el servidor transfiere automáticamente el control al usuario después de procesar el texto en el [**método Speak.**](speak-method.md) Se reproduce un tono MIDI opcional para que el usuario empiece a hablar. Esto permite al usuario proporcionar entradas incluso si la aplicación que conduce el carácter no pudo proporcionar pausas lógicas en su salida.

También puede usar el método [**Listen para**](listen-method.md) iniciar la entrada de voz. Al llamar a este método, se activa el reconocimiento de voz durante un período de tiempo predefinido. Si no hay ninguna entrada durante este intervalo, Microsoft Agent desactiva automáticamente el motor de reconocimiento de voz y libera el canal de audio. Esto evita el bloqueo de la entrada o salida desde el dispositivo de audio y minimiza la sobrecarga del procesador que usa el reconocimiento de voz cuando está conectado. También puede usar el método **Listen** para desactivar la entrada de voz. Sin embargo, tenga en cuenta que, dado que el motor de reconocimiento de voz funciona de forma asincrónica, el efecto puede no ser inmediato. Como resultado, es posible recibir un evento [**Command**](command-event.md) incluso después de que el código se llame **Escuchar** para desactivar la entrada de voz.

Para admitir la entrada de voz, defina una gramática , un conjunto de  palabras para [](/windows/desktop/lwef/the-command-object) las que quiere que el motor de reconocimiento de voz escuche y coincida como la configuración de Voz para un comando en la colección [**Comandos.**](/windows/desktop/lwef/the-commands-collection-object)  Puede incluir palabras opcionales y alternativas y secuencias repetidas en la gramática. Tenga en cuenta que el Agente no habilita la tecla de acceso rápido Listening  hasta que uno de sus clientes haya cargado correctamente un motor de voz o haya creado una voz para uno de sus **objetos Command.**

Si el usuario presiona la tecla de acceso rápido Listening o la aplicación cliente llama al método [**Listen**](listen-method.md) para iniciar la entrada de voz, el motor de reconocimiento de voz intenta hacer coincidir la entrada de una expresión con la gramática de los comandos que se han definido y devuelve la información al servidor. A continuación, el servidor notifica a la aplicación cliente mediante el [**evento Command**](command-event.md) ([**IAgentNotifySink::Command**](iagentnotifysink--command.md)); devolver el objeto [**UserInput**](/windows/desktop/lwef/iagentuserinput) que incluye el identificador de comando de la mejor coincidencia y las dos siguientes coincidencias alternativas (si las hay), una puntuación de confianza y el texto correspondiente para cada coincidencia.

El servidor también notifica a la aplicación cliente cuando coincide con la entrada de voz con uno de sus comandos proporcionados. Aunque el identificador del comando **es NULL,** sigue teniendo la puntuación de confianza y el texto coincidentes. Cuando está en modo de escucha, el servidor reproduce automáticamente la animación asignada al estado **De escucha del** carácter. A continuación, cuando se detecta realmente una expresión, el servidor reproduce la animación **de** estado de audiencia del carácter. El servidor mantendrá el carácter en un estado de excepción hasta que la expresión haya finalizado. Esto proporciona los comentarios sociales adecuados para que el usuario los introduzca.

Si el usuario deshabilita la entrada de voz en Opciones avanzadas de caracteres, también se deshabilitará la tecla de acceso rápido Escucha. Del mismo modo, si se intenta llamar al [**método Listen**](listen-method.md) cuando la entrada de voz está deshabilitada, se producirá un error en el método.

 

 
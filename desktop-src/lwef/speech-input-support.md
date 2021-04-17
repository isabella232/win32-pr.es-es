---
title: Compatibilidad con entrada de voz
description: Compatibilidad con entrada de voz
ms.assetid: 4702b941-fcc9-4d00-aba2-eca624b6d417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8ecb6f2ddfbbe10f8b892ce922cd466eca96890
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105656357"
---
# <a name="speech-input-support"></a>Compatibilidad con entrada de voz

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Además de admitir la interacción con el mouse y el teclado, Microsoft Agent incluye compatibilidad directa para la entrada de voz. Dado que la compatibilidad del agente de Microsoft con la entrada de voz se basa en Microsoft SAPI (interfaz de programación de aplicaciones de voz), puede usar el agente de Microsoft con los motores de control y comandos de reconocimiento de voz que incluyen la compatibilidad necesaria con SAPI. Para obtener más información sobre los requisitos del motor de voz, vea [requisitos de compatibilidad del motor de voz](requirements-for-speech-recognition-engines.md).

Microsoft proporciona un motor de reconocimiento de voz de comando y control que puede usar con el agente de Microsoft. Para obtener más información, consulte [selección del motor de voz](speech-engine-selection.md).

El usuario puede iniciar la entrada de voz si presiona y mantiene presionada la tecla de silencio para escuchar la lectura. En este modo de escucha, si el motor de voz recibe el inicio de la entrada oral, mantiene el canal de audio abierto hasta que detecta el final del utterance. Sin embargo, cuando no se recibe la entrada, no bloquea la salida de audio. Esto permite al usuario emitir varios comandos de voz mientras mantiene presionada la tecla y el carácter puede responder cuando el usuario no está hablando.

El modo de escucha agota el tiempo de espera una vez que el usuario libera la clave de escucha. El usuario puede ajustar el tiempo de espera de este modo mediante las opciones de caracteres avanzadas. No se puede establecer este tiempo de espera desde el código de la aplicación cliente.

Si un carácter intenta hablar mientras el usuario está hablando, se produce un error en la salida audible del carácter aunque el texto se siga mostrando en el globo de palabras. Si el carácter tiene el canal de audio mientras se presiona la tecla de escucha, el servidor transfiere automáticamente el control al usuario después de procesar el texto en el método [**Speak**](speak-method.md) . Se reproduce un tono MIDI opcional para señalar al usuario para que empiece a hablar. Esto permite al usuario proporcionar la entrada incluso si la aplicación que conduce el carácter no proporcionó pausas lógicas en su salida.

También puede usar el método [**Listen**](listen-method.md) para iniciar la entrada de voz. La llamada a este método activa el reconocimiento de voz durante un período de tiempo predefinido. Si no hay ninguna entrada durante este intervalo, el agente de Microsoft desactiva automáticamente el motor de reconocimiento de voz y libera el canal de audio. Esto evita bloquear la entrada o salida del dispositivo de audio y minimiza la sobrecarga del procesador que el reconocimiento de voz usa cuando está activado. También puede usar el método **Listen** para desactivar la entrada de voz. Sin embargo, tenga en cuenta que, dado que el motor de reconocimiento de voz funciona de forma asincrónica, el efecto puede no ser inmediato. Como resultado, es posible recibir un evento de [**comando**](command-event.md) incluso después de que el código llamado **escuche** para desactivar la entrada de voz.

Para admitir la entrada de voz, se define una *gramática*, un conjunto de palabras en las que se desea que el motor de reconocimiento de voz escuche y coincida como la configuración de **voz** de un [**comando**](/windows/desktop/lwef/the-command-object) en la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Puede incluir palabras opcionales y alternativas y secuencias repetidas en la gramática. Tenga en cuenta que el agente no habilita la tecla de acceso rápido de escucha hasta que uno de sus clientes ha cargado correctamente un motor de voz o ha creado una **voz** para uno de sus objetos de **comando** .

Si el usuario presiona la tecla de método de escucha o la aplicación cliente llama al método [**Listen**](listen-method.md) para iniciar la entrada de voz, el motor de reconocimiento de voz intenta hacer coincidir la entrada de un utterance con la gramática de los comandos que se han definido y devuelve la información de vuelta al servidor. A continuación, el servidor notifica a la aplicación cliente mediante el evento de [**comando**](command-event.md) ([**IAgentNotifySink:: Command**](iagentnotifysink--command.md)); devolver el objeto [**UserInput**](/windows/desktop/lwef/iagentuserinput) que incluye el identificador de comando de la mejor coincidencia y las dos coincidencias alternativas siguientes (si existen), una puntuación de confianza y el texto coincidente para cada coincidencia.

El servidor también notifica a la aplicación cliente cuando coincide con la entrada de voz a uno de sus comandos proporcionados. Aunque el identificador de comando es **null**, se obtiene la puntuación de confianza y el texto coincidentes. En el modo de escucha, el servidor reproduce automáticamente la animación asignada al estado de **escucha** del carácter. A continuación, cuando se detecta un utterance realmente, el servidor reproduce la animación del estado de la **audición** del carácter. El servidor mantendrá el carácter en un estado Attentive hasta que haya finalizado utterance. Esto proporciona los comentarios sociales adecuados para señalar al usuario para la entrada.

Si el usuario deshabilita la entrada de voz en opciones de caracteres avanzadas, también se deshabilitará la Hotkey de escucha. Del mismo modo, si se intenta llamar al método [**Listen**](listen-method.md) cuando la entrada de voz está deshabilitada, se producirá un error en el método.

 

 
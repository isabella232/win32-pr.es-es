---
title: Problemas de entrada de voz
description: Problemas de entrada de voz
ms.assetid: b42664a2-9615-4e15-97a6-115e9556096b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d135ac8a098f52066854c6003c22caa7290efbd01c8038bda116cd843b21a2e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246234"
---
# <a name="speech-input-problems"></a>Problemas de entrada de voz

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

### <a name="the-character-does-not-respond-to-my-spoken-input"></a>El carácter no responde a mi entrada hablada.

Este síntoma puede deberse a una serie de problemas. Pruebe lo siguiente para aislar el problema:

-   Compruebe que el micrófono está conectado correctamente. Es una buena idea probarlo con otra aplicación de entrada de sonido para asegurarse de que funciona correctamente.
-   Compruebe que está instalado un motor de voz compatible. En Windows 95, Windows 98 y Windows NT 4.0, abra el Panel de control. Si encuentra el objeto de voz, ábralo y mostrará los motores de voz disponibles e instalados en el sistema.
-   Compruebe que la tarjeta de sonido es compatible con Microsoft Windows 95, Windows 98 o Windows NT.

    La mejor manera de hacerlo es ejecutar la aplicación Sound Recorder que viene con Windows. Normalmente se puede encontrar en el menú Inicio. Haga clic en el botón Inicio, haga clic en Programas, accesorios, multimediay, a continuación, haga clic en Grabadora de sonido. Cuando se muestre la ventana Grabadora de sonido, haga clic en **el botón Grabar** y hable con el micrófono. La línea de la ventana debe animarse en respuesta a la entrada de voz.

    Si la aplicación Sound Recorder no funciona en el sistema, póngase en contacto con el departamento de soporte técnico del fabricante de la tarjeta de sonido para obtener ayuda. Es posible que la tarjeta de sonido no sea compatible con Windows o que haya un problema con los controladores de software de la tarjeta de sonido.

-   Compruebe que la entrada de sonido para la entrada de voz está establecida correctamente.
    1.  Abra el objeto De entrada de voz en el Panel de control. Si el objeto De voz no está presente, instale uno.
    2.  Seleccione el motor de entrada de voz que ha instalado.
    3.  Elija el botón Asistente para Configuración micrófono. Si este botón aparece deshabilitado, no se instala un motor de voz compatible o es posible que el motor de voz instalado no admita el ajuste automático.
-   Compruebe que la aplicación o página web habilitada para agente admite la entrada de voz. No todas las páginas (o aplicaciones) admiten la entrada de voz. Mantenga presionada la tecla Escuchando. Normalmente, será la clave de bloqueo de desplazamiento, a menos que la cambie. Debe aparecer una ventana emergente debajo del carácter. El texto de la sugerencia le mostrará el estado de escucha del carácter. Si no aparece ninguna sugerencia, la aplicación o la página web no admiten la entrada de voz o no tiene instalado un motor de voz compatible. Si aparece la sugerencia e indica que el carácter está escuchando, diga uno de los comandos de voz del carácter. Si no sabe qué comandos de voz están disponibles, suelte la tecla Escuchando y haga clic con el botón derecho en el carácter. A continuación, elija Abrir ventana comandos de voz en el menú emergente. Si el comando no aparece, la compatibilidad con voz no está disponible para la aplicación o página web que está usando. Si aparece, mantenga presionada la tecla Escuchando de nuevo. Si la sugerencia De escucha aparece debajo del carácter e indica que el carácter está escuchando, diga uno de los comandos enumerados en la ventana. Si el carácter no responde, vaya al paso siguiente.
-   Compruebe que ninguna otra aplicación está usando actualmente el dispositivo de salida de audio.
-   Compruebe que el uso de MIDI por parte de Microsoft Agent no está bloqueando el canal de audio (consulte Aplicaciones que [reproducen MIDI sin](output-problems.md)salida de audio cuando Microsoft Agent ejecuta " en la sección Problemas de salida).
-   Si ha seguido los pasos anteriores, pero sigue teniendo problemas con la entrada de voz, compruebe que la tarjeta de sonido y el software del controlador son compatibles con el motor de voz que está usando. Consulte con el soporte técnico para la tarjeta de sonido y el fabricante del motor de voz.

### <a name="the-midi-tone-seems-to-disrupts-speech-input"></a>El tono MIDI parece interrumpir la entrada de voz.

Reduzca el volumen de MIDI mediante los pasos siguientes.

1.  Abra la ventana Control de volumen haciendo clic con el botón derecho en el icono del altavoz en la barra de tareas o abriendo el objeto Multimedia en la Panel de control. Haga clic en el botón Volumen de la sección Reproducción de la página Audio.
2.  Reduzca el volumen de MIDI moviendo el control deslizante hacia abajo.

### <a name="the-character-does-not-respond-to-voice-input-but-i-can-hear-my-voice-through-my-speakers-when-i-talk-into-my-microphone"></a>El carácter no responde a la entrada de voz, pero puedo escuchar mi voz a través de mis altavoces cuando hable con el micrófono.

La tarjeta de sonido no está configurada correctamente para su uso con Microsoft Agent. Elija el Asistente para Configuración micrófono en la hoja de propiedades del objeto Voz en el Panel de control. Consulte los pasos de "El carácter no responde a mi entrada[hablada"](#the-character-does-not-respond-to-my-spoken-input)para obtener información sobre cómo acceder a este botón.

 

 





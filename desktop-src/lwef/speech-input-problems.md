---
title: Problemas de entrada de voz
description: Problemas de entrada de voz
ms.assetid: b42664a2-9615-4e15-97a6-115e9556096b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a7b29a85c79996eb0c01260c8e2b738fcd926f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994123"
---
# <a name="speech-input-problems"></a>Problemas de entrada de voz

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

### <a name="the-character-does-not-respond-to-my-spoken-input"></a>El carácter no responde a la entrada oral.

Este síntoma puede deberse a una serie de problemas. Intente lo siguiente para aislar el problema:

-   Compruebe que el micrófono está correctamente conectado. Es una buena idea probarla con otra aplicación de entrada de sonido para asegurarse de que funciona correctamente.
-   Compruebe que se ha instalado un motor de voz compatible. En Windows 95, Windows 98 y Windows NT 4,0, abra el panel de control. Si encuentra allí el objeto de voz, ábralo y mostrará los motores de voz disponibles e instalados en el sistema.
-   Compruebe que la tarjeta de sonido es compatible con Microsoft Windows 95, Windows 98 o Windows NT.

    La mejor manera de hacerlo es ejecutar la aplicación de grabadora de sonidos que viene con Windows. Normalmente se puede encontrar en el menú Inicio. Haga clic en el botón Inicio, en programas, en accesorios, en multimedia y, a continuación, en grabadora de sonidos. Cuando aparezca la ventana grabadora de sonidos, haga clic en el botón **grabar** y hable con el micrófono. La línea de la ventana debe animarse en respuesta a la entrada de voz.

    Si la aplicación de grabadora de sonidos no funciona en el sistema, póngase en contacto con el Departamento de soporte técnico del fabricante de la tarjeta de sonido para obtener ayuda. Es posible que la tarjeta de sonido no sea compatible con Windows o que haya un problema con los controladores de software de la tarjeta de sonido.

-   Compruebe que la entrada de sonido para la entrada de voz está establecida correctamente.
    1.  Abra el objeto entrada de voz en el panel de control. Si el objeto de voz no está presente, instale uno.
    2.  Seleccione el motor de entrada de voz que ha instalado.
    3.  Elija el botón Asistente para configuración de micrófono. Si este botón aparece deshabilitado, es posible que no se haya instalado un motor de voz compatible o que el motor de voz instalado no admita el ajuste automático.
-   Compruebe que la aplicación habilitada para el agente o la página web admiten la entrada de voz. No todas las páginas (o aplicaciones) admiten la entrada de voz. Mantenga presionada la tecla de escucha. Normalmente, será la tecla Bloq Despl, a menos que la haya cambiado. Una ventana emergente debe aparecer debajo del carácter. El texto de la sugerencia le indicará el estado de escucha del carácter. Si no aparece ninguna sugerencia, significa que la aplicación o la página web no admiten la entrada de voz o que no tiene instalado un motor de voz compatible. Si aparece la sugerencia e indica que el carácter está escuchando, hable con uno de los comandos de voz del carácter. Si no sabe qué comandos de voz están disponibles, libere la clave de escucha y haga clic con el botón secundario en el carácter. A continuación, elija Abrir ventana comandos de voz en el menú emergente. Si el comando no aparece, la compatibilidad con voz no está disponible para la aplicación o la página web que está usando. Si aparece, mantenga presionada la tecla de escucha. Si la sugerencia de escucha aparece debajo del carácter e indica que el carácter está escuchando, hable con uno de los comandos enumerados en la ventana. Si el carácter no responde, vaya al paso siguiente.
-   Compruebe que ninguna otra aplicación está usando el dispositivo de salida de audio.
-   Compruebe que el uso del agente de Microsoft de MIDI no está bloqueando el canal de audio (consulte [las aplicaciones que reproducen MIDI no tienen salida de audio cuando se está ejecutando el agente de Microsoft](output-problems.md)) en la sección problemas de salida.
-   Si siguió los pasos anteriores pero sigue teniendo problemas con la entrada de voz, compruebe que la tarjeta de sonido y el software de controlador son compatibles con el motor de voz que está usando. Consulte con el soporte técnico de la tarjeta de sonido y el fabricante del motor de voz.

### <a name="the-midi-tone-seems-to-disrupts-speech-input"></a>El tono MIDI parece interrumpir la entrada de voz.

Reduzca el volumen MIDI mediante los pasos siguientes.

1.  Para abrir la ventana control de volumen, haga clic con el botón secundario en el icono de altavoz de la barra de tareas o abra el objeto multimedia en el panel de control. Haga clic en el botón volumen en la sección reproducción de la página audio.
2.  Reduzca el volumen MIDI moviendo el control deslizante hacia abajo.

### <a name="the-character-does-not-respond-to-voice-input-but-i-can-hear-my-voice-through-my-speakers-when-i-talk-into-my-microphone"></a>El carácter no responde a la entrada de voz, pero puedo escuchar mi voz a través de mis altavoces al hablar con el micrófono.

La tarjeta de sonido no está configurada correctamente para su uso con el agente de Microsoft. Elija el Asistente para configuración de micrófono en la hoja de propiedades del objeto voz en el panel de control. Vea los pasos para "[el carácter no responde a la entrada oral](#the-character-does-not-respond-to-my-spoken-input)" para obtener información sobre cómo obtener acceso a este botón.

 

 





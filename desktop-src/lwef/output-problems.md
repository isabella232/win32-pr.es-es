---
title: Problemas de salida
description: Problemas de salida
ms.assetid: 45423b7e-f648-408c-9cff-f7cf1affc42a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f19afb705e1d71b3b47bc44c35a51cb83029932287c582b0481ff6a5b078049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961055"
---
# <a name="output-problems"></a>Problemas de salida

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

### <a name="the-character-leaves-images-or-trails-behind-when-it-moves"></a>El carácter deja imágenes o huellas detrás cuando se mueve.

Cuando un carácter del Agente se anima, requiere que las ventanas de la aplicación detrás del carácter se actualicen a tiempo. Cuando el carácter se mueve por la pantalla, a veces es normal ver algunas imágenes residuales que desaparecen rápidamente (en función de la velocidad del equipo y las aplicaciones que se ejecutan). Si no lo hacen, la causa puede ser la siguiente:

-   El sistema no cumple los requisitos mínimos del sistema para el Agente .
-   La ventana de aplicación detrás del carácter no procesa las actualizaciones a tiempo. Intente arrastrar el carácter sobre el escritorio o una ventana de carpeta, o apague algunas de las aplicaciones. Si ve una mejora apreciable, el problema puede ser inevitable.
-   Es posible que no tenga instalada la versión oficial de Microsoft Internet Explorer 4.0 (o posterior). Las primeras versiones anteriores de Internet Explorer 4.0 no controló la actualización de la pantalla correctamente. Esto daría lugar a imágenes residuales del carácter restante en la pantalla. Para corregir el problema, instale la versión oficial más reciente de Internet Explorer ( [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) ).
-   Puede haber un problema con los controladores de pantalla o el hardware del sistema. Asegúrese de que tiene los controladores más recientes para el hardware gráfico. Si el problema persiste, es posible que quiera ponerse en contacto con su proveedor de PC.

### <a name="the-character-doesnt-produce-any-audio-output-when-it-speaks"></a>El carácter no genera ninguna salida de audio cuando habla.

Este síntoma podría tener varias causas. Pruebe lo siguiente para aislar el problema:

-   Compruebe que los altavoces están conectados y que la tarjeta de sonido es compatible con Windows. Es una buena idea probarlos con otra aplicación de sonido para confirmar que la salida de audio funciona correctamente.
-   Compruebe que la aplicación o página web habilitada para agente admite la entrada de voz. No todas las páginas de ejemplo admiten la entrada de voz. Mantenga presionada la tecla Escuchando (normalmente será la tecla Desplace Lock a menos que la cambie). Debe aparecer una ventana emergente debajo del carácter. El texto de la sugerencia le mostrará el estado de escucha del carácter. Si no aparece ninguna sugerencia, la aplicación o la página web no admiten la entrada de voz o no tiene instalado un motor de voz compatible. Si aparece la sugerencia e indica que el carácter está escuchando, diga uno de los comandos de voz del carácter. Si no sabe qué comandos de voz están disponibles: suelte la tecla Escuchando y haga clic con el botón derecho en el carácter y, a continuación, elija Abrir ventana comandos de voz en el menú emergente. Si el comando no aparece, la compatibilidad con voz no está disponible para la aplicación o página web que está usando. Si aparece, mantenga presionada la tecla Escuchando de nuevo. Si la sugerencia De escucha aparece debajo del carácter e indica que el carácter está escuchando, diga uno de los comandos enumerados en la ventana. Si el carácter no responde, vaya al paso siguiente.
-   Compruebe que ninguna otra aplicación está usando actualmente el dispositivo de salida de audio.
-   Compruebe que el carácter que está usando se ha configurado para la salida hablada. (Es posible que tenga que consultar con el sitio web o el proveedor de la aplicación).
-   Compruebe que la configuración de Microsoft Agent está habilitada para la salida hablada.
-   Si el carácter usa un motor de texto a voz (TTS) para generar una salida hablada, compruebe que ha instalado un motor TTS compatible. Por ejemplo, cuando se instala como un Internet Explorer complemento 4.0, solo se instalan los componentes principales de Microsoft Agent. Los componentes principales no incluyen un motor de texto a voz. Sin este motor de TTS (un motor compatible Speech API Microsoft), los caracteres de ejemplo de Microsoft Agent no producirán resultados hablados.
-   Compruebe que el uso de MIDI por parte de Microsoft Agent no está bloqueando el canal de audio (vea el tema siguiente, Aplicaciones que reproducen MIDI no tienen ninguna salida de audio cuando se ejecuta Microsoft Agent).

### <a name="applications-that-play-midi-have-no-audio-output-when-microsoft-agent-is-running"></a>Las aplicaciones que reproducen MIDI no tienen ninguna salida de audio cuando se ejecuta Microsoft Agent.

Microsoft Agent usa MIDI para reproducir un tono al presionar la tecla De escucha. Si descubre que esto interfiere con otras aplicaciones que reproducen MIDI o interfiere con la entrada de voz, puede desactivar la opción Reproducir tono cuando se puede hablar en las propiedades de Microsoft Agent.

### <a name="i-get-the-following-message-an-outgoing-call-cannot-be-made-since-the-application-is-dispatching-an-input-synchronous-call"></a>Aparece el mensaje siguiente: No se puede realizar una llamada saliente, ya que la aplicación envía una llamada sincrónica de entrada.

Este mensaje puede producirse en las siguientes circunstancias:

Cuando se cierra una página web que incluye Microsoft Agent (haciendo clic con el botón derecho en la entrada de la barra de tareas de la página y seleccionando Cerrar en el menú emergente), esto puede ocurrir. Esto se debe a un problema de tiempo entre el Agente y el explorador cuando se apagan al mismo tiempo. El error es inofensivo. Haga clic en Aceptar para descartar el mensaje.

Lo que ocurrió fue que la página web habilitada para agente (o aplicación) intentó solicitar un motor de texto a voz (TTS) específico. Speechapi.dll no se instaló.

### <a name="the-speech-engines-dont-seem-to-work-with-microsoft-agent-in-windows-xp"></a>¿Los motores de voz no parecen funcionar con Microsoft Agent en Windows XP?

Microsoft Agent usa SAPI 4.0 para proporcionar servicios de voz. Windows Sin embargo, XP ahora se suministra con SAPI 5.0, que no proporciona compatibilidad con versiones anteriores para su predecesor. Afortunadamente, SAPI 4.0 y SAPI 5.0 pueden coexistir en el mismo Windows XP.

Para que los motores de voz funcionen con Microsoft Agent en Windows XP, instale primero los archivos binarios en tiempo de ejecución de [SAPI 4.0](https://activex.microsoft.com/activex/controls/sapi/spchapi.exe)y, a continuación, instale los motores de voz concretos.

### <a name="the-speech-engines-used-to-work-with-microsoft-agent-until-i-upgraded-to-windows-xp-what-happened"></a>Los motores de voz que se usan para trabajar con Microsoft Agent hasta que actualizó a Windows XP. ¿Qué ha ocurrido?

Vea la pregunta y respuesta anteriores. El proceso de actualización Windows XP puede haber quitado la compatibilidad con SAPI 4.0 ya existente en el equipo. Vuelva a instalar los motores de voz SAPI 4.0 y SAPI 4.0 después de actualizar a Windows XP.

### <a name="i-installed-the-tts3000-text-to-speech-engines-onto-my-computer-that-runs-windows-xp-or-windows-2000-and-correctly-edited-my-programming-accordingly-for-their-use-the-microsoft-agent-characters-speak-audibly-using-these-tts3000-text-to-speech-engines-when-i-or-other-local-administrators-are-logged-in-but-not-when-other-users-without-administrator-privileges-are-logged-into-this-computer-on-windows-98-and-windows-me-these-tts3000-text-to-speech-engines-work-correctly-for-both-sets-of-users-how-can-i-fix-this"></a>He instalado los motores de texto a voz TTS3000 en mi equipo que ejecuta Windows XP (o Windows 2000) y edité correctamente mi programación en consecuencia para su uso. Los caracteres de Microsoft Agent hablan con voz y voz mediante estos motores de texto a voz TTS3000 cuando yo u otros administradores locales inician sesión, pero no cuando otros usuarios sin *privilegios* de administrador inician sesión en este equipo. En Windows 98 y Windows me, estos motores de texto a voz de TTS3000 funcionan correctamente para ambos conjuntos de usuarios. ¿Cómo lo puedo corregir?

Deberá configurar los permisos de seguridad para algunas de las claves del Registro de los motores de texto a voz de TTS3000 para habilitar su uso por parte de las cuentas de usuario sin privilegios de administrador. Esto se puede lograr con el Editor del Registro del sistema operativo.

### <a name="i-followed-the-procedure-described-as-a-solution-to-the-problem-stated-in-the-previous-question-this-worked-fine-so-that-the-microsoft-agent-characters-could-speak-audibly-using-these-tts3000-text-to-speech-engines-when-users-without-administrator-privileges-were-logged-into-the-windows-xp-or-windows-2000-computer-now-months-later-these-same-tts3000-text-to-speech-engines-have-stopped-working-again-what-happened"></a>He seguido el procedimiento descrito como una solución al problema indicado en la pregunta anterior. Esto funcionaba bien para que los caracteres de Microsoft Agent pudieran hablar de forma sonruta mediante estos motores de texto a voz TTS3000 cuando los usuarios sin *privilegios* de administrador se registraban en el equipo Windows XP (o Windows 2000). Ahora, meses después, estos mismos motores de texto a voz de TTS3000 han dejado de funcionar de nuevo. ¿Qué ha ocurrido?

Al seguir el procedimiento descrito proporcionado para la pregunta anterior, esto proporcionaba a las cuentas de usuario que no son de administrador permisos de control total para las claves del Registro necesarias. Es posible que uno de estos usuarios haya editado los valores a sabiendas o sin saberlo, haya cambiado los permisos de nuevo o incluso haya eliminado la clave del Registro por completo.

Compruebe si estas claves del Registro y sus permisos se han editado, eliminado o cambiado desde entonces. Si es necesario, vuelva a cambiar estas claves del Registro y sus permisos, o vuelva a instalar el texto a voz de TTS3000.

 

 





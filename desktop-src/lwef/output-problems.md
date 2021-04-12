---
title: Problemas de salida
description: Problemas de salida
ms.assetid: 45423b7e-f648-408c-9cff-f7cf1affc42a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d909052feb2463637a8eab6343353f0af617c06
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104358726"
---
# <a name="output-problems"></a>Problemas de salida

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

### <a name="the-character-leaves-images-or-trails-behind-when-it-moves"></a>El carácter deja imágenes o rastros cuando se mueve.

Cuando un carácter del agente se anima, requiere que las ventanas de la aplicación detrás del carácter se actualicen a tiempo. Cuando el carácter se mueve por la pantalla, es normal ver algunas imágenes residuales que desaparecen rápidamente (en función de la velocidad del equipo y las aplicaciones que se están ejecutando). Si no es así, la causa puede ser la siguiente:

-   El sistema no cumple los requisitos mínimos del sistema para el agente.
-   La ventana de la aplicación detrás del carácter no procesa las actualizaciones de manera oportuna. Intente arrastrar el carácter sobre el escritorio o una ventana de carpeta, o bien cierre algunas de sus aplicaciones. Si ve una mejora apreciable, el problema puede ser inevitable.
-   Es posible que no tenga instalada la versión oficial de Microsoft Internet Explorer 4,0 (o posterior). Las primeras versiones preliminares de Internet Explorer 4,0 no administraron correctamente la actualización de la pantalla. Esto daría lugar a que queden imágenes residuales del carácter en la pantalla. Para solucionar el problema, instale la versión oficial más reciente de Internet Explorer ( [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) ).
-   Puede haber un problema con los controladores de pantalla o el hardware del sistema. Asegúrese de que dispone de los controladores más recientes para el hardware gráfico. Si el problema persiste, es posible que desee ponerse en contacto con el proveedor de su PC.

### <a name="the-character-doesnt-produce-any-audio-output-when-it-speaks"></a>El carácter no genera ninguna salida de audio cuando habla.

Este síntoma podría tener varias causas. Intente lo siguiente para aislar el problema:

-   Compruebe que los altavoces están conectados y que la tarjeta de sonido es compatible con Windows. Es una buena idea probarla con otra aplicación de sonido para confirmar que la salida de audio funciona correctamente.
-   Compruebe que la aplicación habilitada para el agente o la página web admiten la entrada de voz. No todas las páginas de ejemplo admiten la entrada de voz. Mantenga presionada la tecla de escucha (normalmente será la tecla Bloq Despl, a menos que la cambie). Una ventana emergente debe aparecer debajo del carácter. El texto de la sugerencia le indicará el estado de escucha del carácter. Si no aparece ninguna sugerencia, significa que la aplicación o la página web no admiten la entrada de voz o que no tiene instalado un motor de voz compatible. Si aparece la sugerencia e indica que el carácter está escuchando, hable con uno de los comandos de voz del carácter. Si no sabe qué comandos de voz están disponibles: libere la clave de escucha y haga clic con el botón secundario en el carácter y, a continuación, elija Abrir ventana comandos de voz en el menú emergente. Si el comando no aparece, la compatibilidad con voz no está disponible para la aplicación o la página web que está usando. Si aparece, mantenga presionada la tecla de escucha. Si la sugerencia de escucha aparece debajo del carácter e indica que el carácter está escuchando, hable con uno de los comandos enumerados en la ventana. Si el carácter no responde, vaya al paso siguiente.
-   Compruebe que ninguna otra aplicación está usando el dispositivo de salida de audio.
-   Compruebe que el carácter que está usando se ha configurado para la salida de voz. (Puede que tenga que consultar con el sitio web o el proveedor de la aplicación).
-   Compruebe que la configuración del agente de Microsoft está habilitada para la salida de voz.
-   Si el carácter utiliza un motor de conversión de texto a voz (TTS) para generar la salida oral, compruebe que ha instalado un motor de TTS compatible. Por ejemplo, cuando se instala como un componente de complemento de Internet Explorer 4,0, solo se instalan los componentes principales del agente de Microsoft. Los componentes principales no incluyen un motor de conversión de texto a voz. Sin este motor TTS (un motor compatible con Microsoft Speech API), los caracteres de ejemplo de Microsoft Agent no generarán una salida de voz.
-   Compruebe que el uso de MIDI de Microsoft Agent no está bloqueando el canal de audio (consulte el siguiente tema, las aplicaciones que reproducen MIDI no tienen salida de audio cuando se está ejecutando el agente de Microsoft).

### <a name="applications-that-play-midi-have-no-audio-output-when-microsoft-agent-is-running"></a>Las aplicaciones que reproducen MIDI no tienen salida de audio cuando se está ejecutando el agente de Microsoft.

El agente de Microsoft usa MIDI para reproducir un tono cuando se presiona la tecla de escucha. Si observa que esto interfiere con otras aplicaciones que reproducen MIDI o interfieren con la entrada de voz, puede desactivar la opción Reproducir tono cuando pueda hablar en las propiedades del agente de Microsoft.

### <a name="i-get-the-following-message-an-outgoing-call-cannot-be-made-since-the-application-is-dispatching-an-input-synchronous-call"></a>Obtengo el siguiente mensaje: no se puede realizar una llamada saliente porque la aplicación está enviando una llamada sincrónica de entrada.

Este mensaje puede producirse en las siguientes circunstancias:

Cuando se cierra una página web que incluye el agente de Microsoft (al hacer clic con el botón derecho en la entrada de la barra de tareas de la página y elegir cerrar en el menú emergente), esto puede ocurrir. Esto se debe a un problema de sincronización entre el agente y el explorador cuando se cierran al mismo tiempo. El error es inofensivo. Haga clic en Aceptar para descartar el mensaje.

Lo que se produjo fue que la página web (o aplicación) habilitada para el agente intentaba solicitar un motor de texto a voz (TTS) específico. Speechapi.dll no se instaló.

### <a name="the-speech-engines-dont-seem-to-work-with-microsoft-agent-in-windows-xp"></a>Los motores de voz no parecen funcionar con el agente de Microsoft en Windows XP

El agente de Microsoft usa SAPI 4,0 para proporcionar servicios de voz. Windows XP no obstante, ahora se incluye en SAPI 5,0, que no proporciona compatibilidad con versiones anteriores para su predecesor. Afortunadamente, SAPI 4,0 y SAPI 5,0 pueden coexistir en el mismo equipo con Windows XP.

Para que los motores de voz funcionen con el agente de Microsoft en Windows XP, instale primero los [archivos binarios en tiempo de ejecución de SAPI 4,0](https://activex.microsoft.com/activex/controls/sapi/spchapi.exe)y, a continuación, instale los motores de voz concretos.

### <a name="the-speech-engines-used-to-work-with-microsoft-agent-until-i-upgraded-to-windows-xp-what-happened"></a>Los motores de voz usados para trabajar con el agente de Microsoft hasta que se actualizó a Windows XP. ¿Qué ha ocurrido?

Vea la pregunta y la respuesta anteriores. Es posible que el proceso de actualización de Windows XP haya quitado la compatibilidad de SAPI 4,0 que ya existe en el equipo. Solo tiene que volver a instalar el tiempo de ejecución de SAPI 4,0 y los motores de voz de SAPI 4,0 después de la actualización a Windows XP.

### <a name="i-installed-the-tts3000-text-to-speech-engines-onto-my-computer-that-runs-windows-xp-or-windows-2000-and-correctly-edited-my-programming-accordingly-for-their-use-the-microsoft-agent-characters-speak-audibly-using-these-tts3000-text-to-speech-engines-when-i-or-other-local-administrators-are-logged-in-but-not-when-other-users-without-administrator-privileges-are-logged-into-this-computer-on-windows-98-and-windows-me-these-tts3000-text-to-speech-engines-work-correctly-for-both-sets-of-users-how-can-i-fix-this"></a>Instalé los motores de texto a voz de TTS3000 en el equipo que ejecuta Windows XP (o Windows 2000) y editó correctamente mi programación en consecuencia para su uso. Los caracteres del agente de Microsoft hablan de un uso audible de estos motores de texto a voz de TTS3000 cuando I u otros administradores locales inician sesión, pero no cuando otros usuarios *sin privilegios de administrador* se registran en este equipo. En Windows 98 y Windows me, estos motores de texto a voz de TTS3000 funcionan correctamente para ambos conjuntos de usuarios. ¿Cómo lo puedo corregir?

Tendrá que configurar los permisos de seguridad para algunas de las claves del registro de los motores de texto a voz de TTS3000 para permitir su uso por parte de las cuentas de usuario sin privilegios de administrador. Esto puede realizarse con el editor del registro del sistema operativo.

### <a name="i-followed-the-procedure-described-as-a-solution-to-the-problem-stated-in-the-previous-question-this-worked-fine-so-that-the-microsoft-agent-characters-could-speak-audibly-using-these-tts3000-text-to-speech-engines-when-users-without-administrator-privileges-were-logged-into-the-windows-xp-or-windows-2000-computer-now-months-later-these-same-tts3000-text-to-speech-engines-have-stopped-working-again-what-happened"></a>He seguido el procedimiento descrito como solución al problema indicado en la pregunta anterior. Esto funcionó bien para que los caracteres de Microsoft Agent pudieran hablar de forma audible mediante estos motores de texto a voz de TTS3000 cuando los usuarios *sin privilegios de administrador* se registraban en el equipo con Windows XP (o Windows 2000). Ahora, meses más tarde, estos mismos motores de texto a voz de TTS3000 han dejado de funcionar de nuevo. ¿Qué ha ocurrido?

Cuando siguió el procedimiento descrito en la pregunta anterior, se proporcionaron permisos de control total a las claves del registro necesarias para las cuentas de usuario sin privilegios de administrador. Es posible que uno de estos usuarios pueda haber editado los valores de forma consciente o inconsciente, haber cambiado los permisos de nuevo o incluso haber eliminado por completo la clave del registro.

Compruebe si estas claves del registro y sus permisos se han editado, eliminado o cambiado de otro modo desde. Si es necesario, vuelva a cambiar estas claves del registro y sus permisos, o vuelva a instalar el texto a voz de TTS3000.

 

 





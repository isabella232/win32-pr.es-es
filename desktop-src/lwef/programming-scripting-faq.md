---
title: Preguntas más frecuentes sobre scripting de programación
description: Preguntas más frecuentes sobre scripting de programación
ms.assetid: 84078c5b-7b04-48fa-9d0a-d95393c323eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dec468eb5147968ca0db774f081212a78cf40d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104074978"
---
# <a name="programming-scripting-faq"></a>Preguntas más frecuentes sobre scripting de programación

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

### <a name="when-i-use-microsoft-visual-basic-or-other-development-tools-for-scripting-microsoft-agent-i-do-not-see-all-the-properties-and-events-used-in-your-samples-how-do-i-access-them"></a>Cuando utilizo Microsoft Visual Basic (u otras herramientas de desarrollo) para scripting Microsoft Agent, no veo todas las propiedades y eventos usados en los ejemplos. ¿Cómo acceder a ellas?

La mayoría de los eventos, métodos y propiedades que admite el control de Microsoft Agent solo se exponen en tiempo de ejecución. Consulte [programar el control de Microsoft Agent](programming-the-microsoft-agent-control.md) para obtener más información.

### <a name="the-map-tag-or-some-other-tag-doesnt-seem-to-work"></a>Parece que la etiqueta de mapa (o alguna otra etiqueta) no funciona.

Algunas etiquetas incluyen cadenas entre comillas. En algunos lenguajes de programación, como Microsoft Visual Basic y Visual Basic Scripting Edition, es posible que tenga que usar dos comillas para designar el parámetro de la etiqueta o concatenar un carácter de comilla doble como parte de la cadena. Este último se muestra en este Visual Basic ejemplo:

Agente1. Characters ("genio"). Diga "este es \\ map =" + Chr (34) + "texto hablado" \_ + Chr (34) + "=" + Chr (34) + "texto de globo" + Chr (34) + " \\ ."

Para la programación en C, C++ y Java, preceda a las barras diagonales inversas y comillas dobles con una barra diagonal inversa. Por ejemplo:

BSTR bszSpeak = SysAllocString (L "This is \\ \\ map = \\ " texto hablado \\ "= \\ " texto de globo \\ " \\ \\ ");

pCharacter->Speak (bszSpeak,......);

> [!Note]  
> El agente de Microsoft no admite todas las etiquetas especificadas en Microsoft Speech API. Además, la compatibilidad con algunos parámetros puede depender del motor de conversión de texto a voz instalado. Para obtener más información, consulte [etiquetas de salida de voz del agente de Microsoft](microsoft-agent-speech-output-tags.md).

 

### <a name="i-dont-seem-to-get-requeststart-and-requestcomplete-events-in-my-script-or-program"></a>No me gusta obtener los eventos RequestStart y RequestComplete en mi script (o programa).

Esto puede deberse a uno de los siguientes problemas:

-   El lenguaje de programación no es totalmente compatible con los controles ActiveX. Consulte la documentación para asegurarse de que admite la interfaz ActiveX y los eventos de los objetos ActiveX.
-   En una página web con scripts, se ha producido un error en la instalación o carga de otro control. Asegúrese de que todos los demás controles estén instalados y cargados correctamente sin Microsoft Agent.
-   En una página web con scripts con Marcos, tiene la `<OBJECT>` etiqueta del control Microsoft Agent en una página y los eventos se incluyen en la secuencia de comandos en otra página. Los eventos solo se envían a la página que hospeda el control.

### <a name="i-am-using-the-microsoft-agent-control-with-other-activex-controls-on-my-webpage-and-i-dont-seem-to-get-any-events"></a>Utilizo el control Microsoft Agent con otros controles ActiveX en mi página web y no me parece recibir ningún evento.

Compruebe si los otros controles están instalados correctamente. Si otro control ActiveX no se registra correctamente, es posible que el control de Microsoft Agent reciba sus eventos.

### <a name="what-programming-languages-can-i-use-to-program-the-microsoft-agent-control"></a>¿Qué lenguajes de programación se pueden usar para programar el control de Microsoft Agent?

El agente de Microsoft debe ser compatible con cualquier lenguaje que admita la interfaz ActiveX. Incluye ejemplos de código para Visual Basic, VBScript, JScript, C/C++ y Java.

### <a name="can-i-access-the-parameters-returned-from-microsoft-agent-using-jscript"></a>¿Puedo tener acceso a los parámetros devueltos por el agente de Microsoft mediante JScript?

Sí, pero actualmente la única forma de hacerlo es usar la `<SCRIPT LANGUAGE="JScript" FOR="*object*" EVENT="event()">` Sintaxis. Aunque esta sintaxis es compatible con Microsoft Internet Explorer, otros exploradores no lo admiten, por lo que puede que desee evitar el uso de JScript para esta parte del script de la página.

### <a name="can-microsoft-agent-be-used-with-speech-recognition-or-speech-synthesis-text-to-speech-or-tts-engines-other-than-those-supplied-by-microsoft"></a>¿Se puede usar el agente de Microsoft con el reconocimiento de voz o los motores de síntesis de voz (texto a voz o TTS) distintos de los proporcionados por Microsoft?

Sí, siempre que el motor admita las interfaces de Microsoft Speech API (SAPI) 4,0 necesarias para el agente de Microsoft. Consulte con el proveedor del motor. Para obtener detalles completos sobre las interfaces SAPI que requiere Microsoft Agent, consulte [requisitos de compatibilidad del motor de voz](speech-engine-support-requirements.md).

### <a name="my-page-includes-html-object-tags-for-microsoft-agent-the-lernout--hauspie-truvoice-tts-engine-and-the-microsoft-command-and-control-speech-recognition-engine-but-not-all-the-components-install"></a>Mi página incluye etiquetas de objeto HTML para el agente de Microsoft, el motor de Lernout & Hauspie TruVoice TTS y el motor de reconocimiento de voz de control y comando de Microsoft, pero no todos los componentes de instalación.

Normalmente, el problema se puede corregir actualizando la página. Como práctica general, es mejor especificar primero la etiqueta de control de agente de Microsoft `<OBJECT>` , después el motor de Lernout & Hauspie TruVoice y, a continuación, el comando y controlar el motor de reconocimiento de voz.

### <a name="after-calling-the-moveto-method-my-character-seems-to-freeze-even-though-i-have-return-animations-assigned-to-moving-state-animations"></a>Después de llamar al método moveTo, mi carácter parece inmovilizarse aunque se hayan devuelto animaciones para mover animaciones de estado.

Al reproducir una animación, los servicios de animación continúan mostrando su último fotograma hasta que se llama a otra animación. Por lo tanto, debe reproducir otra animación después de llamar a [**moveTo**](moveto-method.md). Si ha definido una animación de **devolución** para la animación de estado en **movimiento** , el servidor la reproducirá primero.

### <a name="when-i-query-the-characters-pitch-property-it-returns-a-value-of--1"></a>Cuando se consulta la propiedad de paso del carácter, devuelve un valor de-1.

Esto sucede si el carácter se ha compilado con la propiedad de tono predeterminada de un motor de voz. es decir, el paso no se cambió cuando se compiló el carácter.

### <a name="when-my-code-attempts-to-set-the-tts-mode-id-for-a-text-to-speech-engine-i-get-the-following-error-an-outgoing-call-cannot-be-made-since-the-application-is-dispatching-an-input-synchronous-call"></a>Cuando mi código intenta establecer el identificador de modo TTS para un motor de texto a voz, aparece el siguiente error: no se puede realizar una llamada saliente porque la aplicación está enviando una llamada sincrónica de entrada.

Para establecer la propiedad TTSModeID, debe tener Speech.dll instalado. Normalmente, se trata de una parte del código de instalación del motor de voz. También puede instalarlo instalando el panel de control de objetos de voz, disponible en la página de descargas de Microsoft Agent.

### <a name="when-i-retry-loading-a-character-that-failed-to-load-the-call-fails-with-a-character-already-loaded-error"></a>Al Reintentar cargar un carácter que no se pudo cargar, se produce un error en la llamada con el error "carácter ya cargado".

El control Microsoft Agent no descarga un objeto de carácter (libera la referencia) cuando no se puede cargar el archivo de caracteres asociado. Si desea volver a intentar cargar el carácter, debe llamar explícitamente a [**Unload**](unload-method.md) antes de llamar a [**Load**](load-method.md) la segunda vez. Si intenta hacerlo desde un script de página web, también debe preceder la llamada de **descarga** con una instrucción On Error Resume Next, o bien se producirá un error en la llamada a **Unload** . (Tenga en cuenta que JScript no tiene la instrucción On Error Resume Next).

Sin embargo, es posible que no tenga que incluir código para reintentar de inmediato la carga de un carácter cuando no se puede cargar el archivo. Microsoft Internet Explorer y el componente de servidor de Microsoft Agent intentan volver a intentarlo varias veces, por lo que es posible que el intento de realizar una carga correcta sea remoto. Una estrategia mejor consiste en esperar (establecer un temporizador) unos segundos antes de volver a intentarlo.

### <a name="how-can-i-install-microsoft-agent-as-part-of-my-application-or-from-my-web-server"></a>¿Cómo se puede instalar el agente de Microsoft como parte de mi aplicación o del servidor Web?

Puede instalar el agente desde el sitio web de Microsoft incluyendo su *CLSID en una etiqueta de objeto HTML*. Sin embargo, si desea incluir e instalar el agente desde su propio programa de instalación de la aplicación o desde su propio servidor, debe descargar el archivo. cab de instalación automática de Microsoft Agent, descargándolo desde la página de descargas. Al descargar, elija la opción Guardar en lugar de ejecutar del explorador. Cada vez que se ejecuta este archivo, se instalará automáticamente el agente de Microsoft en el equipo de destino. Por lo tanto, puede especificar el archivo en el script de instalación.

No intente instalar el agente de Microsoft mediante la copia de sus diversos. Los archivos dll y intentan registrarlos usted mismo. No se admite el intento de instalar el agente por cualquier otro medio que ejecute su archivo contenedor de instalación automática.

El sistema de destino también debe incluir las versiones recientes de MSVCRT.DLL (tiempo de ejecución de VC + +), REGSVR32.EXE (herramienta de registro incluida en Microsoft VC + +) y COM. La mejor manera de asegurarse de que se instalan las versiones correctas es requerir la instalación de Microsoft Internet Explorer 3,02 o posterior. Sin embargo, también puede conceder una licencia para estos requisitos de tiempo de ejecución. (Para obtener la versión más reciente de COM, obtenga acceso a la actualización DCOM desde el sitio web de Microsoft).

Microsoft Agent 2,0 no se instalará en Microsoft Windows 2000 ya que esta versión del sistema operativo ya incluye el agente.

### <a name="can-i-use-the-visual-basic-setup-wizard-to-install-microsoft-agent"></a>¿Puedo usar el Asistente para la instalación de Visual Basic para instalar el agente de Microsoft?

Aunque puede crear su propio programa de instalación mediante el código de Visual Basic (VB) no puede usar el Asistente para la instalación de Visual Basic para hacerlo. Para instalar el agente desde VB, puede usar el comando Shell, especificando el archivo contenedor de instalación automática de Microsoft Agent.

### <a name="how-do-i-install-microsoft-agent-on-windows-2000"></a>Cómo instalar el agente de Microsoft en Windows 2000

Microsoft Agent 2,0 no se instala en Windows 2000 porque ya está incluido como parte del sistema operativo.

### <a name="agentsvr-crashes-when-speak-is-called-with-a-wav-file"></a>AgentSvr se bloquea cuando se llama a Speak con un archivo WAV.

Esto puede producirse cuando el carácter ha estado usando TTS para la salida de voz y luego cambia para usar un archivo WAV. No se proporcionó texto en el primer parámetro del método Speak.

Para evitar el bloqueo, incluya un carácter de espacio en el primer parámetro del método Speak, incluso si no tiene salida de texto.

### <a name="even-though-i-have-already-installed-the-agent-language-component-dll-for-a-particular-language-i-still-got-an-error-that-the-component-is-missing-when-i-set-the-characters-language-to-that-language"></a>Aunque ya he instalado el componente de idioma del agente (DLL) para un idioma determinado, todavía obtengo un error que le falta el componente al establecer el idioma del carácter en ese idioma.

Esto suele suceder cuando se tienen aplicaciones de agente como Microsoft Office 2000 abiertas al instalar el componente de idioma del agente. Cierre todas las aplicaciones e inténtelo de nuevo. Si el problema persiste, reinicie el equipo y podrá establecer el ID. de idioma ahora.

### <a name="when-i-use-the-ampersand--symbol-the-text-around-the-symbol-in-the-characters-word-balloons-is-truncated"></a>Cuando utilizo el símbolo "&", se trunca el texto alrededor del símbolo en los globos de palabra del carácter.

Se trata de un problema conocido. Puede solucionar este fin mediante el uso de la etiqueta de mapa. Por ejemplo, para mostrar "A & B" en el globo de palabra del carácter, use "A \\ map =" y "=" && " \\ B" en la instrucción Speak.

### <a name="my-application-allows-users-to-change-the-default-character-and-when-they-do-the-program-crashes"></a>Mi aplicación permite a los usuarios cambiar el carácter predeterminado y, cuando lo hacen, el programa se bloquea.

Hay dos causas posibles:

Si cambia el identificador del modo TTS del carácter predeterminado y, a continuación, permite al usuario cambiar el carácter predeterminado a través de ShowDefaultCharacterProperties, AgentSvr se bloqueará.

Este problema se ha corregido en los sistemas operativos Windows 2000 y Windows XP. Para evitar el bloqueo en otras plataformas, no debe permitir que el usuario cambie el carácter predeterminado después de cambiar el identificador del modo TTS del carácter predeterminado o no use el carácter predeterminado de la aplicación o la Página Web.

Si la aplicación no usa caracteres de agente suministrados por Microsoft, asegúrese de que el carácter personalizado usa una paleta con una paleta completa de 256 colores. Para obtener más información, consulte el documento Designing Characters for Microsoft Agent.

### <a name="my-page-loads-the-agent-character-from-multiple-frames-with-ie-5-i-get-the-microsoft-agent-failed-to-load-error"></a>Mi página carga el carácter del agente desde varios fotogramas. Con IE 5, obtengo que el agente de Microsoft no pudo cargar el error.

Se trata de un problema conocido con IE 5. Se produjo un cambio en la forma en que el explorador controla un evento determinado, lo que hace que el script HTML empiece a ejecutarse antes de que se inicie AgentSvr. Para que la página funcione con todas las versiones del explorador, debe agregar esta línea al script:

AgentControl. Connected = true

que crea explícitamente una conexión a AgentSvr. Tenga en cuenta que solo tiene que hacer esto si la página carga el agente desde varios fotogramas.

### <a name="when-my-application-tries-to-install-microsoft-agent-on-windows-2000-or-windows-xp-i-get-the-error-that-agent-is-not-compatible-with-windows-2000-or-windows-xp"></a>Cuando mi aplicación intenta instalar el agente de Microsoft en Windows 2000 (o Windows XP), obtengo el error que el agente no es compatible con Windows 2000 (o Windows XP).

Una versión anterior del archivo. cab del componente principal del agente MSAGENT.exe, cuando se ejecuta en Windows 2000 (y Windows XP), bloqueará la instalación y mostrará un mensaje de error inexacto que indica que el agente no es compatible con la versión del sistema operativo que se está ejecutando. De hecho, los componentes principales de Microsoft Agent 2,0 se incluyen como parte de Windows 2000 (y Windows XP) y ya están instalados de forma predeterminada a través del programa de instalación de Windows.

En esta versión, se quita la comprobación y el archivo de instalación no mostrará el mensaje de error mencionado en Windows 2000 (o Windows XP). Tenga en cuenta que este es el único cambio en el archivo de instalación y no hay ningún cambio de código en los propios componentes principales del agente. Por lo tanto, no se ve afectado por esta actualización si ya tiene instalado el agente 2,0 o si el sitio Web usa una etiqueta de objeto para desencadenar descargas automáticas de los componentes principales del agente desde el almacén de objetos de Microsoft.

Si incluye el archivo de instalación del componente principal del agente con la aplicación, o si publica el archivo de instalación en el servidor, puede que desee descargar esta actualización. Para ello, haga clic aquí y seleccione la opción "guardar este programa en disco". Para estas circunstancias, debe tener una licencia de distribución de agentes válida y actual.

Como alternativa, también puede solucionar este problema mediante la opción silenciosa al instalar la versión anterior del archivo de instalación de MSAGENT.exe. El comando de Shell es:

**MSAGENT.exe/q: a**

Lo mismo se aplica a los componentes de idioma del agente que se publicaron originalmente en el 1998 de octubre. Se produjo una comprobación que impediría la instalación de los componentes de los idiomas árabe, Francés, alemán, hebreo, Italiano, Japonés, Coreano, Chino simplificado, español y chino tradicional en Windows 2000 (y Windows XP). Las versiones más recientes de estos archivos de instalación, junto con los 19 idiomas adicionales agregados en marzo de 2000, no contienen esta comprobación y se instalarán correctamente en Windows 2000 (y Windows XP).

### <a name="my-customized-character-exhibits-some-unexpected-behavior-with-its-transparency-color-on-windows-2000-and-windows-xp"></a>Mi carácter personalizado exhibe un comportamiento inesperado con el color de transparencia en Windows 2000 (y Windows XP).

Se trata de un problema conocido para los caracteres creados con una paleta de menos de 256 colores. Los problemas con estos caracteres incluyen el color de transparencia que se muestra en el fondo, el texto de globo transparente, el borde de globo transparente o el fondo de globo transparente. Tenga en cuenta que estos caracteres pueden hacer que las aplicaciones se bloqueen cuando se cargan en el cuadro de diálogo Selector de caracteres del agente o en la galería del Asistente para Microsoft Office. Los caracteres personalizados deben usar una paleta completa con 256 colores. Puede usar la paleta de ejemplo proporcionada para los caracteres del ayudante de Office como punto de partida con una paleta de colores 256 completa.

### <a name="the-character-does-not-use-the-british-english-tts-engine-even-though-i-have-set-its-language-id-to-british-english-h0809"></a>El carácter no usa el motor de TTS en inglés británico, aunque he establecido su identificador de idioma en inglés británico &h0809.

En primer lugar, asegúrese de que tiene instalados todos los componentes necesarios: los componentes principales del agente, los archivos binarios de tiempo de ejecución de SAPI y un motor de TTS en inglés SAPI4 compatible con el TTS3000, como el motor de inglés británico del Reino Unido, disponible para su descarga en la página de descargas del agente. Si el carácter sigue sin usar el motor de TTS en inglés británico, es probable que también tenga instalado un motor TTS en Inglés de Estados Unidos. Dado que tanto el inglés británico como el inglés americano comparten el mismo idioma principal (Inglés) y el inglés americano es el valor predeterminado, el agente seleccionará el primer motor de TTS inglés disponible, tal y como lo devolvió SAPI. Para usar un motor de TTS en inglés británico, utilice en su lugar la propiedad TTSModeID del carácter. Por ejemplo, el TTSModeID de la voz macho de inglés británico de TTS3000 es {227A0E41-A92A-11d1-B17B-0020AFED142E}. En Microsoft Visual Basic puede usar este motor estableciendo el valor de TTSModeID de Merlin como se indica a continuación:

AgentControl. Characters ("Merlin"). TTSModeID = {227A0E41-A92A-11d1-B17B-0020AFED142E}

### <a name="when-the-characters-volume-is-set-to-zero-using-the-speech-tag-vol0-it-either-has-no-effects-or-crashes-the-agentsvr"></a>Cuando el volumen del carácter se establece en cero mediante la etiqueta de voz \\ Vol = 0 \\ , no tiene ningún efecto o se bloquea el AgentSvr.

Se trata de un problema conocido. En los sistemas operativos Windows 95, Windows 98 y Windows me, el volumen del carácter no cambia, pero permanecerá en el nivel establecido anteriormente. En las plataformas Windows NT 4,0, Windows 2000 y Windows XP, esto hará que AgentSvr se bloquee, aunque no se haya instalado un motor TTS. Dado que el intervalo del volumen del carácter, de 0 (silencio) a 65535 (volumen máximo), es grande y la diferencia entre los niveles sucesivos no es muy importante, la solución alternativa consiste en establecer el volumen en 1 en lugar de 0 cuando se desea que la voz del carácter sea inaudible.

### <a name="my-customized-characters-return-animation-does-not-play-correctly-after-the-movedown-moveleft-moveright-andor-moveup-animations"></a>La animación devuelta del carácter personalizado no se reproduce correctamente después de las animaciones MoveDown, MoveLeft, MoveRight y/o MoveUp.

Asegúrese de que una animación de hablar simple está asignada al estado hablando. Por ejemplo, puede usar un solo fotograma compuesto por la posición neutra del carácter con superposiciones de la boca.

 

 





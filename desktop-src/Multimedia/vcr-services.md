---
title: Servicios de VCR
description: Servicios de VCR
ms.assetid: 140220f7-df7b-46e2-8374-e1200d873f3b
keywords:
- Arquitectura de control del sistema de vídeo (VISCA)
- VISCA (arquitectura de control del sistema de vídeo)
- Controlador de MCI VISCA
- Controlador VISCA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d884c38d224182db7eef8db0f0cd80b14e3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903677"
---
# <a name="vcr-services"></a>Servicios de VCR

Windows proporciona servicios de VCR a través de un controlador de dispositivo que se basa en el conjunto de comandos MCI para VCR. En esta sección se describe el controlador de la arquitectura de control del sistema de vídeo (VISCA) de MCI y se explica cómo usarlo para controlar un VCR.

El tipo de dispositivo *VCR* controla los VCR. Para obtener una lista de los comandos MCI reconocidos por los dispositivos VCR, consulte [conjunto de comandos VCR](vcr-command-set.md).

## <a name="the-mci-visca-driver"></a>El controlador VISCA de MCI

El controlador VISCA de MCI controla el VCR compatible con Sony VISCA, como CVD-1000 VDeck. El controlador VISCA controla el transporte de cinta, los sintonizadores de canales y los canales de entrada y salida de VCR.

## <a name="searching-and-positioning-with-a-vcr"></a>Búsqueda y posicionamiento con un VCR

El controlador VISCA usa dos métodos para realizar el seguimiento del movimiento de cinta en el transporte de cinta VCR: *información de código de tiempo* y *contadores de cinta*. La información del código de tiempo es la información de tiempo que se ha grabado en la cinta de vídeo. La mayoría de los VCR permiten grabar los códigos de tiempo sin destruir las pistas de audio y vídeo. Los contadores de cinta calculan la cantidad de cinta que viaja por encima de la cabeza de vídeo para obtener una posición.

Tanto la información de código de tiempo como los contadores de cinta aumentan a medida que la cinta de vídeo se mueve de principio a fin. Debido a su precisión, el uso de información de código de tiempo para colocar una cinta de vídeo casi siempre es preferible al uso de contadores de cinta.

Las marcas de comandos MCI para especificar la información de posición se expresan como dependencias de tiempo: "formato de hora", "duración", "desde", "hasta" y "Buscar". (Además, el comando [**status**](status.md) "Position" devuelve su valor de hora en el formato de hora actual).

El controlador VISCA usa el comando [**set**](set.md) "modo de tiempo" para seleccionar el tipo de ubicación que se va a usar con una cinta de vídeo. Cuando el modo de tiempo se establece en "código de tiempo", los comandos de **Estado** "posición" y **establecer** el "formato de hora" usan el código de tiempo de la cinta de vídeo. Cuando el modo de tiempo se establece en "Counter", los comandos de **Estado** "Position" y **set** "Time Format" usan contadores.

Una aplicación puede establecer el modo de hora en "detectar" si no importa que haya dos orígenes de información de posición. En el modo de detección, el controlador VISCA usa información de código de tiempo para la posición cuando se produce cualquiera de las siguientes condiciones:

-   La información del código de tiempo está presente cuando se abre el controlador.
-   Puede cambiar una cinta de vídeo con el comando **set** "puerta abierta" y la información de código de tiempo está presente en la cinta de vídeo.
-   Se reemite el comando [**set**](set.md) "modo de tiempo".

Si no se encuentra la información de código de tiempo, el controlador utiliza los contadores de cinta.

Para determinar el método de posicionamiento actual, emita el comando de [**Estado**](status.md) "tipo de hora", que devuelve "código de tiempo" o "contador". También puede identificar el modo de posicionamiento actual mediante el comando **Estado** "modo de tiempo", que devuelve "código de tiempo", "contador" o "detectar".

El comando **status** "Counter" recupera el valor del contador de cinta actual, independientemente del método de posicionamiento actual; sin embargo, puede usar este contador solo lectura con el comando [**set**](set.md) "Counter".

El controlador VISCA puede recuperar el formato de código de tiempo nativo registrado en una cinta de vídeo mediante los comandos de **Estado** " **tipo de código** de tiempo" y "velocidad de fotogramas". Por ejemplo, si el tipo de código de tiempo es "SMPTE" y la velocidad de fotogramas es 25, el formato de código de tiempo nativo registrado en la cinta de vídeo es SMPTE 25.

El controlador VISCA también puede recuperar la resolución del contador mediante el comando **status** "Counter Resolution", que devuelve "seconds" o "frames". El formato del contador todavía podría estar establecido en SMPTE 30, pero el valor devuelto solo devuelve un fotograma de 0. Si el tipo de hora actual es counter, esta resolución también se aplica al valor devuelto por **status** "Position".

## <a name="capturing-frames"></a>Capturar fotogramas

Los comandos de captura de fotogramas proporcionan imágenes fijas para un *dispositivo de captura de fotogramas*. Un dispositivo de captura de fotogramas es una parte independiente del hardware capaz de leer y almacenar la imagen de vídeo. El controlador VISCA admite el comando [**Freeze**](freeze.md) ([**\_ desbloqueo de MCI**](mci-freeze.md)) para estabilizar una imagen fija para la captura. Además, se puede usar el comando [**unfreeze**](unfreeze.md) (no [**\_ Freeze**](mci-unfreeze.md)) para reiniciar el transporte de cinta después de un comando **Freeze** .

El comando **Freeze** proporciona una imagen corregida y de alta calidad basada en el tiempo para un dispositivo de captura de fotogramas. Este comando existe porque es posible que un dispositivo no siempre entregue su imagen de salida de máxima calidad durante la reproducción o mientras está en pausa. Esta imagen de vídeo no es adecuada para la captura.

El comando **unfreeze** desbloquea el transporte de cinta y reanuda el modo de transporte en vigor antes del comando **Freeze** .

Cuando la aplicación necesite grabar una imagen de vídeo en el VCR, use el comando **inmovilizar** "entrada" o el comando de [**pila**](cue.md) ([**\_ pista de MCI**](mci-cue.md)) para grabar la imagen.

## <a name="selecting-inputs"></a>Seleccionar entradas

El controlador VISCA admite tres tipos de entrada: vídeo, audio y código de tiempo. Las entradas de vídeo incluyen dos canales estándar (líneas 1 y 2), un canal SVideo, un canal auxiliar y un canal de un sintonizador interno. Las entradas de audio incluyen dos canales estándar (líneas 1 y 2) y un canal de un sintonizador interno. La entrada de código de tiempo es interna para el VCR.

Las salidas normales llevan las entradas seleccionadas actualmente cuando se graba el VCR o cuando se detiene el transporte de cinta y llevan el contenido de la cinta de vídeo cuando el transporte de cinta se está reproduciendo o pausado. Las salidas supervisadas llevan la misma información que las salidas normales más la información del canal y el código de tiempo actual.

Suponiendo que las entradas externas adecuadas estén conectadas al VCR y haya decidido qué desea grabar, puede seleccionar las entradas que se van a registrar. Por ejemplo, para grabar o ver desde el vídeo "Svideo" y las entradas de audio "línea 1", usaría los comandos [**setvideo**](setvideo.md) ([**MCI \_ setvideo**](mci-setvideo.md)) y [**SetAudio**](setaudio.md) ([**MCI \_ SetAudio**](mci-setaudio.md)) para seleccionar estos orígenes de entrada. Puede comprobar estas selecciones mediante el comando [**status**](status.md) ([**MCI \_ status**](mci-status.md)).

De forma predeterminada, el monitor muestra exactamente lo que aparece como resultado. Sin embargo, a veces es posible que desee ver un origen mientras graba desde otro. Esta es una práctica común con el sintonizador. Por ejemplo, puede que desee ver el canal 4 mientras graba Channel 7. En este caso, tiene dos entradas de sintonizador lógico. Puede configurar el VCR mediante el uso de los siguientes comandos:

## <a name="to-review-one-source-while-recording-from-another"></a>Para revisar un origen mientras se graba desde otro

1.  Use el comando [**settuner**](settuner.md) ([**MCI \_ settuner**](mci-settuner.md)) para seleccionar los canales que se van a ver y grabar.
2.  Use el comando **setvideo** para seleccionar el origen de grabación de vídeo.
3.  Use el comando [**SetAudio**](setaudio.md) para seleccionar el origen de la grabación de audio.
4.  Use el comando [**setvideo**](setvideo.md) para enrutar la entrada de vídeo Channel 4 a la salida supervisada para mostrarla en pantalla.
5.  Use el comando [**SetAudio**](setaudio.md) para enrutar la entrada de audio Channel 4 a la salida supervisada para reproducir el audio.
6.  Compruebe las selecciones mediante el comando [**status**](status.md) .

El controlador VISCA también admite un tipo de entrada especial para audio y vídeo denominado *silenciar*. Silenciar permite seleccionar "sin entrada", lo que resulta útil al grabar una señal en blanco.

## <a name="selecting-recording-tracks"></a>Selección de pistas de grabación

Existen tres tipos de pistas de grabación en una cinta de vídeo: vídeo, audio y código de tiempo. Solo tiene una pista de vídeo o de código de tiempo, pero puede usar más de una pista de audio. Al hacerlo, realice el seguimiento 1 de la pista de audio principal.

El controlador VISCA admite dos modos de funcionamiento: ensamblar e insertar. En el *modo de ensamblado*, todas las pistas se seleccionan para grabarse. En el *modo de inserción*, las pistas pueden seleccionarse de forma independiente para la grabación. La mayoría de los VCR están en modo de ensamblado de forma predeterminada. Use el comando [**set**](set.md) ([**\_ set de MCI**](mci-set.md)) para cambiar estos modos.

## <a name="recording-and-editing"></a>Grabación y edición

El comando [**registro**](record.md) ([**\_ registro de MCI**](mci-record.md)) proporciona una grabación simple y tiene una precisión aproximada de 1 segundo a la posición inicial. Para grabar con más precisión, o si espera editar el contenido de vídeo mientras se operan varias Barajas simultáneamente, debe usar el comando [**CUE**](cue.md) ([**\_ pista de MCI**](mci-cue.md)).

El comando **CUE** prepara el dispositivo para grabarlo o reproducirlo. Use el comando **CUE** "Input" para preparar el dispositivo para la grabación. El comando **CUE** es necesario porque una aplicación debe saber cuándo el dispositivo está listo para ejecutar el comando (y porque puede tardar varios minutos en prepararse para un comando [**Play**](play.md) ([**\_ reproducción de MCI**](mci-play.md)) o **registro** ).

El VCR se prepara para grabarse o reproducirlo buscando *en el punto*, que es la posición actual o la posición especificada mediante el comando "desde" de la **pila** . Sin embargo, si se especifica el marcador "preroll" con el comando **CUE** , el VCR se sitúa en la distancia de preplantar desde el punto. La marca "preroll" también indica que el VCR usa cualquier modo de edición aplicable, por lo que es importante usar "preroll", especialmente cuando se desea la grabación más precisa. (Use el comando [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) con la marca "puede preroll" para comprobar si se admite el modo de reversión.

> [!Note]  
> Al grabar con las posiciones "desde" y "hasta", la posición "desde" se incluye en la edición y la posición "para" no.

 

Para obtener más información sobre la grabación, consulte [grabación](recording.md).

## <a name="using-the-clock-while-editing"></a>Usar el reloj mientras se edita

Al editar, es posible que desee grabar segmentos de un VCR en otro. Puede empezar a grabar en un momento determinado y colocarlo en un VCR mientras otro comienza a reproducirse al mismo tiempo y posición especificando una acción (reproducir o grabar), una posición y una hora para cada VCR.

Ambos VCR deben usar el mismo reloj para este tipo de edición; el reloj ayuda a sincronizar ambos dispositivos. Puede determinar si dos VCR comparten el mismo reloj mediante el comando [**status**](status.md) ([**MCI \_ status**](mci-status.md)) con la marca "Clock ID" para consultar cada VCR. Si los números de identificación devueltos por el comando **status** son los mismos, los dispositivos usan el mismo reloj. Como recurso compartido, el reloj se puede conectar a varios VCR. El controlador VISCA solo admite un reloj compartido.

También puede determinar la resolución del reloj mediante el comando de **Estado** "tasa de incremento del reloj". Este comando devuelve el número de incrementos que admite el reloj por segundo. Por ejemplo, si el reloj se actualiza cada milisegundo, el comando devuelve 1000 como la tasa de incremento del reloj. La ventaja de usar la tasa de incremento es que la tasa se expresa como un entero; de lo contrario, el incremento sería un valor de punto flotante de (precisión simple o doble). Como un entero, la manipulación de la tasa de incremento es una operación sencilla y no es susceptible a errores de redondeo. Puede restablecer el reloj mediante el comando [**set**](set.md) ([**\_ set MCI**](mci-set.md)) con la marca "Clock 0" (cero).

Al emitir un comando [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)), [**Record**](record.md) ([**\_ registro MCI**](mci-record.md)) o [**Seek**](seek.md) ([**MCI \_ Seek**](mci-seek.md)), puede especificar Cuándo se va a ejecutar el comando. Las características de los VCR que se usan determinan cuándo se debe iniciar cada VCR. El tiempo debe tener en cuenta la cantidad de reversión que requiere cada dispositivo y la cantidad de tiempo necesario para completar los comandos MCI utilizados para configurar la sesión de edición. Para ello, recupere la hora de reloj y agregue un intervalo de espera de 5 a 10 segundos. (El intervalo de espera debe ser lo suficientemente largo como para permitir que se complete la ejecución del prelanzamiento y los comandos MCI pendientes).

Para asegurarse de que el período de espera es suficientemente largo, coloque el comando de **registro** en la aplicación y Compruebe la hora inmediatamente anterior. Si el intervalo es demasiado corto, reinicie el comando **Play** . Como alternativa, puede comprobar la hora inmediatamente después del último comando del script para comprobar que hay suficiente tiempo para enviar y completar todos los comandos.

 

 





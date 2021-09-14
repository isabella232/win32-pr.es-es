---
title: Servicios VCR
description: Servicios VCR
ms.assetid: 140220f7-df7b-46e2-8374-e1200d873f3b
keywords:
- Arquitectura de control del sistema de vídeo (VISCA)
- VISCA (Arquitectura de control del sistema de vídeo)
- Controlador VISCA de MCI
- Controlador VISCA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d884c38d224182db7eef8db0f0cd80b14e3a08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245684"
---
# <a name="vcr-services"></a>Servicios VCR

Windows servicios VCR a través de un controlador de dispositivo que se basa en el conjunto de comandos MCI para los VCR. En esta sección se describe el controlador MCI Video System Control Architecture (VISCA) y se explica cómo usarlo para controlar un VCR.

El *tipo de dispositivo vcr* controla las VCR. Para obtener una lista de los comandos MCI reconocidos por los dispositivos VCR, vea [Conjunto de comandos de VCR.](vcr-command-set.md)

## <a name="the-mci-visca-driver"></a>El controlador VISCA de MCI

El controlador de MCI VISCA controla los VCR compatibles con Visca de Gama, como el VDeck CVD-1000. El controlador VISCA controla el transporte de cinta, los tuneres de canal y los canales de entrada y salida de VCR.

## <a name="searching-and-positioning-with-a-vcr"></a>Búsqueda y posicionamiento con un VCR

El controlador VISCA usa dos métodos para realizar un  seguimiento del movimiento de la cinta de vídeo dentro del transporte de cintas VCR: información de códigos de tiempo y *contadores de cinta.* La información del código de tiempo es información de tiempo que se ha registrado en la cinta de vídeo. La mayoría de los VCR permiten grabar códigos de tiempo sin destruir pistas de audio y vídeo. Los contadores de cinta calculan la cantidad de cinta de vídeo que se desplaza más allá de la cabeza de la cinta de vídeo para obtener una posición.

La información del código de tiempo y los contadores de cinta aumentan a medida que la cinta de vídeo se mueve de principio a fin. Debido a su precisión, el uso de información de código de tiempo para colocar una cinta de vídeo es casi siempre preferible al uso de contadores de cinta.

Las marcas de comandos de MCI para especificar la información de posicionamiento se expresan como dependencias de tiempo: "formato de hora", "duración", "de", "a" y "buscar". (Además, el [**comando**](status.md) "position" de estado devuelve su valor de hora en el formato de hora actual).

El controlador VISCA usa el [**comando set**](set.md) "time mode" para seleccionar el tipo de posicionamiento que se usará con una cinta de vídeo. Cuando el modo de hora se establece en "timecode", los comandos **de** estado "position" y **set** "time format" usan el código de tiempo en la cinta de vídeo. Cuando el modo de hora se establece en "counter", los comandos **de** estado "position" y **set** "time format" usan contadores.

Una aplicación puede establecer el modo de tiempo en "detectar" si no importa que pueda haber dos orígenes de información de posición. Cuando está en modo de detección, el controlador VISCA usa información de código de tiempo para el posicionamiento cuando se produce cualquiera de las condiciones siguientes:

-   La información del código de tiempo está presente cuando se abre el controlador.
-   Puede cambiar una cinta de vídeo con **el** comando "door open" establecido y la información del código de tiempo está presente en la cinta de vídeo.
-   Se [**vuelve a**](set.md) emitir el comando set "time mode".

Si no se encuentra la información del código de tiempo, el controlador usa los contadores de cinta.

Para determinar el método de posicionamiento actual, emita el comando [**de**](status.md) estado "tipo de hora", que devuelve "código de tiempo" o "contador". También puede identificar el modo de posicionamiento actual mediante el comando de estado **"time** mode", que devuelve "timecode", "counter" o "detect".

El **comando** "counter" de estado recupera el valor del contador de cinta actual, independientemente del método de posicionamiento actual; sin embargo, este contador solo se puede usar con el [**comando set**](set.md) "counter".

El controlador VISCA puede recuperar el formato de código de tiempo nativo registrado en una cinta de vídeo mediante los comandos de estado **"tipo** de código de tiempo" y **"velocidad** de fotogramas" de estado juntos. Por ejemplo, si el tipo de código de tiempo es "smpte" y la velocidad de fotogramas es 25, el formato de código de tiempo nativo registrado en la cinta de vídeo es SMPTE 25.

El controlador VISCA también puede recuperar la resolución del contador mediante el comando **de** estado "counter resolution", que devuelve "segundos" o "fotogramas". El formato del contador todavía puede establecerse en SMPTE 30, pero el valor devuelto devuelve solo un marco de 0. Si el tipo de hora actual es counter, esta resolución se aplica también al valor devuelto por **el estado** "position".

## <a name="capturing-frames"></a>Captura de fotogramas

Los comandos de captura de fotogramas proporcionan imágenes fijas para un *dispositivo de captura de fotogramas.* Un dispositivo de captura de fotogramas es un fragmento de hardware independiente capaz de leer y almacenar la imagen de vídeo. El controlador VISCA admite el [**comando freeze**](freeze.md) [**(MCI \_ FREEZE)**](mci-freeze.md)para estabilizar una imagen fija para la captura. Además, el [**comando unfreeze**](unfreeze.md) [**(MCI \_ UNFREEZE)**](mci-unfreeze.md)se puede usar para reiniciar el transporte de cintas después de un **comando freeze.**

El **comando freeze** proporciona una imagen de base de tiempo de alta calidad, estabilizada y con base de tiempo corregida para un dispositivo de captura de fotogramas. Este comando existe porque es posible que un dispositivo no siempre entregue su imagen de salida de máxima calidad durante la reproducción o mientras está en pausa. esta imagen de vídeo no es adecuada para la captura.

El **comando unfreeze** desbloquea el transporte de cinta y reanuda el modo de transporte en vigor antes del **comando freeze.**

Cuando la aplicación necesite grabar una imagen de  vídeo en el VCR, use el comando inmovilizar "input" o el comando [**cue**](cue.md) [**(MCI \_ CUE)**](mci-cue.md)para grabar la imagen.

## <a name="selecting-inputs"></a>Selección de entradas

El controlador VISCA admite tres tipos de entrada: vídeo, audio y código de tiempo. Las entradas de vídeo incluyen dos canales estándar (líneas 1 y 2), un canal SVideo, un canal auxiliar y un canal de un tuner interno. Las entradas de audio incluyen dos canales estándar (líneas 1 y 2) y un canal de un afinador interno. La entrada del código de tiempo es interna del VCR.

Las salidas normales llevan las entradas seleccionadas actualmente cuando el VCR está grabando o cuando se detiene el transporte de cinta, y llevan el contenido de la cinta cuando el transporte de cinta se está reproduciendo o pausando. Las salidas supervisadas llevan la misma información que las salidas normales, además del código de tiempo actual y la información del canal.

Suponiendo que las entradas externas adecuadas estén conectadas a su VCR y haya decidido lo que desea grabar, puede seleccionar las entradas que se van a grabar. Por ejemplo, para grabar o ver desde el vídeo "svideo" y las entradas de audio de "línea 1", usaría los comandos [**setvideo**](setvideo.md) ([**MCI \_ SETVIDEO**](mci-setvideo.md)) y [**setaudio**](setaudio.md) ([**MCI \_ SETAUDIO**](mci-setaudio.md)) para seleccionar estos orígenes de entrada. Puede comprobar estas selecciones mediante el comando [**status**](status.md) ([**MCI \_ STATUS**](mci-status.md)).

De forma predeterminada, el monitor muestra exactamente lo que aparece como salida. En ocasiones, sin embargo, es posible que quiera ver un origen mientras graba desde otro. Se trata de una práctica común con el afinador. Por ejemplo, es posible que quiera ver el canal 4 mientras graba el canal 7. En este caso, tiene dos entradas de afinador lógico. Puede configurar vcr mediante los siguientes comandos:

## <a name="to-review-one-source-while-recording-from-another"></a>Para revisar un origen mientras se graba desde otro

1.  Use el [**comando settuner**](settuner.md) ([**MCI \_ SETTUNER**](mci-settuner.md)) para seleccionar los canales que desea ver y grabar.
2.  Use el **comando setvideo** para seleccionar el origen de grabación de vídeo.
3.  Use el [**comando setaudio**](setaudio.md) para seleccionar el origen de grabación de audio.
4.  Use el [**comando setvideo**](setvideo.md) para enrutar la entrada de vídeo del canal 4 a la salida supervisada para mostrarla en pantalla.
5.  Use el [**comando setaudio**](setaudio.md) para enrutar la entrada de audio del canal 4 a la salida supervisada para reproducir el audio.
6.  Compruebe las selecciones mediante el [**comando status.**](status.md)

El controlador VISCA también admite un tipo de entrada especial para audio y vídeo denominado *mute*. La exclusión mutua permite seleccionar "sin entrada", lo que resulta útil al grabar una señal en blanco.

## <a name="selecting-recording-tracks"></a>Selección de pistas de grabación

Existen tres tipos de pistas de grabación en una cinta de vídeo: vídeo, audio y código de tiempo. Solo tiene una pista de vídeo o código de tiempo, pero puede usar más de una pista de audio. Al hacerlo, realice la pista 1 como pista de audio principal.

El controlador VISCA admite dos modos de funcionamiento: ensamblar e insertar. En *modo de ensamblado,* se seleccionan todas las pistas que se van a grabar. En *el modo de inserción,* las pistas se pueden seleccionar de forma independiente para la grabación. La mayoría de los VCR están en modo de ensamblado de forma predeterminada. Use el [**comando set**](set.md) ([**MCI \_ SET**](mci-set.md)) para cambiar estos modos.

## <a name="recording-and-editing"></a>Grabación y edición

El [**comando record**](record.md) ([**MCI \_ RECORD**](mci-record.md)) proporciona una grabación sencilla y es preciso aproximadamente a 1 segundo de la posición inicial. Para grabar con más precisión, o si espera editar el contenido del vídeo mientras se usan simultáneamente varias barajas, debe usar el comando [**cue**](cue.md) [**(MCI \_ CUE).**](mci-cue.md)

El **comando cue** prepara el dispositivo para grabar o reproducir. Use el **comando cue** "input" para preparar el dispositivo para la grabación. El **comando cue** es necesario porque una aplicación debe saber cuándo el dispositivo está listo para [](play.md) realizar el comando (y porque puede tardar varios minutos en prepararse para una reproducción [**(MCI \_ PLAY)**](mci-play.md)o un comando **de** registro).

El VCR se prepara para grabar o reproducir buscando en el punto , que es la posición actual o la posición especificada mediante el comando **"from"** de la indicación. Sin embargo, si se especifica la marca "preroll" con el comando **cue,** el VCR se coloca a sí mismo la distancia previa a la inscripción desde el punto inicial. La marca "preroll" también indica que vcr usa cualquier modo de edición aplicable, por lo que es importante que use "preroll", especialmente cuando se desea la grabación más precisa. (Use el [**comando capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) con la marca "puede realizar la inscripción previa" para comprobar si se admite el modo de inscripción previa).

> [!Note]  
> Cuando se graba con las posiciones "from" y "to", la posición "from" se incluye en la edición y la posición "to" no.

 

Para obtener más información sobre la grabación, vea [Grabación de](recording.md).

## <a name="using-the-clock-while-editing"></a>Usar el reloj durante la edición

Al editar, es posible que desee registrar segmentos de un VCR a otro. Puede empezar a grabar a una hora y posición concretas en un VCR, mientras que otro empieza a reproducirse al mismo tiempo y a la misma posición especificando una acción (reproducción o grabación), una posición y una hora para cada VCR.

Ambos VCR deben usar el mismo reloj para este tipo de edición; el reloj ayuda a sincronizar ambos dispositivos. Puede determinar si dos VCR comparten el mismo reloj mediante el comando [**status**](status.md) ([**MCI \_ STATUS**](mci-status.md)) con la marca "clock id" para consultar cada VCR. Si los números de identificación devueltos por el **comando de** estado son los mismos, los dispositivos usan el mismo reloj. Como recurso compartido, el reloj se puede conectar a varios VCR. El controlador VISCA solo admite un reloj compartido.

También puede determinar la resolución del reloj mediante el **comando** de estado "velocidad de incremento del reloj". Este comando devuelve el número de incrementos que admite el reloj por segundo. Por ejemplo, si el reloj se actualiza cada milisegundo, el comando devuelve 1000 como velocidad de incremento del reloj. La ventaja de usar la tasa de incremento es que la velocidad se expresa como un entero; De lo contrario, el incremento sería un valor de punto flotante (de precisión sencilla o doble). Como entero, manipular la tasa de incremento es una operación sencilla y no es susceptible a errores de redondeo. Puede restablecer el reloj mediante el comando [**set**](set.md) ([**MCI \_ SET**](mci-set.md)) con la marca "clock 0" (cero).

Al emitir un comando [**play**](play.md) ([**MCI \_ PLAY**](mci-play.md)), [**record**](record.md) ([**MCI \_ RECORD**](mci-record.md)) o [**seek**](seek.md) ([**MCI \_ SEEK**](mci-seek.md)), puede especificar cuándo se va a ejecutar el comando. Las características de los VCR que se usan determinan cuándo iniciar cada VCR. El tiempo debe tener en cuenta la cantidad de inscripción previa que requiere cada dispositivo y la cantidad de tiempo necesaria para completar los comandos de MCI usados para configurar la sesión de edición. Para ello, recupere la hora del reloj y agregue un intervalo de espera de 5 a 10 segundos. (El intervalo de espera debe ser lo suficientemente largo como para permitir que la inscripción previa y los comandos de MCI pendientes terminen de ejecutarse).

Para asegurarse de que el período de espera es lo suficientemente largo, coloque el comando **de** registro en último lugar en la aplicación y compruebe la hora inmediatamente anterior. Si el intervalo es demasiado corto, reinicie el **comando play.** Como alternativa, puede comprobar la hora inmediatamente posterior al último comando del script para comprobar que hay tiempo suficiente para enviar y completar todos los comandos.

 

 





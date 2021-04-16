---
title: Clasificaciones de comandos MCI
description: Clasificaciones de comandos MCI
ms.assetid: e03edfab-06c9-4337-935b-9effd2996c2e
keywords:
- Comandos MCI, clasificaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1524e6aa2094679e91acddb9dbfbb8cb480eb39f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531893"
---
# <a name="classifications-of-mci-commands"></a>Clasificaciones de comandos MCI

MCI define cuatro clasificaciones de comandos: System, Required, Basic y Extended. En la lista siguiente se describen estas clasificaciones de comandos:

-   Los *comandos del sistema* se controlan mediante MCI directamente, en lugar de hacerlo por el controlador.
-   Los *comandos obligatorios* se controlan mediante el controlador. Todos los controladores MCI deben admitir los comandos y las marcas necesarios.
-   Algunos dispositivos usan *comandos básicos* (o comandos opcionales). Si un dispositivo admite un comando básico, debe admitir un conjunto definido de marcas para ese comando.
-   Los *comandos extendidos* son específicos de un tipo de dispositivo o controlador. Los comandos extendidos incluyen comandos, como los comandos [**Put**](put.md) ([**MCI \_ Put**](mci-put.md)) y [**Where**](where.md) ([**MCI \_ Where**](mci-where.md)) para los tipos de dispositivo **DigitalVideo** y **Overlay** , y extensiones a comandos existentes (como la marca "stretch" del comando [**status**](status.md) ([**MCI \_ status**](mci-status.md)) para el tipo de dispositivo superpuesto).

Aunque el sistema y los comandos necesarios son el conjunto de comandos mínimo para cualquier controlador MCI, los comandos básicos y extendidos no son compatibles con todos los controladores. La aplicación siempre puede usar los comandos obligatorios y del sistema y sus marcas, pero si necesita usar un comando o una marca básica o extendida, primero debe consultar el controlador mediante el comando [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)). En las secciones siguientes se resumen los comandos específicos de cada categoría.

## <a name="system-commands"></a>Comandos del sistema

MCI procesa los siguientes comandos del sistema directamente, en lugar de pasarlos a dispositivos MCI.



| String                 | Message                             | Descripción                            |
|------------------------|-------------------------------------|----------------------------------------|
| [**break**](break.md) | [**interrupción de MCI \_**](mci-break.md)     | Establece una clave de interrupción para un dispositivo MCI.    |
| [sysinfo](sysinfo.md) | [**MCI \_ SYSINFO**](mci-sysinfo.md) | Devuelve información acerca de los dispositivos MCI. |



 

## <a name="required-commands"></a>Comandos necesarios

Todos los dispositivos MCI admiten los siguientes comandos necesarios.



| String                           | Message                                   | Descripción                                                                                                               |
|----------------------------------|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**pueda**](capability.md) | [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) | Obtiene las capacidades de un dispositivo.                                                                                     |
| [**cercanos**](close.md)           | [**\_cerrar MCI**](mci-close.md)           | Cierra el dispositivo.                                                                                                        |
| [**superclase**](info.md)             | [**información de MCI \_**](mci-info.md)             | Obtiene información de texto de un dispositivo.                                                                                |
| [**Ábra**](open.md)             | [**MCI \_ abierto**](mci-open.md)             | Inicializa el dispositivo.                                                                                                   |
| [**status**](status.md)         | [**Estado de MCI \_**](mci-status.md)         | Obtiene información de estado del dispositivo. Algunas de las marcas de este comando no son necesarias, por lo que también es un comando básico. |



 

Los dispositivos también deben admitir un conjunto estándar de marcas de comandos para los comandos necesarios.

## <a name="basic-commands"></a>Comandos básicos

La lista siguiente resume los comandos básicos. El uso de estos comandos mediante un dispositivo MCI es opcional.



| String                   | Message                           | Descripción                                                                                                                                                                                                                             |
|--------------------------|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dataloader**](load.md)     | [**carga de MCI \_**](mci-load.md)     | Carga los datos de un archivo.                                                                                                                                                                                                                 |
| [**temporalmente**](pause.md)   | [**pausa de MCI \_**](mci-pause.md)   | Detiene la reproducción. La reproducción o grabación se puede reanudar en la posición actual.                                                                                                                                                            |
| [**reproducción**](play.md)     | [**reproducción de MCI \_**](mci-play.md)     | Inicia la transmisión de datos de salida.                                                                                                                                                                                                        |
| [**registro**](record.md) | [**registro de MCI \_**](mci-record.md) | Inicia el registro de datos de entrada.                                                                                                                                                                                                            |
| [**Recuper**](resume.md) | [**\_reanudación de MCI**](mci-resume.md) | Reanuda la reproducción o grabación en un dispositivo en pausa.                                                                                                                                                                                        |
| [**guardar**](save.md)     | [**\_Guardar MCI**](mci-save.md)     | Guarda los datos en un archivo de disco.                                                                                                                                                                                                              |
| [**desean**](seek.md)     | [**búsqueda de MCI \_**](mci-seek.md)     | Busca hacia delante o hacia atrás.                                                                                                                                                                                                              |
| [**set**](set.md)       | [**MCI \_ set**](mci-set.md)       | Establece el estado operativo del dispositivo.                                                                                                                                                                                                 |
| [**status**](status.md) | [**ESTADO DE MCI**](mci-status.md)  | Obtiene información de estado sobre el dispositivo. Este también es un comando obligatorio; puesto que algunas de sus marcas no son necesarias, también se enumeran aquí. (Los elementos opcionales admiten dispositivos que usan medios lineales con posiciones identificables). |
| [**detener**](stop.md)     | [**detención de MCI \_**](mci-stop.md)     | Detiene la reproducción.                                                                                                                                                                                                                          |



 

Si un controlador admite un comando básico, también debe admitir un conjunto estándar de marcas para el comando.

## <a name="extended-commands"></a>Comandos extendidos

Algunos dispositivos MCI tienen comandos adicionales o agregan marcas a comandos existentes. Aunque algunos comandos extendidos solo se aplican a un controlador de dispositivo específico, la mayoría de ellos se aplican a todos los controladores de un tipo de dispositivo determinado. Por ejemplo, el conjunto de comandos para el tipo de dispositivo **Sequencer** amplía el comando [**set**](set.md) ([**\_ set MCI**](mci-set.md)) para agregar formatos de hora que son necesarios para los secuenciadores MIDI.

No debe suponer que el dispositivo admite los comandos extendidos o las marcas. Puede usar el comando [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) para determinar si se admite una característica específica y la aplicación debe estar preparada para tratar con los valores devueltos "comando no admitido" o "función no admitida".

Los siguientes comandos extendidos están disponibles con los tipos de dispositivo enumerados.



| String                         | Message                                 | Tipos de dispositivo            | Descripción                                                                                       |
|--------------------------------|-----------------------------------------|-------------------------|---------------------------------------------------------------------------------------------------|
| [**configurar**](configure.md) | [**configuración de MCI \_**](mci-configure.md) | digitalvideo            | Muestra un cuadro de diálogo de configuración.                                                              |
| [**indicación**](cue.md)             | [**\_pista MCI**](mci-cue.md)             | digitalvideo, waveaudio | Se prepara para reproducir o grabar.                                                                |
| [**elimínelos**](delete.md)       | [**eliminación de MCI \_**](mci-delete.md)       | waveaudio               | Elimina un segmento de datos del archivo multimedia.                                                       |
| [salida](escape.md)           | [**ESCAPE de MCI \_**](mci-escape.md)       | videodisco               | Envía información personalizada a un dispositivo.                                                             |
| [**Inmovilice**](freeze.md)       | [**inmovilización de MCI \_**](mci-freeze.md)       | overlay                 | Deshabilita la adquisición de vídeo en el búfer de fotogramas.                                                   |
| [**pondrán**](put.md)             | [**COLOCACIÓN DE MCI**](mci-put.md)              | DigitalVideo, superposición   | Define las ventanas de origen, de destino y de marco.                                               |
| [**alcanzar**](realize.md)     | [**\_obtener MCI**](mci-realize.md)     | digitalvideo            | Indica al dispositivo que seleccione y dé su paleta en un contexto de dispositivo de la ventana mostrada. |
| [**setaudio**](setaudio.md)   | [**MCI \_ SETAUDIO**](mci-setaudio.md)  | digitalvideo            | Establece los parámetros de audio para el vídeo.                                                                  |
| [**setvideo**](setvideo.md)   | [**MCI \_ SETVIDEO**](mci-setvideo.md)  | digitalvideo            | Establece los parámetros de vídeo.                                                                            |
| [**marcar**](signal.md)       | [**señal de MCI \_**](mci-signal.md)       | digitalvideo            | Identifica una posición especificada con una señal.                                                    |
| [**bucle**](spin.md)           | [**giro de MCI \_**](mci-spin.md)           | videodisco               | Inicia el giro del disco o detiene el disco.                                         |
| [**pasar**](step.md)           | [**\_paso MCI**](mci-step.md)           | DigitalVideo, Videodisc | Pasos para reproducir una o más tramas hacia delante o hacia atrás.                                             |
| [**liberar**](unfreeze.md)   | [**desbloqueo de MCI \_**](mci-unfreeze.md)   | overlay                 | Habilita el búfer de fotogramas para adquirir datos de vídeo.                                                   |
| [**Update**](update.md)       | [**actualización de MCI \_**](mci-update.md)       | digitalvideo            | Vuelve a dibujar el marco actual en el contexto del dispositivo.                                               |
| [**where**](where.md)         | [**MCI DONDE**](mci-where.md)          | DigitalVideo, superposición   | Obtiene el rectángulo que especifica el área de origen, destino o marco.                          |
| [**ventana**](window.md)       | [**\_ventana MCI**](mci-window.md)       | DigitalVideo, superposición   | Controla la ventana de presentación.                                                                      |



 

 

 





---
title: Clasificaciones de comandos de MCI
description: Clasificaciones de comandos de MCI
ms.assetid: e03edfab-06c9-4337-935b-9effd2996c2e
keywords:
- Comandos de MCI, clasificaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1524e6aa2094679e91acddb9dbfbb8cb480eb39f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369823"
---
# <a name="classifications-of-mci-commands"></a>Clasificaciones de comandos de MCI

MCI define cuatro clasificaciones de comandos: system, required, basic y extended. En la lista siguiente se describen estas clasificaciones de comandos:

-   *Los comandos del* sistema se controlan mediante MCI directamente, en lugar de por el controlador.
-   *El controlador* controla los comandos necesarios. Todos los controladores de MCI deben admitir los comandos y marcas necesarios.
-   *Algunos dispositivos* usan comandos básicos (u comandos opcionales). Si un dispositivo admite un comando básico, debe admitir un conjunto definido de marcas para ese comando.
-   *Los comandos extendidos* son específicos de un tipo de dispositivo o controlador. Los comandos extendidos incluyen comandos, como los comandos [](status.md) [**put**](put.md) ([**MCI \_ PUT**](mci-put.md)) y [**where**](where.md) ([**MCI \_ WHERE**](mci-where.md)) para los tipos de dispositivo **digitalvideo** y **overlay,** y extensiones a comandos existentes (como la marca "stretch" del comando status [**(MCI \_ STATUS)**](mci-status.md)para el tipo de dispositivo de superposición).

Aunque el sistema y los comandos necesarios son el conjunto mínimo de comandos para cualquier controlador MCI, los comandos básicos y extendidos no son compatibles con todos los controladores. La aplicación siempre puede usar el sistema y los comandos necesarios y sus marcas, pero si necesita usar un comando o una marca básico o extendido, primero debe consultar el controlador mediante el comando [**capability**](capability.md) [**(MCI \_ GETDEVCAPS).**](mci-getdevcaps.md) En las secciones siguientes se resumen los comandos específicos de cada categoría.

## <a name="system-commands"></a>Comandos del sistema

MCI procesa los siguientes comandos del sistema directamente, en lugar de pasarlos a dispositivos MCI.



| String                 | Message                             | Descripción                            |
|------------------------|-------------------------------------|----------------------------------------|
| [**break**](break.md) | [**MCI \_ BREAK**](mci-break.md)     | Establece una clave de interrupción para un dispositivo MCI.    |
| [Sysinfo](sysinfo.md) | [**SYSINFO de MCI \_**](mci-sysinfo.md) | Devuelve información sobre los dispositivos MCI. |



 

## <a name="required-commands"></a>Comandos necesarios

Todos los dispositivos MCI admiten los siguientes comandos necesarios.



| String                           | Message                                   | Descripción                                                                                                               |
|----------------------------------|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Capacidad**](capability.md) | [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) | Obtiene las funcionalidades de un dispositivo.                                                                                     |
| [**Cerca**](close.md)           | [**MCI \_ CLOSE**](mci-close.md)           | Cierra el dispositivo.                                                                                                        |
| [**Información**](info.md)             | [**INFORMACIÓN \_ de MCI**](mci-info.md)             | Obtiene información textual de un dispositivo.                                                                                |
| [**Abierto**](open.md)             | [**MCI \_ OPEN**](mci-open.md)             | Inicializa el dispositivo.                                                                                                   |
| [**status**](status.md)         | [**ESTADO \_ DE MCI**](mci-status.md)         | Obtiene información de estado del dispositivo. Algunas de las marcas de este comando no son necesarias, por lo que también es un comando básico. |



 

Los dispositivos también deben admitir un conjunto estándar de marcas de comandos para los comandos necesarios.

## <a name="basic-commands"></a>Comandos básicos

En la lista siguiente se resumen los comandos básicos. El uso de estos comandos por parte de un dispositivo MCI es opcional.



| String                   | Message                           | Descripción                                                                                                                                                                                                                             |
|--------------------------|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Carga**](load.md)     | [**MCI \_ LOAD**](mci-load.md)     | Carga datos de un archivo.                                                                                                                                                                                                                 |
| [**Pausa**](pause.md)   | [**PAUSA \_ DE MCI**](mci-pause.md)   | Deja de reproducirse. La reproducción o grabación se pueden reanudar en la posición actual.                                                                                                                                                            |
| [**Jugar**](play.md)     | [**MCI \_ PLAY**](mci-play.md)     | Inicia la transmisión de datos de salida.                                                                                                                                                                                                        |
| [**grabar**](record.md) | [**REGISTRO \_ de MCI**](mci-record.md) | Inicia la grabación de los datos de entrada.                                                                                                                                                                                                            |
| [**Reanudar**](resume.md) | [**MCI \_ RESUME**](mci-resume.md) | Reanuda la reproducción o grabación en un dispositivo en pausa.                                                                                                                                                                                        |
| [**Salvar**](save.md)     | [**MCI \_ SAVE**](mci-save.md)     | Guarda los datos en un archivo de disco.                                                                                                                                                                                                              |
| [**Buscar**](seek.md)     | [**MCI \_ SEEK**](mci-seek.md)     | Busca hacia delante o hacia atrás.                                                                                                                                                                                                              |
| [**Establecer**](set.md)       | [**MCI \_ SET**](mci-set.md)       | Establece el estado operativo del dispositivo.                                                                                                                                                                                                 |
| [**status**](status.md) | [**ESTADO DE MCI**](mci-status.md)  | Obtiene información de estado sobre el dispositivo. También es un comando obligatorio; dado que algunas de sus marcas no son necesarias, también se muestra aquí. (Los elementos opcionales admiten dispositivos que usan medios lineales con posiciones identificables). |
| [**Parada**](stop.md)     | [**MCI \_ STOP**](mci-stop.md)     | Deja de reproducirse.                                                                                                                                                                                                                          |



 

Si un controlador admite un comando básico, también debe admitir un conjunto estándar de marcas para el comando.

## <a name="extended-commands"></a>Comandos extendidos

Algunos dispositivos MCI tienen comandos adicionales o agregan marcas a los comandos existentes. Aunque algunos comandos extendidos solo se aplican a un controlador de dispositivo específico, la mayoría de ellos se aplican a todos los controladores de un tipo de dispositivo determinado. Por ejemplo, el conjunto de comandos para el tipo de dispositivo **sequencer** amplía el comando [**set**](set.md) ([**MCI \_ SET**](mci-set.md)) para agregar los formatos de tiempo necesarios para los secuenciadores DE LÍNEA.

No debe suponer que el dispositivo admite los comandos extendidos o las marcas. Puede usar el comando [**capability**](capability.md) [**(MCI \_ GETDEVCAPS)**](mci-getdevcaps.md)para determinar si se admite una característica específica y la aplicación debe estar lista para tratar con valores devueltos de "comando no admitido" o "función no compatible".

Los siguientes comandos extendidos están disponibles con los tipos de dispositivo enumerados.



| String                         | Message                                 | Tipos de dispositivo            | Descripción                                                                                       |
|--------------------------------|-----------------------------------------|-------------------------|---------------------------------------------------------------------------------------------------|
| [**Configurar**](configure.md) | [**MCI \_ CONFIGURE**](mci-configure.md) | digitalvideo            | Muestra un cuadro de diálogo de configuración.                                                              |
| [**Cue**](cue.md)             | [**MCI \_ CUE**](mci-cue.md)             | digitalvideo, waveaudio | Se prepara para reproducir o grabar.                                                                |
| [**Eliminar**](delete.md)       | [**MCI \_ DELETE**](mci-delete.md)       | waveaudio               | Elimina un segmento de datos del archivo multimedia.                                                       |
| [Escapar](escape.md)           | [**ESCAPE \_ de MCI**](mci-escape.md)       | Videodisco               | Envía información personalizada a un dispositivo.                                                             |
| [**Congelar**](freeze.md)       | [**MCI \_ FREEZE**](mci-freeze.md)       | overlay                 | Deshabilita la adquisición de vídeo en el búfer de fotogramas.                                                   |
| [**Poner**](put.md)             | [**MCI PUT**](mci-put.md)              | digitalvideo, overlay   | Define las ventanas de origen, destino y marco.                                               |
| [**darse cuenta de**](realize.md)     | [**MCI \_ REALIZE**](mci-realize.md)     | digitalvideo            | Indica al dispositivo que seleccione y se dé cuenta de su paleta en un contexto de dispositivo de la ventana mostrada. |
| [**setaudio**](setaudio.md)   | [**MCI \_ SETAUDIO**](mci-setaudio.md)  | digitalvideo            | Establece parámetros de audio para vídeo.                                                                  |
| [**setvideo**](setvideo.md)   | [**MCI \_ SETVIDEO**](mci-setvideo.md)  | digitalvideo            | Establece parámetros de vídeo.                                                                            |
| [**Señal**](signal.md)       | [**MCI \_ SIGNAL**](mci-signal.md)       | digitalvideo            | Identifica una posición especificada con una señal.                                                    |
| [**giro**](spin.md)           | [**MCI \_ SPIN**](mci-spin.md)           | Videodisco               | Inicia el disco girando o impide que el disco gira.                                         |
| [**Paso**](step.md)           | [**PASO \_ de MCI**](mci-step.md)           | digitalvideo, videodisc | Avanza o invierte la reproducción de uno o varios fotogramas.                                             |
| [**Descongelar**](unfreeze.md)   | [**MCI \_ UNFREEZE**](mci-unfreeze.md)   | overlay                 | Permite que el búfer de fotogramas adquiera datos de vídeo.                                                   |
| [**actualizar**](update.md)       | [**ACTUALIZACIÓN \_ de MCI**](mci-update.md)       | digitalvideo            | Vuelve a dibujar el marco actual en el contexto del dispositivo.                                               |
| [**where**](where.md)         | [**MCI WHERE**](mci-where.md)          | digitalvideo, overlay   | Obtiene el rectángulo que especifica el origen, el destino o el área de marco.                          |
| [**Ventana**](window.md)       | [**VENTANA \_ MCI**](mci-window.md)       | digitalvideo, overlay   | Controla la ventana de presentación.                                                                      |



 

 

 





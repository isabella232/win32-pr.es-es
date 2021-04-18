---
title: Grabando
description: Grabando
ms.assetid: 0026eb1d-5be1-4090-801b-f1c65c179f42
keywords:
- Comando MCI_RECORD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4248b2d4bbdd984ad23a772f0adca04581afca1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665589"
---
# <a name="recording"></a>Grabando

La especificación de MCI general admite la grabación con vídeo digital-video, secuenciador MIDI, grabadora de casete de vídeo (VCR) y dispositivos de audio de onda. sin embargo, solo los dispositivos de audio y VCR implementan actualmente funciones de grabación. Puede insertar o sobrescribir información grabada en un archivo o registro existente en un archivo nuevo. Para grabar en un archivo existente, abra un dispositivo de audio de forma de onda y un archivo tal como lo haría normalmente. Para grabar en un nuevo archivo, cuando se abre el dispositivo, especifique "nuevo" como nombre del dispositivo si usa la interfaz de cadena de comandos. Si usa la interfaz de mensaje de comando, especifique un nombre de archivo de longitud cero.

Cuando MCI crea un archivo nuevo para grabar, el formato de datos se establece en un formato predeterminado especificado por el controlador de dispositivo. Para usar un formato distinto del predeterminado, puede usar el comando [**set**](set.md) (Set de [**MCI \_**](mci-set.md)).

Para iniciar la grabación, use el comando [**grabar**](record.md) (o el [**\_ registro MCI**](mci-record.md) y la estructura [**\_ \_ parms del registro MCI**](mci-record-parms.md) ).

Si graba en modo de inserción en un archivo existente, puede usar las marcas "desde" (MCI \_ desde) y "hasta" (MCI \_ hasta) del comando **registro** para especificar las posiciones inicial y final de la grabación. Por ejemplo, si graba en un archivo de 20 segundos de duración y comienza a grabar en 5 segundos y finaliza la grabación en 10 segundos, el archivo resultante tendrá una longitud de 25 segundos. El archivo tendrá un segmento de 5 segundos insertado 5 segundos en la grabación original.

Si registra con el modo de sobrescritura en un archivo existente, puede usar las marcas "desde" y "para" para especificar las ubicaciones de inicio y finalización de la sección que se va a sobrescribir. Por ejemplo, si graba en un archivo de 20 segundos de duración y comienza a grabar en 5 segundos y finaliza la grabación a 10 segundos, todavía tiene una grabación de 20 segundos, pero se reemplazará la sección que empieza en 5 segundos hasta los 10 segundos.

Si no especifica una ubicación final, la grabación continúa hasta que se envía un comando [**Stop**](stop.md) ([**MCI \_ Stop**](mci-stop.md)) o hasta que el controlador se queda sin espacio libre en disco. Si graba en un archivo nuevo, puede omitir el marcador "de" o establecerlo en cero para iniciar la grabación al principio de un archivo nuevo. Puede especificar una ubicación de finalización para finalizar la grabación al grabar en un archivo nuevo.

A veces, el comando de [**registro**](record.md) tiene una precisión de solo 1 segundo de la ubicación inicial, como con dispositivos VCR. Para registrar con más precisión, debe usar el comando [**CUE**](cue.md) ([**la \_ pila MCI**](mci-cue.md)). Este comando es reconocido por dispositivos digitales, VCR y de audio de forma de onda. Para obtener más información acerca de la grabación con dispositivos VCR, consulte los [servicios de VCR](vcr-services.md).

## <a name="saving-a-recorded-file"></a>Guardar un archivo grabado

Una vez finalizada la grabación, use el comando [**Guardar**](save.md) (o [**MCI \_ Save**](mci-save.md) y [**MCI \_ Save \_ parms**](mci-save-parms.md) Structure) para guardar la grabación antes de cerrar el dispositivo.

> [!Note]  
> Si cierra el dispositivo sin guardar, se perderán los datos grabados.

 

## <a name="checking-input-levels-pcm-only"></a>Comprobar los niveles de entrada (sólo PCM)

Para obtener el nivel de la señal de entrada antes de grabarla en un dispositivo PCM (modulación por pulsos de código), use el comando [**status**](status.md) ([**MCI \_ status**](mci-status.md)). Especifique el indicador "nivel" (o la marca del elemento de estado de MCI \_ \_ y establezca el miembro **dwItem** de la estructura de [**Estado de MCI \_ \_ parms**](mci-status-parms.md) en el nivel de estado de onda de MCI \_ \_ \_ ). Se devuelve el nivel promedio de la señal de entrada. El valor del canal izquierdo está en la palabra de orden superior y el valor de la derecha o del canal mono está en la palabra de orden inferior.

El nivel de entrada se representa como un valor sin signo. En ejemplos de 8 bits, este valor se encuentra en el intervalo de 0 a 127 (0x7F). En los ejemplos de 16 bits, se encuentra en el intervalo de 0 a 32.767 (0x7FFF).

 

 





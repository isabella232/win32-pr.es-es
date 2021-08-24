---
title: Grabación
description: Grabación
ms.assetid: 0026eb1d-5be1-4090-801b-f1c65c179f42
keywords:
- MCI_RECORD comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27033dde148a6f99a1168eea4d6c0a97aea82881638ccb6d6f5535632e897148
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805515"
---
# <a name="recording"></a>Grabación

La especificación general de MCI admite la grabación con digital-video, secuenciador MIDI, grabadora de cámara de vídeo (VCR) y dispositivos de audio de forma de onda. sin embargo, actualmente solo los dispositivos de audio de forma de onda y VCR implementan funcionalidades de grabación. Puede insertar o sobrescribir la información registrada en un archivo o registro existente en un archivo nuevo. Para grabar en un archivo existente, abra un dispositivo y un archivo de audio de forma de onda como lo haría normalmente. Para grabar en un archivo nuevo, al abrir el dispositivo, especifique "new" como nombre del dispositivo si usa la interfaz de cadena de comandos. Si usa la interfaz de mensaje de comando, especifique un nombre de archivo de longitud cero.

Cuando MCI crea un nuevo archivo para la grabación, el formato de datos se establece en un formato predeterminado especificado por el controlador de dispositivo. Para usar un formato distinto del formato predeterminado, puede usar el [**comando set**](set.md) ([**MCI \_ SET**](mci-set.md)).

Para empezar a grabar, use el [**comando record**](record.md) (o [**MCI \_ RECORD**](mci-record.md) y la estructura [**\_ MCI RECORD \_ PARMS).**](mci-record-parms.md)

Si graba en modo de inserción en un archivo existente, puede usar las marcas "from" (MCI FROM) y \_ "to" (MCI TO) del comando de registro para especificar las posiciones inicial y final para la \_ grabación.  Por ejemplo, si graba en un archivo que tiene una duración de 20 segundos y comienza la grabación a 5 segundos y finaliza la grabación en 10 segundos, el archivo resultante tendrá una duración de 25 segundos. El archivo tendrá un segmento de 5 segundos insertado 5 segundos en la grabación original.

Si registra con el modo de sobrescritura en un archivo existente, puede usar las marcas "from" y "to" para especificar las ubicaciones inicial y final de la sección que se sobrescribe. Por ejemplo, si graba en un archivo con una duración de 20 segundos y empieza a grabar a 5 segundos y termina la grabación en 10 segundos, todavía tiene una grabación de 20 segundos, pero se habrá reemplazado la sección que comienza en 5 segundos y termina en 10 segundos.

Si no especifica una ubicación final, la grabación continúa hasta que se envía un comando [**stop**](stop.md) [**(MCI \_ STOP)**](mci-stop.md)o hasta que el controlador se queda sin espacio libre en disco. Si graba en un archivo nuevo, puede omitir la marca "from" o establecerla en cero para iniciar la grabación al principio de un nuevo archivo. Puede especificar una ubicación final para finalizar la grabación al grabar en un archivo nuevo.

A [**veces,**](record.md) el comando de registro es preciso en solo 1 segundo de la ubicación inicial, como con los dispositivos VCR. Para grabar con más precisión, debe usar el [**comando cue**](cue.md) ([**MCI \_ CUE**](mci-cue.md)). Este comando lo reconocen los dispositivos digital-video, VCR y de audio de forma de onda. Para obtener más información acerca de cómo grabar con dispositivos VCR, vea [VcR Services](vcr-services.md).

## <a name="saving-a-recorded-file"></a>Guardar un archivo grabado

Una vez completada la grabación, use el comando [**save**](save.md) (o [**MCI \_ SAVE**](mci-save.md) y la estructura [**MCI \_ SAVE \_ PARMS)**](mci-save-parms.md) para guardar la grabación antes de cerrar el dispositivo.

> [!Note]  
> Si cierra el dispositivo sin guardar, se perderán los datos registrados.

 

## <a name="checking-input-levels-pcm-only"></a>Comprobación de los niveles de entrada (solo PCM)

Para obtener el nivel de la señal de entrada antes de grabar en un dispositivo de entrada de audio de forma de onda PCM (pulse code Desaconstura), use el comando [**status**](status.md) ([**MCI \_ STATUS**](mci-status.md)). Especifique la marca "level" (o la marca MCI STATUS ITEM y establezca el miembro dwItem de la estructura \_ \_ [**MCI \_ STATUS \_ PARMS**](mci-status-parms.md) en MCI WAVE  \_ STATUS \_ \_ LEVEL). Se devuelve el nivel medio de señal de entrada. El valor del canal izquierdo está en la palabra de orden superior y el valor de canal único o derecho está en la palabra de orden inferior.

El nivel de entrada se representa como un valor sin signo. En el caso de las muestras de 8 bits, este valor está en el intervalo de 0 a 127 (0x7F). Para ejemplos de 16 bits, está en el intervalo de 0 a 32 767 (0x7FFF).

 

 





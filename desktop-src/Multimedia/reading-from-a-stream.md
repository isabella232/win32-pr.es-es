---
title: Leer de una secuencia
description: Leer de una secuencia
ms.assetid: be961f06-cf5f-4093-9b31-7d1d69e62fec
keywords:
- AVIStreamInfo función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cc7ecd606a33503557e7c7209bff68015756523
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995252"
---
# <a name="reading-from-a-stream"></a>Leer de una secuencia

Puede recuperar información sobre un flujo abierto mediante la función [**AVIStreamInfo**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) . Esta función rellena la estructura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) con información como el tipo de datos de la secuencia, el método de compresión que se usa al escribir datos de flujo, el tamaño de búfer sugerido, la velocidad de reproducción y una descripción de texto de la secuencia.

Algunos miembros de la estructura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) también están presentes en la estructura [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) . La información de la estructura **AVIFILEINFO** se aplica a todo el archivo. La información de la estructura **AVISTREAMINFO** es específica de la secuencia a la que se accede y tiene prioridad sobre la información de la estructura **AVIFILEINFO** .

Si una secuencia tiene asociada información complementaria, puede recuperar esta información mediante la función [**AVIStreamReadData**](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata) . Esta función devuelve la información en un búfer proporcionado por la aplicación. La información de la secuencia complementaria podría incluir la configuración de los métodos de compresión y descompresión usados en una secuencia. Puede obtener el tamaño de búfer necesario mediante la macro [**AVIStreamDataSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize) .

Puede recuperar información de formato sobre una secuencia mediante la función [**AVIStreamReadFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat) . Esta función devuelve una estructura específica de la secuencia en un búfer proporcionado por la aplicación. En el caso de una secuencia de vídeo, el búfer contiene información de formato en una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . En el caso de una secuencia de audio, el búfer contiene información de formato en una estructura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) o [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) . Para otros tipos de secuencias, el controlador de flujo devuelve información específica de la secuencia. Puede determinar el tamaño de búfer necesario usando **AVIStreamReadFormat** y especificando una dirección de búfer **null** o mediante la macro [**AVIStreamFormatSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize) .

Puede recuperar el contenido multimedia de una secuencia mediante la función [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) . Esta función copia los datos sin procesar de la secuencia en un búfer proporcionado por la aplicación. En el caso de las secuencias de vídeo, esta función recupera las imágenes de mapa Dete que componen el contenido del marco. En el caso de las secuencias de audio, esta función recupera muestras de audio de forma de onda que componen el contenido del sonido. Puede determinar el tamaño de búfer necesario usando **AVIStreamRead** y especificando una dirección de búfer **null** o mediante la macro [**AVIStreamSampleSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize) .

Algunos controladores de secuencias AVI presentan retrasos asociados con la inicialización o la inicialización de software y hardware. Puede informar a estos controladores para prepararse para el streaming de datos mediante la función [**AVIStreamBeginStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming) . Esta función permite al controlador de flujo asignar e inicializar los recursos que necesita. Para informar a estos controladores cuando ha finalizado el streaming, utilice la función [**AVIStreamEndStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming) . Esta función permite al controlador de secuencias desasignar los recursos asignados para **AVIStreamBeginStreaming**.

La función [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) no proporciona servicios de descompresión. Para obtener información sobre cómo comprimir y descomprimir secuencias de audio, consulte [Administrador de compresión de audio](audio-compression-manager.md). Para obtener información sobre cómo comprimir y descomprimir secuencias de vídeo, consulte [Administrador de compresión de vídeo](video-compression-manager.md). Para obtener información sobre cómo comprimir y descomprimir fotogramas individuales en una secuencia de vídeo, consulte [trabajar con datos de vídeo comprimidos en un flujo](working-with-compressed-video-data-in-a-stream.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Operaciones con secuencias](stream-operations.md)
</dt> </dl>

 

 
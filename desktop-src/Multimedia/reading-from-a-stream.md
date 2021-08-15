---
title: Lectura desde un flujo
description: Lectura desde un flujo
ms.assetid: be961f06-cf5f-4093-9b31-7d1d69e62fec
keywords:
- Función AVIStreamInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c56e1bd34fb9b0555c4eb0ed86944be3b7603645865144ac053604cd515cb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371656"
---
# <a name="reading-from-a-stream"></a>Lectura desde un flujo

Puede recuperar información sobre una secuencia abierta mediante la [**función AVIStreamInfo.**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) Esta función rellena la estructura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) con información como el tipo de datos de la secuencia, el método de compresión utilizado al escribir datos de flujo, el tamaño de búfer sugerido, la velocidad de reproducción y una descripción de texto de la secuencia.

Algunos miembros de la [**estructura AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) también están presentes en la [**estructura AVIFILEINFO.**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) La información de la **estructura AVIFILEINFO** se aplica a todo el archivo. La información de la **estructura AVISTREAMINFO** es específica de la secuencia a la que se accede y tiene prioridad sobre la información de la **estructura AVIFILEINFO.**

Si una secuencia tiene información adicional asociada, puede recuperar esta información mediante la [**función AVIStreamReadData.**](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata) Esta función devuelve la información en un búfer proporcionado por la aplicación. La información de flujo adicional puede incluir opciones de configuración para los métodos de compresión y descompresión que se usan en una secuencia. Puede obtener el tamaño de búfer necesario mediante la [**macro AVIStreamDataSize.**](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize)

Puede recuperar información de formato sobre una secuencia mediante la [**función AVIStreamReadFormat.**](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat) Esta función devuelve una estructura específica del flujo en un búfer proporcionado por la aplicación. Para una secuencia de vídeo, el búfer contiene información de formato en una [**estructura BITMAPINFO.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) En el caso de una secuencia de audio, el búfer contiene información de formato en una [**estructura DE FORMATEMA O**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) [**PCMWAVEFORMAT.**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) Para otros tipos de flujo, el controlador de flujo devuelve información específica de la secuencia. Puede determinar el tamaño de búfer necesario mediante **AVIStreamReadFormat** y especificando una dirección de búfer **NULL** o mediante la macro [**AVIStreamFormatSize.**](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize)

Puede recuperar el contenido multimedia de una secuencia mediante la [**función AVIStreamRead.**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) Esta función copia los datos sin procesar de la secuencia en un búfer proporcionado por la aplicación. En el caso de las secuencias de vídeo, esta función recupera las imágenes de mapa de bits que son el contenido del fotograma. En el caso de las secuencias de audio, esta función recupera muestras de audio de forma de onda que son el contenido del sonido. Puede determinar el tamaño de búfer necesario mediante **AVIStreamRead** y especificando una dirección de búfer **NULL** o mediante la macro [**AVIStreamSampleSize.**](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize)

Algunos controladores de flujo AVI presentan retrasos asociados con la inicialización o coordinación de software y hardware. Puede informar a estos controladores de que se preparen para el streaming de datos mediante la [**función AVIStreamBeginStreaming.**](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming) Esta función permite al controlador de flujo asignar e inicializar los recursos que necesita. Para informar a estos controladores cuando haya finalizado el streaming, use la [**función AVIStreamEndStreaming.**](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming) Esta función permite que el controlador de secuencias desasigne los recursos que asignó **para AVIStreamBeginStreaming.**

La [**función AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) no proporciona servicios de descompresión. Para obtener información sobre cómo comprimir y descomprimir secuencias de audio, vea [Administrador de compresión de audio](audio-compression-manager.md). Para obtener información sobre cómo comprimir y descomprimir secuencias de vídeo, vea [Administrador de compresión de vídeo](video-compression-manager.md). Para obtener información sobre cómo comprimir y descomprimir fotogramas individuales en una secuencia de vídeo, vea Trabajar con datos [de vídeo comprimidos en una secuencia.](working-with-compressed-video-data-in-a-stream.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Operaciones con secuencias](stream-operations.md)
</dt> </dl>

 

 
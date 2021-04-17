---
title: Procesamiento de los datos de audio
description: Procesamiento de los datos de audio
ms.assetid: ba41e3f4-d991-4da6-9091-7a7e42622e76
keywords:
- Complementos de Media Player de Windows, método echo de ejemplo DoProcessOutput
- complementos, método echo de ejemplo DoProcessOutput
- Complementos de procesamiento de señal digital, ejemplo echo método DoProcessOutput
- Complementos DSP, método echo de ejemplo DoProcessOutput
- Ejemplo de complemento DSP de eco, método DoProcessOutput
- Ejemplo de complemento DSP de eco, datos de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc14acb99aed20825ff970025363c6a795a0c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704723"
---
# <a name="processing-the-audio-data"></a>Procesamiento de los datos de audio

La implementación predeterminada de **DoProcessOutput** comienza mediante la recuperación de un puntero a una estructura **WAVEFORMATEX** válida, tal como se hizo en **AllocateStreamingResources**. A continuación, usa la información de esa estructura para calcular el número de muestras en el búfer de entrada en espera de ser procesadas. El código siguiente procede de la implementación predeterminada:


```C++
// Get a pointer to the valid WAVEFORMATEX structure
// for the current media type.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;

// Calculate the number of samples to process.
DWORD dwSamplesToProcess = (*cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;

```



A continuación, el código inspecciona el miembro **wBitsPerSample** para determinar la profundidad de bits del audio. Este valor se usa en una instrucción switch para proporcionar procesamiento independiente para audio de 8 y 16 bits.

## <a name="differences-between-8-bit-and-16-bit-audio"></a>Diferencias entre audio de 8 y 16 bits

Hay diferencias importantes entre el audio de 8 y 16 bits. Por lo tanto, las rutinas de procesamiento para crear el efecto de eco son diferentes. Los dos formatos se diferencian de las siguientes maneras:

-   Cada formato tiene un tamaño de muestra diferente: los ejemplos de 8 bits ocupan un byte de memoria, mientras que los ejemplos de 16 bits ocupan dos bytes.
-   Cada formato representa la amplitud de audio de forma diferente. el audio de 8 bits se representa mediante un entero sin signo con un intervalo de 0 a 255; un valor de 128 representa el silencio. el audio de 16 bits se representa mediante un entero con signo con un intervalo de-32768 a 32767; un valor de cero representa el silencio.

Aunque el proceso de creación del efecto de eco es fundamentalmente idéntico para cada formato, los detalles deben diferir ligeramente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 





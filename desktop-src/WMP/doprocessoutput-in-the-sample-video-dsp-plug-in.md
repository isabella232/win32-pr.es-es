---
title: DoProcessOutput en el complemento DSP de vídeo de ejemplo
description: DoProcessOutput en el complemento DSP de vídeo de ejemplo
ms.assetid: 67536e35-a049-49c8-bd89-fad1fab37e6c
keywords:
- Reproductor de Windows Media complementos, DSP de vídeo
- complementos, DSP de vídeo
- complementos de procesamiento de señales digitales, DoProcessOutput
- Complementos de DSP, DoProcessOutput
- complementos de DSP de vídeo, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b031ecddc4f7a1e4a83d4f8a7d8db3b975957789d7f887bf8b12438407624205
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680605"
---
# <a name="doprocessoutput-in-the-sample-video-dsp-plug-in"></a>DoProcessOutput en el complemento DSP de vídeo de ejemplo

Dado que un complemento DSP de vídeo normalmente admite varios formatos de vídeo, es conveniente separar el código de implementación de procesamiento en una función independiente para cada formato. Esto significa que la implementación de **DoProcessOutput para** complementos DSP de vídeo es relativamente sencilla.

La implementación en el complemento de ejemplo comprueba primero si el usuario ha habilitado el complemento. Si el complemento está deshabilitado, el código copia los datos proporcionados en el búfer de entrada en el búfer de salida sin cambiarlo, como se muestra en el código siguiente:


```C++
// Test whether the plug-in has been disabled by the user.
if (!m_bEnabled)
{
    // Just copy the data without changing it. You should
    // also do any necessary format conversion here.
    memcpy(pbOutputData, pbInputData, m_dwBufferSize);
    *cbBytesProcessed = m_dwBufferSize;

    return S_OK;
}

```



Si el complemento está habilitado, el código simplemente realiza una serie de comprobaciones en el **miembro de subtipo** de tipo de medio de entrada para determinar el formato de vídeo actual. Cuando se encuentra una coincidencia, el código llama a la función de procesamiento adecuada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de un complemento DSP de vídeo**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 





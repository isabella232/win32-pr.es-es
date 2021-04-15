---
title: DoProcessOutput en el complemento DSP de vídeo de ejemplo
description: DoProcessOutput en el complemento DSP de vídeo de ejemplo
ms.assetid: 67536e35-a049-49c8-bd89-fad1fab37e6c
keywords:
- Complementos de Windows Media Player, DSP de vídeo
- complementos, DSP de vídeo
- Complementos de procesamiento de señal digital, DoProcessOutput
- Complementos DSP, DoProcessOutput
- Complementos de DSP de vídeo, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3bc844890930209a1c6007213d3c466f0cd15b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695248"
---
# <a name="doprocessoutput-in-the-sample-video-dsp-plug-in"></a>DoProcessOutput en el complemento DSP de vídeo de ejemplo

Dado que un complemento de DSP de vídeo suele admitir varios formatos de vídeo, es conveniente separar el código de implementación de procesamiento en una función independiente para cada formato. Esto significa que la implementación de **DoProcessOutput** para complementos de DSP de vídeo es relativamente sencilla.

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



Si el complemento está habilitado, el código simplemente realiza una serie de comprobaciones en el miembro de **subtipo** de tipo de medio de entrada para determinar el formato de vídeo actual. Cuando se encuentra una coincidencia, el código llama a la función de procesamiento adecuada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de un complemento DSP de vídeo**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 





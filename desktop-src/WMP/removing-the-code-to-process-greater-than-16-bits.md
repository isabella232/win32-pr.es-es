---
title: Quitar el código para procesar más de 16 bits
description: Quitar el código para procesar más de 16 bits
ms.assetid: 90c165e1-bc77-42a5-878d-056762c62991
keywords:
- Reproductor de Windows Media complementos, método DoProcessOutput de ejemplo de Eco
- plug-ins,Echo sample DoProcessOutput (método DoProcessOutput de ejemplo de eco)
- complementos de procesamiento de señales digitales, método DoProcessOutput de ejemplo de eco
- Complementos DE DSP, método DoProcessOutput de ejemplo de eco
- Ejemplo de complemento DSP de eco, método DoProcessOutput
- Ejemplo de complemento DSP de eco, procesamiento superior a 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac539488b505ed345af1cd998fe6a4142ba31c706d09ea48760b65335e8726b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934005"
---
# <a name="removing-the-code-to-process-greater-than-16-bits"></a>Quitar el código para procesar más de 16 bits

Dado que este ejemplo solo procesa audio de 8 o 16 bits, debe modificar el código en **CEcho::ValidateMediaType** para devolver DMO E TYPE NOT ACCEPTED para tipos de medios mayores de \_ \_ \_ \_ 16 bits. Para ello, debe cambiar el código del bloque de modificadores que prueba formatos de tipo WAVE \_ FORMAT \_ EXTENSIBLE. Reemplace el código del asistente por el código de ejemplo siguiente:


```C++
case WAVE_FORMAT_EXTENSIBLE:
    {
         // Sample size is greater than 16-bit or is multichannel.
        WAVEFORMATEXTENSIBLE *pWaveXT = (WAVEFORMATEXTENSIBLE *) pWave;

        if (KSDATAFORMAT_SUBTYPE_PCM != pWaveXT->SubFormat)
        {
            return DMO_E_TYPE_NOT_ACCEPTED;
        }
    }
    break;

```



A continuación, elimine o comente las secciones de código de **DoProcessOutput** que controlan el audio de alta resolución de bits. Estas son las secciones que comienzan por el caso 24 y el caso 32.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 





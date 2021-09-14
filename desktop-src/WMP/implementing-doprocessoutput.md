---
title: Implementación de DoProcessOutput
description: Implementación de DoProcessOutput
ms.assetid: c6fbcfc0-741b-4aa7-9109-e06810a2e081
keywords:
- Reproductor de Windows Media complementos,DSP de audio
- complementos, DSP de audio
- complementos de procesamiento de señal digital,DoProcessOutput
- Complementos de DSP,DoProcessOutput
- complementos DSP de audio,DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68562444a3a8f0bfacad26fc5246181d33cefa2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160584"
---
# <a name="implementing-doprocessoutput"></a>Implementación de DoProcessOutput

Para procesar datos de audio, deberá realizar varios pasos en **DoProcessOutput**. En los pasos siguientes se usa el código de ejemplo del asistente para complementos como ejemplos. Si desea crear un complemento DSP de audio que procese el contenido multimedia del mismo tipo que el código de ejemplo del asistente para complementos, solo tendrá que cambiar el código de procesamiento real al que se hace referencia en el paso 6. A continuación se indican todos los pasos implementados **en DoProcessOutput**:

-   Si el complemento no está habilitado actualmente, simplemente copie los datos sin modificar en el búfer de salida. Si el complemento convierte los datos en un formato diferente, también debe realizar el procesamiento de conversión aquí.

    ```C++
    // Test whether the plug-in is disabled by the user.
    if (!m_bEnabled)
    {
        // Just copy the data without changing it.
        memcpy(pbOutputData, m_pbInputData, *cbBytesProcessed);

        return S_OK;
    }
    
    ```

    

    -   Recupera un puntero a la estructura de formato de entrada. Deberá recuperar datos de miembro de esta estructura, así que copie el puntero de *m \_ mtInput*.**pbformat** a una variable de puntero local de un tipo que coincide con el tipo de estructura de formato. En el ejemplo siguiente se almacena un puntero a una estructura de formato de **entrada DESATEX:**

    ```C++
    WAVEFORMATEX *pWave = (WAVEFORMATEX*) m_mtInput.pbFormat;
    
    ```

    

    -   Calcule el número de muestras que se procesarán. El código de ejemplo que genera el asistente para complementos realiza este paso dividiendo el número de bytes que se procesarán por el miembro **nBlockAlign** de la estructura de formato de entrada DESATEX y, a continuación, multiplicando el resultado por el número de canales, que se almacenaron en el **miembro nChannels.** El ejemplo siguiente es del código de ejemplo del asistente para complementos:

    ```C++
    DWORD dwSamplesToProcess = (cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;
    
    ```

    

    1.  Determine la profundidad de bits del audio. El código de ejemplo del asistente para complementos determina el audio de 8 o 16 bits inspeccionando el miembro **wBitsPerSample** de la estructura **DESVASEATEX.** A continuación, usa ese valor en una instrucción switch para proporcionar rutinas de procesamiento independientes para cada profundidad de bits. Es posible que tenga que usar una técnica diferente al tratar con otros tipos de formato y profundidades de bits.
    2.  Cree un bucle para recorrer los ejemplos de audio en el búfer de entrada.
    3.  Recuperar un ejemplo del búfer de entrada. Para ello, desreferencia el puntero de datos de entrada y almacena el resultado en una variable de tipo int. Para el audio de 16 bits, debe volver a convertir el puntero BYTE a un puntero corto para controlar la mayor precisión de la muestra de audio. Una vez que tenga el valor , puede incrementar inmediatamente el puntero *pbInputData* para que apunta al ejemplo siguiente. En los ejemplos siguientes se muestra esto:

    ```C++
    // For 8-bit audio.
    int i = *pbInputData++;  
    
    ```

    

    O bien

    ```C++
    // For 16-bit audio.
    // Recast the pointer.
    short *pwInputData = (short *) pbInputData; 

    // Enter the loop and then get the input sample.
    int i = *pwInputData++;
    
    ```

    

    1.  Realice el procesamiento. Aquí es donde se aplican los algoritmos que cambian el ejemplo de algún modo. Lo que haga aquí es su parte.
    2.  Escriba los datos procesados en el búfer de salida. Incremente inmediatamente el puntero al búfer de salida, como en el ejemplo siguiente:

    ```C++
    *pwOutputData++ = i;
    
    ```

    

    1.  Repita el bucle hasta que se hayan procesado todas las muestras.
    2.  Devuelve un **HRESULT adecuado.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de un complemento dsp de audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 





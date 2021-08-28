---
description: Adaptive Differential Pulse Code Compression (ADPCM) es un formato de compresión con pérdida que se implementa para XAudio2 para proporcionar características adicionales para especificar el tamaño del bloque de ejemplo de compresión.
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: Información general de ADPCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1be1155d6d9f5a542b605c497ce28aa34191c0ac129582c18ec4a47b9f510f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962724"
---
# <a name="adpcm-overview"></a>Información general de ADPCM

Adaptive Differential Pulse Code Compression (ADPCM) es un formato de compresión con pérdida que se implementa para XAudio2 para proporcionar características adicionales para especificar el tamaño del bloque de ejemplo de compresión. Con un formato de compresión con pérdida, algunos datos se modifican y se pierden durante la compresión. ADPCM puede lograr relaciones de compresión de hasta 4:1.

La implementación de ADPCM para XAudio2 proporciona características adicionales para especificar el tamaño del bloque de ejemplo de compresión. ADPCM permite al diseñador de audio elegir una configuración que sea un riesgo adecuado entre el tamaño, la calidad y la resolución (para colocar puntos de bucle).

XAudio2 usa una versión modificada del códec Microsoft ADPCM que admite el formato de datos extendido necesario para proporcionar tamaños de bloque de ejemplo personalizados. Por este motivo, los motores de audio que no admiten esta versión del códec ADPCM no pueden reproducir datos de audio XAudio2.

> [!Note]  
> Actualmente, la compresión ADPCM solo está disponible para Windows, incluido XNA Game Studio Express para Windows implementaciones.

 

## <a name="adpcm-encoding"></a>Codificación de ADPCM

Los datos de audio se codifican en ADPCM mediante la herramienta de línea de comandos AdpcmEncode.

-   AdpcmEncode

    Para codificar archivos de audio como ADPCM para su uso con XAudio2, use la herramienta de línea de comandos **AdpcmEncode.**

## <a name="adpcm-decoding"></a>ADPCM Decoding

La decodificación de software de ADPCM se admite en XAudio2.

-   XAudio2

    Para usar datos codificados por ADPCM en XAudio2, debe inicializar una estructura **ADPCMWAVEFORMAT** con valores específicos de ADPCM y pasarla como argumento a [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) al crear una voz de origen. Para obtener un ejemplo de carga y reproducción de un sonido en XAudio2, vea [Cómo: Reproducir un sonido con XAudio2.](how-to--play-a-sound-with-xaudio2.md)

## <a name="samplesperblock"></a>SamplesPerBlock

La compresión ADPCM funciona mediante la separación de la forma de onda en bloques y la predicción de la variación de las muestras de forma de onda dentro de cada bloque. El tamaño de los bloques se mide en muestras. El tamaño de bloque más pequeño es de 32 muestras y el más alto es de 512 muestras.

Los bloques más grandes permiten una mejor compresión, lo que da como resultado tamaños de archivo más pequeños, pero a costa de la calidad del sonido y la resolución para alinear los puntos de bucle.

En general, la modificación del valor SamplesPerBlock da como resultado estos resultados:



| If SamplesPerBlock...      | Compresión de archivos | Calidad de sonido | Resolución de puntos de bucle |
|----------------------------|------------------|---------------|-----------------------|
| Aumentos (hasta un máximo de 512)  | Aumenta        | Disminuye     | Disminuye             |
| Disminuciones (hasta un mínimo de 32) | Disminuye        | Aumenta     | Aumenta             |



 

## <a name="restrictions"></a>Restricciones

Dado que ADPCM usa bloques de ejemplo alineados uno tras otro, una onda comprimida con ADPCM puede tener un bloque parcial sin terminar al final. El descodificador de ADPCM genera silencio para el resto de este bloque parcial, lo que evita que la onda se reenvía sin problemas.

El valor del parámetro *SamplesPerBlock* afecta a la resolución con la que puede alinear los datos de onda y los puntos de bucle.

Si intenta aplicar la compresión a una onda no alineada, recibirá un error o una advertencia en función de si la onda se usa en cualquier evento de reproducción en bucle. No se puede comprimir una ola usada en los eventos de reproducción en bucle. Quítelo de los eventos de reproducción en bucle y vuelva a aplicar la compresión.

Si usa la onda exclusivamente en modo sin bucle, no se aplica la restricción de alineación de bloques de ejemplo.

## <a name="adpcm-file-structure"></a>Estructura de archivos ADPCM

Un archivo ADPCM es un archivo RIFF estándar con los siguientes tipos de fragmento.



| FCC de fragmentos     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RIFF          | Fragmento RIFF estándar que contiene un tipo de archivo con el valor WAVE en los primeros cuatro bytes de su sección de datos y los otros fragmentos del archivo en el resto de su sección de datos.                                                                                                                                                                                                                                                                 |
| Fmt           | Contiene el encabezado de formato para el archivo ADPCM. Los datos de este fragmento corresponden a una **estructura ADPCMWAVEFORMAT.**                                                                                                                                                                                                                                                                                                                             |
| datos          | Contiene los datos de audio de ADPCM codificados. Cuando se usa ADPCM en XAudio2, es necesario leer el contenido del fragmento de datos en un búfer y pasarlo a una voz de origen como miembro **pAudioData** de una estructura [**\_ BUFFER de XAUDIO2.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) No es necesario intercambiar en bytes el contenido del fragmento de datos.                                                                                                                            |
| smpl y wsmp | Tipos de fragmento opcionales que contienen la información de bucle para el archivo ADPCM. Cuando se usa ADPCM en XAudio2, los valores contenidos en los fragmentos smpl o wsmp se usan para rellenar los miembros **LoopBeginLoopLength** y **LoopCount** de la estructura BUFFER de [**XAUDIO2. \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) En la Xbox 360, debe intercambiar en bytes los datos cargados desde un fragmento de smpl para tener en cuenta la diferencia de endianidad entre Windows y Xbox 360. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 

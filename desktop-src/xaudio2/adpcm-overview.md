---
description: Adaptive Differential Pulse Code Modulation (ADPCM) es un formato de compresión con pérdida que se implementa para XAudio2 con el fin de proporcionar características adicionales para especificar el tamaño del bloque de ejemplo de compresión.
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: Información general de ADPCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb918a611cb0840b2f02dfb13b547b795fb3304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716385"
---
# <a name="adpcm-overview"></a>Información general de ADPCM

Adaptive Differential Pulse Code Modulation (ADPCM) es un formato de compresión con pérdida que se implementa para XAudio2 con el fin de proporcionar características adicionales para especificar el tamaño del bloque de ejemplo de compresión. Con un formato de compresión con pérdida, algunos datos se modifican y se pierden durante la compresión. ADPCM puede lograr relaciones de compresión de hasta 4:1.

La implementación de ADPCM para XAudio2 proporciona características adicionales para especificar el tamaño del bloque de ejemplo de compresión. ADPCM permite al diseñador de audio elegir una configuración que es un compromiso adecuado entre el tamaño, la calidad y la resolución (para colocar puntos de bucle).

XAudio2 usa una versión modificada del códec Microsoft ADPCM que admite el formato de datos extendidos necesario para proporcionar tamaños de bloque de ejemplo personalizados. Por esta razón, los motores de audio que no admiten esta versión del códec ADPCM no pueden reproducir los datos de audio de XAudio2.

> [!Note]  
> Actualmente, la compresión ADPCM solo está disponible para Windows, incluidas las implementaciones de XNA Game Studio Express para Windows.

 

## <a name="adpcm-encoding"></a>Codificación ADPCM

Los datos de audio se codifican en ADPCM mediante la herramienta de línea de comandos AdpcmEncode.

-   AdpcmEncode

    Para codificar archivos de audio como ADPCM para su uso con XAudio2, use la herramienta de línea de comandos **AdpcmEncode** .

## <a name="adpcm-decoding"></a>Descodificación ADPCM

La descodificación de software de ADPCM es compatible con XAudio2.

-   XAudio2

    Para usar datos codificados ADPCM en XAudio2, debe inicializar una estructura **ADPCMWAVEFORMAT** con valores específicos de ADPCM y pasarla como argumento a [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) cuando cree una voz de origen. Para obtener un ejemplo de carga y reproducción de un sonido en XAudio2, consulte [Cómo: reproducir un sonido con xaudio2](how-to--play-a-sound-with-xaudio2.md).

## <a name="samplesperblock"></a>SamplesPerBlock

La compresión ADPCM funciona mediante la separación de la forma de onda en bloques y la predicción de la variación de los ejemplos de la forma de onda en cada bloque. El tamaño de los bloques se mide en ejemplos. El tamaño de bloque más pequeño es 32 ejemplos y el más alto es 512 ejemplos.

Los bloques más grandes permiten una mejor compresión, lo que da lugar a tamaños de archivo más pequeños, pero a costa de una calidad y resolución de sonido para alinear puntos de bucle.

En general, la modificación del valor de SamplesPerBlock produce estos inconvenientes:



| Si SamplesPerBlock...      | Compresión de archivos | Calidad del sonido | Resolución del punto de bucle |
|----------------------------|------------------|---------------|-----------------------|
| Aumenta (hasta el máximo 512)  | Medida        | DISMINUI     | DISMINUI             |
| Disminuye (baja a min 32) | DISMINUI        | Medida     | Medida             |



 

## <a name="restrictions"></a>Restricciones

Dado que ADPCM usa bloques de ejemplo que se alinean uno tras otro, una onda comprimida con ADPCM puede tener un bloque parcial sin terminar en su extremo. El descodificador ADPCM genera un silencio para el resto de este bloque parcial, lo que evita que la onda se repita sin problemas.

El valor del parámetro *SamplesPerBlock* afecta a la resolución con la que se pueden alinear los datos de onda y los puntos de bucle.

Si intenta aplicar la compresión a una onda no alineada, obtendrá un error o una advertencia dependiendo de si se usa la onda en cualquier evento de reproducción de bucle. No se puede comprimir una onda utilizada en ningún evento de reproducción de bucle. Quítelo de los eventos de reproducción en bucle y vuelva a aplicar la compresión.

Si usa la ola exclusivamente en el modo sin bucles, la restricción de alineación de bloque de ejemplo no se aplica.

## <a name="adpcm-file-structure"></a>Estructura de archivos ADPCM

Un archivo ADPCM es un archivo RIFF estándar con los siguientes tipos de fragmentos.



| Fragmento FCC     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RIFF          | Fragmento RIFF estándar que contiene un tipo de archivo con el valor WAVE en los primeros cuatro bytes de su sección de datos y los demás fragmentos del archivo en el resto de la sección de datos.                                                                                                                                                                                                                                                                 |
| FMT           | Contiene el encabezado de formato del archivo ADPCM. Los datos de este fragmento se corresponden con una estructura **ADPCMWAVEFORMAT** .                                                                                                                                                                                                                                                                                                                             |
| datos          | Contiene los datos de audio ADPCM codificados. Al usar ADPCM en XAudio2, debe leer el contenido del fragmento de datos en un búfer y pasarlo a una voz de origen como el miembro **pAudioData** de una estructura de [**\_ búfer de XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . No es necesario intercambiar bytes en el contenido del fragmento de datos.                                                                                                                            |
| smpl y wsmp | Tipos de fragmentos opcionales que contienen la información de bucle del archivo ADPCM. Al usar ADPCM en XAudio2, los valores contenidos en los fragmentos de Smpl o wsmp se usan para rellenar los miembros **LoopBeginLoopLength** y **LoopCount** de la estructura de [**\_ búfer de XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . En la consola Xbox 360, debe intercambiar bytes de los datos cargados desde un fragmento smpl para tener en cuenta la diferencia modos endian entre Windows y Xbox 360. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 

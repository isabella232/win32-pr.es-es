---
description: Las voces de XAudio2 pueden realizar conversiones automáticas de velocidad de muestra si la velocidad de muestra de entrada es diferente de la velocidad de muestra de entrada de sus voces de salida.
ms.assetid: be34ce62-6552-45e2-a247-830ab55ea9ec
title: Conversiones de velocidad de muestra de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d437a45f9e896826bedc1418382fb257201722d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279358"
---
# <a name="xaudio2-sample-rate-conversions"></a>Conversiones de velocidad de muestra de XAudio2

Las voces de XAudio2 pueden realizar conversiones automáticas de velocidad de muestra si la velocidad de muestra de entrada es diferente de la velocidad de muestra de entrada de sus voces de salida.

Las conversiones de velocidad de muestra siguen estas reglas:

-   La velocidad de muestra de entrada de voz es fija.

    Las voces solo pueden controlar la velocidad de muestra de entrada especificada cuando se crearon. En [**el caso de**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) voces y [**voces de submezcla**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice), se especifica la velocidad de muestra de entrada con el argumento *InputSampleRate* para las funciones [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) y [**IXAudio2:: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice) . En el caso de las voces de origen, la velocidad de muestra de entrada de la voz se especifica mediante el argumento pSourceFormat para la función [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) .

-   Todas las voces de salida de una voz deben tener la misma velocidad de muestra de entrada.

    Las voces pueden convertir la velocidad de muestra de entrada a cualquier velocidad de muestra de salida, pero todas las voces de salida de la voz deben tener la misma velocidad de muestra de entrada. Por ejemplo, una voz puede generar una salida a cualquier número de voces con una velocidad de muestra de entrada de 22 kHz. Sin embargo, si esa misma voz tuviera varias voces de salida, cada una de las cuales tenía una velocidad de muestra de entrada diferente, el gráfico de audio no sería válido.

-   El procesamiento de la conversión de velocidad de muestra solo se produce cuando es necesario.

    La conversión de datos de audio a una velocidad de muestra diferente supone más sobrecarga de procesamiento, lo que es preferible evitar. Si la velocidad de muestra de entrada de una voz coincide con la velocidad de muestra de entrada de sus voces de salida, esta conversión no se realiza y se acorta el tiempo de procesamiento.

-   La velocidad de muestra de salida puede variar a lo largo de la vida de una voz.

    La velocidad de muestra de salida de una voz no es fija. Siempre y cuando todas sus voces de salida tengan la misma velocidad de muestra de entrada, el gráfico de audio será válido. Si se cambia una voz para que se genere en nuevas voces con una velocidad de muestra de entrada diferente, la voz se convertirá a la velocidad de muestra de entrada de las nuevas voces.

Hay algunos escenarios en los que es necesario agregar una voz de submezcla para realizar la conversión de velocidad de muestra entre las voces. Si una voz necesita enviarse a voces con varias velocidades de muestra de entrada, solo una de las voces puede ser una salida directa de la voz original. Dado que todas las voces de salida de una voz deben tener la misma velocidad de muestra de entrada, las demás voces reciben la salida indirectamente. Debe haber una voz de submezcla con la velocidad de muestra de entrada correcta que viene entre la voz original y la de salida deseada.

Por ejemplo, imagine una voz de origen con una velocidad de muestra de entrada de 22 kHz, que debe generarse en una voz de submezcla con una velocidad de muestra de entrada de 11 kHz y una voz de maestro con una velocidad de muestra de entrada de 44,1 kHz. Dado que las dos voces de salida tienen velocidades de muestra de entrada diferentes, debe insertar más voces de submezcla entre la voz original y sus voces de salida prepensadas. Para mantener la fidelidad de la voz de origen y evitar conversiones costosas innecesarias a velocidades de muestreo más altas, debe insertar en el gráfico dos voces de mezcla con una velocidad de entrada de ejemplo de 22 kHz. Una voz de submezcla tendría una salida de 11 kHz a la voz de la submezcla con el efecto de reverberación, y la otra voz de submezcla se enviaría a la voz de masterización en 44,1 kHz.

## <a name="examples-of-sample-rate-conversion-in-audio-graphs"></a>Ejemplos de conversión de velocidad de ejemplo en gráficos de audio

Todas las voces tienen la misma velocidad de entrada de ejemplo; no se realiza ninguna conversión de velocidad de muestra en el gráfico de audio.![no se realiza ninguna conversión de velocidad de muestra en el gráfico de audio.](images/xaudio2-sample-rate-conversions-1.png)

Todas las voces tienen la misma velocidad de entrada de ejemplo excepto la voz de mastering; la conversión de la frecuencia de muestreo solo se realiza en los datos que van a la voz de la maestra. ![la conversión de la frecuencia de muestreo solo se realiza en los datos que van a la voz de la maestra.](images/xaudio2-sample-rate-conversions-2.png)

Las voces tienen tasas de entrada de ejemplo diferentes y requieren más voces de submezcla para realizar conversiones de velocidad de muestra. la conversión de la frecuencia de muestreo se realiza en varios lugares del gráfico de audio. ![la conversión de la frecuencia de muestreo se realiza en varios lugares del gráfico de audio.](images/xaudio2-sample-rate-conversions-3.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Voces](voices.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> </dl>

 

 

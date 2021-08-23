---
description: Las voces XAudio2 pueden realizar conversiones automáticas de frecuencia de muestreo si su frecuencia de muestreo de entrada es diferente de la frecuencia de muestreo de entrada de sus voces de salida.
ms.assetid: be34ce62-6552-45e2-a247-830ab55ea9ec
title: Conversiones de frecuencia de muestreo de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82983d1d9307551e516f1b8b60676b4b250450da65f416c340446c5a906f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962539"
---
# <a name="xaudio2-sample-rate-conversions"></a>Conversiones de frecuencia de muestreo de XAudio2

Las voces XAudio2 pueden realizar conversiones automáticas de frecuencia de muestreo si su frecuencia de muestreo de entrada es diferente de la frecuencia de muestreo de entrada de sus voces de salida.

Las conversiones de frecuencia de ejemplo siguen estas reglas:

-   La frecuencia de muestreo de entrada de voz es fija.

    Las voces solo pueden controlar la frecuencia de muestreo de entrada especificada cuando se crearon. Para las voces [**maestras**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) y las [**voces de submezcla,**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)la frecuencia de muestreo de entrada se especifica con el argumento *InputSampleRate* para las funciones [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) e [**IXAudio2::CreateSubmixVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice) Para las voces de origen, el argumento pSourceFormat especifica la frecuencia de muestreo de entrada de la voz para la [**función IXAudio2::CreateSourceVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)

-   Todas las voces de salida de una voz deben tener la misma frecuencia de muestreo de entrada.

    Las voces pueden convertir de su velocidad de muestreo de entrada a cualquier velocidad de muestreo de salida, pero todas las voces de salida de la voz deben tener la misma velocidad de muestreo de entrada. Por ejemplo, una voz podría generar cualquier número de voces con una frecuencia de muestreo de entrada de 22 kHz. Sin embargo, si esa misma voz tuviera varias voces de salida, cada una de las cuales tenía una frecuencia de muestreo de entrada diferente, el gráfico de audio no sería válido.

-   El procesamiento de conversión de frecuencia de muestreo solo se produce cuando es necesario.

    La conversión de datos de audio a una frecuencia de muestreo diferente conlleva una mayor sobrecarga de procesamiento, que es preferible evitar. Si la frecuencia de muestreo de entrada de una voz coincide con la velocidad de muestreo de entrada de sus voces de salida, esta conversión no se realiza y se reduce el tiempo de procesamiento.

-   La frecuencia de muestreo de salida puede variar a lo largo de la vida de una voz.

    La frecuencia de muestreo de salida de una voz no es fija. Siempre que todas sus voces de salida tengan la misma frecuencia de muestreo de entrada, el gráfico de audio será válido. Si se cambia una voz para que se muestre a nuevas voces con una velocidad de muestreo de entrada diferente, la voz se convertirá a la velocidad de muestreo de entrada de las nuevas voces.

Hay algunos escenarios en los que es necesario agregar una voz de submezcla para realizar la conversión de frecuencia de muestreo entre voces. Si una voz necesita generarse en voces con varias velocidades de muestreo de entrada, solo una de las voces puede ser una salida directa de la voz original. Dado que todas las voces de salida de una voz deben tener la misma velocidad de muestreo de entrada, las demás voces reciben la salida indirectamente. Debe haber una submezcla de voz con la velocidad de muestreo de entrada correcta que se encuentra entre la voz original y la voz de salida deseada.

Por ejemplo, considere una voz de origen con una velocidad de muestreo de entrada de 22 kHz, que debe generar una voz de submezcla con una velocidad de muestreo de entrada de 11 kHz y una voz maestra con una velocidad de muestreo de entrada de 44,1 kHz. Dado que las dos voces de salida tienen velocidades de muestreo de entrada diferentes, debe insertar más voces de submezcla entre la voz original y sus voces de salida previstas. Para mantener la fidelidad de la voz de origen y evitar conversiones costosas innecesarias a velocidades de muestreo más altas, debe insertar dos voces de submezcla con velocidades de entrada de muestra de 22 khz en el gráfico. Una voz de submezcla generaría una salida a 11 khz a la voz de submezcla con el efecto de reverberación y la otra voz de submezcla generaría a la voz maestra a 44,1 khz.

## <a name="examples-of-sample-rate-conversion-in-audio-graphs"></a>Ejemplos de conversión de frecuencia de muestreo en gráficos de audio

Todas las voces tienen la misma velocidad de entrada de ejemplo; no se realiza ninguna conversión de frecuencia de muestreo en el gráfico de audio.![no se realiza ninguna conversión de frecuencia de muestreo en el gráfico de audio.](images/xaudio2-sample-rate-conversions-1.png)

Todas las voces tienen la misma velocidad de entrada de ejemplo, excepto la voz maestra. La conversión de frecuencia de muestreo solo se realiza en los datos que van a la voz maestra. ![La conversión de frecuencia de muestreo solo se realiza en los datos que van a la voz maestra.](images/xaudio2-sample-rate-conversions-2.png)

Las voces tienen diferentes velocidades de entrada de ejemplo y requieren más voces de submezclación para realizar conversiones de frecuencia de muestreo. La conversión de frecuencia de muestreo se realiza en varios lugares del gráfico de audio. ![La conversión de frecuencia de muestreo se realiza en varios lugares del gráfico de audio.](images/xaudio2-sample-rate-conversions-3.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Voces](voices.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> </dl>

 

 

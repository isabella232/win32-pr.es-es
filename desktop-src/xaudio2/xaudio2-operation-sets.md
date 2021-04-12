---
description: En esta información general se presentan varios métodos de XAudio2 que se pueden llamar como parte de un conjunto de operaciones.
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: Conjuntos de operaciones de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90955fc0557f3f84840436c121f768caff4af81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279359"
---
# <a name="xaudio2-operation-sets"></a>Conjuntos de operaciones de XAudio2

En esta información general se presentan varios métodos de XAudio2 que se pueden llamar como parte de un conjunto de operaciones.

Varios métodos de XAudio2 toman el argumento *OperationSet* , que permite que se llamen como parte de un grupo diferido. En un momento dado, puede aplicar un conjunto completo de cambios simultáneamente llamando a la función [**IXAudio2:: commitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con el identificador *OperationSet* para ese grupo. El identificador es un número arbitrario. Por lo tanto, permite que partes independientes del código de cliente apliquen cambios atómicos independientes al gráfico sin ningún conflicto. La práctica recomendada es que el cliente incremente un contador global siempre que necesite generar un identificador único de *OperationSet* . Se garantiza que un conjunto de cambios en el gráfico, aplicados de forma atómica, es preciso para la muestra. Por ejemplo, las voces se iniciarán en sincronización.

Si establece *OperationSet* en \_ la confirmación de XAUDIO2 \_ Now, el cambio se aplica inmediatamente. Surte efecto en el primer paso de procesamiento de audio después de la llamada al método. Si llama a [**commitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con \_ la confirmación de XAUDIO2 \_ All, se realizan cambios en todos los conjuntos de operaciones pendientes, independientemente de su identificador *OperationSet* .

Ciertos métodos surten efecto inmediatamente cuando se les llama desde una devolución de llamada de XAudio2 con un *OperationSet* de la confirmación de xaudio2 \_ \_ ahora. Todos los demás métodos que toman un argumento *OperationSet* solo surten efecto en el siguiente paso de procesamiento una vez que se llama al método (si se llama con la confirmación de XAUDIO2 \_ \_ ahora), o después de llamar a [**commitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con el mismo *OperationSet*. Debido a esto, es posible que ciertas llamadas al método no se realicen siempre en el mismo orden en el que se llamaron.

Todas las operaciones pendientes se confirman de forma atómica cuando se llama a [**IXAudio2:: StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) . Los métodos a los que se llama mientras se detiene el motor surten efecto inmediatamente, independientemente del valor de *OperationSet* proporcionado. Al reiniciar el motor, XAudio2 vuelve al modo asincrónico.

Los escenarios simples en los que los conjuntos de operaciones son útiles son los ejemplos siguientes.

-   Iniciar varias voces simultáneamente.
-   Enviar simultáneamente un búfer a una voz, establecer los parámetros de voz e iniciar la voz.
-   Realización de un cambio a gran escala en el gráfico, como la conexión de todas las voces de origen a una nueva voz de submezcla.

Vea [Cómo: agrupar métodos de audio como un conjunto de operaciones](how-to--group-audio-methods-as-an-operation-set.md) para obtener un ejemplo del uso de un conjunto de operaciones.

## <a name="operation-set-methods"></a>Métodos de conjunto de operaciones

Puede llamar a los métodos siguientes como parte de un conjunto de operaciones.

-   [**IXAudio2SourceVoice::ExitLoop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop)
-   [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)
-   [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio)
-   [**IXAudio2Voice::D isableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)
-   [**IXAudio2Voice::EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)
-   [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
-   [**IXAudio2Voice::SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)
-   [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)
-   [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [**IXAudio2SourceVoice:: Stop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

Tal y como se ha descrito anteriormente, el código de cliente debe llamar finalmente a la función [**IXAudio2:: commitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) para ejecutar los cambios aplazados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conjuntos de operaciones](operation-sets.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: agrupar métodos de audio como un conjunto de operaciones](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 

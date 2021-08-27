---
description: En esta introducción se presentan varios métodos XAudio2 a los que puede llamar como parte de un conjunto de operaciones.
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: Conjuntos de operaciones XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a7f16edfa461d9944691bc4535debc05f820150dadf746caece85cb68c9f97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089415"
---
# <a name="xaudio2-operation-sets"></a>Conjuntos de operaciones XAudio2

En esta introducción se presentan varios métodos XAudio2 a los que puede llamar como parte de un conjunto de operaciones.

Varios métodos XAudio2 toman el *argumento OperationSet,* que permite llamarlos como parte de un grupo aplazado. En un momento específico, puede aplicar un conjunto completo de cambios simultáneamente llamando a la función [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con el identificador *OperationSet* para ese grupo. El identificador es un número arbitrario. Por lo tanto, permite que partes independientes del código de cliente apliquen cambios atómicos independientes al gráfico sin conflictos. La práctica recomendada es que el cliente incremente un contador global siempre que necesite generar un identificador *OperationSet único* y nuevo. Se garantiza que un conjunto de cambios en el gráfico, aplicados de forma atómica, son precisos para la muestra. Por ejemplo, las voces se iniciarán en sincronización.

Si establece *OperationSet en* XAUDIO2 \_ COMMIT \_ NOW, el cambio se aplica inmediatamente. Tiene efecto en el primer paso de procesamiento de audio después de la llamada al método . Si llama a [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con XAUDIO2 COMMIT ALL, se realizan cambios en todos los conjuntos de operaciones pendientes, independientemente de su \_ \_ identificador *OperationSet.*

Ciertos métodos tienen efecto inmediatamente cuando se les llama desde una devolución de llamada XAudio2 con *un OperationSet* de XAUDIO2 \_ COMMIT \_ NOW. Todos los demás métodos que toman un argumento *OperationSet* solo tienen efecto en el siguiente paso de procesamiento después de llamar al método (si se llama con XAUDIO2 COMMIT NOW) o después de llamar a \_ \_ [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) con el mismo *OperationSet*. Debido a esto, es posible que determinadas llamadas a métodos no siempre se sucedan en el mismo orden en que se llamaron.

Todas las operaciones pendientes se confirman de forma [**atómica cuando se llama a IXAudio2::StopEngine.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) Los métodos a los que se llama mientras se detiene el motor se aplican inmediatamente, independientemente del *valor OperationSet* proporcionado. Al reiniciar el motor, XAudio2 vuelve al modo asincrónico.

Entre los escenarios sencillos en los que los conjuntos de operaciones son útiles se incluyen los ejemplos siguientes.

-   Iniciar varias voces simultáneamente.
-   Enviar simultáneamente un búfer a una voz, establecer los parámetros de voz e iniciar la voz.
-   Realizar un cambio a gran escala en el gráfico, como conectar todas las voces de origen a una nueva voz de submezcla.

Vea [Cómo: Agrupar métodos de audio como un conjunto de operaciones](how-to--group-audio-methods-as-an-operation-set.md) para obtener un ejemplo del uso de un conjunto de operaciones.

## <a name="operation-set-methods"></a>Métodos del conjunto de operaciones

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
-   [**IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [**IXAudio2SourceVoice::Stop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

Como se ha descrito anteriormente, el código de cliente debe llamar en última instancia a la [**función IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) para ejecutar los cambios aplazados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conjuntos de operaciones](operation-sets.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: agrupar métodos de audio como un conjunto de operaciones](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 

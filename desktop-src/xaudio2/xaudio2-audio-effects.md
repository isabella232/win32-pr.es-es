---
description: Un efecto de audio es un objeto que toma datos de audio entrantes y realiza alguna operación en los datos antes de pasarlo. Puede usar un efecto para realizar diversas tareas, como agregar reverberación a una secuencia de audio y supervisar los niveles de volumen máximo.
ms.assetid: 8c3fa4ca-dcff-bd23-7220-7d0aeb6c6068
title: Efectos de audio de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886edb81718f772f7dec31f799b1612ca701c2327468ad554fe80a17c1f69ec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082859"
---
# <a name="xaudio2-audio-effects"></a>Efectos de audio de XAudio2

Un efecto de audio es un objeto que toma datos de audio entrantes y realiza alguna operación en los datos antes de pasarlo. Puede usar un efecto para realizar diversas tareas, como agregar reverberación a una secuencia de audio y supervisar los niveles de volumen máximo.

## <a name="effect-chains"></a>Cadenas de efecto

Cualquier voz XAudio2 puede hospedar una cadena de efectos de audio. Puede usar una matriz de estructuras [**DE \_ \_ DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) DE EFECTO XAUDIO2 para especificar cadenas de efecto. Cada descriptor contiene un puntero a un objeto de efecto proporcionado por el cliente. Estos objetos deben implementar las interfaces de objeto de procesamiento de audio (APO). Consulte información [general de XAPO](xapo-overview.md) para obtener más información sobre el modelo DEPO.

El cliente puede modificar dinámicamente las cadenas de efecto (mientras se ejecuta el motor XAudio2), los efectos se pueden habilitar o deshabilitar individualmente y se pueden cambiar los parámetros de efecto, todo ello sin ninguna interrupción del audio. Cada vez que cambia cualquier aspecto del gráfico de efectos, XAudio2 vuelve a optimizar el gráfico para evitar el procesamiento innecesario. Vea [**IXAudio2Voice::SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), [**IXAudio2Voice::EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)y [**IXAudio2Voice::SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters).

Después de adjuntar un efecto a una voz XAudio2, XAudio2 toma el control del efecto y el cliente no debe realizar ninguna otra llamada a él. La manera más sencilla de asegurarse de que esto es liberar todos los punteros al efecto.

Los efectos de una cadena de efectos de voz XAudio2 determinada deben consumir y generar audio de punto flotante a la velocidad de muestreo de procesamiento de esa voz. El único aspecto del formato de audio que pueden cambiar es el recuento de canales (por ejemplo, un efecto de reverberación puede convertir los datos mono a 5.1). El cliente puede usar el [**\_ \_ DESCRIPTOR DE EFECTO XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor).**Campo OutputChannels** para especificar el número de canales que debe generar cada efecto. Se produce un error en la cadena de efectos si alguno de los efectos no puede cumplir estos requisitos o si un efecto genera una serie de canales que el efecto siguiente no puede controlar. Se producirá un error en las llamadas [**IXAudio2Voice::EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) o [**IXAudio2Voice::D isableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) que hacen que la cadena de efectos deje de cumplir estos requisitos.

Las interfaces DE APO usadas en XAudio2 deben ser *destructivas.* Esto significa que siempre sobrescriben los datos que encuentran en sus búferes de salida. De lo contrario, el audio resultante podría ser incorrecto porque XAudio2 no garantiza que estos búferes se hayan inicializado previamente con silencio.

## <a name="xaudio2-built-in-effects"></a>Efectos integrados de XAudio2

En la tabla siguiente se muestra el conjunto de efectos de audio integrados proporcionados por XAudio2 y sus métodos de creación. 

| Efecto       | Método de creación                                              |
|--------------|--------------------------------------------------------------|
| Reverberación       | [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)           |
| Medidor de volumen | [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter) |



 

Para obtener un ejemplo de creación y uso de una instancia de un efecto de audio, [vea Cómo: Crear una cadena de efectos.](how-to--create-an-effect-chain.md)

## <a name="custom-effects-in-xaudio2"></a>Efectos personalizados en XAudio2

La [API de XAPO](xapo-overview.md) proporciona un marco para crear efectos de audio personalizados que puede usar en XAudio2. Para obtener un ejemplo de cómo crear un efecto personalizado con XAPO, vea [Cómo: Crear un XAPO.](how-to--create-an-xapo.md)

## <a name="xapo-effect-library-xapofx"></a>Biblioteca de efectos de XAPO (XAPOFX)

[XAPOFX proporciona](xapofx-overview.md) una biblioteca adicional de XAPOs y un mecanismo común para crearlos. Para obtener un ejemplo del uso de XAPOFX con XAudio2, vea [Cómo: Usar XAPOFX en XAudio2.](how-to--use-xapofx-in-xaudio2.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos de audio](audio-effects.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> </dl>

 

 

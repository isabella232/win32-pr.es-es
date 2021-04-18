---
description: Un efecto de audio es un objeto que toma los datos de audio entrantes y realiza alguna operación en los datos antes de pasarlos. Puede usar un efecto para realizar diversas tareas, como agregar la reverberación a una secuencia de audio y supervisar los niveles de volumen máximo.
ms.assetid: 8c3fa4ca-dcff-bd23-7220-7d0aeb6c6068
title: Efectos de audio de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8de87a65ea4321b5e8d73a837f79a3e56e8e3a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720376"
---
# <a name="xaudio2-audio-effects"></a>Efectos de audio de XAudio2

Un efecto de audio es un objeto que toma los datos de audio entrantes y realiza alguna operación en los datos antes de pasarlos. Puede usar un efecto para realizar diversas tareas, como agregar la reverberación a una secuencia de audio y supervisar los niveles de volumen máximo.

## <a name="effect-chains"></a>Cadenas de efectos

Cualquier voz de XAudio2 puede hospedar una cadena de efectos de audio. Puede usar una matriz de estructuras [**de \_ \_ descriptor de efectos de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) para especificar cadenas de efectos. Cada descriptor contiene un puntero a un objeto de efecto proporcionado por el cliente. Estos objetos deben implementar las interfaces del objeto de procesamiento de audio (APO). Vea la información [General de XAPO](xapo-overview.md) para obtener más información sobre el modelo de APO.

El cliente puede modificar dinámicamente las cadenas de efectos (mientras se ejecuta el motor de XAudio2), los efectos se pueden habilitar o deshabilitar individualmente, y los parámetros de efecto se pueden cambiar, todo ello sin ninguna interrupción del audio. Cada vez que cambia cualquier aspecto del gráfico de efectos, XAudio2 vuelve a optimizar el gráfico para evitar un procesamiento innecesario. Vea [**IXAudio2Voice:: SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), [**IXAudio2Voice:: EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)y [**IXAudio2Voice:: SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters).

Una vez que se adjunta un efecto a una voz de XAudio2, XAudio2 toma el control del efecto y el cliente no debe realizar ninguna llamada adicional a él. La manera más sencilla de asegurarse de esto es liberar todos los punteros al efecto.

Los efectos de la cadena de efecto de una voz determinada de XAudio2 deben consumir y producir audio de punto flotante en la velocidad de muestreo de procesamiento de la voz. El único aspecto del formato de audio que pueden cambiar es el número de canales (por ejemplo, un efecto de reverberación puede convertir los datos mono en 5,1). El cliente puede usar el [**\_ \_ descriptor de efectos de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor).**Campo OutputChannels** para especificar el número de canales que debe producir cada efecto. Se produce un error en la cadena de efectos si alguno de los efectos no puede cumplir estos requisitos, o si un efecto produce un número de canales que el siguiente efecto no puede controlar. Cualquier [**IXAudio2Voice:: EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) o [**IXAudio2Voice::D isableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) llama a, lo que provocará un error en la cadena de efectos para dejar de cumplir estos requisitos.

Las interfaces de APO usadas en XAudio2 deben ser *destructivas*. Esto significa que siempre sobrescriben los datos que encuentren en sus búferes de salida. De lo contrario, el audio resultante podría ser incorrecto porque XAudio2 no garantiza que estos búferes se hayan inicializado previamente con silencio.

## <a name="xaudio2-built-in-effects"></a>Efectos integrados de XAudio2

En la tabla siguiente se muestra el conjunto de efectos de audio integrados que proporciona XAudio2 y sus métodos de creación. 

| Efecto       | Método de creación                                              |
|--------------|--------------------------------------------------------------|
| Reverbera       | [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)           |
| Medidor de volumen | [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter) |



 

Para obtener un ejemplo de creación y uso de una instancia de un efecto de audio, consulte [Cómo: crear una cadena de efectos](how-to--create-an-effect-chain.md).

## <a name="custom-effects-in-xaudio2"></a>Efectos personalizados en XAudio2

La API de [XAPO](xapo-overview.md) proporciona un marco para crear efectos de audio personalizados que puede usar en XAudio2. Para obtener un ejemplo de cómo crear un efecto personalizado con XAPO, consulte [Cómo: crear un xapo](how-to--create-an-xapo.md).

## <a name="xapo-effect-library-xapofx"></a>Biblioteca de efectos de XAPO (XAPOFX)

[XAPOFX](xapofx-overview.md) proporciona una biblioteca adicional de XAPOs y un mecanismo común para crearlos. Para obtener un ejemplo del uso de XAPOFX con XAudio2, consulte [Cómo: usar XAPOFX en xaudio2](how-to--use-xapofx-in-xaudio2.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos de audio](audio-effects.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> </dl>

 

 

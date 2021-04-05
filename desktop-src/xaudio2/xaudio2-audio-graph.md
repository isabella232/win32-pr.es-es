---
description: El conjunto de todas las voces, con sus efectos contenidos y sus interconexiones, se conoce como el gráfico de procesamiento de audio.
ms.assetid: 4fa45dbf-3811-c91c-7561-3b896e9e1f03
title: Gráfico de audio de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb265bd6bc2547acd04ca41cceb58ad12896fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279362"
---
# <a name="xaudio2-audio-graph"></a>Gráfico de audio de XAudio2

El conjunto de todas las voces, con sus efectos contenidos y sus interconexiones, se conoce como el gráfico de procesamiento de audio. El gráfico toma un conjunto de secuencias de audio del cliente como entrada, las procesa y entrega el resultado final a un dispositivo de audio. Todo el procesamiento de audio se realiza en un subproceso independiente con una periodicidad definida por el cuanto del gráfico (actualmente, 10 milisegundos en Microsoft Windows y 5 1/3 milisegundos en Xbox 360). Cada Quantum milisegundos, el subproceso se reactiva y dispersa los milisegundos de los datos de audio a través del gráfico completo. Para obtener un ejemplo de cómo crear un gráfico de audio básico, consulte Cómo: [compilar un gráfico básico de procesamiento de audio](how-to--build-a-basic-audio-processing-graph.md).

Un gráfico de audio simple:

![un gráfico de audio simple](images/xaudio2-audio-graph.png)

El cliente puede controlar el estado del gráfico dinámicamente mientras se está ejecutando. Las acciones de control pueden incluir la adición y eliminación de entradas y salidas, el cambio de los efectos internos y las interconexiones, el establecimiento de parámetros en los efectos, la habilitación y deshabilitación de partes del gráfico, etc. Para obtener un ejemplo de cómo cambiar dinámicamente un gráfico de audio, consulte [Cómo: agregar o quitar voces dinámicamente de un gráfico de audio](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).

## <a name="processing-the-graph"></a>Procesar el gráfico

Cualquier llamada al método que afecte a cualquier objeto del gráfico se considera que está afectando a un cambio de estado del gráfico. Entre los cambios de estado del gráfico se incluyen los siguientes:

-   Crear y destruir voces
-   Inicio o detención de voces
-   Cambiar los destinos de una voz
-   Modificar cadenas de efectos
-   Habilitar o deshabilitar efectos
-   Establecer parámetros en los efectos o en los SRCs, filtros, volúmenes y mezcladores integrados

Cualquier conjunto de cambios de estado del gráfico se puede combinar y realizar como una transacción atómica. Estas operaciones atómicas se conocen como conjuntos de operaciones. Se describen en la introducción a los [conjuntos de operaciones de XAudio2](xaudio2-operation-sets.md) .

## <a name="internal-data-representation"></a>Representación de datos internos

Los datos de audio dentro del gráfico de XAudio2 siempre se almacenan y procesan en formato PCM de punto flotante de 32 bits. Sin embargo, el número de canales y la velocidad de muestreo pueden variar dentro del gráfico. El formato en el que una voz determinada procesa audio viene determinado por el tipo de voz y los parámetros que se usan para crear la voz.



| Tipo de voz                                                                                                      | Parámetros                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)                                                              | El número de canales y la velocidad de muestreo de las voces a las que la voz de origen envía audio.         |
| [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) y [ **IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) | Los argumentos *InputChannels* y *InputSampleRate* usados para crear la voz de submezcla o de creación de registro. |



 

## <a name="format-conversion"></a>Conversión de formato

XAudio2 controla cualquier conversión de canal o velocidad de muestra que se requiera a medida que el audio viaja de una voz a otra, con las siguientes limitaciones:

-   Todas las voces de destino de una voz determinada deben ejecutarse con la misma velocidad de muestra
-   Los efectos de una cadena de efectos pueden cambiar el número de canales del audio, pero no su velocidad de muestra
-   El número de canales de salida de una cadena de efectos debe coincidir con el de las voces a las que envía
-   No se puede realizar ningún cambio de gráfico dinámico, lo que interrumpiría las reglas anteriores

En el lado de entrada, las voces de origen pueden leer datos en cualquier formato PCM válido o en cualquiera de los formatos comprimidos compatibles con XAudio2. Si se comprimen los datos de entrada, se descodifican en PCM de punto flotante antes de que se realice cualquier otro procesamiento.

En el lado de salida, las voces de masterización solo pueden generar datos PCM. Estos datos siempre satisfarán las mismas restricciones descritas anteriormente para los datos PCM entrantes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Gráficos de audio](audio-graphs.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: crear un gráfico de procesamiento de audio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Cómo: agregar o quitar voces de un gráfico de audio dinámicamente](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)
</dt> <dt>

[Cómo: usar voces de submezcla](how-to--use-submix-voices.md)
</dt> <dt>

[Cómo: crear un efecto en cadena](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 




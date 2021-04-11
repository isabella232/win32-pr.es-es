---
description: XAudio2 puede llamar a las funciones proporcionadas por el cliente para notificarle de forma asincrónica ciertos eventos que tienen lugar en el subproceso de procesamiento de audio.
ms.assetid: 4fbd4229-f7ac-33b3-b4b7-f09150a60598
title: Devoluciones de llamadas de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee191ad8c15d238a065c837c6fb192befbe7a51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361561"
---
# <a name="xaudio2-callbacks"></a>Devoluciones de llamadas de XAudio2

XAudio2 puede llamar a las funciones proporcionadas por el cliente para notificarle de forma asincrónica ciertos eventos que tienen lugar en el subproceso de procesamiento de audio. Estas devoluciones de llamada pueden ser globales o específicas para una voz de origen determinada. Para recibir devoluciones de llamada del motor global, el cliente debe proporcionar una instancia de una clase que implemente la interfaz [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) al inicializar XAudio2. Para recibir devoluciones de llamada de voz de origen, el cliente debe proporcionar una instancia de una clase que implemente la interfaz [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) al crear voces de origen. Para obtener más información, consulte **IXAudio2EngineCallback** y **IXAudio2VoiceCallback**.

Debe implementar devoluciones de llamada cuidadosamente para evitar que se produzcan interrupciones en el audio. Cada vez que se ejecuta una devolución de llamada, XAudio2 no puede generar audio. Los retrasos de más de unos milisegundos pueden producir un problema de audio. Los retrasos de esta naturaleza también generan resultados del depurador. Esto indica posibles problemas de rendimiento. Como mínimo, las funciones de devolución de llamada no deben hacer lo siguiente:

-   Acceder al disco duro u otro almacenamiento permanente
-   Realizar llamadas de API costosas o de bloqueo
-   Sincronizar con otras partes del código de cliente
-   Requerir un uso significativo de la CPU

Si el diseño del cliente requiere una devolución de llamada para desencadenar acciones como las mencionadas anteriormente, la devolución de llamada debe indicar a un subproceso de cliente diferente que realice el trabajo. Puede hacerlo con un mecanismo de **SetEvent** sencillo o con mecanismos más sofisticados como una cola de comandos sin bloqueos utilizada por otro subproceso.

## <a name="ixaudio2enginecallback"></a>IXAudio2EngineCallback

La clase [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) contiene métodos que notifican al cliente cuando se producen determinados eventos en el motor de XAudio2. Estos métodos deben ser implementados por el cliente de XAudio2. XAudio2 llama a estos métodos por medio de un puntero de interfaz proporcionado por el cliente mediante el método [**IXAudio2:: RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) . Todos estos métodos devuelven **void**, en lugar de **HRESULT**.

## <a name="ixaudio2voicecallback"></a>IXAudio2VoiceCallback

La clase [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) contiene métodos que notifican al cliente cuando se producen determinados eventos en una voz de origen específica de XAudio2. XAudio2 llama a estos métodos por medio de un puntero de interfaz proporcionado por el cliente en [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice). Al igual que con [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback), estos métodos deben ser implementados por el cliente de XAudio2 y devolver **void** en lugar de un **valor HRESULT**.

Como se mencionó anteriormente, es fundamental que las implementaciones proporcionadas por el cliente de estas devoluciones de llamada devuelvan lo más rápido posible, preferiblemente en un milisegundo. Las devoluciones de llamada se ejecutan en el subproceso de procesamiento de audio y todo el procesamiento se interrumpe hasta que se devuelve la devolución de llamada. Un retraso en una devolución de llamada puede producir fácilmente un problema de audio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Devoluciones de llamada](callbacks.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: usar devoluciones de llamadas de voces de origen](how-to--use-source-voice-callbacks.md)
</dt> <dt>

[Cómo: usar devoluciones de llamadas de motores](how-to--use-engine-callbacks.md)
</dt> <dt>

[Cómo: transmitir un sonido de un disco](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 

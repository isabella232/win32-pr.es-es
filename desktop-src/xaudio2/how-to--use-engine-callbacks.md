---
description: Puede notificar al código de cliente de XAudio2 los eventos del motor registrando una instancia de una clase que implementa la interfaz IXAudio2EngineCallback con el motor de XAudio2.
ms.assetid: 006a8cb6-c24c-f7d1-9e8b-9cb2baa046c0
title: 'Cómo: usar devoluciones de llamadas de motores'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04adec0efd0625157740488d70be7896688d1176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424012"
---
# <a name="how-to-use-engine-callbacks"></a>Cómo: usar devoluciones de llamadas de motores

Puede notificar al código de cliente de XAudio2 los eventos del motor registrando una instancia de una clase que implementa la interfaz [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) con el motor de xaudio2. Esto permite al código de cliente de XAudio2 realizar un seguimiento de Cuándo se está produciendo el procesamiento de audio y cuándo reiniciar el motor en caso de que se produzca un error crítico.

## <a name="to-use-an-engine-callback"></a>Para utilizar una devolución de llamada del motor

En los pasos siguientes se registra un objeto para controlar los eventos del motor.

1.  Cree una clase que herede de la interfaz [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) .

    Todos los métodos de [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) son puramente virtuales y deben definirse. El método de interés en este ejemplo es [**IXAudio2EngineCallback:: OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), que establece una marca para señalar el bucle principal del juego que se ha producido un error crítico. Los métodos restantes, [**IXAudio2EngineCallback:: OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) y [**IXAudio2EngineCallback:: OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), son códigos auxiliares en este ejemplo.

    ```
    class EngineCallback : public IXAudio2EngineCallback
    {
        void OnProcessingPassEnd () {}
        void OnProcessingPassStart() {}
        void OnCriticalError (HRESULT Error) {}
    };
    ```

    

2.  Use [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) para crear una instancia del motor de XAudio2.

    ```
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  Use [**IXAudio2:: RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) para registrar la devolución de llamada del motor.

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  Si no necesita más devoluciones de llamada del motor, llame a [**IXAudio2:: UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).

    ```
    pXAudio2->UnregisterForCallbacks( &engineCallback );
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Devoluciones de llamada](callbacks.md)
</dt> <dt>

[Devoluciones de llamadas de XAudio2](xaudio2-callbacks.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: crear un gráfico de procesamiento de audio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Cómo: transmitir un sonido de un disco](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 

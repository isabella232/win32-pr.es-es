---
description: Puede notificar al código de cliente XAudio2 de eventos del motor registrando una instancia de una clase que implementa la interfaz IXAudio2EngineCallback con el motor XAudio2.
ms.assetid: 006a8cb6-c24c-f7d1-9e8b-9cb2baa046c0
title: 'Cómo: usar devoluciones de llamadas de motores'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc51e673be6972c1c5ba012c12f616e1bfe78a345081fee683aba83b6944c17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054375"
---
# <a name="how-to-use-engine-callbacks"></a>Cómo: usar devoluciones de llamadas de motores

Puede notificar al código de cliente XAudio2 de eventos del motor registrando una instancia de una clase que implementa la interfaz [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) con el motor XAudio2. Esto permite que el código de cliente XAudio2 realice un seguimiento de cuándo se está produciendo el procesamiento de audio y cuándo reiniciar el motor en caso de error crítico.

## <a name="to-use-an-engine-callback"></a>Para usar una devolución de llamada del motor

En los pasos siguientes se registra un objeto para controlar los eventos del motor.

1.  Cree una clase que herede de la [**interfaz IXAudio2EngineCallback.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)

    Todos los métodos [**de IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) son puramente virtuales y deben definirse. El método de interés en este ejemplo es [**IXAudio2EngineCallback::OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), que establece una marca para indicar al bucle de juego principal que se ha producido un error crítico. Los métodos restantes, [**IXAudio2EngineCallback::OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) e [**IXAudio2EngineCallback::OnProcessingPassEnd,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend)son códigos auxiliares en este ejemplo.

    ```
    class EngineCallback : public IXAudio2EngineCallback
    {
        void OnProcessingPassEnd () {}
        void OnProcessingPassStart() {}
        void OnCriticalError (HRESULT Error) {}
    };
    ```

    

2.  Use [**XAudio2Create para**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) crear una instancia del motor XAudio2.

    ```
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  Use [**IXAudio2::RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) para registrar la devolución de llamada del motor.

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  Si ya no necesita la devolución de llamada del motor, llame [**a IXAudio2::UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).

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

 

 

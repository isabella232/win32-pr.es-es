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
# <a name="how-to-use-engine-callbacks"></a><span data-ttu-id="ea975-103">Cómo: usar devoluciones de llamadas de motores</span><span class="sxs-lookup"><span data-stu-id="ea975-103">How to: Use Engine Callbacks</span></span>

<span data-ttu-id="ea975-104">Puede notificar al código de cliente de XAudio2 los eventos del motor registrando una instancia de una clase que implementa la interfaz [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) con el motor de xaudio2.</span><span class="sxs-lookup"><span data-stu-id="ea975-104">You can notify the XAudio2 client code of engine events by registering an instance of a class implementing the [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) interface with the XAudio2 engine.</span></span> <span data-ttu-id="ea975-105">Esto permite al código de cliente de XAudio2 realizar un seguimiento de Cuándo se está produciendo el procesamiento de audio y cuándo reiniciar el motor en caso de que se produzca un error crítico.</span><span class="sxs-lookup"><span data-stu-id="ea975-105">This allows the XAudio2 client code to keep track of when audio processing is occurring, and when to restart the engine in the event of a critical error.</span></span>

## <a name="to-use-an-engine-callback"></a><span data-ttu-id="ea975-106">Para utilizar una devolución de llamada del motor</span><span class="sxs-lookup"><span data-stu-id="ea975-106">To use an engine callback</span></span>

<span data-ttu-id="ea975-107">En los pasos siguientes se registra un objeto para controlar los eventos del motor.</span><span class="sxs-lookup"><span data-stu-id="ea975-107">The following steps register an object to handle engine events.</span></span>

1.  <span data-ttu-id="ea975-108">Cree una clase que herede de la interfaz [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) .</span><span class="sxs-lookup"><span data-stu-id="ea975-108">Create a class that inherits from the [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) interface.</span></span>

    <span data-ttu-id="ea975-109">Todos los métodos de [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) son puramente virtuales y deben definirse.</span><span class="sxs-lookup"><span data-stu-id="ea975-109">All methods of [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) are purely virtual and must be defined.</span></span> <span data-ttu-id="ea975-110">El método de interés en este ejemplo es [**IXAudio2EngineCallback:: OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), que establece una marca para señalar el bucle principal del juego que se ha producido un error crítico.</span><span class="sxs-lookup"><span data-stu-id="ea975-110">The method of interest in this example is [**IXAudio2EngineCallback::OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), which sets a flag to signal the main game loop that a critical error has occurred.</span></span> <span data-ttu-id="ea975-111">Los métodos restantes, [**IXAudio2EngineCallback:: OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) y [**IXAudio2EngineCallback:: OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), son códigos auxiliares en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ea975-111">The remaining methods, [**IXAudio2EngineCallback::OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) and [**IXAudio2EngineCallback::OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), are stubs in this example.</span></span>

    ```
    class EngineCallback : public IXAudio2EngineCallback
    {
        void OnProcessingPassEnd () {}
        void OnProcessingPassStart() {}
        void OnCriticalError (HRESULT Error) {}
    };
    ```

    

2.  <span data-ttu-id="ea975-112">Use [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) para crear una instancia del motor de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="ea975-112">Use [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) to create an instance of the XAudio2 engine.</span></span>

    ```
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  <span data-ttu-id="ea975-113">Use [**IXAudio2:: RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) para registrar la devolución de llamada del motor.</span><span class="sxs-lookup"><span data-stu-id="ea975-113">Use [**IXAudio2::RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) to register the engine callback.</span></span>

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  <span data-ttu-id="ea975-114">Si no necesita más devoluciones de llamada del motor, llame a [**IXAudio2:: UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).</span><span class="sxs-lookup"><span data-stu-id="ea975-114">If you don't need the engine callback any more, call [**IXAudio2::UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).</span></span>

    ```
    pXAudio2->UnregisterForCallbacks( &engineCallback );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="ea975-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea975-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea975-116">Devoluciones de llamada</span><span class="sxs-lookup"><span data-stu-id="ea975-116">Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="ea975-117">Devoluciones de llamadas de XAudio2</span><span class="sxs-lookup"><span data-stu-id="ea975-117">XAudio2 Callbacks</span></span>](xaudio2-callbacks.md)
</dt> <dt>

[<span data-ttu-id="ea975-118">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="ea975-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="ea975-119">Cómo: crear un gráfico de procesamiento de audio básico</span><span class="sxs-lookup"><span data-stu-id="ea975-119">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="ea975-120">Cómo: transmitir un sonido de un disco</span><span class="sxs-lookup"><span data-stu-id="ea975-120">How to: Stream a Sound from Disk</span></span>](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 

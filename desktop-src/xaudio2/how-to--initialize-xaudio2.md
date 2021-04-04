---
description: XAudio2 se inicializa para la reproducción de audio mediante la creación de una instancia del motor de XAudio2 y la creación de una voz de maestro.
ms.assetid: 4db2e7fc-0a87-0344-a07c-3abf2b21af32
title: 'Cómo: inicializar XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a613c1ae2b7c3a7f0c55ab5349a0a605aaeb2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908141"
---
# <a name="how-to-initialize-xaudio2"></a><span data-ttu-id="f8e0d-103">Cómo: inicializar XAudio2</span><span class="sxs-lookup"><span data-stu-id="f8e0d-103">How to: Initialize XAudio2</span></span>

<span data-ttu-id="f8e0d-104">XAudio2 se inicializa para la reproducción de audio mediante la creación de una instancia del motor de XAudio2 y la creación de una voz de maestro.</span><span class="sxs-lookup"><span data-stu-id="f8e0d-104">XAudio2 is initialized for audio playback by creating an instance of the XAudio2 engine, and creating a mastering voice.</span></span>

<span data-ttu-id="f8e0d-105">**Para inicializar XAudio2**</span><span class="sxs-lookup"><span data-stu-id="f8e0d-105">**To initialize XAudio2**</span></span>

1.  <span data-ttu-id="f8e0d-106">Asegúrese de que ha inicializado COM.</span><span class="sxs-lookup"><span data-stu-id="f8e0d-106">Make sure you have initialized COM.</span></span> <span data-ttu-id="f8e0d-107">Para una aplicación de la tienda Windows, esto se hace como parte de la inicialización de la Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="f8e0d-107">For a Windows Store app, this is done as part of initializing the Windows Runtime.</span></span> <span data-ttu-id="f8e0d-108">De lo contrario, use [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="f8e0d-108">Otherwise, use [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    ```
    HRESULT hr;
    hr = CoInitializeEx( nullptr, COINIT_MULTITHREADED );
    if (FAILED(hr))
        return hr;
    ```



2.  <span data-ttu-id="f8e0d-109">Use la función [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) para crear una instancia del motor de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="f8e0d-109">Use the [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) function to create an instance of the XAudio2 engine.</span></span>

    ```
    IXAudio2* pXAudio2 = nullptr;
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  <span data-ttu-id="f8e0d-110">Use el método [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) para crear una voz de maestro.</span><span class="sxs-lookup"><span data-stu-id="f8e0d-110">Use the [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) method to create a mastering voice.</span></span>

    <span data-ttu-id="f8e0d-111">Las voces de maestro encapsulan un dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="f8e0d-111">The mastering voices encapsulates an audio device.</span></span> <span data-ttu-id="f8e0d-112">Es el destino final de todo el audio que pasa a través de un gráfico de audio.</span><span class="sxs-lookup"><span data-stu-id="f8e0d-112">It is the ultimate destination for all audio that passes through an audio graph.</span></span>

    ```
    IXAudio2MasteringVoice* pMasterVoice = nullptr;
    if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a><span data-ttu-id="f8e0d-113">Notas para aplicaciones de la tienda Windows</span><span class="sxs-lookup"><span data-stu-id="f8e0d-113">Notes for Windows Store apps</span></span>

<span data-ttu-id="f8e0d-114">Se recomienda usar un [puntero inteligente](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) para administrar la duración de los objetos de XAUDIO2 de una manera segura de excepciones.</span><span class="sxs-lookup"><span data-stu-id="f8e0d-114">We recommend that you make use of a [smart pointer](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) to manage the lifetime of XAUDIO2 objects in an exception safe manner.</span></span> <span data-ttu-id="f8e0d-115">En el caso de las aplicaciones de la tienda Windows, puede usar la plantilla de puntero inteligente [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) de la biblioteca de plantillas de C++ Windows Runtime (WRL).</span><span class="sxs-lookup"><span data-stu-id="f8e0d-115">For Windows Store apps, you can use the [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) smart pointer template from the Windows Runtime C++ Template Library (WRL).</span></span>


```C++
Microsoft::WRL::ComPtr<IXAudio2> XAudio2;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &XAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    throw Platform::Exception::CreateException(hr);

IXAudio2MasteringVoice* pMasterVoice = nullptr;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
    return hr;
```



> [!Note]  
> <span data-ttu-id="f8e0d-116">Asegúrese de que todos los objetos secundarios de XAUDIO2 estén totalmente liberados antes de liberar el objeto [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .</span><span class="sxs-lookup"><span data-stu-id="f8e0d-116">Ensure that all XAUDIO2 child objects are fully released before you release the [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f8e0d-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f8e0d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8e0d-118">Introducción de XAudio2</span><span class="sxs-lookup"><span data-stu-id="f8e0d-118">XAudio2 Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="f8e0d-119">Cómo: cargar archivos de datos de audio en XAudio2</span><span class="sxs-lookup"><span data-stu-id="f8e0d-119">How to: Load Audio Data Files in XAudio2</span></span>](how-to--load-audio-data-files-in-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="f8e0d-120">Cómo: reproducir un sonido con XAudio2</span><span class="sxs-lookup"><span data-stu-id="f8e0d-120">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 

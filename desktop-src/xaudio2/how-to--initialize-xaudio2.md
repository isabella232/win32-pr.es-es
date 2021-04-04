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
# <a name="how-to-initialize-xaudio2"></a>Cómo: inicializar XAudio2

XAudio2 se inicializa para la reproducción de audio mediante la creación de una instancia del motor de XAudio2 y la creación de una voz de maestro.

**Para inicializar XAudio2**

1.  Asegúrese de que ha inicializado COM. Para una aplicación de la tienda Windows, esto se hace como parte de la inicialización de la Windows Runtime. De lo contrario, use [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    ```
    HRESULT hr;
    hr = CoInitializeEx( nullptr, COINIT_MULTITHREADED );
    if (FAILED(hr))
        return hr;
    ```



2.  Use la función [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) para crear una instancia del motor de XAudio2.

    ```
    IXAudio2* pXAudio2 = nullptr;
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  Use el método [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) para crear una voz de maestro.

    Las voces de maestro encapsulan un dispositivo de audio. Es el destino final de todo el audio que pasa a través de un gráfico de audio.

    ```
    IXAudio2MasteringVoice* pMasterVoice = nullptr;
    if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Notas para aplicaciones de la tienda Windows

Se recomienda usar un [puntero inteligente](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) para administrar la duración de los objetos de XAUDIO2 de una manera segura de excepciones. En el caso de las aplicaciones de la tienda Windows, puede usar la plantilla de puntero inteligente [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) de la biblioteca de plantillas de C++ Windows Runtime (WRL).


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
> Asegúrese de que todos los objetos secundarios de XAUDIO2 estén totalmente liberados antes de liberar el objeto [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción de XAudio2](getting-started.md)
</dt> <dt>

[Cómo: cargar archivos de datos de audio en XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> <dt>

[Cómo: reproducir un sonido con XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 

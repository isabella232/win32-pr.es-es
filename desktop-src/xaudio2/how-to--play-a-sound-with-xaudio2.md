---
description: En este tema se describen los pasos mínimos necesarios para reproducir datos de audio cargados previamente en XAudio2.
ms.assetid: 5172b31c-d2af-45aa-5bd4-b62502f3c047
title: 'Cómo: reproducir un sonido con XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ee2636ae9b6513dba9a479d63e0fd14be2c198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542534"
---
# <a name="how-to-play-a-sound-with-xaudio2"></a><span data-ttu-id="016da-103">Cómo: reproducir un sonido con XAudio2</span><span class="sxs-lookup"><span data-stu-id="016da-103">How to: Play a Sound with XAudio2</span></span>

<span data-ttu-id="016da-104">En este tema se describen los pasos mínimos necesarios para reproducir datos de audio cargados previamente en XAudio2.</span><span class="sxs-lookup"><span data-stu-id="016da-104">This topic describes the minimum steps required to play previously-loaded audio data in XAudio2.</span></span> <span data-ttu-id="016da-105">Después de inicializar XAudio2 (consulte [Cómo: inicializar xaudio2](how-to--initialize-xaudio2.md)) y cargar los datos de audio (consulte Cómo: [cargar archivos de datos de audio en XAudio2](how-to--load-audio-data-files-in-xaudio2.md)), puede reproducir un sonido mediante la creación de una voz de origen y el paso de datos de audio.</span><span class="sxs-lookup"><span data-stu-id="016da-105">After you initialize XAudio2 (see [How to: Initialize XAudio2](how-to--initialize-xaudio2.md)) and load the audio data (see How to: [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)), you can play a sound by creating a source voice and passing audio data to it.</span></span>

## <a name="to-play-a-sound"></a><span data-ttu-id="016da-106">Para reproducir un sonido</span><span class="sxs-lookup"><span data-stu-id="016da-106">To play a sound</span></span>

1.  <span data-ttu-id="016da-107">Inicialice el motor de XAudio2 siguiendo los pasos descritos en [Cómo: inicializar xaudio2](how-to--initialize-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="016da-107">Initialize the XAudio2 engine by following the steps described in [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>
2.  <span data-ttu-id="016da-108">Rellene una estructura [**de \_ búfer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) de [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) y XAUDIO2 siguiendo los pasos descritos en [Cómo: cargar archivos de datos de audio en XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="016da-108">Populate a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure by following the steps described in [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="016da-109">Dependiendo del formato de los datos de audio, puede que tenga que usar una estructura de datos mayor que contenga una estructura [**WaveFormatEx**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) en lugar de una **WAVEFORMATEX**.</span><span class="sxs-lookup"><span data-stu-id="016da-109">Depending on the format of the audio data, you may need to use a larger data structure containing a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) structure in place of a **WAVEFORMATEX**.</span></span> <span data-ttu-id="016da-110">Vea la página de referencia de **WAVEFORMATEX** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="016da-110">See the **WAVEFORMATEX** reference page for more information.</span></span>

     

3.  <span data-ttu-id="016da-111">Cree una voz de origen llamando al método [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) en una instancia del motor de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="016da-111">Create a source voice by calling the [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) method on an instance of the XAudio2 engine.</span></span> <span data-ttu-id="016da-112">El formato de la voz se especifica mediante los valores establecidos en una estructura [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) .</span><span class="sxs-lookup"><span data-stu-id="016da-112">The format of the voice is specified by the values set in a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) structure.</span></span>
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  <span data-ttu-id="016da-113">Envíe un [**\_ búfer de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) a la voz de origen mediante la función [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).</span><span class="sxs-lookup"><span data-stu-id="016da-113">Submit an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) to the source voice using the function [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).</span></span>
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > <span data-ttu-id="016da-114">Los datos de ejemplo de audio a los que la aplicación todavía "posee" los puntos de *búfer* y deben permanecer asignados y accesibles hasta que el sonido deje de reproducirse.</span><span class="sxs-lookup"><span data-stu-id="016da-114">The audio sample data to which *buffer* points is still 'owned' by the app and must remain allocated and accessible until the sound stops playing.</span></span>

     

5.  <span data-ttu-id="016da-115">Utilice la función [**iniciar**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) para iniciar la voz de origen.</span><span class="sxs-lookup"><span data-stu-id="016da-115">Use the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function to start the source voice.</span></span> <span data-ttu-id="016da-116">Dado que todas las voces de XAudio2 envían su salida a la voz de masterización de forma predeterminada, el audio de la voz de origen se convierte automáticamente en el dispositivo de audio seleccionado en la inicialización.</span><span class="sxs-lookup"><span data-stu-id="016da-116">Since all XAudio2 voices send their output to the mastering voice by default, audio from the source voice automatically makes its way to the audio device selected at initialization.</span></span> <span data-ttu-id="016da-117">En un gráfico de audio más complicado, la voz de origen tendría que especificar la voz a la que se debe enviar la salida.</span><span class="sxs-lookup"><span data-stu-id="016da-117">In a more complicated audio graph, the source voice would have to specify the voice to which its output should be sent.</span></span>
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a><span data-ttu-id="016da-118">Notas para aplicaciones de la tienda Windows</span><span class="sxs-lookup"><span data-stu-id="016da-118">Notes for Windows Store apps</span></span>

<span data-ttu-id="016da-119">Se recomienda usar un [puntero inteligente](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) para administrar la duración de los objetos de XAUDIO2 de una manera segura de excepciones.</span><span class="sxs-lookup"><span data-stu-id="016da-119">We recommend that you make use of a [smart pointer](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) to manage the lifetime of XAUDIO2 objects in an exception safe manner.</span></span> <span data-ttu-id="016da-120">En el caso de las aplicaciones de la tienda Windows, puede usar la plantilla de puntero inteligente [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) de la biblioteca de plantillas de C++ Windows Runtime (WRL).</span><span class="sxs-lookup"><span data-stu-id="016da-120">For Windows Store apps, you can use the [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) smart pointer template from the Windows Runtime C++ Template Library (WRL).</span></span>


```
Microsoft::WRL::ComPtr<IXAudio2SourceVoice> SourceVoice;
HRESULT hr;
if( FAILED(hr = pXAudio2->CreateSourceVoice( &SourceVoice, (WAVEFORMATEX*)&wfx ) ) )
    throw Platform::Exception::CreateException(hr); 

if( FAILED(hr = SourceVoice->SubmitSourceBuffer( &buffer ) ) )
    throw Platform::Exception::CreateException(hr); 

if ( FAILED(hr = SourceVoice->Start( 0 ) ) )
    throw Platform::Exception::CreateException(hr);
```



> [!Note]  
> <span data-ttu-id="016da-121">Asegúrese de que todos los punteros inteligentes a objetos de XAUDIO2 se liberan por completo antes de liberar el objeto [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .</span><span class="sxs-lookup"><span data-stu-id="016da-121">Ensure that all smart pointers to XAUDIO2 objects are fully released before you release the [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="016da-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="016da-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="016da-123">Introducción de XAudio2</span><span class="sxs-lookup"><span data-stu-id="016da-123">XAudio2 Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="016da-124">Cómo: inicializar XAudio2</span><span class="sxs-lookup"><span data-stu-id="016da-124">How to: Initialize XAudio2</span></span>](how-to--initialize-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="016da-125">Cómo: cargar archivos de datos de audio en XAudio2</span><span class="sxs-lookup"><span data-stu-id="016da-125">How to: Load Audio Data Files in XAudio2</span></span>](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 

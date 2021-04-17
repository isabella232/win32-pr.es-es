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
# <a name="how-to-play-a-sound-with-xaudio2"></a>Cómo: reproducir un sonido con XAudio2

En este tema se describen los pasos mínimos necesarios para reproducir datos de audio cargados previamente en XAudio2. Después de inicializar XAudio2 (consulte [Cómo: inicializar xaudio2](how-to--initialize-xaudio2.md)) y cargar los datos de audio (consulte Cómo: [cargar archivos de datos de audio en XAudio2](how-to--load-audio-data-files-in-xaudio2.md)), puede reproducir un sonido mediante la creación de una voz de origen y el paso de datos de audio.

## <a name="to-play-a-sound"></a>Para reproducir un sonido

1.  Inicialice el motor de XAudio2 siguiendo los pasos descritos en [Cómo: inicializar xaudio2](how-to--initialize-xaudio2.md).
2.  Rellene una estructura [**de \_ búfer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) de [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) y XAUDIO2 siguiendo los pasos descritos en [Cómo: cargar archivos de datos de audio en XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md).
    > [!Note]  
    > Dependiendo del formato de los datos de audio, puede que tenga que usar una estructura de datos mayor que contenga una estructura [**WaveFormatEx**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) en lugar de una **WAVEFORMATEX**. Vea la página de referencia de **WAVEFORMATEX** para obtener más información.

     

3.  Cree una voz de origen llamando al método [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) en una instancia del motor de XAudio2. El formato de la voz se especifica mediante los valores establecidos en una estructura [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) .
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  Envíe un [**\_ búfer de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) a la voz de origen mediante la función [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > Los datos de ejemplo de audio a los que la aplicación todavía "posee" los puntos de *búfer* y deben permanecer asignados y accesibles hasta que el sonido deje de reproducirse.

     

5.  Utilice la función [**iniciar**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) para iniciar la voz de origen. Dado que todas las voces de XAudio2 envían su salida a la voz de masterización de forma predeterminada, el audio de la voz de origen se convierte automáticamente en el dispositivo de audio seleccionado en la inicialización. En un gráfico de audio más complicado, la voz de origen tendría que especificar la voz a la que se debe enviar la salida.
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Notas para aplicaciones de la tienda Windows

Se recomienda usar un [puntero inteligente](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) para administrar la duración de los objetos de XAUDIO2 de una manera segura de excepciones. En el caso de las aplicaciones de la tienda Windows, puede usar la plantilla de puntero inteligente [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) de la biblioteca de plantillas de C++ Windows Runtime (WRL).


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
> Asegúrese de que todos los punteros inteligentes a objetos de XAUDIO2 se liberan por completo antes de liberar el objeto [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción de XAudio2](getting-started.md)
</dt> <dt>

[Cómo: inicializar XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[Cómo: cargar archivos de datos de audio en XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 

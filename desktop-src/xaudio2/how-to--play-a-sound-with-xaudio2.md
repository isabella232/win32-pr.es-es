---
description: En este tema se describen los pasos mínimos necesarios para reproducir datos de audio cargados previamente en XAudio2.
ms.assetid: 5172b31c-d2af-45aa-5bd4-b62502f3c047
title: 'Cómo: reproducir un sonido con XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cfa5cb2a7a47b7fb54e6a7e9f098a545b0c630c6c27889d7aa6eff1242121d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082919"
---
# <a name="how-to-play-a-sound-with-xaudio2"></a>Cómo: reproducir un sonido con XAudio2

En este tema se describen los pasos mínimos necesarios para reproducir datos de audio cargados previamente en XAudio2. Después de inicializar XAudio2 (vea Cómo: Inicializar [XAudio2)](how-to--initialize-xaudio2.md)y cargar los datos de audio (vea Cómo: Cargar archivos de datos de audio en [XAudio2),](how-to--load-audio-data-files-in-xaudio2.md)puede reproducir un sonido creando una voz de origen y pasando datos de audio a él.

## <a name="to-play-a-sound"></a>Para reproducir un sonido

1.  Inicialice el motor XAudio2 siguiendo los pasos descritos [en Cómo: Inicializar XAudio2.](how-to--initialize-xaudio2.md)
2.  Rellene una [**estructura DE BÚFERES DE FORMAPOATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) y [**XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) siguiendo los pasos descritos en Cómo: Cargar archivos de datos de [audio en XAudio2.](how-to--load-audio-data-files-in-xaudio2.md)
    > [!Note]  
    > Según el formato de los datos de audio, es posible que deba usar una estructura de datos más grande que contenga una estructura [**DE FORMA DESATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) en lugar de **UNA FORMA DE ONDAATEX**. Para más información, consulte la página de referencia de **LAATEX.**

     

3.  Cree una voz de origen llamando al método [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) en una instancia del motor XAudio2. El formato de la voz se especifica mediante los valores establecidos en una [**estructura DESATEX.**](/windows/win32/api/mmreg/ns-mmreg-waveformatex)
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  Envíe un [**búfer de XAUDIO2 \_ a**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) la voz de origen mediante la [**función SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > Los datos de  ejemplo de audio en los que los puntos de búfer siguen siendo "propiedad" de la aplicación y deben permanecer asignados y accesibles hasta que el sonido deje de reproducirse.

     

5.  Use la [**función Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) para iniciar la voz de origen. Puesto que todas las voces de XAudio2 envían su salida a la voz maestra de forma predeterminada, el audio de la voz de origen se abre automáticamente al dispositivo de audio seleccionado en la inicialización. En un gráfico de audio más complicado, la voz de origen tendría que especificar la voz a la que se debe enviar su salida.
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Notas de las Windows store

Se recomienda usar un [](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) puntero inteligente para administrar la duración de los objetos XAUDIO2 de forma segura para excepciones. Para Windows store, puede usar la plantilla de puntero inteligente [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) de la biblioteca de plantillas de C++ (WRL) de Windows Runtime.


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
> Asegúrese de que todos los punteros inteligentes a objetos XAUDIO2 estén totalmente liberados antes de liberar el [**objeto IXAudio2.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[XAudio2 Tareas iniciales](getting-started.md)
</dt> <dt>

[Cómo: inicializar XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[Cómo: cargar archivos de datos de audio en XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 

---
description: En este artículo se presentan algunos ejemplos sencillos que muestran cómo implementar el sonido espacial mediante objetos de audio espacial estáticos, objetos de audio espacial dinámico y objetos de audio espacial que usan la función de transferencia relativa de la cabeza (HRTF) de Microsoft.
ms.assetid: C99C342E-0BD9-486A-92AA-F8DCB72C1B00
title: Representación del sonido espacial mediante objetos de audio espacial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd541026aa3e144ec8333c8ac045a17970735f17
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164846"
---
# <a name="render-spatial-sound-using-spatial-audio-objects"></a>Representación del sonido espacial mediante objetos de audio espacial

En este artículo se presentan algunos ejemplos sencillos que muestran cómo implementar el sonido espacial mediante objetos de audio espacial estáticos, objetos de audio espacial dinámico y objetos de audio espacial que usan la función de transferencia relativa de la cabeza (HRTF) de Microsoft. Los pasos de implementación de las tres técnicas son muy similares y en este artículo se proporciona un ejemplo de código estructurado de forma similar para cada técnica. Para obtener ejemplos completos de implementaciones de audio espacial del mundo real, consulte el repositorio [de GitHub de](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio)ejemplos de sonido espacial de Microsoft . Para obtener información general sobre Windows Sonic, la solución de nivel de plataforma de Microsoft para la compatibilidad con el sonido espacial en Xbox y Windows, consulte [Spatial Sound](spatial-sound.md).

## <a name="render-audio-using-static-spatial-audio-objects"></a>Representación de audio mediante objetos de audio espacial estáticos

Un objeto de audio estático se usa para representar el sonido en uno de los 18 canales de audio estáticos definidos en la [**enumeración AudioObjectType.**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) Cada uno de estos canales representa un altavoz real o virtualizado en un punto fijo del espacio que no se mueve con el tiempo. Los canales estáticos que están disponibles en un dispositivo determinado dependen del formato de sonido espacial que se esté utilizando. Para obtener una lista de los formatos admitidos y sus recuentos de canales, vea [Sonido espacial](spatial-sound.md).

Al inicializar una secuencia de audio espacial, debe especificar cuál de los canales estáticos disponibles usará la secuencia. Las siguientes definiciones de constantes de ejemplo se pueden usar para especificar configuraciones comunes del hablante y obtener el número de canales disponibles para cada uno.


```C++
const AudioObjectType ChannelMask_Mono = AudioObjectType_FrontCenter;
const AudioObjectType ChannelMask_Stereo = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight);
const AudioObjectType ChannelMask_2_1 = (AudioObjectType)(ChannelMask_Stereo | AudioObjectType_LowFrequency);
const AudioObjectType ChannelMask_Quad = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight | AudioObjectType_BackLeft | AudioObjectType_BackRight);
const AudioObjectType ChannelMask_4_1 = (AudioObjectType)(ChannelMask_Quad | AudioObjectType_LowFrequency);
const AudioObjectType ChannelMask_5_1 = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight | AudioObjectType_FrontCenter | AudioObjectType_LowFrequency | AudioObjectType_SideLeft | AudioObjectType_SideRight);
const AudioObjectType ChannelMask_7_1 = (AudioObjectType)(ChannelMask_5_1 | AudioObjectType_BackLeft | AudioObjectType_BackRight);

const UINT32 MaxStaticObjectCount_7_1_4 = 12;
const AudioObjectType ChannelMask_7_1_4 = (AudioObjectType)(ChannelMask_7_1 | AudioObjectType_TopFrontLeft | AudioObjectType_TopFrontRight | AudioObjectType_TopBackLeft | AudioObjectType_TopBackRight);

const UINT32 MaxStaticObjectCount_7_1_4_4 = 16;
const AudioObjectType ChannelMask_7_1_4_4 = (AudioObjectType)(ChannelMask_7_1_4 | AudioObjectType_BottomFrontLeft | AudioObjectType_BottomFrontRight |AudioObjectType_BottomBackLeft | AudioObjectType_BottomBackRight);

const UINT32 MaxStaticObjectCount_8_1_4_4 = 17;
const AudioObjectType ChannelMask_8_1_4_4 = (AudioObjectType)(ChannelMask_7_1_4_4 | AudioObjectType_BackCenter);
```



El primer paso para representar el audio espacial es obtener el punto de conexión de audio al que se enviarán los datos de audio. Cree una instancia de [**MMDeviceEnumerator y**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) llame a [**GetDefaultAudioEndpoint para**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) obtener el dispositivo de representación de audio predeterminado.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Al crear una secuencia de audio espacial, debe especificar el formato de audio que usará la secuencia proporcionando una [estructura DESATEX.](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) Si va a reproducir audio desde un archivo, el formato normalmente viene determinado por el formato del archivo de audio. En este ejemplo se usa un formato mono de 32 bits y 48Hz.


```C++
WAVEFORMATEX format;
format.wFormatTag = WAVE_FORMAT_IEEE_FLOAT;
format.wBitsPerSample = 32;
format.nChannels = 1;
format.nSamplesPerSec = 48000;
format.nBlockAlign = (format.wBitsPerSample >> 3) * format.nChannels;
format.nAvgBytesPerSec = format.nBlockAlign * format.nSamplesPerSec;
format.cbSize = 0;
```



El siguiente paso en la representación de audio espacial es inicializar una secuencia de audio espacial. En primer lugar, obtenga una instancia de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) mediante una [**llamada a IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Llame [**a ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) para asegurarse de que se admite el formato de audio que está usando. Cree un evento que la canalización de audio usará para notificar a la aplicación que está lista para más datos de audio.

Rellene una [**estructura SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) que se usará para inicializar la secuencia de audio espacial. En este ejemplo, el campo **StaticObjectTypeMask** se establece en la constante **ChannelMask \_ Stereo** definida anteriormente en este artículo, lo que significa que la secuencia de audio solo puede usar los canales derecho e izquierdo. Dado que en este ejemplo solo se usan objetos de audio estáticos y no objetos dinámicos, el **campo MaxDynamicObjectCount** se establece en 0. El **campo** Categoría se establece en un miembro de la enumeración [**AUDIO STREAM \_ \_ CATEGORY,**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) que define cómo el sistema mezcla el sonido de esta secuencia con otros orígenes de audio.

Llame [**a ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) para activar la secuencia.


```C++
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;

// Activate ISpatialAudioClient on the desired audio-device 
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = ChannelMask_Stereo;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = 0;
streamParams.Category = AudioCategory_SoundEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT activationParams;
PropVariantInit(&activationParams);
activationParams.vt = VT_BLOB;
activationParams.blob.cbSize = sizeof(streamParams);
activationParams.blob.pBlobData = reinterpret_cast<BYTE *>(&streamParams);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;
hr = spatialAudioClient->ActivateSpatialAudioStream(&activationParams, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);
```



> [!Note]  
> Al usar las interfaces [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) en un título del Kit de desarrollo de Xbox One (XDK), primero debe llamar a **EnableSpatialAudio** antes de llamar a [**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) o [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Si no lo hace, se devolverá un \_ error E NOINTERFACE de la llamada a Activate. **EnableSpatialAudio** solo está disponible para los títulos de XDK y no es necesario llamar a para las aplicaciones de plataforma universal de Windows que se ejecutan en Xbox One ni para dispositivos que no Xbox One.

 

Declare un puntero para un [**objeto ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) que se usará para escribir datos de audio en un canal estático. Las aplicaciones típicas usarán un objeto para cada canal especificado en el **campo StaticObjectTypeMask.** Para simplificar, en este ejemplo solo se usa un único objeto de audio estático.


```C++
// In this simple example, one object will be rendered
Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObjectFrontLeft;
```



Antes de entrar en el bucle de representación de audio, llame a [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) para indicar a la canalización multimedia que empiece a solicitar datos de audio. En este ejemplo se usa un contador para detener la representación de audio después de 5 segundos.

Dentro del bucle de representación, espere a que se señale el evento de finalización del búfer, proporcionado cuando se inicializó la secuencia de audio espacial. Debe establecer un límite de tiempo de espera razonable, como 100 ms, al esperar al evento porque cualquier cambio en el tipo de representación o el punto de conexión hará que ese evento nunca se señale. En este caso, puede llamar a [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) para intentar restablecer la secuencia de audio espacial.

A continuación, llame a [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) para que el sistema sepa que está a punto de rellenar los búferes de los objetos de audio con datos. Este método devuelve el número de objetos de audio dinámicos disponibles, no utilizados en este ejemplo, y el número de fotogramas del búfer para los objetos de audio representados por esta secuencia.

Si aún no se ha creado un objeto de audio espacial estático, cree uno o varios llamando a [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), pasando un valor de la enumeración [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) que indica el canal estático en el que se representa el audio del objeto.

A continuación, llame a [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) para obtener un puntero al búfer de audio del objeto de audio espacial. Este método también devuelve el tamaño del búfer, en bytes. En este ejemplo se usa un método auxiliar, **WriteToAudioObjectBuffer,** para rellenar el búfer con datos de audio. Este método se muestra más adelante en este artículo. Después de escribir en el búfer, el ejemplo comprueba si se ha alcanzado la duración de 5 segundos del objeto y, si es así, se llama a [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) para que la canalización de audio sepa que no se escribirá más audio con este objeto y el objeto está establecido en **nullptr** para liberar sus recursos.

Después de escribir datos en todos los objetos de audio, llame a [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) para que el sistema sepa que los datos están listos para la representación. Solo puede llamar a **GetBuffer** entre una llamada a **BeginUpdatingAudioObjects** y **EndUpdatingAudioObjects**.


```C++
// Start streaming / rendering 
hr = spatialAudioStream->Start();

// This example will render 5 seconds of audio samples
UINT totalFrameCount = format.nSamplesPerSec * 5;

bool isRendering = true;
while (isRendering)
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        hr = spatialAudioStream->Reset();

        if (hr != S_OK)
        {
            // handle the error
            break;
        }
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of dynamic objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStream->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    if (audioObjectFrontLeft == nullptr)
    {
        hr = spatialAudioStream->ActivateSpatialAudioObject(AudioObjectType::AudioObjectType_FrontLeft, &audioObjectFrontLeft);
        if (hr != S_OK) break;
    }

    // Get the buffer to write audio data
    hr = audioObjectFrontLeft->GetBuffer(&buffer, &bufferLength);

    if (totalFrameCount >= frameCount)
    {
        // Write audio data to the buffer
        WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, 200.0f, format.nSamplesPerSec);

        totalFrameCount -= frameCount;
    }
    else
    {
        // Write audio data to the buffer
        WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), totalFrameCount, 750.0f, format.nSamplesPerSec);

        // Set end of stream for the last buffer 
        hr = audioObjectFrontLeft->SetEndOfStream(totalFrameCount);

        audioObjectFrontLeft = nullptr; // Release the object

        isRendering = false;
    }

    // Let the audio engine know that the object data are available for processing now
    hr = spatialAudioStream->EndUpdatingAudioObjects();
};
```



Cuando haya terminado de representar audio espacial, detenga la secuencia de audio espacial mediante una llamada a [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop). Si no va a volver a usar la secuencia, libera sus recursos mediante una llamada a [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).


```C++
// Stop the stream
hr = spatialAudioStream->Stop();

// Don't want to start again, so reset the stream to free its resources
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



El **método auxiliar WriteToAudioObjectBuffer** escribe un búfer completo de muestras o el número de muestras restantes especificado por nuestro límite de tiempo definido por la aplicación. Esto también podría determinarse, por ejemplo, por el número de muestras restantes en un archivo de audio de origen. Se genera una onda sincrómica simple, cuya frecuencia se escala mediante el parámetro de entrada *frequency,* y se escribe en el búfer.


```C++
void WriteToAudioObjectBuffer(FLOAT* buffer, UINT frameCount, FLOAT frequency, UINT samplingRate)
{
    const double PI = 4 * atan2(1.0, 1.0);
    static double _radPhase = 0.0;

    double step = 2 * PI * frequency / samplingRate;

    for (UINT i = 0; i < frameCount; i++)
    {
        double sample = sin(_radPhase);

        buffer[i] = FLOAT(sample);

        _radPhase += step; // next frame phase

        if (_radPhase >= 2 * PI)
        {
            _radPhase -= 2 * PI;
        }
    }
}
```



## <a name="render-audio-using-dynamic-spatial-audio-objects"></a>Representación de audio mediante objetos de audio espacial dinámico

Los objetos dinámicos permiten representar audio desde una posición arbitraria en el espacio, en relación con el usuario. La posición y el volumen de un objeto de audio dinámico se pueden cambiar con el tiempo. Los juegos normalmente usarán la posición de un objeto 3D en el mundo del juego para especificar la posición del objeto de audio dinámico asociado a él. En el ejemplo siguiente se usará una estructura simple, **My3dObject**, para almacenar el conjunto mínimo de datos necesarios para representar un objeto . Estos datos incluyen un puntero a [**un objeto ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), la posición, la velocidad, el volumen y la frecuencia de tono del objeto y un valor que almacena el número total de fotogramas para los que el objeto debe representar el sonido.


```C++
struct My3dObject
{
    Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObject;
    Windows::Foundation::Numerics::float3 position;
    Windows::Foundation::Numerics::float3 velocity;
    float volume;
    float frequency; // in Hz
    UINT totalFrameCount;
};
```



Los pasos de implementación de los objetos de audio dinámicos son en gran medida los mismos que los pasos para los objetos de audio estáticos descritos anteriormente. En primer lugar, obtenga un punto de conexión de audio.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



A continuación, inicialice la secuencia de audio espacial. Obtenga una instancia de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) mediante una llamada [**a IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Llame [**a ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) para asegurarse de que se admite el formato de audio que está usando. Cree un evento que la canalización de audio usará para notificar a la aplicación que está lista para más datos de audio.

Llame [**a ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) para recuperar el número de objetos dinámicos admitidos por el sistema. Si esta llamada devuelve 0, los objetos de audio espacial dinámico no se admiten ni se habilitan en el dispositivo actual. Para obtener información sobre cómo habilitar el audio espacial y para obtener más información sobre el número de objetos de audio dinámico disponibles para diferentes formatos de audio espacial, vea [Spatial Sound](spatial-sound.md).

Al rellenar la estructura [**SpatialAudioObjectRenderStreamActivationParams,**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) establezca el campo **MaxDynamicObjectCount** en el número máximo de objetos dinámicos que usará la aplicación.

Llame [**a ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) para activar la secuencia.


```C++
// Activate ISpatialAudioClient on the desired audio-device 
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

UINT32 maxDynamicObjectCount;
hr = spatialAudioClient->GetMaxDynamicObjectCount(&maxDynamicObjectCount);

if (maxDynamicObjectCount == 0)
{
    // Dynamic objects are unsupported
    return;
}

// Set the maximum number of dynamic audio objects that will be used
SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = AudioObjectType_None;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = min(maxDynamicObjectCount, 4);
streamParams.Category = AudioCategory_GameEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT pv;
PropVariantInit(&pv);
pv.vt = VT_BLOB;
pv.blob.cbSize = sizeof(streamParams);
pv.blob.pBlobData = (BYTE *)&streamParams;

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;;
hr = spatialAudioClient->ActivateSpatialAudioStream(&pv, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);
```



A continuación se muestra algún código específico de la aplicación para admitir este ejemplo, que genera dinámicamente objetos de audio posicionados aleatoriamente y los almacena en un vector.


```C++
// Used for generating a vector of randomized My3DObject structs
std::vector<My3dObject> objectVector;
std::default_random_engine gen;
std::uniform_real_distribution<> pos_dist(-25, 25); // uniform distribution for random position
std::uniform_real_distribution<> vel_dist(-1, 1); // uniform distribution for random velocity
std::uniform_real_distribution<> vol_dist(0.5, 1.0); // uniform distribution for random volume
std::uniform_real_distribution<> pitch_dist(40, 400); // uniform distribution for random pitch
int spawnCounter = 0;
```



Antes de entrar en el bucle de representación de audio, llame a [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) para indicar a la canalización multimedia que empiece a solicitar datos de audio.

Dentro del bucle de representación, espere a que se señale el evento de finalización del búfer que proporcionamos cuando se inicializó la secuencia de audio espacial. Debe establecer un límite de tiempo de espera razonable, como 100 ms, al esperar al evento porque cualquier cambio en el tipo de representación o el punto de conexión hará que ese evento nunca se señale. En este caso, puede llamar a [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) para intentar restablecer la secuencia de audio espacial.

A continuación, llame a [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) para que el sistema sepa que está a punto de rellenar los búferes de los objetos de audio con datos. Este método devuelve el número de objetos de audio dinámicos disponibles y el número de fotogramas del búfer para los objetos de audio representados por esta secuencia.

Cada vez que el contador de generación alcance el valor especificado, activaremos un nuevo objeto de audio dinámico mediante una llamada a [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) especificando [**AudioObjectType \_ Dynamic.**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) Si ya se han asignado todos los objetos de audio dinámico disponibles, este método devolverá **SPLAUDCLNT \_ E NO MORE \_ \_ \_ OBJECTS**. En este caso, puede elegir liberar uno o varios objetos de audio previamente activados en función de la priorización específica de la aplicación. Una vez creado el objeto de audio dinámico, se agrega a una nueva estructura **My3dObject,** con valores aleatorios de posición, velocidad, volumen y frecuencia, que luego se agregan a la lista de objetos activos.

A continuación, itera todos los objetos activos, representados en este ejemplo con la **estructura My3dObject** definida por la aplicación. Para cada objeto de audio, llame a [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) para obtener un puntero al búfer de audio del objeto de audio espacial. Este método también devuelve el tamaño del búfer, en bytes. Método auxiliar, **WriteToAudioObjectBuffer,** para rellenar el búfer con datos de audio. Después de escribir en el búfer, el ejemplo actualiza la posición del objeto de audio dinámico llamando a [**ISpatialAudioObject::SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition). El volumen del objeto de audio también se puede modificar llamando a [**SetVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume). Si no actualiza la posición o el volumen del objeto, conservará la posición y el volumen desde la última vez que se estableció. Si se ha alcanzado la duración definida por la aplicación del objeto, se llama a [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) para que la canalización de audio sepa que no se escribirá más audio con este objeto y el objeto se establece en **nullptr** para liberar sus recursos.

Después de escribir datos en todos los objetos de audio, llame a [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) para que el sistema sepa que los datos están listos para la representación. Solo puede llamar a **GetBuffer** entre una llamada a **BeginUpdatingAudioObjects** y **EndUpdatingAudioObjects**.


```C++
// Start streaming / rendering 
hr = spatialAudioStream->Start();

do
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        break;
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of active objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStream->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    // Spawn a new dynamic audio object every 200 iterations
    if (spawnCounter % 200 == 0 && spawnCounter < 1000)
    {
        // Activate a new dynamic audio object
        Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObject;
        hr = spatialAudioStream->ActivateSpatialAudioObject(AudioObjectType::AudioObjectType_Dynamic, &audioObject);

        // If SPTLAUDCLNT_E_NO_MORE_OBJECTS is returned, there are no more available objects
        if (SUCCEEDED(hr))
        {
            // Init new struct with the new audio object.
            My3dObject obj = {
                audioObject,
                Windows::Foundation::Numerics::float3(static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen))),
                Windows::Foundation::Numerics::float3(static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen))),
                static_cast<float>(static_cast<float>(vol_dist(gen))),
                static_cast<float>(static_cast<float>(pitch_dist(gen))),
                format.nSamplesPerSec * 5 // 5 seconds of audio samples
            };

            objectVector.insert(objectVector.begin(), obj);
        }
    }
    spawnCounter++;

    // Loop through all dynamic audio objects
    std::vector<My3dObject>::iterator it = objectVector.begin();
    while (it != objectVector.end())
    {
        it->audioObject->GetBuffer(&buffer, &bufferLength);

        if (it->totalFrameCount >= frameCount)
        {
            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, it->frequency, format.nSamplesPerSec);

            // Update the position and volume of the audio object
            it->audioObject->SetPosition(it->position.x, it->position.y, it->position.z);
            it->position += it->velocity;
            it->audioObject->SetVolume(it->volume);

            it->totalFrameCount -= frameCount;

            ++it;
        }
        else
        {
            // If the audio object reaches its lifetime, set EndOfStream and release the object

            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), it->totalFrameCount, it->frequency, format.nSamplesPerSec);

            // Set end of stream for the last buffer 
            hr = it->audioObject->SetEndOfStream(it->totalFrameCount);

            it->audioObject = nullptr; // Release the object

            it->totalFrameCount = 0;

            it = objectVector.erase(it);
        }
    }

    // Let the audio-engine know that the object data are available for processing now
    hr = spatialAudioStream->EndUpdatingAudioObjects();
} while (objectVector.size() > 0);
```



Cuando haya terminado de representar audio espacial, detenga la secuencia de audio espacial mediante una llamada a [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop). Si no va a volver a usar la secuencia, libera sus recursos mediante una llamada a [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).


```C++
// Stop the stream 
hr = spatialAudioStream->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



## <a name="render-audio-using-dynamic-spatial-audio-objects-for-hrtf"></a>Representación de audio mediante objetos de audio espacial dinámico para HRTF

Otro conjunto de API, [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) e [**ISpatialAudioObjectForHrtf,**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf)habilitan el audio espacial que usa la función de transferencia relativa a la cabeza (HRTF) de Microsoft para atenuar los sonidos para simular la posición del emisor en el espacio, en relación con el usuario, que se puede cambiar con el tiempo. Además de la posición, los objetos de audio HRTF permiten especificar una orientación en el espacio, una directividad en la que se emite el sonido, como una forma de cono o de cono, y un modelo de decadencia a medida que el objeto se mueve cada vez más cerca del agente de escucha virtual. Tenga en cuenta que estas interfaces HRTF solo están disponibles cuando el usuario ha seleccionado Windows Sonic para auriculares como motor de audio espacial para el dispositivo. Para obtener información sobre cómo configurar un dispositivo para que use Windows Sonic para auriculares, vea [Spatial Sound](spatial-sound.md).

Las API [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) e [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) permiten a una aplicación usar explícitamente la ruta de acceso Windows Sonic para auriculares representación directa. Estas API no admiten formatos de sonido espacial, como Dolby Atmos for Home Theater o Dolby Atmos for Headphones, ni la conmutación de formato de salida controlada por el consumidor a través del panel de **control** Sonido ni la reproducción en altavoces. Estas interfaces están diseñadas para su uso en aplicaciones de Windows Mixed Reality que desean usar funcionalidades específicas de Windows Sonic para auriculares (como valores preestablecidos del entorno y lanzamiento basado en distancia especificados mediante programación, fuera de las canalizaciones de creación de contenido típicas). La mayoría de los juegos y escenarios de realidad virtual prefieren usar [**ISpatialAudioClient en su**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) lugar. Los pasos de implementación de ambos conjuntos de API son casi idénticos, por lo que es posible implementar ambas tecnologías y cambiar en tiempo de ejecución en función de la característica disponible en el dispositivo actual.

Las aplicaciones de realidad mixta normalmente usarán la posición de un objeto 3D en el mundo virtual para especificar la posición del objeto de audio dinámico asociado a él. En el ejemplo siguiente se usará una estructura simple, **My3dObjectForHrtf,** para almacenar el conjunto mínimo de datos necesarios para representar un objeto . Estos datos incluyen un puntero a [**un objeto ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), la posición, la orientación, la velocidad y la frecuencia de tono del objeto y un valor que almacena el número total de fotogramas para los que el objeto debe representar el sonido.


```C++
struct My3dObjectForHrtf
{
    Microsoft::WRL::ComPtr<ISpatialAudioObjectForHrtf> audioObject;
    Windows::Foundation::Numerics::float3 position;
    Windows::Foundation::Numerics::float3 velocity;
    float yRotationRads;
    float deltaYRotation;
    float frequency; // in Hz
    UINT totalFrameCount;
};
```



Los pasos de implementación de los objetos de audio HRTF dinámicos son en gran medida los mismos que los pasos para los objetos de audio dinámicos descritos en la sección anterior. En primer lugar, obtenga un punto de conexión de audio.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



A continuación, inicialice la secuencia de audio espacial. Obtenga una instancia de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) llamando a [**IMMDevice::Activate.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) Llame [**a ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) para asegurarse de que se admite el formato de audio que está usando. Cree un evento que la canalización de audio usará para notificar a la aplicación que está lista para más datos de audio.

Llame [**a ISpatialAudioClient::GetMaxDynamicObjectCount para**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) recuperar el número de objetos dinámicos admitidos por el sistema. Si esta llamada devuelve 0, los objetos de audio espacial dinámico no se admiten ni se habilitan en el dispositivo actual. Para obtener información sobre cómo habilitar el audio espacial y para obtener más información sobre el número de objetos de audio dinámicos disponibles para diferentes formatos de audio espacial, vea [Sonido espacial](spatial-sound.md).

Al rellenar la estructura [**SpatialAudioHrtfActivationParams,**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) establezca el **campo MaxDynamicObjectCount** en el número máximo de objetos dinámicos que usará la aplicación. Los parámetros de activación para HRTF admiten algunos parámetros adicionales, como [**SpatialAudioHrtfDistanceDecay,**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay) [**SpatialAudioHrtfDirectivityUnion,**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion) [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype)y [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), que especifican los valores predeterminados de estos valores para los nuevos objetos creados a partir de la secuencia. Estos parámetros son opcionales. Establezca los campos en **nullptr para** no proporcionar valores predeterminados.

Llame [**a ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) para activar la secuencia.


```C++
// Activate ISpatialAudioClient on the desired audio-device 
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStreamForHrtf>  spatialAudioStreamForHrtf;
hr = spatialAudioClient->IsSpatialAudioStreamAvailable(__uuidof(spatialAudioStreamForHrtf), NULL);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

UINT32 maxDynamicObjectCount;
hr = spatialAudioClient->GetMaxDynamicObjectCount(&maxDynamicObjectCount);

SpatialAudioHrtfActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = AudioObjectType_None;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = min(maxDynamicObjectCount, 4);
streamParams.Category = AudioCategory_GameEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = NULL;

SpatialAudioHrtfDistanceDecay decayModel;
decayModel.CutoffDistance = 100;
decayModel.MaxGain = 3.98f;
decayModel.MinGain = float(1.58439 * pow(10, -5));
decayModel.Type = SpatialAudioHrtfDistanceDecayType::SpatialAudioHrtfDistanceDecay_NaturalDecay;
decayModel.UnityGainDistance = 1;

streamParams.DistanceDecay = &decayModel;

SpatialAudioHrtfDirectivity directivity;
directivity.Type = SpatialAudioHrtfDirectivityType::SpatialAudioHrtfDirectivity_Cone;
directivity.Scaling = 1.0f;

SpatialAudioHrtfDirectivityCone cone;
cone.directivity = directivity;
cone.InnerAngle = 0.1f;
cone.OuterAngle = 0.2f;

SpatialAudioHrtfDirectivityUnion directivityUnion;
directivityUnion.Cone = cone;
streamParams.Directivity = &directivityUnion;

SpatialAudioHrtfEnvironmentType environment = SpatialAudioHrtfEnvironmentType::SpatialAudioHrtfEnvironment_Large;
streamParams.Environment = &environment;

SpatialAudioHrtfOrientation orientation = { 1,0,0,0,1,0,0,0,1 }; // identity matrix
streamParams.Orientation = &orientation;

PROPVARIANT pv;
PropVariantInit(&pv);
pv.vt = VT_BLOB;
pv.blob.cbSize = sizeof(streamParams);
pv.blob.pBlobData = (BYTE *)&streamParams;

hr = spatialAudioClient->ActivateSpatialAudioStream(&pv, __uuidof(spatialAudioStreamForHrtf), (void**)&spatialAudioStreamForHrtf);
```



A continuación se muestra un código específico de la aplicación para admitir este ejemplo, que genera dinámicamente objetos de audio situados aleatoriamente y los almacena en un vector.


```C++
// Used for generating a vector of randomized My3DObject structs
std::vector<My3dObjectForHrtf> objectVector;
std::default_random_engine gen;
std::uniform_real_distribution<> pos_dist(-10, 10); // uniform distribution for random position
std::uniform_real_distribution<> vel_dist(-.02, .02); // uniform distribution for random velocity
std::uniform_real_distribution<> yRotation_dist(-3.14, 3.14); // uniform distribution for y-axis rotation
std::uniform_real_distribution<> deltaYRotation_dist(.01, .02); // uniform distribution for y-axis rotation
std::uniform_real_distribution<> pitch_dist(40, 400); // uniform distribution for random pitch

int spawnCounter = 0;
```



Antes de entrar en el bucle de representación de audio, llame a [**ISpatialAudioObjectRenderStreamForHrtf::Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) para indicar a la canalización multimedia que comience a solicitar datos de audio.

Dentro del bucle de representación, espere a que se señale el evento de finalización del búfer que se proporcionó cuando se inicializó la secuencia de audio espacial. Debe establecer un límite de tiempo de espera razonable, como 100 ms, al esperar al evento porque cualquier cambio en el tipo de representación o el punto de conexión hará que ese evento nunca se señale. En este caso, puede llamar a [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) para intentar restablecer la secuencia de audio espacial.

A continuación, llame a [**ISpatialAudioRenderStreamForHrtf::BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) para que el sistema sepa que está a punto de rellenar los búferes de los objetos de audio con datos. Este método devuelve el número de objetos de audio dinámicos disponibles, no utilizados en este ejemplo, y el número de fotogramas del búfer para los objetos de audio representados por esta secuencia.

Siempre que el contador de generación alcance el valor especificado, activaremos un nuevo objeto de audio dinámico llamando a [**ISpatialAudioRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) especificando [**AudioObjectType \_ Dynamic.**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) Si ya se han asignado todos los objetos de audio dinámico disponibles, este método devolverá **SPLAUDCLNT \_ E NO MORE \_ \_ \_ OBJECTS**. En este caso, puede optar por liberar uno o varios objetos de audio activados previamente en función de la priorización específica de la aplicación. Una vez creado el objeto de audio dinámico, se agrega a una nueva estructura **My3dObjectForHrtf,** con valores aleatorios de posición, rotación, velocidad, volumen y frecuencia, que se agregan a la lista de objetos activos.

A continuación, itera todos los objetos activos, representados en este ejemplo con la estructura **My3dObjectForHrtf** definida por la aplicación. Para cada objeto de audio, llame a [**ISpatialAudioObjectForHrtf::GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) para obtener un puntero al búfer de audio del objeto de audio espacial. Este método también devuelve el tamaño del búfer, en bytes. El método auxiliar **WriteToAudioObjectBuffer,** enumerado anteriormente en este artículo, para rellenar el búfer con datos de audio. Después de escribir en el búfer, el ejemplo actualiza la posición y la orientación del objeto de audio HRTF llamando a [**ISpatialAudioObjectForHrtf::SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) e [**ISpatialAudioObjectForHrtf::SetOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation). En este ejemplo, se usa un método auxiliar, **CalculateEmitterConeOrientationMatrix,** para calcular la matriz de orientación dada la dirección en la que apunta el objeto 3D. A continuación se muestra la implementación de este método. El volumen del objeto de audio también se puede modificar llamando a [**ISpatialAudioObjectForHrtf::SetGain**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain). Si no actualiza la posición, la orientación o el volumen del objeto, conservará la posición, la orientación y el volumen desde la última vez que se estableció. Si se ha alcanzado la duración definida por la aplicación del objeto, se llama a [**ISpatialAudioObjectForHrtf::SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) para que la canalización de audio sepa que no se escribirá más audio con este objeto y el objeto se establece en **nullptr** para liberar sus recursos.

Después de escribir datos en todos los objetos de audio, llame a [**ISpatialAudioRenderStreamForHrtf::EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) para que el sistema sepa que los datos están listos para la representación. Solo puede llamar a **GetBuffer** entre una llamada a **BeginUpdatingAudioObjects** y **EndUpdatingAudioObjects**.


```C++
// Start streaming / rendering 
hr = spatialAudioStreamForHrtf->Start();

do
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        break;
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of active objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStreamForHrtf->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    // Spawn a new dynamic audio object every 200 iterations
    if (spawnCounter % 200 == 0 && spawnCounter < 1000)
    {
        // Activate a new dynamic audio object
        Microsoft::WRL::ComPtr<ISpatialAudioObjectForHrtf> audioObject;
        hr = spatialAudioStreamForHrtf->ActivateSpatialAudioObjectForHrtf(AudioObjectType::AudioObjectType_Dynamic, &audioObject);

        // If SPTLAUDCLNT_E_NO_MORE_OBJECTS is returned, there are no more available objects
        if (SUCCEEDED(hr))
        {
            // Init new struct with the new audio object.
            My3dObjectForHrtf obj = { audioObject,
                Windows::Foundation::Numerics::float3(static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen))),
                Windows::Foundation::Numerics::float3(static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen))),
                static_cast<float>(static_cast<float>(yRotation_dist(gen))),
                static_cast<float>(static_cast<float>(deltaYRotation_dist(gen))),
                static_cast<float>(static_cast<float>(pitch_dist(gen))),
                format.nSamplesPerSec * 5 // 5 seconds of audio samples
            };

            objectVector.insert(objectVector.begin(), obj);
        }
    }
    spawnCounter++;

    // Loop through all dynamic audio objects
    std::vector<My3dObjectForHrtf>::iterator it = objectVector.begin();
    while (it != objectVector.end())
    {
        it->audioObject->GetBuffer(&buffer, &bufferLength);

        if (it->totalFrameCount >= frameCount)
        {
            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, it->frequency, format.nSamplesPerSec);

            // Update the position and volume of the audio object
            it->audioObject->SetPosition(it->position.x, it->position.y, it->position.z);
            it->position += it->velocity;


            Windows::Foundation::Numerics::float3 emitterDirection = Windows::Foundation::Numerics::float3(cos(it->yRotationRads), 0, sin(it->yRotationRads));
            Windows::Foundation::Numerics::float3 listenerDirection = Windows::Foundation::Numerics::float3(0, 0, 1);
            DirectX::XMFLOAT4X4 rotationMatrix;

            DirectX::XMMATRIX rotation = CalculateEmitterConeOrientationMatrix(emitterDirection, listenerDirection);
            XMStoreFloat4x4(&rotationMatrix, rotation);

            SpatialAudioHrtfOrientation orientation = {
                rotationMatrix._11, rotationMatrix._12, rotationMatrix._13,
                rotationMatrix._21, rotationMatrix._22, rotationMatrix._23,
                rotationMatrix._31, rotationMatrix._32, rotationMatrix._33
            };

            it->audioObject->SetOrientation(&orientation);
            it->yRotationRads += it->deltaYRotation;

            it->totalFrameCount -= frameCount;

            ++it;
        }
        else
        {
            // If the audio object reaches its lifetime, set EndOfStream and release the object

            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), it->totalFrameCount, it->frequency, format.nSamplesPerSec);

            // Set end of stream for the last buffer 
            hr = it->audioObject->SetEndOfStream(it->totalFrameCount);

            it->audioObject = nullptr; // Release the object

            it->totalFrameCount = 0;

            it = objectVector.erase(it);
        }
    }

    // Let the audio-engine know that the object data are available for processing now
    hr = spatialAudioStreamForHrtf->EndUpdatingAudioObjects();

} while (objectVector.size() > 0);
```



Cuando haya terminado de representar el audio espacial, detenga la secuencia de audio espacial llamando a [**ISpatialAudioRenderRenderStreamForHrtf::Stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)). Si no va a usar la secuencia de nuevo, libera sus recursos mediante una llamada a [**ISpatialAudioRenderRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).


```C++
// Stop the stream 
hr = spatialAudioStreamForHrtf->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStreamForHrtf->Reset();

CloseHandle(bufferCompletionEvent);
```



En el ejemplo de código siguiente se muestra la implementación del método auxiliar **CalculateEmitterConeOrientationMatrix** que se usó en el ejemplo anterior para calcular la matriz de orientación dada la dirección en la que apunta el objeto 3D.


```C++
DirectX::XMMATRIX CalculateEmitterConeOrientationMatrix(Windows::Foundation::Numerics::float3 listenerOrientationFront, Windows::Foundation::Numerics::float3 emitterDirection)
{
    DirectX::XMVECTOR vListenerDirection = DirectX::XMLoadFloat3(&listenerOrientationFront);
    DirectX::XMVECTOR vEmitterDirection = DirectX::XMLoadFloat3(&emitterDirection);
    DirectX::XMVECTOR vCross = DirectX::XMVector3Cross(vListenerDirection, vEmitterDirection);
    DirectX::XMVECTOR vDot = DirectX::XMVector3Dot(vListenerDirection, vEmitterDirection);
    DirectX::XMVECTOR vAngle = DirectX::XMVectorACos(vDot);
    float angle = DirectX::XMVectorGetX(vAngle);

    // The angle must be non-zero
    if (fabsf(angle) > FLT_EPSILON)
    {
        // And less than PI
        if (fabsf(angle) < DirectX::XM_PI)
        {
            return DirectX::XMMatrixRotationAxis(vCross, angle);
        }

        // If equal to PI, find any other non-collinear vector to generate the perpendicular vector to rotate about
        else
        {
            DirectX::XMFLOAT3 vector = { 1.0f, 1.0f, 1.0f };
            if (listenerOrientationFront.x != 0.0f)
            {
                vector.x = -listenerOrientationFront.x;
            }
            else if (listenerOrientationFront.y != 0.0f)
            {
                vector.y = -listenerOrientationFront.y;
            }
            else // if (_listenerOrientationFront.z != 0.0f)
            {
                vector.z = -listenerOrientationFront.z;
            }
            DirectX::XMVECTOR vVector = DirectX::XMLoadFloat3(&vector);
            vVector = DirectX::XMVector3Normalize(vVector);
            vCross = DirectX::XMVector3Cross(vVector, vEmitterDirection);
            return DirectX::XMMatrixRotationAxis(vCross, angle);
        }
    }

    // If the angle is zero, use an identity matrix
    return DirectX::XMMatrixIdentity();
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sonido espacial](spatial-sound.md)
</dt> <dt>

[**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)
</dt> <dt>

[**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)
</dt> </dl>

 

 

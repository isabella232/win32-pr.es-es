---
title: Tareas iniciales con XInput
description: XInput es una API que permite a las aplicaciones recibir entradas del controlador de Xbox para Windows. Se admiten los efectos de sonido del controlador y la entrada y salida de voz.
ms.assetid: 7b5eec3e-b3da-de5c-c926-8258c1418ef0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a9ca17e3046db676887290b9b9dcbb7318f2dc89d4dd9543cbe790bf271b60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962504"
---
# <a name="getting-started-with-xinput"></a>Tareas iniciales con XInput

XInput es una API que permite a las aplicaciones recibir entradas del controlador de Xbox para Windows. Se admiten los efectos de sonido del controlador y la entrada y salida de voz.

En este tema se proporciona una breve introducción a las funcionalidades de XInput y cómo configurarla en una aplicación. Incluye lo siguiente:

-   [Introducción a XInput](#introduction-to-xinput)
    -   [El controlador de Xbox](#the-xbox-controller)
-   [Uso de XInput](#using-xinput)
    -   [Varios controladores](#multiple-controllers)
    -   [Obtención del estado del controlador](#getting-controller-state)
    -   [Zona de desastres](#dead-zone)
    -   [Establecer efectos de vibración](#setting-vibration-effects)
    -   [Obtención de identificadores de dispositivo de audio](#getting-audio-device-identifiers)
    -   [Obtención de GUID de Direct Sound (solo SDK de DirectX heredado)](#getting-directsound-guids-legacy-directx-sdk-only)
-   [Temas relacionados](#related-topics)

## <a name="introduction-to-xinput"></a>Introducción a XInput

La consola Xbox usa un controlador de juegos que es compatible con Windows. Las aplicaciones pueden usar la API XInput para comunicarse con estos controladores cuando están conectados a un equipo Windows (se pueden conectar hasta cuatro controladores únicos a la vez).

Con esta API, se puede consultar cualquier controlador Xbox conectado para ver su estado y se pueden establecer efectos de vibración. Los controladores que tienen el casco conectado también se pueden consultar para los dispositivos de entrada y salida de sonido que se pueden usar con el casco para el procesamiento de voz.

### <a name="the-xbox-controller"></a>El controlador de Xbox

El controlador de Xbox tiene dos sticks direccionales análogos, cada uno con un botón digital, dos desencadenadores análogos, un panel direccional digital con cuatro direcciones y ocho botones digitales. Los estados de cada una de estas entradas se devuelven en la estructura [**\_ XINPUT GAMEPAD**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) cuando se llama a la función [**XInputGetState.**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate)

El controlador también tiene dos motores de vibración para proporcionar al usuario efectos de comentarios de fuerza. Las velocidades de estos motores se especifican en la estructura [**vibration de XINPUT \_**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) que se pasa a la función [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) para establecer los efectos de vibración.

Opcionalmente, se puede conectar un casco al controlador. El casco tiene un micrófono para la entrada de voz y un auricular para la salida de sonido. Puede llamar a la función [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) o a la función [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) heredada para obtener los identificadores de dispositivo correspondientes a los dispositivos del micrófono y el micrófono. A continuación, puede usar [core Audio API para](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) recibir entradas de voz y enviar salidas de sonido.

## <a name="using-xinput"></a>Uso de XInput

El uso de XInput es tan sencillo como llamar a las funciones XInput según sea necesario. Con las funciones XInput, puede recuperar el estado del controlador, obtener los IDs de audio de los cascos y establecer los efectos del controlador.

### <a name="multiple-controllers"></a>Varios controladores

La API XInput admite hasta cuatro controladores conectados en cualquier momento. Todas las funciones XInput requieren un *parámetro dwUserIndex* que se pasa para identificar el controlador que se está configurando o consultando. Este identificador estará en el intervalo de 0 a 3 y XInput lo establecerá automáticamente. El número corresponde al puerto al que está conectado el controlador y no se puede modifica.

Cada controlador muestra el identificador que usa al encender un cuadrante en el "anillo de luz" en el centro del controlador. Un *valor dwUserIndex* de 0 corresponde al cuadrante superior izquierdo; la numeración continúa alrededor del anillo en el sentido de las agujas del reloj.

Las aplicaciones deben admitir varios controladores.

### <a name="getting-controller-state"></a>Obtención del estado del controlador

A lo largo de la duración de una aplicación, es probable que la obtención del estado de un controlador se haga con más frecuencia. De marco a marco en una aplicación de juego, se debe recuperar el estado y actualizar la información del juego para reflejar los cambios del controlador.

Para recuperar el estado, use la [**función XInputGetState:**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate)

```cpp
DWORD dwResult;    
for (DWORD i=0; i< XUSER_MAX_COUNT; i++ )
{
    XINPUT_STATE state;
    ZeroMemory( &state, sizeof(XINPUT_STATE) );

    // Simply get the state of the controller from XInput.
    dwResult = XInputGetState( i, &state );

    if( dwResult == ERROR_SUCCESS )
    {
        // Controller is connected
    }
    else
    {
        // Controller is not connected
    }
}
```

Tenga en cuenta que el valor devuelto [**de XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) se puede usar para determinar si el controlador está conectado. Las aplicaciones deben definir una estructura para contener información interna del controlador. Esta información debe compararse con los resultados de **XInputGetState** para determinar qué cambios, como las pulsaciones de botón o las diferencias del controlador análogo, se realizaron en ese marco. En el ejemplo anterior, *g \_ Controllers representa* esta estructura.

Una vez que se ha recuperado el estado en una estructura [**XINPUT \_ STATE,**](/windows/desktop/api/XInput/ns-xinput-xinput_state) puede comprobar si hay cambios y obtener información específica sobre el estado del controlador.

El *miembro dwPacketNumber* de la estructura [**XINPUT \_ STATE**](/windows/desktop/api/XInput/ns-xinput-xinput_state) se puede usar para comprobar si el estado del controlador ha cambiado desde la última llamada a [**XInputGetState.**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) Si *dwPacketNumber* no cambia entre dos llamadas secuenciales a **XInputGetState,** no se ha realizado ningún cambio de estado. Si difiere, la aplicación debe comprobar el miembro *Gamepad* de la estructura **XINPUT \_ STATE** para obtener información de estado más detallada.

Por motivos de rendimiento, no llame a [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) para una ranura de usuario "vacía" en cada fotograma. Se recomienda que, en su lugar, alete las comprobaciones de los nuevos controladores cada pocos segundos.

### <a name="dead-zone"></a>Zona de desastres

Para que los usuarios tengan una experiencia de juego coherente, el juego debe implementar correctamente la zona de in dead zone. La zona fallida son valores de "movimiento" notificados por el controlador, incluso cuando los controladores análogos están intactos y centrados. También hay una zona de in dead zone para los dos desencadenadores análogos.

> [!Note]  
> Los juegos que usan XInput que no filtran la zona de in dead zone experimentarán un juego deficiente. Tenga en cuenta que algunos controladores son más sensibles que otros, por lo que la zona de acceso no encontrado puede variar de unidad a unidad. Se recomienda probar los juegos con varios controladores de Xbox en sistemas diferentes.

Las aplicaciones deben usar "zonas fallidas" en entradas análogas (desencadenadores, sticks) para indicar cuándo se ha realizado un movimiento lo suficiente en el stick o desencadenador para que se considere válido.

La aplicación debe comprobar si hay zonas fallidas y responder de forma adecuada, como en este ejemplo:

```cpp
XINPUT_STATE state = g_Controllers[i].state;

float LX = state.Gamepad.sThumbLX;
float LY = state.Gamepad.sThumbLY;

//determine how far the controller is pushed
float magnitude = sqrt(LX*LX + LY*LY);

//determine the direction the controller is pushed
float normalizedLX = LX / magnitude;
float normalizedLY = LY / magnitude;

float normalizedMagnitude = 0;

//check if the controller is outside a circular dead zone
if (magnitude > INPUT_DEADZONE)
{
    //clip the magnitude at its expected maximum value
    if (magnitude > 32767) magnitude = 32767;

    //adjust magnitude relative to the end of the dead zone
    magnitude -= INPUT_DEADZONE;

    //optionally normalize the magnitude with respect to its expected range
    //giving a magnitude value of 0.0 to 1.0
    normalizedMagnitude = magnitude / (32767 - INPUT_DEADZONE);
}
else //if the controller is in the deadzone zero out the magnitude
{
    magnitude = 0.0;
    normalizedMagnitude = 0.0;
}

//repeat for right thumb stick
```

En este ejemplo se calcula el vector de dirección del controlador y la distancia a lo largo del vector que se ha presionado el controlador. Esto permite la aplicación de una zona de inerte circular simplemente comprobando si la magnitud del controlador es mayor que el valor de la zona de inerte. Además, el código normaliza la magnitud del controlador, que luego se puede multiplicar por un factor específico del juego para convertir la posición del controlador en unidades relevantes para el juego.

Tenga en cuenta que puede definir sus propias zonas de acceso no activas para los sticks y desencadenadores (en cualquier lugar desde 0-65534), o puede usar las zonas no activas proporcionadas definidas como XINPUT \_ GAMEPAD \_ LEFT THUMB \_ \_ DEADZONE, XINPUT \_ GAMEPAD RIGHT THUMB DEADZONE y \_ \_ \_ XINPUT \_ GAMEPAD TRIGGER THRESHOLD en \_ \_ XInput.h:

```cpp
#define XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE  7849
#define XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE 8689
#define XINPUT_GAMEPAD_TRIGGER_THRESHOLD    30
```

Una vez que se aplica la zona de distribución, puede resultar útil escalar el intervalo resultante de punto flotante \[ 0.0..1.0 (como en el ejemplo anterior) y, opcionalmente, aplicar una transformación no \] lineal.

Por ejemplo, con los juegos de conducción, puede ser útil cubo el resultado para proporcionar una mejor sensación a la conducción de los automóviles mediante un gamepad, ya que la protección del resultado proporciona más precisión en los intervalos inferiores, lo que es deseable, ya que los jugadores suelen aplicar fuerza suave para obtener un movimiento sutil o aplicar fuerza fuerte en una dirección para obtener respuesta de escritorio remoto.

### <a name="setting-vibration-effects"></a>Establecer efectos de vibración

Además de obtener el estado del controlador, también puede enviar datos de vibración al controlador para modificar los comentarios proporcionados al usuario del controlador. El controlador contiene dos motores que se pueden controlar de forma independiente pasando valores a la [**función XInputSetState.**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate)

La velocidad de cada motor se puede especificar mediante un valor WORD en la estructura [**vibration XINPUT \_**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) que se pasa a la función [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) como se indica a continuación:

```cpp
XINPUT_VIBRATION vibration;
ZeroMemory( &vibration, sizeof(XINPUT_VIBRATION) );
vibration.wLeftMotorSpeed = 32000; // use any value between 0-65535 here
vibration.wRightMotorSpeed = 16000; // use any value between 0-65535 here
XInputSetState( i, &vibration );
```

Tenga en cuenta que el motor derecho es el motor de alta frecuencia, el motor izquierdo es el motor de baja frecuencia. No siempre tienen que establecerse en la misma cantidad, ya que proporcionan efectos diferentes.

### <a name="getting-audio-device-identifiers"></a>Obtención de identificadores de dispositivo de audio

El casco de un xbox Controller tiene estas funciones:

-   Grabación de sonido con un micrófono
-   Reproducir el sonido con un auricular

Use este código para obtener los identificadores de dispositivo para el casco:

```cpp
WCHAR renderId[ 256 ] = {0};
WCHAR captureId[ 256 ] = {0};
UINT rcount = 256;
UINT ccount = 256;

XInputGetAudioDeviceIds( i, renderId, &rcount, captureId, &ccount );
```

Después de obtener los identificadores de dispositivo, puede crear las interfaces adecuadas. Por ejemplo, si usa XAudio 2.8, use este código para crear una voz maestra para este dispositivo:

```cpp
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;

IXAudio2MasteringVoice* pMasterVoice = NULL;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice, XAUDIO2_DEFAULT_CHANNELS, XAUDIO2_DEFAULT_SAMPLERATE, 0, renderId, NULL, AudioCategory_Communications ) ) )
    return hr;
```

Para obtener información sobre cómo usar el identificador de dispositivo captureId, consulte [Captura de una secuencia.](/windows/desktop/CoreAudio/capturing-a-stream)

### <a name="getting-directsound-guids-legacy-directx-sdk-only"></a>Obtención de GUID de Direct Sound (solo SDK de DirectX heredado)

El casco que se puede conectar a un controlador de Xbox tiene dos funciones: puede grabar el sonido con un micrófono y reproducir el sonido con un casco. En la API XInput, estas funciones se logran a través de [Direct Sound,](/previous-versions/windows/desktop/ee416960(v=vs.85))mediante las interfaces **IDirect Sound8** **e IDirectCaptureCapture8.**

Para asociar el micrófono de casco y el micrófono con sus interfaces [Direct Sound](/previous-versions/windows/desktop/ee416960(v=vs.85)) adecuadas, debe obtener los Direct SoundGUID para los dispositivos de captura y representación mediante una llamada a [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).

> [!Note]  
> No se recomienda el uso de [Direct Sound](/previous-versions/windows/desktop/ee416960(v=vs.85)) heredado y no está disponible en Windows Store. La información de esta sección solo se aplica a la versión del SDK de DirectX de XInput (XInput 1.3). La versión Windows 8 de XInput (XInput 1.4) usa exclusivamente los identificadores de dispositivo de Windows Audio Session API (WASAPI) que se obtienen a través de [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).

```cpp
XInputGetDSoundAudioDeviceGuids( i, &dsRenderGuid, &dsCaptureGuid );

```

Una vez recuperados los GUID, puede crear las interfaces adecuadas mediante una llamada a DirectSoundCreate8 y DirectCaptureCreate8 de la siguiente manera:

```cpp
// Create IDirectSound8 using the controller's render device
if( FAILED( hr = DirectSoundCreate8( &dsRenderGuid, &pDS, NULL ) ) )
   return hr;

// Set coop level to DSSCL_PRIORITY
if( FAILED( hr = pDS->SetCooperativeLevel( hWnd, DSSCL_NORMAL ) ) )
   return hr;

// Create IDirectSoundCapture using the controller's capture device
if( FAILED( hr = DirectSoundCaptureCreate8( &dsCaptureGuid, &pDSCapture, NULL ) ) )
   return hr;
```

## <a name="related-topics"></a>Temas relacionados

[Referencia de programación](programming-reference.md)
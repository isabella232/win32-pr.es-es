---
title: Introducción con XInput
description: XInput es una API que permite que las aplicaciones reciban datos de la controladora Xbox para Windows. Se admiten efectos de Rumble de controlador y entrada y salida de voz.
ms.assetid: 7b5eec3e-b3da-de5c-c926-8258c1418ef0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f590f54bbb2641881cf89cd6d31539d75665c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791895"
---
# <a name="getting-started-with-xinput"></a>Introducción con XInput

XInput es una API que permite que las aplicaciones reciban datos de la controladora Xbox para Windows. Se admiten efectos de Rumble de controlador y entrada y salida de voz.

En este tema se proporciona una breve introducción a las capacidades de XInput y cómo configurarlo en una aplicación. Incluye lo siguiente:

-   [Introducción a XInput](#introduction-to-xinput)
    -   [La controladora Xbox](#the-xbox-controller)
-   [Usar XInput](#using-xinput)
    -   [Varios controladores](#multiple-controllers)
    -   [Obtención del estado del controlador](#getting-controller-state)
    -   [Zona muerta](#dead-zone)
    -   [Establecer efectos de vibración](#setting-vibration-effects)
    -   [Obtener identificadores de dispositivo de audio](#getting-audio-device-identifiers)
    -   [Obtener GUID de DirectSound (solo DirectX SDK heredado)](#getting-directsound-guids-legacy-directx-sdk-only)
-   [Temas relacionados](#related-topics)

## <a name="introduction-to-xinput"></a>Introducción a XInput

La consola Xbox usa un controlador de juegos compatible con Windows. Las aplicaciones pueden usar la API de XInput para comunicarse con estos controladores cuando están conectados a un equipo Windows (hasta cuatro controladores únicos se pueden conectar a la vez).

Con esta API, se puede consultar el estado de cualquier controlador Xbox conectado y se pueden establecer efectos de vibración. Los controladores con auriculares conectados también pueden consultarse para dispositivos de entrada y salida de sonido que se pueden usar con los auriculares para el procesamiento de voz.

### <a name="the-xbox-controller"></a>La controladora Xbox

El controlador Xbox tiene dos palos análogos, cada uno con un botón digital, dos desencadenadores analógicos, un panel direccional digital con cuatro direcciones y ocho botones digitales. Los Estados de cada una de estas entradas se devuelven en la estructura de [**\_ controlador de juegos de XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) cuando se llama a la función [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) .

El controlador también tiene dos motores de vibración para proporcionar al usuario efectos de la respuesta de fuerza. Las velocidades de estos motores se especifican en la estructura de [**\_ vibración de XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) que se pasa a la función [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) para establecer efectos de vibración.

Opcionalmente, se pueden conectar auriculares al controlador. Los auriculares tienen un micrófono para la entrada de voz y un auricular para la salida de sonido. Puede llamar a la función [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) o [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) heredada para obtener los identificadores de dispositivo que corresponden a los dispositivos para el micrófono y el auricular. Después, puede usar las [API de audio básica](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) para recibir entrada de voz y enviar la salida de sonido.

## <a name="using-xinput"></a>Usar XInput

El uso de XInput es tan sencillo como llamar a las funciones de XInput según sea necesario. Con las funciones de XInput, puede recuperar el estado del controlador, obtener los identificadores de audio de los auriculares y establecer los efectos de Rumble del controlador.

### <a name="multiple-controllers"></a>Varios controladores

La API de XInput admite hasta cuatro controladores conectados en cualquier momento. Todas las funciones de XInput requieren un parámetro *dwUserIndex* que se pasa para identificar el controlador que se establece o se consulta. Este identificador estará en el intervalo de 0-3 y lo establece automáticamente XInput. El número corresponde al puerto en el que está conectado el controlador y no es modificable.

Cada controlador muestra el identificador que está usando al iluminar un cuadrante en el "anillo de luz" en el centro del controlador. Un valor de *dwUserIndex* de 0 corresponde al cuadrante superior izquierdo; la numeración continúa alrededor del anillo en el orden en el sentido de las agujas del reloj.

Las aplicaciones deben admitir varios controladores.

### <a name="getting-controller-state"></a>Obtención del estado del controlador

A lo largo de la duración de una aplicación, la obtención del estado de un controlador probablemente se realizará con más frecuencia. De un marco a otro en una aplicación de juego, se debe recuperar el estado y actualizar la información del juego para reflejar los cambios del controlador.

Para recuperar el estado, utilice la función [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) :

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

Tenga en cuenta que el valor devuelto de [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) se puede usar para determinar si el controlador está conectado. Las aplicaciones deben definir una estructura que contenga información interna del controlador; Esta información debe compararse con los resultados de **XInputGetState** para determinar qué cambios, como pulsaciones de botones o diferencias de controlador analógicas, se hicieron en ese marco. En el ejemplo anterior, *g \_ Controllers* representa una estructura de este tipo.

Una vez que el estado se ha recuperado en una estructura de [**\_ Estado de XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_state) , puede comprobarlo en busca de cambios y obtener información específica sobre el estado del controlador.

El miembro *dwPacketNumber* de la estructura de [**\_ Estado de XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_state) se puede usar para comprobar si el estado del controlador ha cambiado desde la última llamada a [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate). Si *dwPacketNumber* no cambia entre dos llamadas secuenciales a **XInputGetState**, no habrá ningún cambio en el estado. Si es diferente, la aplicación debe comprobar el miembro del *controlador de juegos* de la estructura de **\_ Estado de XInput** para obtener información de estado más detallada.

Por motivos de rendimiento, no llame a [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) para un espacio de usuario "vacío" en cada fotograma. En su lugar, se recomienda que destaque las comprobaciones de los controladores nuevos cada pocos segundos.

### <a name="dead-zone"></a>Zona muerta

Para que los usuarios tengan una experiencia de juego coherente, el juego debe implementar la zona muerta correctamente. La zona muerta es un valor de "movimiento" indicado por el controlador, aunque el thumbsticks analógico no esté tocado y centrado. También hay una zona muerta para los dos desencadenadores analógicos.

> [!Note]  
> Los juegos que usan XInput que no filtran la zona muerta en absoluto experimentarán un juego deficiente. Tenga en cuenta que algunos controladores son más sensibles que otros, por lo que la zona muerta puede variar de una unidad a otra. Se recomienda que pruebe los juegos con varios controladores de Xbox en diferentes sistemas.

Las aplicaciones deben usar "zonas muertas" en las entradas analógicas (desencadenadores, palos) para indicar cuándo se ha realizado un movimiento suficiente en el palo o el desencadenador para que se considere válido.

La aplicación debe comprobar si hay zonas inactivas y responder a appopriately, como en este ejemplo:

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

En este ejemplo se calcula el vector de dirección del controlador y hasta qué punto se ha insertado el controlador. Esto permite la aplicación de un Deadzone circular simplemente comprobando si la magnitud del controlador es mayor que el valor de Deadzone. Además, el código normaliza la magnitud del controlador que se puede multiplicar por un factor específico del juego para convertir la posición del controlador en unidades relevantes para el juego.

Tenga en cuenta que puede definir sus propias zonas inactivas para los palos y los desencadenadores (en cualquier parte de 0-65534), o puede usar el Deadzones proporcionado definido como controlador de juegos de DEADZONE de XINPUT \_ \_ left \_ Thumb \_ , XInput \_ \_ Thumb right de controlador de juegos \_ \_ y \_ \_ \_ umbral de desencadenador de controlador de juegos de XInput en XInput. h:

```cpp
#define XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE  7849
#define XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE 8689
#define XINPUT_GAMEPAD_TRIGGER_THRESHOLD    30
```

Una vez que se aplica Deadzone, puede resultarle útil escalar el \[ punto flotante 0,0.. 1.0 del intervalo resultante \] (como en el ejemplo anterior) y, opcionalmente, aplicar una transformación no lineal.

Por ejemplo, en el caso de los juegos, puede ser útil crear un cubo del resultado para proporcionar una mejor sensación de conducir a los automóviles con un controlador de juegos, ya que elaboración el resultado le proporciona más precisión en los intervalos inferiores, lo que es deseable, ya que los jugadores normalmente aplican la fuerza de forma flexible para obtener una respuesta de Rd.

### <a name="setting-vibration-effects"></a>Establecer efectos de vibración

Además de obtener el estado del controlador, también puede enviar datos de vibración al controlador para modificar los comentarios que se proporcionan al usuario del controlador. El controlador contiene dos motores de Rumble que se pueden controlar de forma independiente pasando valores a la función [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) .

La velocidad de cada motor puede especificarse mediante un valor de palabra en la estructura de [**\_ vibración de XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) que se pasa a la función [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) de la siguiente manera:

```cpp
XINPUT_VIBRATION vibration;
ZeroMemory( &vibration, sizeof(XINPUT_VIBRATION) );
vibration.wLeftMotorSpeed = 32000; // use any value between 0-65535 here
vibration.wRightMotorSpeed = 16000; // use any value between 0-65535 here
XInputSetState( i, &vibration );
```

Tenga en cuenta que el motor derecho es el motor de alta frecuencia, el motor izquierdo es el motor de baja frecuencia. No siempre es necesario establecer en la misma cantidad, ya que proporcionan diferentes efectos.

### <a name="getting-audio-device-identifiers"></a>Obtener identificadores de dispositivo de audio

Los auriculares de un controlador Xbox tienen estas funciones:

-   Grabar sonido con un micrófono
-   Reproducir sonido con un auricular

Use este código para obtener los identificadores de dispositivo para los auriculares:

```cpp
WCHAR renderId[ 256 ] = {0};
WCHAR captureId[ 256 ] = {0};
UINT rcount = 256;
UINT ccount = 256;

XInputGetAudioDeviceIds( i, renderId, &rcount, captureId, &ccount );
```

Después de obtener los identificadores de dispositivo, puede crear las interfaces adecuadas. Por ejemplo, si usa XAudio 2,8, use este código para crear una voz de maestro para este dispositivo:

```cpp
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;

IXAudio2MasteringVoice* pMasterVoice = NULL;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice, XAUDIO2_DEFAULT_CHANNELS, XAUDIO2_DEFAULT_SAMPLERATE, 0, renderId, NULL, AudioCategory_Communications ) ) )
    return hr;
```

Para obtener información sobre cómo usar el identificador de dispositivo captureId, consulte [captura de una secuencia](/windows/desktop/CoreAudio/capturing-a-stream).

### <a name="getting-directsound-guids-legacy-directx-sdk-only"></a>Obtener GUID de DirectSound (solo DirectX SDK heredado)

Los auriculares que se pueden conectar a un controlador de Xbox tienen dos funciones: puede grabar sonido con un micrófono y reproducir sonido con un auricular. En la API de XInput, estas funciones se realizan a través de [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85))mediante el uso de las interfaces **IDirectSound8** y **IDirectSoundCapture8** .

Para asociar el micrófono y el auricular de auriculares con las interfaces de [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) adecuadas, debe obtener el DirectSoundGUIDs de los dispositivos de captura y representación llamando a [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).

> [!Note]  
> No se recomienda el uso de [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) heredado y no está disponible en las aplicaciones de la tienda Windows. La información de esta sección solo se aplica a la versión del SDK de DirectX de XInput (XInput 1,3). La versión de Windows 8 de XInput (XInput 1,4) usa exclusivamente identificadores de dispositivo de la API de sesión de audio de Windows (WASAPI) que se obtienen a través de [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).

```cpp
XInputGetDSoundAudioDeviceGuids( i, &dsRenderGuid, &dsCaptureGuid );

```

Una vez que haya recuperado los GUID, puede crear las interfaces adecuadas llamando a DirectSoundCreate8 y DirectSoundCaptureCreate8 de la siguiente manera:

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
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
# <a name="getting-started-with-xinput"></a><span data-ttu-id="edacc-104">Introducción con XInput</span><span class="sxs-lookup"><span data-stu-id="edacc-104">Getting Started With XInput</span></span>

<span data-ttu-id="edacc-105">XInput es una API que permite que las aplicaciones reciban datos de la controladora Xbox para Windows.</span><span class="sxs-lookup"><span data-stu-id="edacc-105">XInput is an API that allows applications to receive input from the Xbox Controller for Windows.</span></span> <span data-ttu-id="edacc-106">Se admiten efectos de Rumble de controlador y entrada y salida de voz.</span><span class="sxs-lookup"><span data-stu-id="edacc-106">Controller rumble effects and voice input and output are supported.</span></span>

<span data-ttu-id="edacc-107">En este tema se proporciona una breve introducción a las capacidades de XInput y cómo configurarlo en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="edacc-107">This topic provides a brief overview of the capabilities of XInput and how to set it up in an application.</span></span> <span data-ttu-id="edacc-108">Incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="edacc-108">It includes the following:</span></span>

-   [<span data-ttu-id="edacc-109">Introducción a XInput</span><span class="sxs-lookup"><span data-stu-id="edacc-109">Introduction to XInput</span></span>](#introduction-to-xinput)
    -   [<span data-ttu-id="edacc-110">La controladora Xbox</span><span class="sxs-lookup"><span data-stu-id="edacc-110">The Xbox Controller</span></span>](#the-xbox-controller)
-   [<span data-ttu-id="edacc-111">Usar XInput</span><span class="sxs-lookup"><span data-stu-id="edacc-111">Using XInput</span></span>](#using-xinput)
    -   [<span data-ttu-id="edacc-112">Varios controladores</span><span class="sxs-lookup"><span data-stu-id="edacc-112">Multiple Controllers</span></span>](#multiple-controllers)
    -   [<span data-ttu-id="edacc-113">Obtención del estado del controlador</span><span class="sxs-lookup"><span data-stu-id="edacc-113">Getting Controller State</span></span>](#getting-controller-state)
    -   [<span data-ttu-id="edacc-114">Zona muerta</span><span class="sxs-lookup"><span data-stu-id="edacc-114">Dead Zone</span></span>](#dead-zone)
    -   [<span data-ttu-id="edacc-115">Establecer efectos de vibración</span><span class="sxs-lookup"><span data-stu-id="edacc-115">Setting Vibration Effects</span></span>](#setting-vibration-effects)
    -   [<span data-ttu-id="edacc-116">Obtener identificadores de dispositivo de audio</span><span class="sxs-lookup"><span data-stu-id="edacc-116">Getting Audio Device Identifiers</span></span>](#getting-audio-device-identifiers)
    -   [<span data-ttu-id="edacc-117">Obtener GUID de DirectSound (solo DirectX SDK heredado)</span><span class="sxs-lookup"><span data-stu-id="edacc-117">Getting DirectSound GUIDs (legacy DirectX SDK only)</span></span>](#getting-directsound-guids-legacy-directx-sdk-only)
-   [<span data-ttu-id="edacc-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="edacc-118">Related topics</span></span>](#related-topics)

## <a name="introduction-to-xinput"></a><span data-ttu-id="edacc-119">Introducción a XInput</span><span class="sxs-lookup"><span data-stu-id="edacc-119">Introduction to XInput</span></span>

<span data-ttu-id="edacc-120">La consola Xbox usa un controlador de juegos compatible con Windows.</span><span class="sxs-lookup"><span data-stu-id="edacc-120">The Xbox console uses a gaming controller that is compatible with Windows.</span></span> <span data-ttu-id="edacc-121">Las aplicaciones pueden usar la API de XInput para comunicarse con estos controladores cuando están conectados a un equipo Windows (hasta cuatro controladores únicos se pueden conectar a la vez).</span><span class="sxs-lookup"><span data-stu-id="edacc-121">Applications can use the XInput API to communicate with these controllers when they are plugged into a Windows PC (up to four unique controllers can be plugged in at a time).</span></span>

<span data-ttu-id="edacc-122">Con esta API, se puede consultar el estado de cualquier controlador Xbox conectado y se pueden establecer efectos de vibración.</span><span class="sxs-lookup"><span data-stu-id="edacc-122">Using this API, any connected Xbox Controller can be queried for its state, and vibration effects can be set.</span></span> <span data-ttu-id="edacc-123">Los controladores con auriculares conectados también pueden consultarse para dispositivos de entrada y salida de sonido que se pueden usar con los auriculares para el procesamiento de voz.</span><span class="sxs-lookup"><span data-stu-id="edacc-123">Controllers that have the headset attached can also be queried for sound input and output devices that can be used with the headset for voice processing.</span></span>

### <a name="the-xbox-controller"></a><span data-ttu-id="edacc-124">La controladora Xbox</span><span class="sxs-lookup"><span data-stu-id="edacc-124">The Xbox Controller</span></span>

<span data-ttu-id="edacc-125">El controlador Xbox tiene dos palos análogos, cada uno con un botón digital, dos desencadenadores analógicos, un panel direccional digital con cuatro direcciones y ocho botones digitales.</span><span class="sxs-lookup"><span data-stu-id="edacc-125">The Xbox Controller has two analog directional sticks, each with a digital button, two analog triggers, a digital directional pad with four directions, and eight digital buttons.</span></span> <span data-ttu-id="edacc-126">Los Estados de cada una de estas entradas se devuelven en la estructura de [**\_ controlador de juegos de XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) cuando se llama a la función [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) .</span><span class="sxs-lookup"><span data-stu-id="edacc-126">The states of each of these inputs are returned in the [**XINPUT\_GAMEPAD**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) structure when the [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) function is called.</span></span>

<span data-ttu-id="edacc-127">El controlador también tiene dos motores de vibración para proporcionar al usuario efectos de la respuesta de fuerza.</span><span class="sxs-lookup"><span data-stu-id="edacc-127">The controller also has two vibration motors to supply force feedback effects to the user.</span></span> <span data-ttu-id="edacc-128">Las velocidades de estos motores se especifican en la estructura de [**\_ vibración de XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) que se pasa a la función [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) para establecer efectos de vibración.</span><span class="sxs-lookup"><span data-stu-id="edacc-128">The speeds of these motors are specified in the [**XINPUT\_VIBRATION**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) structure that is passed to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function to set vibration effects.</span></span>

<span data-ttu-id="edacc-129">Opcionalmente, se pueden conectar auriculares al controlador.</span><span class="sxs-lookup"><span data-stu-id="edacc-129">Optionally, a headset can be connected to the controller.</span></span> <span data-ttu-id="edacc-130">Los auriculares tienen un micrófono para la entrada de voz y un auricular para la salida de sonido.</span><span class="sxs-lookup"><span data-stu-id="edacc-130">The headset has a microphone for voice input, and a headphone for sound output.</span></span> <span data-ttu-id="edacc-131">Puede llamar a la función [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) o [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) heredada para obtener los identificadores de dispositivo que corresponden a los dispositivos para el micrófono y el auricular.</span><span class="sxs-lookup"><span data-stu-id="edacc-131">You can call the [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) or legacy [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) function to obtain the device identifiers that correspond to the devices for the microphone and headphone.</span></span> <span data-ttu-id="edacc-132">Después, puede usar las [API de audio básica](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) para recibir entrada de voz y enviar la salida de sonido.</span><span class="sxs-lookup"><span data-stu-id="edacc-132">You can then use the [Core Audio APIs](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) to receive voice input and send sound output.</span></span>

## <a name="using-xinput"></a><span data-ttu-id="edacc-133">Usar XInput</span><span class="sxs-lookup"><span data-stu-id="edacc-133">Using XInput</span></span>

<span data-ttu-id="edacc-134">El uso de XInput es tan sencillo como llamar a las funciones de XInput según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="edacc-134">Using XInput is as simple as calling the XInput functions as required.</span></span> <span data-ttu-id="edacc-135">Con las funciones de XInput, puede recuperar el estado del controlador, obtener los identificadores de audio de los auriculares y establecer los efectos de Rumble del controlador.</span><span class="sxs-lookup"><span data-stu-id="edacc-135">Using the XInput functions, you can retrieve controller state, get headset audio IDs, and set controller rumble effects.</span></span>

### <a name="multiple-controllers"></a><span data-ttu-id="edacc-136">Varios controladores</span><span class="sxs-lookup"><span data-stu-id="edacc-136">Multiple Controllers</span></span>

<span data-ttu-id="edacc-137">La API de XInput admite hasta cuatro controladores conectados en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="edacc-137">The XInput API supports up to four controllers connected at any time.</span></span> <span data-ttu-id="edacc-138">Todas las funciones de XInput requieren un parámetro *dwUserIndex* que se pasa para identificar el controlador que se establece o se consulta.</span><span class="sxs-lookup"><span data-stu-id="edacc-138">The XInput functions all require a *dwUserIndex* parameter that is passed in to identify the controller being set or queried.</span></span> <span data-ttu-id="edacc-139">Este identificador estará en el intervalo de 0-3 y lo establece automáticamente XInput.</span><span class="sxs-lookup"><span data-stu-id="edacc-139">This ID will be in the range of 0-3 and is set automatically by XInput.</span></span> <span data-ttu-id="edacc-140">El número corresponde al puerto en el que está conectado el controlador y no es modificable.</span><span class="sxs-lookup"><span data-stu-id="edacc-140">The number corresponds to the port that the controller is plugged into, and is not modifiable.</span></span>

<span data-ttu-id="edacc-141">Cada controlador muestra el identificador que está usando al iluminar un cuadrante en el "anillo de luz" en el centro del controlador.</span><span class="sxs-lookup"><span data-stu-id="edacc-141">Each controller displays which ID it is using by lighting up a quadrant on the "ring of light" in the center of the controller.</span></span> <span data-ttu-id="edacc-142">Un valor de *dwUserIndex* de 0 corresponde al cuadrante superior izquierdo; la numeración continúa alrededor del anillo en el orden en el sentido de las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="edacc-142">A *dwUserIndex* value of 0 corresponds to the top-left quadrant; the numbering proceeds around the ring in clockwise order.</span></span>

<span data-ttu-id="edacc-143">Las aplicaciones deben admitir varios controladores.</span><span class="sxs-lookup"><span data-stu-id="edacc-143">Applications should support multiple controllers.</span></span>

### <a name="getting-controller-state"></a><span data-ttu-id="edacc-144">Obtención del estado del controlador</span><span class="sxs-lookup"><span data-stu-id="edacc-144">Getting Controller State</span></span>

<span data-ttu-id="edacc-145">A lo largo de la duración de una aplicación, la obtención del estado de un controlador probablemente se realizará con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="edacc-145">Throughout the duration of an application, getting state from a controller will probably be done most often.</span></span> <span data-ttu-id="edacc-146">De un marco a otro en una aplicación de juego, se debe recuperar el estado y actualizar la información del juego para reflejar los cambios del controlador.</span><span class="sxs-lookup"><span data-stu-id="edacc-146">From frame to frame in a game application, state should be retrieved and game information updated to reflect the controller changes.</span></span>

<span data-ttu-id="edacc-147">Para recuperar el estado, utilice la función [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) :</span><span class="sxs-lookup"><span data-stu-id="edacc-147">To retrieve state, use the [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) function:</span></span>

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

<span data-ttu-id="edacc-148">Tenga en cuenta que el valor devuelto de [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) se puede usar para determinar si el controlador está conectado.</span><span class="sxs-lookup"><span data-stu-id="edacc-148">Note that the return value of [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) can be used to determine if the controller is connected.</span></span> <span data-ttu-id="edacc-149">Las aplicaciones deben definir una estructura que contenga información interna del controlador; Esta información debe compararse con los resultados de **XInputGetState** para determinar qué cambios, como pulsaciones de botones o diferencias de controlador analógicas, se hicieron en ese marco.</span><span class="sxs-lookup"><span data-stu-id="edacc-149">Applications should define a structure to hold internal controller information; this information should be compared against the results of **XInputGetState** to determine what changes, such as button presses or analog controller deltas, were made that frame.</span></span> <span data-ttu-id="edacc-150">En el ejemplo anterior, *g \_ Controllers* representa una estructura de este tipo.</span><span class="sxs-lookup"><span data-stu-id="edacc-150">In the above example, *g\_Controllers* represents such a structure.</span></span>

<span data-ttu-id="edacc-151">Una vez que el estado se ha recuperado en una estructura de [**\_ Estado de XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_state) , puede comprobarlo en busca de cambios y obtener información específica sobre el estado del controlador.</span><span class="sxs-lookup"><span data-stu-id="edacc-151">Once the state has been retrieved in a [**XINPUT\_STATE**](/windows/desktop/api/XInput/ns-xinput-xinput_state) structure, you can check it for changes and get specific information about controller state.</span></span>

<span data-ttu-id="edacc-152">El miembro *dwPacketNumber* de la estructura de [**\_ Estado de XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_state) se puede usar para comprobar si el estado del controlador ha cambiado desde la última llamada a [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate).</span><span class="sxs-lookup"><span data-stu-id="edacc-152">The *dwPacketNumber* member of the [**XINPUT\_STATE**](/windows/desktop/api/XInput/ns-xinput-xinput_state) structure can be used to check if the state of the controller has changed since the last call to [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate).</span></span> <span data-ttu-id="edacc-153">Si *dwPacketNumber* no cambia entre dos llamadas secuenciales a **XInputGetState**, no habrá ningún cambio en el estado.</span><span class="sxs-lookup"><span data-stu-id="edacc-153">If *dwPacketNumber* does not change between two sequential calls to **XInputGetState**, then there has been no change in state.</span></span> <span data-ttu-id="edacc-154">Si es diferente, la aplicación debe comprobar el miembro del *controlador de juegos* de la estructura de **\_ Estado de XInput** para obtener información de estado más detallada.</span><span class="sxs-lookup"><span data-stu-id="edacc-154">If it differs, then the application should check the *Gamepad* member of the **XINPUT\_STATE** structure to get more detailed state information.</span></span>

<span data-ttu-id="edacc-155">Por motivos de rendimiento, no llame a [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) para un espacio de usuario "vacío" en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="edacc-155">For performance reasons, don't call [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) for an 'empty' user slot every frame.</span></span> <span data-ttu-id="edacc-156">En su lugar, se recomienda que destaque las comprobaciones de los controladores nuevos cada pocos segundos.</span><span class="sxs-lookup"><span data-stu-id="edacc-156">We recommend that you space out checks for new controllers every few seconds instead.</span></span>

### <a name="dead-zone"></a><span data-ttu-id="edacc-157">Zona muerta</span><span class="sxs-lookup"><span data-stu-id="edacc-157">Dead Zone</span></span>

<span data-ttu-id="edacc-158">Para que los usuarios tengan una experiencia de juego coherente, el juego debe implementar la zona muerta correctamente.</span><span class="sxs-lookup"><span data-stu-id="edacc-158">In order for users to have a consistent gameplay experience, your game must implement dead zone correctly.</span></span> <span data-ttu-id="edacc-159">La zona muerta es un valor de "movimiento" indicado por el controlador, aunque el thumbsticks analógico no esté tocado y centrado.</span><span class="sxs-lookup"><span data-stu-id="edacc-159">The dead zone is "movement" values reported by the controller even when the analog thumbsticks are untouched and centered.</span></span> <span data-ttu-id="edacc-160">También hay una zona muerta para los dos desencadenadores analógicos.</span><span class="sxs-lookup"><span data-stu-id="edacc-160">There is also a dead zone for the 2 analog triggers.</span></span>

> [!Note]  
> <span data-ttu-id="edacc-161">Los juegos que usan XInput que no filtran la zona muerta en absoluto experimentarán un juego deficiente.</span><span class="sxs-lookup"><span data-stu-id="edacc-161">Games that use XInput that do not filter dead zone at all will experience poor gameplay.</span></span> <span data-ttu-id="edacc-162">Tenga en cuenta que algunos controladores son más sensibles que otros, por lo que la zona muerta puede variar de una unidad a otra.</span><span class="sxs-lookup"><span data-stu-id="edacc-162">Please note that some controllers are more sensitive than others, thus the dead zone may vary from unit to unit.</span></span> <span data-ttu-id="edacc-163">Se recomienda que pruebe los juegos con varios controladores de Xbox en diferentes sistemas.</span><span class="sxs-lookup"><span data-stu-id="edacc-163">It is recommended that you test your games with several Xbox controllers on different systems.</span></span>

<span data-ttu-id="edacc-164">Las aplicaciones deben usar "zonas muertas" en las entradas analógicas (desencadenadores, palos) para indicar cuándo se ha realizado un movimiento suficiente en el palo o el desencadenador para que se considere válido.</span><span class="sxs-lookup"><span data-stu-id="edacc-164">Applications should use "dead zones" on analog inputs (triggers, sticks) to indicate when a movement has been made sufficiently on the stick or trigger to be considered valid.</span></span>

<span data-ttu-id="edacc-165">La aplicación debe comprobar si hay zonas inactivas y responder a appopriately, como en este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="edacc-165">Your application should check for dead zones and respond appopriately, as in this example:</span></span>

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

<span data-ttu-id="edacc-166">En este ejemplo se calcula el vector de dirección del controlador y hasta qué punto se ha insertado el controlador.</span><span class="sxs-lookup"><span data-stu-id="edacc-166">This example calculates the controller's direction vector and how far along the vector the controller has been pushed.</span></span> <span data-ttu-id="edacc-167">Esto permite la aplicación de un Deadzone circular simplemente comprobando si la magnitud del controlador es mayor que el valor de Deadzone.</span><span class="sxs-lookup"><span data-stu-id="edacc-167">This allows enforcement of a circular deadzone by simply checking whether the controller's magnitude is greater than the deadzone value.</span></span> <span data-ttu-id="edacc-168">Además, el código normaliza la magnitud del controlador que se puede multiplicar por un factor específico del juego para convertir la posición del controlador en unidades relevantes para el juego.</span><span class="sxs-lookup"><span data-stu-id="edacc-168">In addition the code normalizes the controller's magnitude which can then be multiplied by a game specific factor to convert the controller's position to units relevant to the game.</span></span>

<span data-ttu-id="edacc-169">Tenga en cuenta que puede definir sus propias zonas inactivas para los palos y los desencadenadores (en cualquier parte de 0-65534), o puede usar el Deadzones proporcionado definido como controlador de juegos de DEADZONE de XINPUT \_ \_ left \_ Thumb \_ , XInput \_ \_ Thumb right de controlador de juegos \_ \_ y \_ \_ \_ umbral de desencadenador de controlador de juegos de XInput en XInput. h:</span><span class="sxs-lookup"><span data-stu-id="edacc-169">Note that you may define your own dead zones for the sticks and triggers (anywhere from 0-65534), or you may use the provided deadzones defined as XINPUT\_GAMEPAD\_LEFT\_THUMB\_DEADZONE, XINPUT\_GAMEPAD\_RIGHT\_THUMB\_DEADZONE, and XINPUT\_GAMEPAD\_TRIGGER\_THRESHOLD in XInput.h:</span></span>

```cpp
#define XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE  7849
#define XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE 8689
#define XINPUT_GAMEPAD_TRIGGER_THRESHOLD    30
```

<span data-ttu-id="edacc-170">Una vez que se aplica Deadzone, puede resultarle útil escalar el \[ punto flotante 0,0.. 1.0 del intervalo resultante \] (como en el ejemplo anterior) y, opcionalmente, aplicar una transformación no lineal.</span><span class="sxs-lookup"><span data-stu-id="edacc-170">Once the deadzone is enforced, you may find it useful to scale the resulting range \[0.0..1.0\] floating point (as in the example above), and optionally apply a non-linear transform.</span></span>

<span data-ttu-id="edacc-171">Por ejemplo, en el caso de los juegos, puede ser útil crear un cubo del resultado para proporcionar una mejor sensación de conducir a los automóviles con un controlador de juegos, ya que elaboración el resultado le proporciona más precisión en los intervalos inferiores, lo que es deseable, ya que los jugadores normalmente aplican la fuerza de forma flexible para obtener una respuesta de Rd.</span><span class="sxs-lookup"><span data-stu-id="edacc-171">For example, with driving games, it may be helpful to cube the result to provide a better feel to driving the cars using a gamepad, as cubing the result gives you more precision in the lower ranges, which is desirable, since gamers typically either apply soft force to get subtle movement or apply hard force all the way in one direction to get rd response.</span></span>

### <a name="setting-vibration-effects"></a><span data-ttu-id="edacc-172">Establecer efectos de vibración</span><span class="sxs-lookup"><span data-stu-id="edacc-172">Setting Vibration Effects</span></span>

<span data-ttu-id="edacc-173">Además de obtener el estado del controlador, también puede enviar datos de vibración al controlador para modificar los comentarios que se proporcionan al usuario del controlador.</span><span class="sxs-lookup"><span data-stu-id="edacc-173">In addition to getting the state of the controller, you may also send vibration data to the controller to alter the feedback provided to the user of the controller.</span></span> <span data-ttu-id="edacc-174">El controlador contiene dos motores de Rumble que se pueden controlar de forma independiente pasando valores a la función [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) .</span><span class="sxs-lookup"><span data-stu-id="edacc-174">The controller contains two rumble motors that can be independently controlled by passing values to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function.</span></span>

<span data-ttu-id="edacc-175">La velocidad de cada motor puede especificarse mediante un valor de palabra en la estructura de [**\_ vibración de XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) que se pasa a la función [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="edacc-175">The speed of each motor can be specified using a WORD value in the [**XINPUT\_VIBRATION**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) structure that is passed to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function as follows:</span></span>

```cpp
XINPUT_VIBRATION vibration;
ZeroMemory( &vibration, sizeof(XINPUT_VIBRATION) );
vibration.wLeftMotorSpeed = 32000; // use any value between 0-65535 here
vibration.wRightMotorSpeed = 16000; // use any value between 0-65535 here
XInputSetState( i, &vibration );
```

<span data-ttu-id="edacc-176">Tenga en cuenta que el motor derecho es el motor de alta frecuencia, el motor izquierdo es el motor de baja frecuencia.</span><span class="sxs-lookup"><span data-stu-id="edacc-176">Note that the right motor is the high-frequency motor, the left motor is the low-frequency motor.</span></span> <span data-ttu-id="edacc-177">No siempre es necesario establecer en la misma cantidad, ya que proporcionan diferentes efectos.</span><span class="sxs-lookup"><span data-stu-id="edacc-177">They do not always need to be set to the same amount, as they provide different effects.</span></span>

### <a name="getting-audio-device-identifiers"></a><span data-ttu-id="edacc-178">Obtener identificadores de dispositivo de audio</span><span class="sxs-lookup"><span data-stu-id="edacc-178">Getting Audio Device Identifiers</span></span>

<span data-ttu-id="edacc-179">Los auriculares de un controlador Xbox tienen estas funciones:</span><span class="sxs-lookup"><span data-stu-id="edacc-179">The headset for an Xbox Controller has these functions:</span></span>

-   <span data-ttu-id="edacc-180">Grabar sonido con un micrófono</span><span class="sxs-lookup"><span data-stu-id="edacc-180">Record sound using a microphone</span></span>
-   <span data-ttu-id="edacc-181">Reproducir sonido con un auricular</span><span class="sxs-lookup"><span data-stu-id="edacc-181">Play back sound using a headphone</span></span>

<span data-ttu-id="edacc-182">Use este código para obtener los identificadores de dispositivo para los auriculares:</span><span class="sxs-lookup"><span data-stu-id="edacc-182">Use this code to obtain the device identifiers for the headset:</span></span>

```cpp
WCHAR renderId[ 256 ] = {0};
WCHAR captureId[ 256 ] = {0};
UINT rcount = 256;
UINT ccount = 256;

XInputGetAudioDeviceIds( i, renderId, &rcount, captureId, &ccount );
```

<span data-ttu-id="edacc-183">Después de obtener los identificadores de dispositivo, puede crear las interfaces adecuadas.</span><span class="sxs-lookup"><span data-stu-id="edacc-183">After you obtain the device identifiers, you can create the appropriate interfaces.</span></span> <span data-ttu-id="edacc-184">Por ejemplo, si usa XAudio 2,8, use este código para crear una voz de maestro para este dispositivo:</span><span class="sxs-lookup"><span data-stu-id="edacc-184">For example, if you use XAudio 2.8, use this code to create a mastering voice for this device:</span></span>

```cpp
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;

IXAudio2MasteringVoice* pMasterVoice = NULL;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice, XAUDIO2_DEFAULT_CHANNELS, XAUDIO2_DEFAULT_SAMPLERATE, 0, renderId, NULL, AudioCategory_Communications ) ) )
    return hr;
```

<span data-ttu-id="edacc-185">Para obtener información sobre cómo usar el identificador de dispositivo captureId, consulte [captura de una secuencia](/windows/desktop/CoreAudio/capturing-a-stream).</span><span class="sxs-lookup"><span data-stu-id="edacc-185">For info about how to use the captureId device identifier, see [Capturing a Stream](/windows/desktop/CoreAudio/capturing-a-stream).</span></span>

### <a name="getting-directsound-guids-legacy-directx-sdk-only"></a><span data-ttu-id="edacc-186">Obtener GUID de DirectSound (solo DirectX SDK heredado)</span><span class="sxs-lookup"><span data-stu-id="edacc-186">Getting DirectSound GUIDs (legacy DirectX SDK only)</span></span>

<span data-ttu-id="edacc-187">Los auriculares que se pueden conectar a un controlador de Xbox tienen dos funciones: puede grabar sonido con un micrófono y reproducir sonido con un auricular.</span><span class="sxs-lookup"><span data-stu-id="edacc-187">The headset that can be connected to an Xbox Controller has two functions: it can record sound using a microphone, and it can play back sound using a headphone.</span></span> <span data-ttu-id="edacc-188">En la API de XInput, estas funciones se realizan a través de [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85))mediante el uso de las interfaces **IDirectSound8** y **IDirectSoundCapture8** .</span><span class="sxs-lookup"><span data-stu-id="edacc-188">In the XInput API, these functions are accomplished through [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)), using the **IDirectSound8** and **IDirectSoundCapture8** interfaces.</span></span>

<span data-ttu-id="edacc-189">Para asociar el micrófono y el auricular de auriculares con las interfaces de [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) adecuadas, debe obtener el DirectSoundGUIDs de los dispositivos de captura y representación llamando a [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).</span><span class="sxs-lookup"><span data-stu-id="edacc-189">To associate the headset microphone and headphone with their appropriate [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) interfaces, you must get the DirectSoundGUIDs for the capture and render devices by calling [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).</span></span>

> [!Note]  
> <span data-ttu-id="edacc-190">No se recomienda el uso de [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) heredado y no está disponible en las aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="edacc-190">Use of the legacy [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) is not recommended, and is not available in Windows Store apps.</span></span> <span data-ttu-id="edacc-191">La información de esta sección solo se aplica a la versión del SDK de DirectX de XInput (XInput 1,3).</span><span class="sxs-lookup"><span data-stu-id="edacc-191">The info in this section only applies to the DirectX SDK version of XInput (XInput 1.3).</span></span> <span data-ttu-id="edacc-192">La versión de Windows 8 de XInput (XInput 1,4) usa exclusivamente identificadores de dispositivo de la API de sesión de audio de Windows (WASAPI) que se obtienen a través de [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).</span><span class="sxs-lookup"><span data-stu-id="edacc-192">The Windows 8 version of XInput (XInput 1.4) exclusively uses Windows Audio Session API (WASAPI) device identifiers that are obtained through [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).</span></span>

```cpp
XInputGetDSoundAudioDeviceGuids( i, &dsRenderGuid, &dsCaptureGuid );

```

<span data-ttu-id="edacc-193">Una vez que haya recuperado los GUID, puede crear las interfaces adecuadas llamando a DirectSoundCreate8 y DirectSoundCaptureCreate8 de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="edacc-193">Once you have retrieved the GUIDs you can create the appropriate interfaces by calling DirectSoundCreate8 and DirectSoundCaptureCreate8 like this:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="edacc-194">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="edacc-194">Related topics</span></span>

[<span data-ttu-id="edacc-195">Referencia de programación</span><span class="sxs-lookup"><span data-stu-id="edacc-195">Programming Reference</span></span>](programming-reference.md)
---
title: Sacar partido de High-Definition movimiento del mouse
description: Este artículo se centra en la mejor manera de optimizar el rendimiento de la entrada de mouse de alta definición en un juego como un dispositivo de presentación de primera persona.
ms.assetid: 0138a248-e8e0-a392-564e-7a9229b94b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebe2abd9487d95b8fe12aa3c6938e21d72d8e2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421096"
---
# <a name="taking-advantage-of-high-definition-mouse-movement"></a>Sacar partido de High-Definition movimiento del mouse

Un mouse de equipo estándar devuelve datos a 400 puntos por pulgada (PPP), mientras que un mouse de alta definición genera datos a 800 ppp o superior. Esto hace que la entrada de un mouse de alta definición sea mucho más precisa que la del mouse estándar. Sin embargo, los datos de alta definición no se pueden obtener a través de los mensajes de MOUSEMOVE estándar de WM \_ . En general, los juegos se beneficiarán de los dispositivos de mouse de alta definición, pero los juegos que obtienen datos de mouse con solo WM \_ MOUSEMOVE no podrán tener acceso a la resolución completa y sin filtrar del mouse.

Varias empresas están fabricando dispositivos de mouse de alta definición, como Microsoft y Logitech. Con la creciente popularidad de los dispositivos de mouse de alta resolución, es importante que los desarrolladores sepan cómo usar la información generada por estos dispositivos de forma óptima. Este artículo se centra en la mejor manera de optimizar el rendimiento de la entrada de mouse de alta definición en un juego como un dispositivo de presentación de primera persona.

## <a name="retrieving-mouse-movement-data"></a>Recuperar datos de movimiento del mouse

Estos son los tres métodos principales para recuperar los datos del mouse:

-   [MOUSEMOVE de WM \_](/windows)
-   [entrada de WM \_](/windows)
-   [DirectInput](#directinput)

Existen ventajas y desventajas de cada método, en función de cómo se usarán los datos.

### <a name="wm_mousemove"></a>MOUSEMOVE de WM \_

El método más sencillo de leer los datos de movimiento del mouse es a través de \_ los mensajes de WM MOUSEMOVE. El siguiente es un ejemplo de cómo leer los datos de movimiento del mouse desde el mensaje de MOUSEMOVE de WM \_ :

```cpp
case WM_MOUSEMOVE:
{
    int xPosAbsolute = GET_X_PARAM(lParam); 
    int yPosAbsolute = GET_Y_PARAM(lParam);
    // ...
    break;
}
```

El principal inconveniente de los datos de WM \_ MOUSEMOVE es que se limita a la resolución de pantalla. Esto significa que si mueve el mouse ligeramente, pero no suficiente para que el puntero se mueva al siguiente píxel, no se genera ningún mensaje de la MOUSEMOVE de WM \_ . Por lo tanto, el uso de este método para leer el movimiento del mouse anula las ventajas de la entrada de alta definición.

Sin embargo, la ventaja de WM \_ MOUSEMOVE es que Windows aplica la aceleración del puntero (también conocida como Ballistics) a los datos del mouse sin procesar, lo que hace que el puntero del mouse se comporte como esperan los clientes. Esto hace que WM \_ MOUSEMOVE sea la opción preferida para el control de puntero (a través de la entrada de WM \_ o DirectInput), ya que resulta en un comportamiento más natural para los usuarios. Aunque WM \_ MOUSEMOVE es idóneo para mover punteros del mouse, no es tan bueno para mover una cámara de primera persona, ya que se perderá la precisión de alta definición.

Para obtener más información sobre WM \_ MouseMove, consulte [**WM \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove).

### <a name="wm_input"></a>entrada de WM \_

El segundo método para obtener los datos del mouse es leer \_ los mensajes de entrada de WM. El procesamiento de \_ mensajes de entrada de WM es más complicado que \_ el procesamiento de mensajes de WM MOUSEMOVE, pero \_ los mensajes de entrada de WM se leen directamente desde la pila dispositivo de interfaz humana (HID) y reflejan los resultados de alta definición.

Para leer los datos de movimiento del mouse desde el mensaje de entrada de WM \_ , primero se debe registrar el dispositivo; el código siguiente proporciona un ejemplo de esto:

```cpp
// you can #include <hidusage.h> for these defines
#ifndef HID_USAGE_PAGE_GENERIC
#define HID_USAGE_PAGE_GENERIC         ((USHORT) 0x01)
#endif
#ifndef HID_USAGE_GENERIC_MOUSE
#define HID_USAGE_GENERIC_MOUSE        ((USHORT) 0x02)
#endif

RAWINPUTDEVICE Rid[1];
Rid[0].usUsagePage = HID_USAGE_PAGE_GENERIC; 
Rid[0].usUsage = HID_USAGE_GENERIC_MOUSE; 
Rid[0].dwFlags = RIDEV_INPUTSINK;   
Rid[0].hwndTarget = hWnd;
RegisterRawInputDevices(Rid, 1, sizeof(Rid[0]));
```

El código siguiente controla \_ los mensajes de entrada de WM en el controlador que winproc de la aplicación:

```cpp
case WM_INPUT: 
{
    UINT dwSize = sizeof(RAWINPUT);
    static BYTE lpb[sizeof(RAWINPUT)];

    GetRawInputData((HRAWINPUT)lParam, RID_INPUT, lpb, &dwSize, sizeof(RAWINPUTHEADER));

    RAWINPUT* raw = (RAWINPUT*)lpb;

    if (raw->header.dwType == RIM_TYPEMOUSE) 
    {
        int xPosRelative = raw->data.mouse.lLastX;
        int yPosRelative = raw->data.mouse.lLastY;
    } 
    break;
}
```

La ventaja de usar la \_ entrada de WM es que el juego recibe datos sin procesar del mouse en el nivel más bajo posible.

La desventaja es que la \_ entrada de WM no tiene ningún Ballistics aplicado a sus datos, por lo que si desea controlar un cursor con estos datos, se requerirá un esfuerzo adicional para que el cursor se comporte como en Windows. Para obtener más información acerca de cómo aplicar el puntero Ballistics, vea [Pointer Ballistics for Windows XP](https://www.microsoft.com/whdc/archive/pointer-bal.mspx).

Para obtener más información sobre la entrada de WM \_ , consulte [acerca de la entrada sin formato](/windows/desktop/inputdev/about-raw-input).

### <a name="directinput"></a>DirectInput

[DirectInput](/windows-hardware/drivers/hid/directinput) es un conjunto de llamadas API que abstrae los dispositivos de entrada en el sistema. Internamente, DirectInput crea un segundo subproceso para leer los datos de entrada de WM \_ y el uso de las API de DirectInput agregará más sobrecarga que simplemente leer directamente la entrada de WM \_ . DirectInput solo es útil para leer datos de los joysticks de DirectInput; sin embargo, si solo necesita admitir la controladora Xbox 360 para Windows, use [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) en su lugar. En general, el uso de DirectInput no ofrece ninguna ventaja cuando se leen datos desde dispositivos de mouse o teclado, y no se recomienda el uso de DirectInput en estos escenarios.

Compare la complejidad del uso de [DirectInput](/windows-hardware/drivers/hid/directinput), que se muestra en el código siguiente, con los métodos descritos anteriormente. Se necesita el siguiente conjunto de llamadas para crear un mouse de DirectInput:

```cpp
LPDIRECTINPUT8 pDI;
LPDIRECTINPUTDEVICE8 pMouse;

hr = DirectInput8Create(GetModuleHandle(NULL), DIRECTINPUT_VERSION, IID_IDirectInput8, (VOID**)&pDI, NULL);
if(FAILED(hr))
    return hr;

hr = pDI->CreateDevice(GUID_SysMouse, &pMouse, NULL);
if(FAILED(hr))
    return hr;

hr = pMouse->SetDataFormat(&c_dfDIMouse2);
if(FAILED(hr))
    return hr;

hr = pMouse->SetCooperativeLevel(hWnd, DISCL_NONEXCLUSIVE | DISCL_FOREGROUND);
if(FAILED(hr))
    return hr;

if(!bImmediate)
{
    DIPROPDWORD dipdw;
    dipdw.diph.dwSize       = sizeof(DIPROPDWORD);
    dipdw.diph.dwHeaderSize = sizeof(DIPROPHEADER);
    dipdw.diph.dwObj        = 0;
    dipdw.diph.dwHow        = DIPH_DEVICE;
    dipdw.dwData            = 16; // Arbitrary buffer size

    if(FAILED(hr = pMouse->SetProperty(DIPROP_BUFFERSIZE, &dipdw.diph)))
        return hr;
}

pMouse->Acquire();
```

Y, a continuación, el dispositivo de mouse de DirectInput puede leerse en cada fotograma:

```cpp
DIMOUSESTATE2 dims2; 
ZeroMemory(&dims2, sizeof(dims2));

hr = pMouse->GetDeviceState(sizeof(DIMOUSESTATE2), &dims2);
if(FAILED(hr)) 
{
    hr = pMouse->Acquire();
    while(hr == DIERR_INPUTLOST) 
        hr = pMouse->Acquire();

    return S_OK; 
}

int xPosRelative = dims2.lX;
int yPosRelative = dims2.lY;
```

## <a name="summary"></a>Resumen

En general, el mejor método para recibir datos de movimiento del mouse de alta definición es la entrada de WM \_ . Si los usuarios solo mueven un puntero del mouse, considere la posibilidad de usar WM \_ MOUSEMOVE para evitar tener que realizar Ballistics de puntero. Ambos mensajes de ventana funcionarán bien incluso si el mouse no es un mouse de alta definición. Al admitir alta definición, los juegos de Windows pueden ofrecer un control más preciso a los usuarios.
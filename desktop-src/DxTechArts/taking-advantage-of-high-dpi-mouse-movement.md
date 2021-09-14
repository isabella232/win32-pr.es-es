---
title: Aprovechar las ventajas del High-Definition del mouse
description: Este artículo se centra en la mejor manera de optimizar el rendimiento de la entrada de mouse de alta definición en un juego como un juego en primera persona.
ms.assetid: 0138a248-e8e0-a392-564e-7a9229b94b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebe2abd9487d95b8fe12aa3c6938e21d72d8e2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063173"
---
# <a name="taking-advantage-of-high-definition-mouse-movement"></a>Aprovechar las ventajas del High-Definition del mouse

Un mouse de equipo estándar devuelve datos a 400 puntos por pulgada (PPP), mientras que un mouse de alta definición genera datos a 800 PPP o superiores. Esto hace que la entrada de un mouse de alta definición sea mucho más precisa que la de un mouse estándar. Sin embargo, los datos de alta definición no se pueden obtener a través de los mensajes ESTÁNDAR DE WM \_ MOUSEMOVE. En general, los juegos se beneficiarán de los dispositivos de mouse de alta definición, pero los juegos que obtienen datos del mouse mediante WM MOUSEMOVE no podrán acceder a la resolución completa y sin filtrar \_ del mouse.

Varias empresas están fabricando dispositivos de mouse de alta definición, como Microsoft y Samsung. Con la creciente popularidad de los dispositivos de mouse de alta resolución, es importante que los desarrolladores comprendan cómo usar la información generada por estos dispositivos de forma óptima. Este artículo se centra en la mejor manera de optimizar el rendimiento de la entrada de mouse de alta definición en un juego como un juego en primera persona.

## <a name="retrieving-mouse-movement-data"></a>Recuperar datos de movimiento del mouse

Estos son los tres métodos principales para recuperar datos del mouse:

-   [WM \_ MOUSEMOVE](/windows)
-   [ENTRADA \_ WM](/windows)
-   [DirectInput](#directinput)

Cada método presenta ventajas y desventajas, en función de cómo se usarán los datos.

### <a name="wm_mousemove"></a>WM \_ MOUSEMOVE

El método más sencillo para leer los datos de movimiento del mouse es a través de mensajes \_ WM MOUSEMOVE. A continuación se muestra un ejemplo de cómo leer los datos de movimiento del mouse desde el mensaje \_ WM MOUSEMOVE:

```cpp
case WM_MOUSEMOVE:
{
    int xPosAbsolute = GET_X_PARAM(lParam); 
    int yPosAbsolute = GET_Y_PARAM(lParam);
    // ...
    break;
}
```

La desventaja principal de los datos de WM \_ MOUSEMOVE es que se limita a la resolución de pantalla. Esto significa que si mueve el mouse ligeramente , pero no es suficiente para hacer que el puntero se mueva al siguiente píxel, no se genera ningún mensaje \_ WM MOUSEMOVE. Por lo tanto, el uso de este método para leer el movimiento del mouse nega las ventajas de la entrada de alta definición.

Sin embargo, la ventaja de WM MOUSEMOVE es que Windows aplica la aceleración de punteros (también conocida como logística) a los datos sin procesar del mouse, lo que hace que el puntero del mouse se comporte como esperan los \_ clientes. Esto hace que WM MOUSEMOVE sea la opción preferida para el control de puntero (sobre WM INPUT o DirectInput), ya que da como resultado un comportamiento \_ más natural para los \_ usuarios. Aunque WM MOUSEMOVE es ideal para mover punteros del mouse, no es tan bueno para mover una cámara en primera persona, ya que se perderá la precisión de alta \_ definición.

Para obtener más información sobre WM \_ MOUSEMOVE, vea [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove).

### <a name="wm_input"></a>ENTRADA \_ WM

El segundo método para obtener datos del mouse es leer mensajes WM \_ INPUT. El procesamiento de mensajes WM INPUT es más complicado que procesar mensajes WM MOUSEMOVE, pero los mensajes WM INPUT se leen directamente desde la pila de dispositivos de interfaz humana (HID) y reflejan los resultados de alta \_ \_ \_ definición.

Para leer los datos de movimiento del mouse desde el mensaje WM INPUT, primero se debe registrar el dispositivo; el código siguiente \_ proporciona un ejemplo de esto:

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

El código siguiente controla los mensajes WM INPUT en el controlador \_ WinProc de la aplicación:

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

La ventaja de usar WM INPUT es que el juego recibe datos sin \_ procesar del mouse en el nivel más bajo posible.

La desventaja es que WM INPUT no tiene ninguna logística aplicada a sus datos, por lo que si desea impulsar un cursor con estos datos, se requiere un esfuerzo adicional para que el cursor se comporte como lo hace \_ en Windows. Para obtener más información sobre cómo aplicar la logística de puntero, vea [Pointer Ballistics for Windows XP](https://www.microsoft.com/whdc/archive/pointer-bal.mspx).

Para obtener más información sobre WM \_ INPUT, vea [Acerca de la entrada sin formato.](/windows/desktop/inputdev/about-raw-input)

### <a name="directinput"></a>DirectInput

[DirectInput](/windows-hardware/drivers/hid/directinput) es un conjunto de llamadas API que abstrae los dispositivos de entrada en el sistema. Internamente, DirectInput crea un segundo subproceso para leer datos DE ENTRADA DE WM y el uso de las API de DirectInput agregará más sobrecarga que simplemente leer \_ WM \_ INPUT directamente. DirectInput solo es útil para leer datos de dispositivos DirectInput. sin embargo, si solo necesita admitir el controlador de Xbox 360 para Windows, use [XInput en su](/windows/desktop/xinput/xinput-game-controller-apis-portal) lugar. En general, el uso de DirectInput no ofrece ninguna ventaja al leer datos de dispositivos de mouse o teclado, y no se recomienda el uso de DirectInput en estos escenarios.

Compare la complejidad del uso [de DirectInput](/windows-hardware/drivers/hid/directinput), que se muestra en el código siguiente, con los métodos descritos anteriormente. Se necesita el siguiente conjunto de llamadas para crear un mouse directInput:

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

A continuación, el dispositivo del mouse DirectInput se puede leer en cada fotograma:

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

En general, el mejor método para recibir datos de movimiento del mouse de alta definición es WM \_ INPUT. Si los usuarios simplemente mueven un puntero del mouse, considere la posibilidad de usar WM MOUSEMOVE para evitar la necesidad de \_ realizar la logística de puntero. Ambos mensajes de ventana funcionarán bien aunque el mouse no sea un mouse de alta definición. Al admitir la alta definición, Windows juegos pueden ofrecer un control más preciso a los usuarios.
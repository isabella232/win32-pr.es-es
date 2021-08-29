---
title: Dispositivos DirectInput y XUSB
description: El controlador de la clase Xbox Common Controller (XUSB) en Windows implementa la interfaz en modo kernel para el archivo DLL XINPUT.
ms.assetid: 8bf47b07-a1b6-7721-2136-3853e72c71ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f06bb814fcf7a4eeffe76258f3f5689512cba60ca2e517ec7f0cff9870f353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926375"
---
# <a name="directinput-and-xusb-devices"></a>Dispositivos DirectInput y XUSB

El controlador de la clase Xbox Common Controller (XUSB) en Windows implementa la interfaz en modo kernel para el archivo DLL XINPUT. Para proporcionar una buena experiencia para los títulos heredados que usan la API [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) con el dispositivo de controlador común, el controlador también exporta una interfaz de clase del dispositivo de interfaz humana (HID), que DirectInput selecciona. Elegimos la asignación de XUSB a HID en función del comportamiento típico en un conjunto de aplicaciones de juegos para la versión original de XINPUT, y actualizamos la asignación para subtipos más recientes. En este tema se describe la asignación.

## <a name="human-interface-device-hid"></a>Dispositivo de interfaz humana (HID)

EL estándar HID es un estándar del comité de Bus serie universal (USB) propuesto originalmente por Microsoft para generalizar los protocolos para los dispositivos de entrada. Consta de un lenguaje de descripción de código de bytes y puede expresar controladores de varios ejes, controladores de varios ejes, controladores de controladores de múltiples ejes, así como controladores para juegos. Dado que este estándar es tan generalizado, es posible que tenga dificultades para escribir software que consuma la entrada de dispositivos arbitrarios. Por lo tanto, para [directInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) API centrada en juegos, hemos desarrollado una suba mapping específica de tipos para animar a los fabricantes de hardware a admitir a través de sus controladores.

- [Definición de clase de dispositivo USB para HID v1.11](https://www.usb.org/document-library/device-class-definition-hid-111)

> [!Important]
> También puede acceder a los dispositivos de entrada HID a través de [rawInput API](../inputdev/about-raw-input.md) y procesar informes de entrada a través de [la API DE HID](/windows-hardware/drivers/hid/introduction-to-hid-concepts) de bajo nivel, pero los comentarios de vibración no funcionarán como con [DirectInput.](/previous-versions/windows/desktop/ee416842(v=vs.85))

## <a name="mappings"></a>Asignaciones

El controlador XUSB implementa una interfaz de clase XUSB y una interfaz de clase HID para dispositivos con el fin de admitir el uso de XINPUT y [DirectInput.](/previous-versions/windows/desktop/ee416842(v=vs.85)) Esta asignación se basa en la información del subtipo XUSB. El controlador implementa cuatro grupos distintos de asignaciones.

| Subtipo XUSB                                      | Asignación                     |
|---------------------------------------------------|-----------------------------|
| XINPUT \_ DEVSUBTYPE \_ GAMEPAD (subtipo 1)           | Controlador para juegos                     |
| XINPUT \_ DEVSUBTYPE \_ WHEEL (subtipo 2)             | Rueda                       |
| XINPUT \_ DEVSUBTYPE \_ STICK DE STICK DE STICK \_ (subtipo 3)     | Stick stick/pad de Stick de Stick/Stick de Stick/     |
| XINPUT \_ DEVSUBTYPE \_ FLIGHT STICK \_ (subtipo 4)     | Flight Stick                |
| XINPUT \_ DEVSUBTYPE \_ DANCE PAD \_ (subtipo 5)        | Valor predeterminado para cualquier subtipo nuevo |
| XINPUT \_ DEVSUBTYPEOPEN \_ (subtipo 6)            | Guitarra                      |
| XINPUT \_ DEVSUBTYPEOPEN \_ \_ ALTERNATE (subtipo 7) |                             |
| KIT DETYPE \_ DEVSUBTYPE DE XINPUT \_ \_ (subtipo 8)         |                             |
| XINPUT \_ DEVSUBTYPE \_ HOLO BASS \_ (subtipo 11)     |                             |
| PANEL \_ XINPUT DEVSUBTYPETIPO \_ DETIPO DE TECLADO \_ (subtipo 19)      |                             |

> [!Note]  
> Las siguientes asignaciones de HID son estáticas. Esto significa que, incluso si el informe de funcionalidades del dispositivo indica que no se admite un botón o un eje determinados, la asignación seguirá incluyéndolo, pero siempre indicará un estado desactivado o un valor central.

## <a name="gamepad"></a>Controlador para juegos

Se trata de la asignación predeterminada y está diseñada en torno al controlador común de Xbox estándar y se expone como un tipo de uso de *Gamepad* HID.

| Control                      | Nombre de uso de HID | Página Uso | Identificador de uso   |
|------------------------------|----------------|------------|------------|
| Left Stick                   | X e Y           | 0x01       | 0x30, 0x31 |
| Right Stick                  | Rx, Ry         | 0x01       | 0x33, 0x34 |
| Desencadenador izquierdo + Desencadenador derecho | Z\*            | 0x01       | 0x32       |
| D-Pad Up, Down, Left, Right  | Hat Switch     | 0x01       | 0x39       |
| A                            | Botón 1       | 0x09       | 0x01       |
| B                            | Botón 2       | 0x09       | 0x02       |
| X                            | Botón 3       | 0x09       | 0x03       |
| Y                            | Botón 4       | 0x09       | 0x04       |
| LB (parachoques izquierdo)             | Botón 5       | 0x09       | 0x05       |
| RB (parachoques derecho)            | Botón 6       | 0x09       | 0x06       |
| ATRÁS                         | Botón 7       | 0x09       | 0x07       |
| START                        | Botón 8       | 0x09       | 0x08       |
| LSB (botón de stick izquierdo)      | Botón 9       | 0x09       | 0x09       |
| RSB (botón de stick derecho)     | Botón 10      | 0x09       | 0x0A       |

> [!Note]  
> ( ): se combina para que Z presente el comportamiento de centrado esperado por la mayoría de los títulos para la rotación; esto significa que no es posible ver todos los valores de combinación de desencadenadores posibles a través de \* [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) y HID.

## <a name="arcade-stickarcade-pad"></a>Stick stick/pad de Stick de Stick de Stick/Stick de Stick de Stick de

Se trata de la asignación diseñada en torno al controlador Stick de Stick y se expone como un *tipo de uso de Gamepad* HID. El panel de Pad de Pad es muy parecido a un stick de Stick de Stick, pero en un factor de forma más pequeño. Estos diseños reemplazan el desencadenador izquierdo análogo y el desencadenador derecho por botones digitales que informan del valor mínimo y máximo del eje.

| Control                     | Nombre de uso de HID | Página Uso | Identificador de uso |
|-----------------------------|----------------|------------|----------|
| D-Pad Up, Down, Left, Right | Hat Switch     | 0x01       | 0x39     |
| A                           | Botón 1       | 0x09       | 0x01     |
| B                           | Botón 2       | 0x09       | 0x02     |
| X                           | Botón 3       | 0x09       | 0x03     |
| Y                           | Botón 4       | 0x09       | 0x04     |
| LB (parachoques izquierdo)            | Botón 5       | 0x09       | 0x05     |
| RB (parachoques derecho)           | Botón 6       | 0x09       | 0x06     |
| ATRÁS                        | Botón 7       | 0x09       | 0x07     |
| START                       | Botón 8       | 0x09       | 0x08     |
| Desencadenador izquierdo                | Botón 9       | 0x09       | 0x09     |
| Desencadenador derecho               | Botón 10      | 0x09       | 0x0A     |

Estos dispositivos pueden o no admitir controles adicionales, pero estos no se exponen mediante la asignación de HID: Left Stick, Right Stick, LSB (botón de stick izquierdo) y RSB (botón de stick derecho).

## <a name="wheel"></a>Rueda

Esta asignación está diseñada en torno a Xbox Race Wheel y se expone como un *tipo de uso DE GAMEPAD* HID.

| Control                                                        | Nombre de uso de HID | Página Uso | Identificador de uso |
|----------------------------------------------------------------|----------------|------------|----------|
| Wheel (Left Stick X)                                           | X              | 0x01       | 0x30     |
| Acelerador Ctrl (desencadenador derecho) + interruptor de acelerador (desencadenador izquierdo) | Z\*            | 0x01       | 0x32     |
| D-Pad Up, Down, Left, Right                                    | Hat Switch     | 0x01       | 0x39     |
| A                                                              | Botón 1       | 0x09       | 0x01     |
| B                                                              | Botón 2       | 0x09       | 0x02     |
| X                                                              | Botón 3       | 0x09       | 0x03     |
| Y                                                              | Botón 4       | 0x09       | 0x04     |
| LB (parachoques izquierdo)                                               | Botón 5       | 0x09       | 0x05     |
| RB (parachoques derecho)                                              | Botón 6       | 0x09       | 0x06     |
| LSB (botón de stick izquierdo)                                        | Botón 7       | 0x09       | 0x07     |
| RSB (botón de stick derecho)                                       | Botón 8       | 0x09       | 0x08     |
| ATRÁS                                                           | Botón 9       | 0x09       | 0x09     |
| START                                                          | Botón 10      | 0x09       | 0x0A     |

> [!Note]  
> ( ): esto se combina para que Z presente el comportamiento de centrado esperado por la mayoría de los títulos para los controles de acelerador y de acelerador; esto significa que no es posible ver todos los valores de combinación de teclas posibles a través de \* [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)).

## <a name="flight-stick"></a>Flight Stick

Esta asignación está diseñada en torno a Xbox Flight Stick y se expone como un tipo de uso *de Hid* HID.

| Control                     | Nombre de uso | Página Uso | Identificador de uso   |
|-----------------------------|------------|------------|------------|
| Flight Stick (Left Stick)   | X e Y       | 0x01       | 0x30, 0x31 |
| POV Hat (Right Stick)       | Rx, Ry     | 0x01       | 0x33, 0x34 |
| Limitación (desencadenador derecho)    | Z          | 0x01       | 0x32       |
| Hasta el desenlace (desencadenador izquierdo)       | Rz         | 0x01       | 0x35       |
| D-Pad Up, Down, Left, Right | Hat Switch | 0x01       | 0x39       |
| Primario (A)          | Botón 1   | 0x09       | 0x01       |
| Secundaria secundaria (B)        | Botón 2   | 0x09       | 0x02       |
| X                           | Botón 3   | 0x09       | 0x03       |
| Y                           | Botón 4   | 0x09       | 0x04       |
| LB (parachoques izquierdo)            | Botón 5   | 0x09       | 0x05       |
| RB (topes derecho)           | Botón 6   | 0x09       | 0x06       |
| ATRÁS                        | Botón 7   | 0x09       | 0x07       |
| START                       | Botón 8   | 0x09       | 0x08       |
| LSB (botón de stick izquierdo)     | Botón 9   | 0x09       | 0x09       |
| RSB (botón de stick derecho)    | Botón 10  | 0x09       | 0x0A       |

> [!Note]  
> Esto se basa en el diseño final de Flight Stick. Dado que esto difiere de las primeras definiciones de Flight Stick, muchos dispositivos tienen un conmutador de modo que admite el modelo antiguo frente al nuevo. Esta asignación supone el nuevo modelo.
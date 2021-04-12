---
title: Dispositivos DirectInput y XUSB
description: El controlador de la clase de controlador común de Xbox (XUSB) en Windows implementa la interfaz de modo kernel para el archivo DLL de XINPUT.
ms.assetid: 8bf47b07-a1b6-7721-2136-3853e72c71ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2b6d2857502c0e0209d94fb6d933618c180fd2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359372"
---
# <a name="directinput-and-xusb-devices"></a>Dispositivos DirectInput y XUSB

El controlador de la clase de controlador común de Xbox (XUSB) en Windows implementa la interfaz de modo kernel para el archivo DLL de XINPUT. Para proporcionar una buena experiencia en el caso de los títulos heredados que usan la API de [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) con el dispositivo de controlador común, el controlador también exporta una interfaz de clase dispositivo de interfaz humana (HID), que es recogida por DirectInput. Elegimos la asignación de XUSB a HID según el comportamiento típico en un conjunto de aplicaciones de juegos para la versión de XINPUT original y actualizamos la asignación para los subtipos más recientes. En este tema se describe la asignación.

## <a name="human-interface-device-hid"></a>Dispositivo de interfaz humana (HID)

El estándar HID es un estándar del Comité de bus serie universal (USB) propuesto originalmente por Microsoft para generalizar los protocolos de los dispositivos de entrada. Consta de un lenguaje de descripción de código de bytes y puede expresar los controladores de juegos, los ratones, los joysticks, los controles de limitación y timón y los controladores de varios ejes. Dado que esta norma está generalizada, puede que tenga dificultades para escribir software que consume datos de dispositivos arbitrarios. Por lo tanto, para la API de [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) centrada en juegos, desarrollamos una subasignación específica de tipos para fomentar la compatibilidad de los fabricantes de hardware a través de sus controladores.

- [Definición de clase de dispositivo USB para HID v 1.11](https://www.usb.org/document-library/device-class-definition-hid-111)

> [!Important]
> También puede acceder a los dispositivos de entrada HID a través de la [API de RawInput](../inputdev/about-raw-input.md) y procesar los informes de entrada a través de la [API HID](/windows-hardware/drivers/hid/introduction-to-hid-concepts) de bajo nivel, pero los comentarios sobre vibraciones no funcionarán como con [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)).

## <a name="mappings"></a>Asignaciones

El controlador XUSB implementa una interfaz de clase XUSB y una interfaz de clase HID para dispositivos con el fin de admitir el uso de XINPUT y [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) . Esta asignación se basa en la información del subtipo XUSB. El controlador implementa cuatro grupos de asignaciones distintos.

| Subtipo XUSB                                      | Asignación                     |
|---------------------------------------------------|-----------------------------|
| \_Controlador de juegos DEVSUBTYPE de XInput \_ (subtipo 1)           | Controlador para juegos                     |
| \_Rueda DEVSUBTYPE de XInput \_ (subtipo 2)             | Rueda                       |
| \_Stick arcade de DEVSUBTYPE de XInput \_ \_ (subtipo 3)     | Stick Arcade/Pad Arcade     |
| DEVSUBTYPE de los vuelos de XINPUT \_ \_ \_ (subtipo 4)     | Stick de vuelo                |
| Controlador de baile de DEVSUBTYPE de XINPUT \_ \_ \_ (subtipo 5)        | Valor predeterminado para cualquier subtipo nuevo |
| DEVSUBTYPE de XINPUT \_ \_ (subtipo 6)            | Guitarra                      |
| \_Alternativa de guitarra DEVSUBTYPE de XInput \_ \_ (subtipo 7) |                             |
| Kit de tambor de DEVSUBTYPE de XINPUT \_ \_ \_ (subtipo 8)         |                             |
| Bajo de DEVSUBTYPE de XINPUT \_ \_ \_ (subtipo 11)     |                             |
| \_Controlador arcade de DEVSUBTYPE de XInput \_ \_ (subtipo 19)      |                             |

> [!Note]  
> Las siguientes asignaciones de HID son estáticas. Esto significa que incluso si el informe de funcionalidades del dispositivo indica que no se admite un botón o un eje determinados, la asignación lo incluirá pero siempre notificará un valor de estado o de centro.

## <a name="gamepad"></a>Controlador para juegos

Esta es la asignación predeterminada y está diseñada en torno al controlador de juegos de controlador común de Xbox estándar y se expone como un tipo de uso HID del controlador de *juegos* .

| Control                      | Nombre de uso de HID | Página uso | IDENTIFICADOR de uso   |
|------------------------------|----------------|------------|------------|
| Stick izquierdo                   | X e Y           | 0x01       | 0x30, 0x31 |
| Stick derecho                  | RX, Ry         | 0x01       | 0x33, 0x34 |
| Desencadenador izquierdo + desencadenador derecho | Z\*            | 0x01       | 0x32       |
| Cruceta hacia arriba, hacia abajo, a la izquierda, a la derecha  | Conmutador Hat     | 0x01       | 0x39       |
| A                            | Botón 1       | 0x09       | 0x01       |
| B                            | Botón 2       | 0x09       | 0x02       |
| X                            | Botón 3       | 0x09       | 0x03       |
| Y                            | Botón 4       | 0x09       | 0x04       |
| LB (reboteadores izquierdo)             | Botón 5       | 0x09       | 0x05       |
| RB (reboteador derecho)            | Botón 6       | 0x09       | 0x06       |
| ATRÁS                         | Botón 7       | 0x09       | 0x07       |
| START                        | Botón 8       | 0x09       | 0x08       |
| LSB (botón de Stick izquierdo)      | Botón 9       | 0x09       | 0x09       |
| RSB (botón de stick derecho)     | Botón 10      | 0x09       | 0x0A       |

> [!Note]  
> ( \* ): Se combina de modo que Z exhibe el comportamiento de centrado que esperan la mayoría de los títulos para la rotación; esto significa que no es posible ver todos los valores posibles de la combinación de desencadenadores a través de [DIRECTINPUT](/previous-versions/windows/desktop/ee416842(v=vs.85)) y HID.

## <a name="arcade-stickarcade-pad"></a>Stick Arcade/Pad Arcade

Esta es la asignación diseñada alrededor del controlador de sticks Arcade y se expone como un tipo de uso HID del *controlador de juegos* . El panel Arcade es muy parecido a un stick Arcade, pero en un factor de forma más pequeño. Estos diseños reemplazan el desencadenador de apertura analógico y el desencadenador derecho por botones digitales que informan del valor de eje mínimo y máximo.

| Control                     | Nombre de uso de HID | Página uso | IDENTIFICADOR de uso |
|-----------------------------|----------------|------------|----------|
| Cruceta hacia arriba, hacia abajo, a la izquierda, a la derecha | Conmutador Hat     | 0x01       | 0x39     |
| A                           | Botón 1       | 0x09       | 0x01     |
| B                           | Botón 2       | 0x09       | 0x02     |
| X                           | Botón 3       | 0x09       | 0x03     |
| Y                           | Botón 4       | 0x09       | 0x04     |
| LB (reboteadores izquierdo)            | Botón 5       | 0x09       | 0x05     |
| RB (reboteador derecho)           | Botón 6       | 0x09       | 0x06     |
| ATRÁS                        | Botón 7       | 0x09       | 0x07     |
| START                       | Botón 8       | 0x09       | 0x08     |
| Desencadenador izquierdo                | Botón 9       | 0x09       | 0x09     |
| Desencadenador derecho               | Botón 10      | 0x09       | 0x0A     |

Estos dispositivos pueden o no admitir controles adicionales, pero no se exponen mediante la asignación de HID: Stick izquierdo, stick derecho, LSB (botón de Stick izquierdo) y RSB (botón de botón de adhesivo derecho).

## <a name="wheel"></a>Rueda

Esta asignación está diseñada en torno a la rueda de carreras de Xbox y se expone como un tipo de uso HID del *controlador de juegos* .

| Control                                                        | Nombre de uso de HID | Página uso | IDENTIFICADOR de uso |
|----------------------------------------------------------------|----------------|------------|----------|
| Rueda (Stick izquierdo X)                                           | X              | 0x01       | 0x30     |
| Pedal de acelerador (desencadenador derecho) + pedal de freno (desencadenador izquierdo) | Z\*            | 0x01       | 0x32     |
| Cruceta hacia arriba, hacia abajo, a la izquierda, a la derecha                                    | Conmutador Hat     | 0x01       | 0x39     |
| A                                                              | Botón 1       | 0x09       | 0x01     |
| B                                                              | Botón 2       | 0x09       | 0x02     |
| X                                                              | Botón 3       | 0x09       | 0x03     |
| Y                                                              | Botón 4       | 0x09       | 0x04     |
| LB (reboteadores izquierdo)                                               | Botón 5       | 0x09       | 0x05     |
| RB (reboteador derecho)                                              | Botón 6       | 0x09       | 0x06     |
| LSB (botón de Stick izquierdo)                                        | Botón 7       | 0x09       | 0x07     |
| RSB (botón de stick derecho)                                       | Botón 8       | 0x09       | 0x08     |
| ATRÁS                                                           | Botón 9       | 0x09       | 0x09     |
| START                                                          | Botón 10      | 0x09       | 0x0A     |

> [!Note]  
> ( \* ): Se combina de modo que Z exhibe el comportamiento de centrado que esperan la mayoría de los títulos para los controles de frenos y aceleradores; esto significa que no es posible ver todos los valores posibles de la combinación del pedal a través de [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)).

## <a name="flight-stick"></a>Stick de vuelo

Esta asignación está diseñada en torno a la caja de vuelo de Xbox y se expone como un tipo de uso HID de *joystick* .

| Control                     | Nombre de uso | Página uso | IDENTIFICADOR de uso   |
|-----------------------------|------------|------------|------------|
| Stick de vuelo (Stick izquierdo)   | X e Y       | 0x01       | 0x30, 0x31 |
| POV Hat (stick derecho)       | RX, Ry     | 0x01       | 0x33, 0x34 |
| Limitación (desencadenador derecho)    | Z          | 0x01       | 0x32       |
| Timón (desencadenador izquierdo)       | Rz         | 0x01       | 0x35       |
| Cruceta hacia arriba, hacia abajo, a la izquierda, a la derecha | Conmutador Hat | 0x01       | 0x39       |
| Armas principales (A)          | Botón 1   | 0x09       | 0x01       |
| Arma secundario (B)        | Botón 2   | 0x09       | 0x02       |
| X                           | Botón 3   | 0x09       | 0x03       |
| Y                           | Botón 4   | 0x09       | 0x04       |
| LB (reboteadores izquierdo)            | Botón 5   | 0x09       | 0x05       |
| RB (reboteador derecho)           | Botón 6   | 0x09       | 0x06       |
| ATRÁS                        | Botón 7   | 0x09       | 0x07       |
| START                       | Botón 8   | 0x09       | 0x08       |
| LSB (botón de Stick izquierdo)     | Botón 9   | 0x09       | 0x09       |
| RSB (botón de stick derecho)    | Botón 10  | 0x09       | 0x0A       |

> [!Note]  
> Esto se basa en el diseño final del stick de vuelo. Dado que esto difiere de las definiciones tempranas del stick de vuelos, muchos dispositivos tienen un modificador de modo que admite el modelo anterior frente al nuevo. Esta asignación supone el nuevo modelo.
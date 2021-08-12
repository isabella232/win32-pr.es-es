---
title: Secuencias de claves
description: Una cadena de secuencia de claves es un conjunto delimitado por comas de identificadores de clave que se usan para simular la secuencia de pulsación y liberación de teclas de un teclado estándar de estilo AT de 101 teclas de EE. UU.
ms.assetid: 6f5301d1-af6e-4b43-8884-c76b2300ba92
keywords:
- Windows Virtual PC Virtual PC, secuencias de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b300c1d417bad30f7a0e06fd8cfb411184eb8f6b800549536c9b6452dcdfefa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591450"
---
# <a name="key-sequences"></a>Secuencias de claves

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Una cadena de secuencia de claves es un conjunto delimitado por comas de identificadores de clave que se usan para simular la secuencia de pulsación y liberación de teclas de un teclado estándar de estilo AT de 101 teclas de EE. UU.

Si aparece un identificador de clave en la cadena sin un modificador anterior, se simula un código presionado por teclas, seguido inmediatamente de su código correspondiente liberado por clave. Los modificadores de clave se pueden usar para cambiar este comportamiento.

Por ejemplo, el **modificador DOWN** enviará el código presionado por la tecla para el siguiente identificador de clave sin enviar el código liberado por clave. Esto resulta útil para simular las teclas Ctrl, Alt y Mayús cuando se mantienen presionadas mientras se envían otras claves. Para liberar la clave, debe incluirse de nuevo en la cadena de clave junto con un modificador **UP** anterior.

## <a name="key-identifiers"></a>Identificadores de clave

En la lista siguiente se detallan las cadenas de identificador de clave válidas. 

| Cadena de identificador de clave | Significado                         |
|-----------------------|---------------------------------|
| Escape de \_ clave           | tecla **Esc**                 |
| Clave \_ F1               | tecla **F1**                  |
| Clave \_ F2               | tecla **F2**                  |
| Clave \_ F3               | tecla **F3**                  |
| Clave \_ F4               | tecla **F4**                  |
| Clave \_ F5               | tecla **F5**                  |
| Clave \_ F6               | tecla **F6**                  |
| Clave \_ F7               | tecla **F7**                  |
| Clave \_ F8               | tecla **F8**                  |
| Clave \_ F9               | tecla **F9**                  |
| Clave \_ F10              | tecla **F10**                 |
| Clave \_ F11              | tecla **F11**                 |
| Clave \_ F12              | tecla **F12**                 |
| \_SysReq de clave           | la **clave SysReq**              |
| Key \_ ScrollLock       | tecla **ScrollLock**          |
| Interrupción \_ de clave            | tecla **Interrumpir**               |
| Key \_ LeftApostrophe   | la **\`** clave                  |
| Clave \_ 1                | la **clave 1**                   |
| Clave \_ 2                | la **tecla 2**                   |
| Clave \_ 3                | la **clave 3**                   |
| Clave \_ 4                | la **clave 4**                   |
| Clave \_ 5                | la **tecla 5**                   |
| Clave \_ 6                | la **clave 6**                   |
| Clave \_ 7                | la **tecla 7**                   |
| Clave \_ 8                | la **clave 8**                   |
| Clave \_ 9                | la **tecla 9**                   |
| Clave \_ 0                | la **clave 0**                   |
| Guión \_ de clave           | la **-** clave                   |
| La \_ clave es igual a           | la **=** clave                   |
| Retroceso \_ de clave        | tecla **Retroceso**           |
| Inserción \_ de claves           | la **clave Ins**                 |
| Inicio \_ de la clave             | la **tecla** Inicio                |
| PageUp \_ de claves           | la **clave PageUp**              |
| Key \_ NumLock          | la **clave NumLock**             |
| División \_ del Teclado        | la **/** clave en el teclado     |
| Multiplicación \_ del Teclado      | la **\*** clave en el teclado    |
| Teclado \_ Menos         | la **-** clave en el teclado     |
| Pestaña \_ Clave              | tecla **Tab**                 |
| Clave \_ Q                | la **clave Q**                   |
| Clave \_ W                | la **clave W**                   |
| Clave \_ E                | la **clave E**                   |
| Clave \_ R                | la **clave de R**                   |
| Clave \_ T                | la **clave T**                   |
| Clave \_ Y                | la **clave Y**                   |
| Clave \_ U                | la **clave U**                   |
| Clave \_ I                | la **clave I**                   |
| Clave \_ O                | tecla **O**                   |
| Clave \_ P                | la **tecla P**                   |
| Key \_ LeftBracket      | la **\[** clave                  |
| Key \_ RightBracket     | la **\]** clave                  |
| Barra \_ diagonal inversa de clave        | la **\\** clave                  |
| Eliminación \_ de claves           | la **clave Delete**              |
| Key \_ End              | la **tecla** End                 |
| Key \_ PageDown         | la **clave PageDown**            |
| KeyPad \_ 7             | la **tecla 7** en el teclado     |
| KeyPad \_ 8             | la **tecla 8** en el teclado     |
| KeyPad \_ 9             | tecla **9** en el teclado     |
| KeyPad \_ Plus          | la **+** clave en el teclado     |
| Clave \_ A                | la **clave A**                   |
| Clave \_ S                | la **tecla S**                   |
| Clave \_ D                | la **clave D**                   |
| Clave \_ F                | tecla **F**                   |
| Clave \_ G                | la **clave G**                   |
| Clave \_ H                | la **tecla H**                   |
| Clave \_ J                | la **clave J**                   |
| Clave \_ K                | la **tecla K**                   |
| Clave \_ L                | la **clave L**                   |
| Key \_ SemiColon        | la **clave ;**                   |
| Key \_ SingleQuote      | la **tecla '**                   |
| Entrada \_ de clave            | la **tecla Entrar**               |
| KeyPad \_ 4             | la **tecla 4** en el teclado     |
| KeyPad \_ 5             | la **tecla 5** en el teclado     |
| KeyPad \_ 6             | la **tecla 6** en el teclado     |
| Key \_ LeftShift        | tecla **Mayús a la** izquierda          |
| Clave \_ Z                | la **clave Z**                   |
| Clave \_ X                | la **tecla X**                   |
| Clave \_ C                | la **clave C**                   |
| Clave \_ V                | la **clave V**                   |
| Clave \_ B                | la **clave B**                   |
| Clave \_ N                | la **tecla N**                   |
| Clave \_ M                | la **clave M**                   |
| Coma \_ de clave            | la **clave ,**                   |
| Período de \_ claves           | .  key                   |
| Barra \_ diagonal de clave            | la **/** clave                   |
| Key \_ RightShift       | tecla **Mayús a la** derecha         |
| Key \_ Up               | tecla **Arriba**                  |
| KeyPad \_ 1             | la **tecla 1** en el teclado     |
| KeyPad \_ 2             | la **tecla 2** en el teclado     |
| KeyPad \_ 3             | la **tecla 3** en el teclado     |
| Entrar en el Teclado \_         | la **tecla Entrar** en el teclado |
| Key \_ LeftCtrl         | tecla **Ctrl de la** izquierda           |
| Key \_ LeftWindows      | tecla **de Windows** izquierda        |
| Key \_ LeftAlt          | tecla **Alt izquierda**            |
| Espacio de \_ claves            | tecla **De** espacio               |
| Key \_ RightAlt         | tecla **Alt** derecha           |
| Key \_ RightWindows     | tecla **de Windows** derecha       |
| Key \_ RightCtrl        | Tecla **Ctrl derecha**          |
| Aplicación \_ clave      | la **clave de** aplicación         |
| Tecla \_ izquierda             | tecla **Izquierda**                |
| Tecla \_ abajo             | tecla **Abajo**                |
| Tecla \_ derecha            | la **tecla** derecha               |
| KeyPad \_ 0             | tecla **0** en el teclado     |
| KeyPad \_ DecimalPoint  | .  clave en el teclado     |



 

## <a name="key-modifiers"></a>Modificadores de clave

En la lista siguiente se detallan las cadenas modificadoras de clave válidas. 

| Cadena modificadora de clave | Significado                                                                                       |
|---------------------|-----------------------------------------------------------------------------------------------|
| ABAJO                | Envíe un código presionado por la tecla para el siguiente identificador de clave sin enviar un código liberado por clave. |
| UP                  | Envíe un código liberado por clave para el siguiente identificador de clave.                                    |
| HOLD                | Pause 200 milisegundos antes de continuar procesando el resto de la cadena de secuencia de claves. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

 
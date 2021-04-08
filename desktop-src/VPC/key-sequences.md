---
title: Secuencias de claves
description: Una cadena de secuencia de claves es un conjunto delimitado por comas de identificadores de clave que se usan para simular la secuencia de pulsación de tecla y de versión de un teclado en estilo estándar 101 de EE. UU..
ms.assetid: 6f5301d1-af6e-4b43-8884-c76b2300ba92
keywords:
- Windows Virtual PC Virtual PC, secuencias de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c973b5aafd3bf02746ac1550ffedf3d4a4c1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793113"
---
# <a name="key-sequences"></a>Secuencias de claves

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Una cadena de secuencia de claves es un conjunto delimitado por comas de identificadores de clave que se usan para simular la secuencia de pulsación de tecla y de versión de un teclado en estilo estándar 101 de EE. UU..

Si aparece un identificador de clave en la cadena sin un modificador anterior, se simula un código presionado con la tecla, seguido inmediatamente del código de lanzamiento de clave correspondiente. Los modificadores de clave se pueden usar para cambiar este comportamiento.

Por ejemplo, el modificador **Down** enviará el código presionado por la tecla para el siguiente identificador de clave sin enviar el código liberado por la clave. Esto resulta útil para simular las teclas Ctrl, Alt y Mayús cuando se mantienen presionadas mientras se envían otras claves. Para liberar la clave, se debe volver a incluir en la cadena de clave junto con un **modificador** anterior.

## <a name="key-identifiers"></a>Identificadores de clave

En la siguiente lista se detallan las cadenas de identificador de clave válidas. 

| Cadena de identificador de clave | Significado                         |
|-----------------------|---------------------------------|
| Escape de clave \_           | tecla **ESC**                 |
| Tecla \_ F1               | tecla **F1**                  |
| Tecla \_ F2               | tecla **F2**                  |
| Tecla \_ F3               | tecla **F3**                  |
| Tecla \_ F4               | tecla **F4**                  |
| Tecla \_ F5               | la tecla **F5**                  |
| Tecla \_ F6               | tecla **F6**                  |
| Tecla \_ F7               | tecla **F7**                  |
| Tecla \_ F8               | tecla **F8**                  |
| Tecla \_ F9               | tecla **F9**                  |
| Tecla \_ F10              | tecla **F10**                 |
| Clave \_ F11              | tecla **F11**                 |
| Tecla \_ F12              | tecla **F12**                 |
| Clave \_ SysReq           | la clave **SysReq**              |
| \_Bloq Despl       | la tecla **ScrollLock**          |
| Salto de clave \_            | tecla **inter**               |
| Clave \_ LeftApostrophe   | la **\`** clave                  |
| Clave \_ 1                | tecla **1**                   |
| Clave \_ 2                | la tecla **2**                   |
| Clave \_ 3                | la tecla **3**                   |
| Clave \_ 4                | tecla **4**                   |
| Clave \_ 5                | la tecla **5**                   |
| Clave \_ 6                | la clave **6**                   |
| Clave \_ 7                | la tecla **7**                   |
| Clave \_ 8                | la tecla **8**                   |
| Clave \_ 9                | la tecla **9**                   |
| Clave \_ 0                | tecla **0**                   |
| Guion de clave \_           | la **-** clave                   |
| La clave \_ es igual a           | la **=** clave                   |
| Retroceso de clave \_        | tecla **retroceso**           |
| Inserción de clave \_           | tecla **ins**                 |
| Inicio de la clave \_             | tecla **Inicio**                |
| Tecla \_ RePág           | tecla **RePág**              |
| Tecla \_ BLOQ NUM          | tecla **BLOQ NUM**             |
| División del teclado \_        | **/** tecla del teclado numérico     |
| Multiplicación del teclado numérico \_      | **\*** tecla del teclado numérico    |
| Teclado \_ menos         | **-** tecla del teclado numérico     |
| \_Pestaña clave              | tecla **Tab**                 |
| Tecla \_ Q                | tecla **Q**                   |
| Clave \_ W                | tecla **W**                   |
| Clave \_ E                | tecla **E**                   |
| Tecla \_ R                | tecla **R**                   |
| Clave \_ T                | tecla **T**                   |
| Clave \_ Y                | tecla **Y**                   |
| Clave \_ U                | tecla **U**                   |
| Clave \_ I                | tecla **I**                   |
| Clave \_ O                | tecla **O**                   |
| Clave \_ P                | tecla **P**                   |
| Clave \_ LeftBracket      | la **\[** clave                  |
| Clave \_ RightBracket     | la **\]** clave                  |
| \_Barra diagonal inversa de clave        | la **\\** clave                  |
| Eliminación de clave \_           | la tecla **Supr**              |
| Extremo de la clave \_              | tecla **fin**                 |
| Tecla \_ Av Pág         | tecla **Av Pág**            |
| Teclado numérico \_ 7             | tecla **7** del teclado numérico     |
| Teclado numérico \_ 8             | tecla **8** del teclado numérico     |
| Teclado numérico \_ 9             | tecla **9** del teclado numérico     |
| Teclado numérico \_ más          | **+** tecla del teclado numérico     |
| Clave \_ A                | tecla **A**                   |
| Clave \_ S                | tecla **S**                   |
| Clave \_ D                | tecla **D**                   |
| Clave \_ F                | tecla **F**                   |
| Clave \_ G                | tecla **G**                   |
| Clave \_ H                | tecla **H**                   |
| Clave \_ J                | tecla **J**                   |
| Clave \_ K                | tecla **K**                   |
| Clave \_ L                | tecla **L**                   |
| Tecla \_ punto y coma        | la clave **;**                   |
| Clave \_ SingleQuote      | tecla **'**                   |
| Tecla \_ entrar            | tecla **entrar**               |
| Teclado numérico \_ 4             | tecla **4** del teclado numérico     |
| Teclado numérico \_ 5             | tecla **5** del teclado numérico     |
| Teclado numérico \_ 6             | tecla **6** del teclado numérico     |
| Clave \_ Mayús Izq        | tecla **MAYÚS izquierda**          |
| Clave \_ Z                | la tecla **Z**                   |
| Clave \_ X                | tecla **X**                   |
| Clave \_ C                | tecla **C**                   |
| Clave \_ V                | tecla **V**                   |
| Clave \_ B                | tecla **B**                   |
| Clave \_ N                | tecla **N**                   |
| Clave \_ M                | tecla **M**                   |
| \_Coma clave            | la **clave**                   |
| \_Período clave           | el **.** key                   |
| \_Barra diagonal clave            | la **/** clave                   |
| Clave \_ Mayús Der       | tecla **MAYÚS derecha**         |
| Tecla \_ arriba               | tecla **arriba**                  |
| Teclado numérico \_ 1             | tecla **1** del teclado numérico     |
| Teclado \_ 2             | tecla **2** del teclado numérico     |
| Teclado numérico \_ 3             | tecla **3** del teclado numérico     |
| Teclado \_ numérico         | tecla **entrar** en el teclado numérico |
| Clave \_ LeftCtrl         | tecla **Ctrl izquierda**           |
| Clave \_ LeftWindows      | tecla **Windows izquierda**        |
| Clave \_ LeftAlt          | la tecla **Alt izquierda**            |
| Espacio de clave \_            | la clave de **espacio**               |
| Clave \_ RightAlt         | la tecla **Alt derecha**           |
| Clave \_ RightWindows     | tecla de **Windows derecha**       |
| Clave \_ RightCtrl        | tecla **Ctrl derecha**          |
| \_Aplicación clave      | la clave de **aplicación**         |
| Tecla \_ izquierda             | la tecla **izquierda**                |
| Tecla \_ abajo             | tecla **abajo**                |
| Tecla \_ derecha            | la tecla **derecha**               |
| Teclado numérico \_ 0             | tecla **0** del teclado numérico     |
| Teclado \_ DecimalPoint  | el **.** tecla del teclado     |



 

## <a name="key-modifiers"></a>Modificadores de clave

En la siguiente lista se detallan las cadenas de modificador de clave válidas. 

| Cadena de modificador de clave | Significado                                                                                       |
|---------------------|-----------------------------------------------------------------------------------------------|
| ABAJO                | Envíe un código presionado por la tecla para el siguiente identificador de clave sin enviar un código de lanzamiento de clave. |
| UP                  | Envíe un código de lanzamiento de claves para el siguiente identificador de clave.                                    |
| HOLD                | PAUSE 200 milisegundos antes de continuar procesando el resto de la cadena de la secuencia de claves. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

 
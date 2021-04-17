---
description: Estas clases representan los dispositivos de entrada de usuario. Una máquina virtual siempre tiene una instancia de cada clase asociada.
ms.assetid: FFCA890D-6102-47BB-B499-4B9D77D75E9B
title: Clases de entrada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2955cadfb00dcc39fed490a9c706b12bb1a8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687196"
---
# <a name="input-classes"></a>Clases de entrada

Estas clases representan los dispositivos de entrada de usuario. Una máquina virtual siempre tiene una instancia de cada clase asociada. Es posible que estos dispositivos no se agreguen o quiten de la máquina virtual. Por lo tanto, no hay instancias del grupo de recursos para dispositivos de teclado o de mouse.

Los dispositivos de teclado y mouse están vinculados a la máquina virtual a través de la Asociación [**MSVM \_ SystemDevice**](msvm-systemdevice.md) . Una máquina virtual contiene un dispositivo de mouse PS2 y uno sintético. Solo hay un dispositivo señalador activo a la vez.

A continuación se enumeran las clases WMI de virtualización relacionadas con la entrada.

## <a name="in-this-section"></a>En esta sección



| Tema                                                          | Descripción                                     |
|----------------------------------------------------------------|-------------------------------------------------|
| [**\_Teclado MSVM**](msvm-keyboard.md)<br/>             | Representa un dispositivo de teclado.<br/>        |
| [**MSVM \_ Ps2Mouse**](msvm-ps2mouse.md)<br/>             | Representa un dispositivo de mouse PS2.<br/>       |
| [**MSVM \_ SyntheticMouse**](msvm-syntheticmouse.md)<br/> | Representa un dispositivo de mouse sintético.<br/> |



 

 

 





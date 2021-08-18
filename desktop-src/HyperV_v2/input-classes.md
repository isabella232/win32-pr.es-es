---
description: Los dispositivos de entrada de usuario se representan mediante estas clases. Una máquina virtual siempre tiene una instancia de cada clase asociada a ella.
ms.assetid: FFCA890D-6102-47BB-B499-4B9D77D75E9B
title: Clases de entrada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5df9c5a2f1d2743e062cf685dc6fd849f33333808315459560dfd840e925135
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644867"
---
# <a name="input-classes"></a>Clases de entrada

Los dispositivos de entrada de usuario se representan mediante estas clases. Una máquina virtual siempre tiene una instancia de cada clase asociada a ella. Estos dispositivos no se pueden agregar ni quitar de la máquina virtual. Por lo tanto, no hay instancias de grupo de recursos para dispositivos de teclado o mouse.

Los dispositivos de teclado y mouse están vinculados a la máquina virtual a través de la [**asociación \_ SystemDevice de Msvm.**](msvm-systemdevice.md) Una máquina virtual contiene un dispositivo PS2 y un dispositivo de mouse sintético. Solo un dispositivo de punto está activo a la vez.

Las siguientes son clases WMI de virtualización relacionadas con la entrada.

## <a name="in-this-section"></a>En esta sección



| Tema                                                          | Descripción                                     |
|----------------------------------------------------------------|-------------------------------------------------|
| [**Teclado de \_ Msvm**](msvm-keyboard.md)<br/>             | Representa un dispositivo de teclado.<br/>        |
| [**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md)<br/>             | Representa un dispositivo del mouse PS2.<br/>       |
| [**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md)<br/> | Representa un dispositivo de mouse sintético.<br/> |



 

 

 





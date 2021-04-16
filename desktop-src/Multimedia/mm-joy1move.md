---
title: Mensaje de MM_JOY1MOVE (mmsystem. h)
description: El \_ mensaje mm JOY1MOVE notifica a la ventana que ha capturado el joystick JOYSTICKID1 que ha cambiado la posición del joystick.
ms.assetid: 317ac0b2-f873-413d-b071-47d840229643
keywords:
- Mensaje de MM_JOY1MOVE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_JOY1MOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a78753bd55f6682b3ac3f1514356d93cb455d162
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676588"
---
# <a name="mm_joy1move-message"></a>\_Mensaje JOY1MOVE mm

El mensaje **mm \_ JOY1MOVE** notifica a la ventana que ha capturado el joystick JOYSTICKID1 que ha cambiado la posición del joystick.


```C++
MM_JOY1MOVE 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifica los botones que se presionan. Puede ser uno o varios de los siguientes valores:



| Requisito | Value |
|--------------|------------------------------------|
| JOY \_ button1 | Se presionó el primer botón del joystick.  |
| JOY \_ BUTTON2 | Se presionó el botón segundo joystick. |
| JOY \_ BUTTON3 | Se presionó el tercer botón del joystick.  |
| JOY \_ BUTTON4 | Se presionó el cuarto botón del joystick. |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Coordenadas x del joystick con respecto a la esquina superior izquierda del área cliente.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*
</dt> <dd>

Coordenada y del joystick con respecto a la esquina superior izquierda del área cliente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Joysticks](joysticks.md)
</dt> <dt>

[Mensajes de joystick multimedia](multimedia-joystick-messages.md)
</dt> </dl>

 

 






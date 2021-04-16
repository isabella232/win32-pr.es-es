---
title: Mensaje de MM_JOY2BUTTONDOWN (mmsystem. h)
description: El \_ mensaje mm JOY2BUTTONDOWN notifica a la ventana que ha capturado el joystick JOYSTICKID2 que se ha presionado un botón.
ms.assetid: b4cd48ea-91ad-48e9-b0ae-58d8ee124171
keywords:
- Mensaje de MM_JOY2BUTTONDOWN de Windows multimedia
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f155fcdc21247e01fd5d730f3f7d4daaba705e65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676587"
---
# <a name="mm_joy2buttondown-message"></a>\_Mensaje JOY2BUTTONDOWN mm

El mensaje **mm \_ JOY2BUTTONDOWN** notifica a la ventana que ha capturado el joystick JOYSTICKID2 que se ha presionado un botón.


```C++
MM_JOY2BUTTONDOWN 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifica el botón que ha cambiado de estado y los botones que se presionan. Puede tener uno de los valores siguientes:



| Requisito | Value |
|-----------------|-------------------------------------------|
| JOY \_ BUTTON1CHG | El primer botón del joystick ha cambiado de estado.  |
| JOY \_ BUTTON2CHG | El segundo botón del joystick ha cambiado de estado. |
| JOY \_ BUTTON3CHG | El tercer botón del joystick ha cambiado de estado.  |
| JOY \_ BUTTON4CHG | El cuarto botón del joystick ha cambiado de estado. |



 

y uno o varios de los siguientes:



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

 

 






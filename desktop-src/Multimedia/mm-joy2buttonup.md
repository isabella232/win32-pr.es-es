---
title: Mensaje de MM_JOY2BUTTONUP (mmsystem. h)
description: El \_ mensaje mm JOY2BUTTONUP notifica a la ventana que ha capturado el joystick JOYSTICKID2 que se ha soltado un botón.
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- Mensaje de MM_JOY2BUTTONUP de Windows multimedia
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7a4f2d23739fc72a6898e2b53fc3e1c330687f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686256"
---
# <a name="mm_joy2buttonup-message"></a>\_Mensaje JOY2BUTTONUP mm

El mensaje **mm \_ JOY2BUTTONUP** notifica a la ventana que ha capturado el joystick JOYSTICKID2 que se ha soltado un botón.


```C++
MM_JOY2BUTTONUP 
fwButton = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

**fwButtons** 
</dt> <dd>

Identifica el botón que ha cambiado de estado y los botones que se presionan. Puede tener uno de los valores siguientes:



| Value                                                                                                                                                            | Significado                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <dt>**JOY \_ BUTTON1CHG**</dt> </dl> | El primer botón del joystick ha cambiado de estado.<br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <dt>**JOY \_ BUTTON2CHG**</dt> </dl> | El segundo botón del joystick ha cambiado de estado.<br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <dt>**JOY \_ BUTTON3CHG**</dt> </dl> | El tercer botón del joystick ha cambiado de estado.<br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <dt>**JOY \_ BUTTON4CHG**</dt> </dl> | El cuarto botón del joystick ha cambiado de estado.<br/> |



 

y uno o varios de los siguientes:



| Value                                                                                                                                                   | Significado                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <dt>**JOY \_ button1**</dt> </dl> | Se presionó el primer botón del joystick.<br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <dt>**JOY \_ BUTTON2**</dt> </dl> | Se presionó el botón segundo joystick.<br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <dt>**JOY \_ BUTTON3**</dt> </dl> | Se presionó el tercer botón del joystick.<br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <dt>**JOY \_ BUTTON4**</dt> </dl> | Se presionó el cuarto botón del joystick.<br/> |



 

</dd> <dt>

**xPos** 
</dt> <dd>

Coordenadas x del joystick con respecto a la esquina superior izquierda del área cliente.

</dd> <dt>

**yPos** 
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

 

 






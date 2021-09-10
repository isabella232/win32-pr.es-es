---
title: MM_JOY1BUTTONDOWN mensaje (Mmsystem.h)
description: El mensaje MM CTRL1BUTTONDOWN notifica a la ventana que ha capturado \_ el botón CTRLID1 que se ha presionado un botón.
ms.assetid: 764f4bb4-134d-46b8-badb-3fb06af31e13
keywords:
- MM_JOY1BUTTONDOWN mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cefb70e5dd47fc14b39dcdeb59043b6827e7b89b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371119"
---
# <a name="mm_joy1buttondown-message"></a>Mensaje \_ MMMIENTO1BUTTONDOWN

El **mensaje MM \_ CTRL1BUTTONDOWN** notifica a la ventana que ha capturado el botón CTRLID1 que se ha presionado un botón.


```C++
MM_JOY1BUTTONDOWN 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifica el botón que ha cambiado el estado y los botones que se presionan. Puede tener uno de los valores siguientes:



| Requisito | Value |
|-----------------|-------------------------------------------|
| \_BUTTON1CHG DE BUTTON1 DE BUTTON1 | El primer botón button ha cambiado de estado.  |
| \_BUTTON2CHG DE BUTTON2 | El segundo botón button ha cambiado de estado. |
| \_BUTTON3CHG DE BUTTON3CHG | El tercer botón button ha cambiado de estado.  |
| \_BUTTON4CHG DE BUTTON4CHG | El cuarto botón button ha cambiado de estado. |



 

y uno o varios de los siguientes:



| Requisito | Value |
|--------------|------------------------------------|
| BOTÓN \_ BUTTON1 DE BUTTON1 DE BUTTON1 | Se presiona el primer botón button button (Botón button).  |
| BUTTON2 \_ DE BUTTON2 PARA BUTTON2 | Se presiona el segundo botón button button (Segundo botón button). |
| BUTTON3 \_ DE BUTTON3 DE BUTTON3 | Se presiona el tercer botón button button (Tercer botón button).  |
| BUTTON4 \_ DE BUTTON4 DE BUTTON4 | Se presiona el cuarto botón button button (Cuarto botón button). |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Coordenada x del ángulo con respecto a la esquina superior izquierda del área cliente.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*
</dt> <dd>

Coordenada y del ángulo con respecto a la esquina superior izquierda del área cliente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Joysticks](joysticks.md)
</dt> <dt>

[Mensajes multimedia multimedia](multimedia-joystick-messages.md)
</dt> </dl>

 

 






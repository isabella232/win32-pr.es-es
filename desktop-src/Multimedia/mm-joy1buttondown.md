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
ms.openlocfilehash: 2d2399eca0de21014b97c9156e6a16349fc5b0b5407b64b022eb077fd59d0609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137196"
---
# <a name="mm_joy1buttondown-message"></a>Mensaje \_ MMAJE1BUTTONDOWN

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

Identifica el botón que ha cambiado de estado y los botones que se presionan. Puede tener uno de los valores siguientes:



| Requisito | Valor |
|-----------------|-------------------------------------------|
| \_BUTTON1CHG DE BUTTON1 DE BUTTON | El primer botón button button ha cambiado de estado.  |
| \_BUTTON2CHG DE BUTTON2 BUTTON2 | El segundo botón button button ha cambiado de estado. |
| \_BUTTON3CHG DE BUTTON3CHG | El tercer botón button button ha cambiado de estado.  |
| \_BUTTON4CHG DE BUTTON4CHG | El cuarto botón button button ha cambiado de estado. |



 

y uno o varios de los siguientes:



| Requisito | Valor |
|--------------|------------------------------------|
| BUTTON1 \_ DE BUTTON1 DE BUTTON1 | Se presiona el primer botón de botones.  |
| BOTÓN \_ BUTTON2 DE BUTTON2 | Se presiona el segundo botón button button (Botón de botones). |
| BOTÓN \_ BUTTON3 DE BUTTON3 | Se presiona el tercer botón de botones.  |
| BOTÓN \_ BUTTON4 DE BUTTON4 | Se presiona el cuarto botón button button (Cuarto botón de botones). |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Coordenada x del borde con respecto a la esquina superior izquierda del área cliente.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*
</dt> <dd>

Coordenada y del borde con respecto a la esquina superior izquierda del área cliente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 






---
title: MM_JOY1MOVE mensaje (Mmsystem.h)
description: El mensaje MMMOV1MOVE notifica a la ventana que ha capturado \_ ELID1 que ha cambiado la posición de la izquierda.
ms.assetid: 317ac0b2-f873-413d-b071-47d840229643
keywords:
- MM_JOY1MOVE mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371138"
---
# <a name="mm_joy1move-message"></a>Mensaje \_ MMMOV1MOVE

El **mensaje \_ MMMOV1MOVE** notifica a la ventana que ha capturado ELID1 que ha cambiado la posición de la izquierda.


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

Identifica los botones que se presionan. Puede ser uno o varios de los valores siguientes:



| Requisito | Value |
|--------------|------------------------------------|
| BOTÓN \_ BUTTON1 DE BUTTON1 DE BUTTON1 | Se presiona el primer botón de botones.  |
| BOTÓN \_ BUTTON2 DE BUTTON2 | Se presiona el segundo botón button button (Botón de botones). |
| BOTÓN \_ BUTTON3 DE BUTTON3 | Se presiona el tercer botón de botones.  |
| BUTTON4 \_ DE BUTTON4 DE BUTTON | Se presiona el cuarto botón button button (Cuarto botón de botones). |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Coordenadas x del borde con respecto a la esquina superior izquierda del área cliente.

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

 

 






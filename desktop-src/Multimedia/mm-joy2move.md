---
title: MM_JOY2MOVE mensaje (Mmsystem.h)
description: El mensaje MMMOV2MOVE notifica a la ventana que ha capturado el botón DE NAVEGACIÓN2 que ha cambiado \_ la posición de la marcha.
ms.assetid: 8dc1c092-3947-43d5-8504-a4e4e121fbcb
keywords:
- MM_JOY2MOVE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY2MOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8921f0ae76d05c429d6750944a26662c1276af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265959"
---
# <a name="mm_joy2move-message"></a>Mensaje \_ MMIJO2MOVE

El **mensaje \_ MMMOV2MOVE** notifica a la ventana que ha capturado el botón DE NAVEGACIÓN2 que ha cambiado la posición de la marcha.


```C++
MM_JOY2MOVE 
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
| BOTÓN \_ BUTTON1 DE BUTTON1 DE BUTTON1 | Se presiona el primer botón button button (Botón button).  |
| BUTTON2 \_ DE BUTTON2 PARA BUTTON2 | Se presiona el segundo botón button button (Segundo botón button). |
| BUTTON3 \_ DE BUTTON3 DE BUTTON3 | Se presiona el tercer botón button button (Tercer botón button).  |
| BUTTON4 \_ DE BUTTON4 DE BUTTON4 | Se presiona el cuarto botón button button (Cuarto botón button). |



 

</dd> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Las coordenadas x del ángulo con respecto a la esquina superior izquierda del área de cliente.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Joysticks](joysticks.md)
</dt> <dt>

[Mensajes multimedia multimedia](multimedia-joystick-messages.md)
</dt> </dl>

 

 






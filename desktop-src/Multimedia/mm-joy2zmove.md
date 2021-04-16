---
title: Mensaje de MM_JOY2ZMOVE (mmsystem. h)
description: El \_ mensaje mm JOY2ZMOVE notifica a la ventana que ha capturado el joystick JOYSTICKID2 que ha cambiado la posición del joystick en el eje z.
ms.assetid: f09a1a11-8c97-4a03-a388-8bf9ab89a3db
keywords:
- Mensaje de MM_JOY2ZMOVE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_JOY2ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d899a4a1c93304075cb166ba805367ceed6ddd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686255"
---
# <a name="mm_joy2zmove-message"></a>\_Mensaje JOY2ZMOVE mm

El mensaje **mm \_ JOY2ZMOVE** notifica a la ventana que ha capturado el joystick JOYSTICKID2 que ha cambiado la posición del joystick en el eje z.


```C++
MM_JOY2ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifica los botones que se presionan. Puede ser uno o varios de los valores siguientes.



| Requisito | Value |
|--------------|------------------------------------|
| JOY \_ button1 | Se presionó el primer botón del joystick.  |
| JOY \_ BUTTON2 | Se presionó el botón segundo joystick. |
| JOY \_ BUTTON3 | Se presionó el tercer botón del joystick.  |
| JOY \_ BUTTON4 | Se presionó el cuarto botón del joystick. |



 

</dd> <dt>

<span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*
</dt> <dd>

Coordenada z del joystick.

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

 

 






---
title: MM_JOY1ZMOVE mensaje (Mmsystem.h)
description: El mensaje MMMUT1ZMOVE notifica a la ventana que ha capturado el valor de LAWID1 que la posición del eje \_ Z ha cambiado.
ms.assetid: 25d98963-03e6-4276-a132-256e8bbfa73b
keywords:
- MM_JOY1ZMOVE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MM_JOY1ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6b0efe11870ac822f7fe8aa0f7aa1deb4856bd8f1394bd1533362d78a3aee00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065545"
---
# <a name="mm_joy1zmove-message"></a>Mensaje \_ MMIJO1ZMOVE

El **mensaje \_ MMMUT1ZMOVE** notifica a la ventana que ha capturado el valor de LAWID1 que la posición del eje Z ha cambiado.


```C++
MM_JOY1ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*
</dt> <dd>

Identifica los botones que se presionan. Puede ser uno o varios de los siguientes valores:



| Requisito | Valor |
|--------------|------------------------------------|
| BOTÓN \_ BUTTON1 DE BUTTON1 DE BUTTON1 | Se presiona el primer botón button button (Botón button).  |
| BUTTON2 \_ DE BUTTON2 PARA BUTTON2 | Se presiona el segundo botón button button (Segundo botón button). |
| BUTTON3 \_ DE BUTTON3 DE BUTTON3 | Se presiona el tercer botón button button (Tercer botón button).  |
| BUTTON4 \_ DE BUTTON4 DE BUTTON4 | Se presiona el cuarto botón button button (Cuarto botón button). |



 

</dd> <dt>

<span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*
</dt> <dd>

Coordenada z del eje.

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

 

 






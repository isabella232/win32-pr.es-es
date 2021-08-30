---
title: MM_JOY2ZMOVE mensaje (Mmsystem.h)
description: El mensaje MMMOV2ZMOVE notifica a la ventana que ha capturado el id. de posición del eje Z que ha cambiado la posición del \_ eje Z.
ms.assetid: f09a1a11-8c97-4a03-a388-8bf9ab89a3db
keywords:
- MM_JOY2ZMOVE mensaje Windows Multimedia
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
ms.openlocfilehash: b9b59a22a4b8fcfa11384a7a89f61657586a9535e8248535641ad37d36dfb0fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807525"
---
# <a name="mm_joy2zmove-message"></a>Mensaje \_ MMMOV2ZMOVE

El **mensaje \_ MMMOV2ZMOVE** notifica a la ventana que ha capturado el id. de posición del eje Z que ha cambiado la posición del eje Z.


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



| Requisito | Valor |
|--------------|------------------------------------|
| BUTTON1 \_ DE BUTTON1 DE BUTTON1 | Se presiona el primer botón de botones.  |
| BOTÓN \_ BUTTON2 DE BUTTON2 | Se presiona el segundo botón button button (Botón de botones). |
| BOTÓN \_ BUTTON3 DE BUTTON3 | Se presiona el tercer botón de botones.  |
| BOTÓN \_ BUTTON4 DE BUTTON4 | Se presiona el cuarto botón button button (Cuarto botón de botones). |



 

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

 

 






---
title: MM_JOY2ZMOVE mensaje (Mmsystem.h)
description: El mensaje MMMOV2ZMOVE notifica a la ventana que ha capturado el id. de posición del eje Z que la posición del eje Z ha \_ cambiado.
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
ms.openlocfilehash: 0d899a4a1c93304075cb166ba805367ceed6ddd3
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371155"
---
# <a name="mm_joy2zmove-message"></a>Mensaje \_ MMMOV2ZMOVE

El **mensaje \_ MMMOV2ZMOVE** notifica a la ventana que ha capturado el id. de posición del eje Z que la posición del eje Z ha cambiado.


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
| BOTÓN \_ BUTTON1 DE BUTTON1 DE BUTTON1 | Se presiona el primer botón de botones.  |
| BOTÓN \_ BUTTON2 DE BUTTON2 | Se presiona el segundo botón button button (Botón de botones). |
| BOTÓN \_ BUTTON3 DE BUTTON3 | Se presiona el tercer botón de botones.  |
| BUTTON4 \_ DE BUTTON4 DE BUTTON | Se presiona el cuarto botón button button (Cuarto botón de botones). |



 

</dd> <dt>

<span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*
</dt> <dd>

Coordenada z del eje.

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

 

 






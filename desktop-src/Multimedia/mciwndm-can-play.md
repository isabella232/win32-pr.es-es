---
title: MCIWNDM_CAN_PLAY mensaje (Vfw.h)
description: El mensaje MCIWNDM CAN PLAY determina si un dispositivo MCI puede reproducir un archivo de datos o \_ \_ contenido de otro tipo. Puede enviar este mensaje explícitamente o mediante la macro MCIWndCanPlay.
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- MCIWNDM_CAN_PLAY mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84d067b01dbce8aaab7c78ab24c3d11fc5d4a3a19b9bfdb663eb653ebc0c553c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374247"
---
# <a name="mciwndm_can_play-message"></a>Mensaje MCIWNDM \_ CAN \_ PLAY

El **mensaje MCIWNDM \_ CAN \_ PLAY** determina si un dispositivo MCI puede reproducir un archivo de datos o contenido de otro tipo. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndCanPlay.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el dispositivo admite la reproducción de los datos o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 






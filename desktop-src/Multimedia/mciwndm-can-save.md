---
title: MCIWNDM_CAN_SAVE mensaje (Vfw.h)
description: El mensaje MCIWNDM \_ CAN SAVE determina si un dispositivo \_ MCI puede guardar datos. Puede enviar este mensaje explícitamente o mediante la macro MCIWndCanSave.
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- MCIWNDM_CAN_SAVE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccab622381208b8213414ed8b156a84e431afffc55acdf2323b0c0a2d31014f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429635"
---
# <a name="mciwndm_can_save-message"></a>MCIWNDM \_ PUEDE \_ GUARDAR mensaje

El **mensaje MCIWNDM \_ CAN \_ SAVE** determina si un dispositivo MCI puede guardar datos. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndCanSave.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** el dispositivo admite guardar o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 






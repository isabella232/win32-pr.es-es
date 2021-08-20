---
title: MCIWNDM_GETDEVICEID mensaje (Vfw.h)
description: El mensaje GETDEVICEID de MCIWNDM recupera el identificador del dispositivo MCI abierto actualmente para usarlo \_ con la función mciSendCommand. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetDeviceID.
ms.assetid: 188f15fa-579a-438e-a812-9a2b684127c0
keywords:
- MCIWNDM_GETDEVICEID mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICEID
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c465ae0a213559c931d8d2e7d6f03da874b9c6c5e7a2ab317e3487d33800656b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117986055"
---
# <a name="mciwndm_getdeviceid-message"></a>Mensaje GETDEVICEID de MCIWNDM \_

El **mensaje \_ GETDEVICEID de MCIWNDM** recupera el identificador del dispositivo MCI abierto actualmente para usarlo con la [**función mciSendCommand.**](/previous-versions//dd757160(v=vs.85)) Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetDeviceID.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)


```C++
MCIWNDM_GETDEVICEID 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
</dt> </dl>

 


---
title: Mensaje de MCIWNDM_GETDEVICEID (VFW. h)
description: El \_ mensaje GETDEVICEID de MCIWNDM recupera el identificador del dispositivo MCI abierto actualmente para usarlo con la función mciSendCommand. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetDeviceID.
ms.assetid: 188f15fa-579a-438e-a812-9a2b684127c0
keywords:
- Mensaje de MCIWNDM_GETDEVICEID de Windows multimedia
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
ms.openlocfilehash: b2f2271b18dcf8f295594031ab2c7c80dd8dec06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078981"
---
# <a name="mciwndm_getdeviceid-message"></a>MCIWNDM \_ GETDEVICEID

El **mensaje \_ GETDEVICEID de MCIWNDM** recupera el identificador del dispositivo MCI abierto actualmente para usarlo con la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) . Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) .


```C++
MCIWNDM_GETDEVICEID 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
</dt> </dl>

 


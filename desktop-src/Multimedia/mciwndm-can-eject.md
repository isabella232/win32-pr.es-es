---
title: Mensaje de MCIWNDM_CAN_EJECT (VFW. h)
description: El \_ mensaje MCIWNDM puede \_ expulsar determina si un dispositivo MCI puede expulsar el contenido multimedia. Puede enviar este mensaje explícitamente o mediante la macro MCIWndCanEject.
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- Mensaje de MCIWNDM_CAN_EJECT de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00ba54c9263e23fdd9830be892e4559ae3755c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803914"
---
# <a name="mciwndm_can_eject-message"></a>MCIWNDM \_ puede \_ expulsar el mensaje

El mensaje **MCIWNDM \_ puede \_ expulsar** determina si un dispositivo MCI puede expulsar el contenido multimedia. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) .


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el dispositivo puede expulsar su medio o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 






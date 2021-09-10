---
title: MCIWNDM_CAN_EJECT mensaje (Vfw.h)
description: El mensaje MCIWNDM \_ CAN EJECT determina si un dispositivo \_ MCI puede expulsar sus medios. Puede enviar este mensaje explícitamente o mediante la macro MCIWndCanEject.
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- MCIWNDM_CAN_EJECT mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370604"
---
# <a name="mciwndm_can_eject-message"></a>Mensaje DE MCIWNDM \_ PUEDE \_ EXPULSAR

El **mensaje MCIWNDM \_ CAN \_ EJECT** determina si un dispositivo MCI puede expulsar sus medios. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndCanEject.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** el dispositivo puede expulsar su medio o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 






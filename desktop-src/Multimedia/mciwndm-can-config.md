---
title: Mensaje de MCIWNDM_CAN_CONFIG (VFW. h)
description: El \_ mensaje MCIWNDM puede \_ configurar determina si un dispositivo MCI puede mostrar un cuadro de diálogo de configuración. Puede enviar este mensaje explícitamente o mediante la macro MCIWndCanConfig.
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- Mensaje de MCIWNDM_CAN_CONFIG de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_CONFIG
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816a8c1dfaec6fc7d7854f8873ce05e74e4de6bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493030"
---
# <a name="mciwndm_can_config-message"></a>MCIWNDM \_ puede \_ configurar el mensaje

El mensaje **MCIWNDM \_ puede \_ configurar** determina si un dispositivo MCI puede mostrar un cuadro de diálogo de configuración. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) .


```C++
MCIWNDM_CAN_CONFIG 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el dispositivo admite la configuración o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
</dt> </dl>

 

 






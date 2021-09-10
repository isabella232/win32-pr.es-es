---
title: MCIWNDM_CAN_CONFIG mensaje (Vfw.h)
description: El mensaje MCIWNDM \_ CAN CONFIG determina si un dispositivo \_ MCI puede mostrar un cuadro de diálogo de configuración. Puede enviar este mensaje explícitamente o mediante la macro MCIWndCanConfig.
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- MCIWNDM_CAN_CONFIG mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370609"
---
# <a name="mciwndm_can_config-message"></a>Mensaje DE CONFIGURACIÓN CAN de MCIWNDM \_ \_

El **mensaje MCIWNDM \_ CAN \_ CONFIG** determina si un dispositivo MCI puede mostrar un cuadro de diálogo de configuración. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndCanConfig.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)


```C++
MCIWNDM_CAN_CONFIG 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** el dispositivo admite la configuración o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
</dt> </dl>

 

 






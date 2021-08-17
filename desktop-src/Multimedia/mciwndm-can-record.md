---
title: MCIWNDM_CAN_RECORD mensaje (Vfw.h)
description: El mensaje MCIWNDM \_ CAN RECORD determina si un dispositivo \_ MCI admite la grabación. Puede enviar este mensaje explícitamente o mediante la macro MCIWndCanRecord.
ms.assetid: b5a789fa-6a88-487d-a374-8f4798ee5a62
keywords:
- MCIWNDM_CAN_RECORD mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_RECORD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df46ce0cbffe17f890e50159a13a93192e67f60e323d6ba711bee6af7ac3f79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429655"
---
# <a name="mciwndm_can_record-message"></a>Mensaje MCIWNDM \_ CAN \_ RECORD

El **mensaje MCIWNDM \_ CAN \_ RECORD** determina si un dispositivo MCI admite la grabación. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndCanRecord.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)


```C++
MCIWNDM_CAN_RECORD 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** el dispositivo admite grabación o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
</dt> </dl>

 

 






---
title: Mensaje de MCIWNDM_CAN_RECORD (VFW. h)
description: El MCIWNDM \_ puede \_ grabar el mensaje determina si un dispositivo MCI admite la grabación. Puede enviar este mensaje explícitamente o mediante la macro MCIWndCanRecord.
ms.assetid: b5a789fa-6a88-487d-a374-8f4798ee5a62
keywords:
- Mensaje de MCIWNDM_CAN_RECORD de Windows multimedia
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
ms.openlocfilehash: 2acbc9efa3ca973c12112a599d1202ad936107a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492611"
---
# <a name="mciwndm_can_record-message"></a>MCIWNDM \_ puede \_ registrar el mensaje

El **MCIWNDM \_ puede \_ grabar** el mensaje determina si un dispositivo MCI admite la grabación. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) .


```C++
MCIWNDM_CAN_RECORD 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el dispositivo admite la grabación o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
</dt> </dl>

 

 






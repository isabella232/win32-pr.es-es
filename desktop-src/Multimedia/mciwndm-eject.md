---
title: MCIWNDM_EJECT mensaje (Vfw.h)
description: El mensaje MCIWNDM \_ EJECT envía un comando a un dispositivo MCI para expulsar sus medios. Puede enviar este mensaje explícitamente o mediante la macro MCIWndEject.
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- MCIWNDM_EJECT mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66c752f192e8f74f2c6e861e581fd22a561bafd9ff6c0f369ba669bc4bf87fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429435"
---
# <a name="mciwndm_eject-message"></a>Mensaje DE MCIWNDM \_ PARA LA EXPULSIÓN

El **mensaje MCIWNDM \_ EJECT** envía un comando a un dispositivo MCI para expulsar sus medios. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndEject.**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)


```C++
MCIWNDM_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 






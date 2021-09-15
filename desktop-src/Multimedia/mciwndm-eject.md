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
ms.openlocfilehash: e41686ce41b82dc48ee6c22ac556606c79c5b24a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476802"
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

 

 






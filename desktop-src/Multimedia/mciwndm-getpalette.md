---
title: MCIWNDM_GETPALETTE mensaje (Vfw.h)
description: El mensaje GETPALETTE de MCIWNDM \_ recupera un identificador de la paleta que usa un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetPalette.
ms.assetid: f8426344-0fee-4419-9d8a-dcee26cb4c28
keywords:
- MCIWNDM_GETPALETTE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 319fe1fedc21c064896c3316d0a45132c034b73c25bf107ee667269a13ed678b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137706"
---
# <a name="mciwndm_getpalette-message"></a>Mensaje GETPALETTE de MCIWNDM \_

El **mensaje \_ GETPALETTE de MCIWNDM** recupera un identificador de la paleta que usa un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetPalette.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)


```C++
MCIWNDM_GETPALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de la paleta si se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
</dt> </dl>

 

 






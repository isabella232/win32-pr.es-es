---
title: MCIWNDM_GETVOLUME mensaje (Vfw.h)
description: El mensaje GETVOLUME de MCIWNDM \_ recupera la configuración de volumen actual de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetVolume.
ms.assetid: 3f1de023-4da8-4899-accc-409701d6e921
keywords:
- MCIWNDM_GETVOLUME mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd514edbf0e49f49bc807f69a2bd5322d6f281475e3ed3c94fa483772580f131
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783305"
---
# <a name="mciwndm_getvolume-message"></a>Mensaje GETVOLUME de MCIWNDM \_

El **mensaje \_ GETVOLUME de MCIWNDM** recupera la configuración de volumen actual de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetVolume.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)


```C++
MCIWNDM_GETVOLUME 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve la configuración del volumen actual. El valor predeterminado es 1000. Los valores más altos indican volúmenes más altos, los valores más bajos indican volúmenes más silenciosos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
</dt> </dl>

 

 






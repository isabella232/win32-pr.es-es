---
title: MCIWNDM_GETVOLUME mensaje (Vfw.h)
description: El mensaje GETVOLUME de MCIWNDM \_ recupera la configuración del volumen actual de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetVolume.
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
ms.openlocfilehash: 4aa11fb13a56dda7cb83e3d6c98b4b66083e91b9
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370687"
---
# <a name="mciwndm_getvolume-message"></a>Mensaje GETVOLUME de MCIWNDM \_

El **mensaje \_ GETVOLUME de MCIWNDM** recupera la configuración del volumen actual de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetVolume.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)


```C++
MCIWNDM_GETVOLUME 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve la configuración del volumen actual. El valor predeterminado es 1000. Los valores más altos indican volúmenes más altos, los valores más bajos indican volúmenes más silenciosos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
</dt> </dl>

 

 






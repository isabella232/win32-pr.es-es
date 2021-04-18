---
title: Mensaje de MCIWNDM_GETVOLUME (VFW. h)
description: El \_ mensaje MCIWNDM GETVOLUME recupera la configuración del volumen actual de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetVolume.
ms.assetid: 3f1de023-4da8-4899-accc-409701d6e921
keywords:
- Mensaje de MCIWNDM_GETVOLUME de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422581"
---
# <a name="mciwndm_getvolume-message"></a>MCIWNDM \_ GETVOLUME

El mensaje **MCIWNDM \_ GETVOLUME** recupera la configuración del volumen actual de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) .


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
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
</dt> </dl>

 

 






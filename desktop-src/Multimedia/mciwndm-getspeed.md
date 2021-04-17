---
title: Mensaje de MCIWNDM_GETSPEED (VFW. h)
description: El \_ mensaje MCIWNDM GETSPEED recupera la velocidad de reproducción de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetSpeed.
ms.assetid: d10a8f88-e85e-449b-8655-bb0832031d59
keywords:
- Mensaje de MCIWNDM_GETSPEED de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c84a8ebb3e97d4543f68f3a237add8eed7706ae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492820"
---
# <a name="mciwndm_getspeed-message"></a>MCIWNDM \_ GETSPEED

El mensaje **MCIWNDM \_ GETSPEED** recupera la velocidad de reproducción de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) .


```C++
MCIWNDM_GETSPEED 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve la velocidad de reproducción si se realiza correctamente. El valor de velocidad normal es 1000. Los valores más grandes indican velocidades más rápidas, los valores más pequeños indican velocidades más lentas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
</dt> </dl>

 

 






---
title: MCIWNDM_GETSPEED mensaje (Vfw.h)
description: El mensaje GETSPEED de MCIWNDM \_ recupera la velocidad de reproducción de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetSpeed.
ms.assetid: d10a8f88-e85e-449b-8655-bb0832031d59
keywords:
- MCIWNDM_GETSPEED mensaje Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069499"
---
# <a name="mciwndm_getspeed-message"></a>Mensaje GETSPEED de MCIWNDM \_

El **mensaje \_ GETSPEED de MCIWNDM** recupera la velocidad de reproducción de un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetSpeed.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)


```C++
MCIWNDM_GETSPEED 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve la velocidad de reproducción si se realiza correctamente. El valor de la velocidad normal es 1000. Los valores más grandes indican velocidades más rápidas, los valores más pequeños indican velocidades más lentas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
</dt> </dl>

 

 






---
title: MCIWNDM_GETEND mensaje (Vfw.h)
description: El mensaje GETEND de MCIWNDM recupera la ubicación del final del contenido de un archivo o \_ dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetEnd.
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- MCIWNDM_GETEND mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETEND
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880b1a464d671ca57e1955d4131776a999d1fb6bd8f17ad5d08139abc64a757b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137736"
---
# <a name="mciwndm_getend-message"></a>Mensaje GETEND de MCIWNDM \_

El **mensaje \_ GETEND de MCIWNDM** recupera la ubicación del final del contenido de un archivo o dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetEnd.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve la ubicación en el formato de hora actual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 






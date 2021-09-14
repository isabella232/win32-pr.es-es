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
ms.openlocfilehash: faec3dd5d9c401d943fbc55ca58e452d3fb25497
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069508"
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



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
</dt> </dl>

 

 






---
title: MCIWNDM_GETZOOM mensaje (Vfw.h)
description: El mensaje GETZOOM de MCIWNDM recupera el valor de zoom actual \_ que usa un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetZoom.
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- MCIWNDM_GETZOOM mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52c247230ffe6269f77b906d874a4cf82a21ed8d3388ffa18193417603e45fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374146"
---
# <a name="mciwndm_getzoom-message"></a>Mensaje GETZOOM de MCIWNDM \_

El **mensaje \_ GETZOOM de MCIWNDM** recupera el valor de zoom actual que usa un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetZoom.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve los valores más recientes usados [**con MCIWNDM \_ SETZOOM.**](mciwndm-setzoom.md)

## <a name="remarks"></a>Comentarios

Un valor devuelto de 100 indica que la imagen no está zoomed. Un valor de 200 indica que la imagen se ha ampliado al doble de su tamaño original. Un valor de 50 indica que la imagen se reduce a la mitad de su tamaño original.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[**MCIWNDM \_ SETZOOM**](mciwndm-setzoom.md)
</dt> </dl>

 

 






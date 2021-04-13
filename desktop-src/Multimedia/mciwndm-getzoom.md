---
title: Mensaje de MCIWNDM_GETZOOM (VFW. h)
description: El \_ mensaje MCIWNDM GETZOOM recupera el valor de zoom actual usado por un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetZoom.
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- Mensaje de MCIWNDM_GETZOOM de Windows multimedia
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
ms.openlocfilehash: fcb4ae1883787f1b86dcc17f2d4a3e0e0ee29ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490120"
---
# <a name="mciwndm_getzoom-message"></a>MCIWNDM \_ GETZOOM

El mensaje **MCIWNDM \_ GETZOOM** recupera el valor de zoom actual usado por un dispositivo MCI. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) .


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve los valores más recientes utilizados con [**MCIWNDM \_ SETZOOM**](mciwndm-setzoom.md).

## <a name="remarks"></a>Observaciones

Un valor devuelto de 100 indica que la imagen no se ha ampliado. Un valor de 200 indica que la imagen se amplía hasta el doble del tamaño original. Un valor de 50 indica que la imagen se reduce a la mitad de su tamaño original.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[**MCIWNDM \_ SETZOOM**](mciwndm-setzoom.md)
</dt> </dl>

 

 






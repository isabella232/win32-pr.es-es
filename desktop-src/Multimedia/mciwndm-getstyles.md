---
title: Mensaje de MCIWNDM_GETSTYLES (VFW. h)
description: El \_ mensaje GETSTYLES de MCIWNDM recupera las marcas que especifican los estilos de ventana de MCIWnd actuales usados por una ventana. Puede enviar este mensaje explícitamente o mediante la macro MCIWndGetStyles.
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- Mensaje de MCIWNDM_GETSTYLES de Windows multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 983e37291977edf2473c2b603cd5b40792fb7989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676949"
---
# <a name="mciwndm_getstyles-message"></a>MCIWNDM \_ GETSTYLES

El **mensaje \_ GETSTYLES de MCIWNDM** recupera las marcas que especifican los estilos de ventana de MCIWnd actuales usados por una ventana. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .


```C++
MCIWNDM_GETSTYLES 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve un valor que representa los estilos actuales de la ventana MCIWnd. El valor devuelto es el operador OR bit a bit de los estilos de ventana MCIWnd (marcas MCIWNDF).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 





